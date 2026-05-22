# SLC-S-SatOps — API Surface

**Solution:** SatOps (Satellite Operations)
**Repository:** [SkylineCommunications/SLC-S-SatOps](https://github.com/SkylineCommunications/SLC-S-SatOps)
**Analysed version:** 1.1.0
**Analysed on:** 2026-05-22

---

## Result: No Typed API Surface

No `I*ApiHelper.cs` file was found in the solution source, and no properties typed as `IRepository<T>`, `IBulkRepository<T>`, `IObservableRepository<T>`, or `I<Entity>Repository` were found anywhere in the `.cs` files.

### What was checked

| Location | What was searched | Found? |
|---|---|---|
| Solution source (`**/*.cs`) | `I*ApiHelper.cs` filename | ❌ No |
| Solution source (`**/*.cs`) | `IRepository<T>` / `IBulkRepository<T>` / `IObservableRepository<T>` usage | ❌ No |
| `Skyline.DataMiner.Dev.Utils.SDM.Abstractions` v1.0.1 | Type named `I*Api` or `I*ApiHelper` | ❌ No (only base `IRepository<T>` / `IBulkRepository<T>` framework interfaces) |
| `Skyline.DataMiner.SDM.Abstractions` v0.2.2 | Type named `I*Api` or `I*ApiHelper` | ❌ No (only base `IObservableRepository<T>` framework interface) |

### What the solution does expose (DOM-only, out of scope)

The solution manages its domain objects via two DOM modules. These are excluded from this landscape (DOM objects are not a typed API surface) but listed here for reference:

**Module: `satellite-management`**
- `Satellite`
- `Transponder`
- `Beam`
- `TransponderPlan` / `TransponderPlanRow`
- `Slot`

**Module: `antenna-management`**
- `EarthStation`
- `Antenna` / `SteerableAntenna` / `FixedAntenna`
- `AntennaControlUnit`
- `FrequencyBand`

All domain model classes are defined in the shared project `DOM Classes/DOM/Applications/` within the solution source.

---

> ⚠️ **No typed API objects to register.** Revisit this file when a typed `ISatOpsApiHelper` (or equivalent) is introduced.
