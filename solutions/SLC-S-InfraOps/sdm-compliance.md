# SLC-S-InfraOps ? SDM Compliance

- **Status:** fail
- **Updated:** 2026-05-22
- **Repository:** `SkylineCommunications/SLC-S-InfraOps`
- **existingIssueUrl:** null
- **existingPrUrl:** null

## Summary
InfraOps registers itself as an SDM solution, but its data and logic layers are implemented as direct DOM helper/wrapper code rather than the SDM 3-tier pattern.

## Findings
- [ERROR] **Tier 1 missing SDM storage models.** Repo-wide inspection found no classes inheriting `SdmObject<T>`, no `[SdmDomStorage]`, and no `[GenerateExposers]`. Storage is implemented through `DomHelper`, `DefinitionHandler<>`, and `DomInstanceWrapper<>` instead (`InfraOpsShared/DOM Classes/DOM/Applications/GlobalInfraOpsModuleHandler.cs`, `InfraOpsShared/DOM Classes/DOM/Applications/All/Handlers/DefinitionHandler.cs`, `InfraOpsShared/DOM Classes/DOM/Applications/DomInstanceWrapper.cs`).
- [WARNING] **Module IDs are not solution-scoped in the `infraops/...` style.** The committed generated IDs use values such as `"(slc)people_organizations"` (`DOM Classes/DOM/Applications/GeneratedDomIds.cs:15-17`), and the populate script also hardcodes `"(slc)cost_billing"` (`People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:72-73`).
- [WARNING] **No generated mapper files were committed.** No `*.g.cs` files were found in the repository.
- [ERROR] **Tier 2 SDM API helper interface is missing.** No `IApiHelper` or `I*ApiHelper` interface exists anywhere in the repo. The closest equivalent is the concrete `GlobalInfraOpsModuleHandler`, which exposes typed handler properties and can be constructed from a connection/message handler (`InfraOpsShared/DOM Classes/DOM/Applications/GlobalInfraOpsModuleHandler.cs:32-42,46-201`; `InfraOpsShared/DOM Classes/DOM/Applications/Asset Manager/AssetManagerHandler.cs:57-95`), but it does not satisfy the required SDM API-helper abstraction.
- [PASS] **Tier 3 registration exists.** `InfraOps - Register Solutions/InfraOps - Register Solutions.cs` calls `engine.GetSdmRegistrar()` and `registrar.Solutions.CreateOrUpdate(...)`.
- [ERROR] **Cross-solution DOM access was found.** `People and Organizations InfraOps - Tool - Populate.cs` opens `new DomHelper(..., "(slc)cost_billing")` and reads contract objects from that external module (`People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:110-111,423-427`), which violates strict encapsulation.

## Evidence
- `Directory.Packages.props` contains `Skyline.DataMiner.SDM.Registration.Automation`, `Skyline.DataMiner.SDM.ObjectLinking.*`, and `Skyline.DataMiner.SDM.Ticketing`, but not `Skyline.DataMiner.SDM` or `Skyline.DataMiner.SDM.Abstractions`.
- `InfraOps.Common/InfraOpsCommon.csproj` references `Skyline.DataMiner.SDM.ObjectLinking.Common` and `Skyline.DataMiner.SDM.Ticketing`, not core SDM storage packages.
- DOM access is centered around `ModuleHandlerBase`, `DefinitionHandler<>`, and wrapper classes rather than an SDM object/repository layer.
- Open GitHub issue/PR search for `sdm`, `dom`, `storage`, and `interoperability` returned no matching open issues or pull requests.

## Verdict
**Fail.** Tier 3 registration is present, but Tier 1 SDM storage and Tier 2 SDM API-helper interfaces are missing, and direct cross-solution DOM access is present.
