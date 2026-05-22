# SLC-S-InfraOps ? Storage / DOM Objects

- **Status:** fail
- **Updated:** 2026-05-22
- **Repository:** `SkylineCommunications/SLC-S-InfraOps`
- **existingIssueUrl:** null
- **existingPrUrl:** null

## Summary
InfraOps uses DOM extensively, but it does so through custom `DomHelper` wrappers instead of SDM storage objects and exposes at least one direct cross-solution DOM dependency.

## Findings
- [ERROR] **No SDM storage attributes were found.** Repo-wide inspection found no `[SdmDomStorage]`, no `[GenerateExposers]`, and no `SdmObject<T>` inheritance.
- [ERROR] **DOM access is implemented directly through helper/wrapper code.** `ModuleHandlerBase` owns a `DomHelper` instance (`DOM Classes/DOM/Applications/ModuleHandlerBase.cs:21-56`), and CRUD flows are implemented via `DefinitionHandler<>` and wrapper classes under `InfraOpsShared/DOM Classes/DOM/Applications/...`.
- [WARNING] **Committed module IDs are prefixed but not solution-scoped in the recommended `infraops/...` style.** The repository contains `"(slc)people_organizations"` in generated IDs and `"(slc)cost_billing"` in the populate script.
- [WARNING] **No generated mapper files (`*.g.cs`) were found.**
- [ERROR] **Direct cross-solution DOM access exists.** `People and Organizations InfraOps - Tool - Populate.cs` creates `_costBillingDomHelper = new DomHelper(..., "(slc)cost_billing")` and then uses it to resolve contract references (`People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:73,77,111,426`).
- [WARNING] **Direct `DomHelper` usage is widespread outside a strict Tier-2 API boundary.** Examples include `GlobalInfraOpsModuleHandler`, `Helper.cs`, `PlanAndBuildHelpers.cs`, and multiple automation scripts.

## Evidence
- `DOM Classes/DOM/Applications/ModuleHandlerBase.cs` and `MediaOpsShared/DOM/Applications/ModuleHandlerBase.cs` construct `DomHelper` directly from `IEngine`/`IConnection`.
- `InfraOpsShared/DOM Classes/DOM/Applications/GlobalInfraOpsModuleHandler.cs` instantiates per-module handlers and exposes typed DOM definition handlers directly.
- `People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs` directly accesses both the local people-organizations DOM module and the external `cost_billing` module.
- Open GitHub issue/PR search for `sdm`, `dom`, `storage`, and `interoperability` returned no matching open issues or pull requests.

## Verdict
**Fail.** DOM storage is present, but it is not implemented with SDM storage objects and it includes direct cross-solution DOM access.
