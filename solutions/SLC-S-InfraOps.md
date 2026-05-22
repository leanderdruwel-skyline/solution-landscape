# SLC-S-InfraOps — API Surface

**Solution:** InfraOps (Infrastructure Operations)
**Repository:** [SkylineCommunications/SLC-S-InfraOps](https://github.com/SkylineCommunications/SLC-S-InfraOps)
**NuGet/devpack source:** [SkylineCommunications/SLC-SDM-InfraOps](https://github.com/SkylineCommunications/SLC-SDM-InfraOps)
**Analysed on:** 2026-05-22

---

## Result: Typed API Objects Found — 6 objects across 2 modules

The typed API surface is published via `SkylineCommunications/SLC-SDM-InfraOps`, which contains two `Common` packages, each with an `I*ApiHelper` interface.

---

## API Objects

### Module: Asset Management

**Interface:** [`IAssetManagementApiHelper`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.AssetManagement.Common/Helpers/IAssetManagementApiHelper.cs)
**Package project:** `SDM.AssetManagement.Common`

| Property Name | Repository Type | Model Type | Model Defined In |
|---|---|---|---|
| `Assets` | `IBulkRepository<Asset>` | `Asset` | [`SDM.AssetManagement.Common/Models/Asset.cs`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.AssetManagement.Common/Models/Asset.cs) |
| `AssetClasses` | `IBulkRepository<AssetClass>` | `AssetClass` | [`SDM.AssetManagement.Common/Models/AssetClass.cs`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.AssetManagement.Common/Models/AssetClass.cs) |
| `PowerPorts` | `IBulkRepository<PowerPort>` | `PowerPort` | [`SDM.AssetManagement.Common/Models/PowerPort.cs`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.AssetManagement.Common/Models/PowerPort.cs) |
| `DataPorts` | `IBulkRepository<DataPort>` | `DataPort` | [`SDM.AssetManagement.Common/Models/DataPort.cs`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.AssetManagement.Common/Models/DataPort.cs) |
| `DeviceTypes` | `IBulkRepository<DeviceType>` | `DeviceType` | [`SDM.AssetManagement.Common/Models/DeviceType.cs`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.AssetManagement.Common/Models/DeviceType.cs) |

---

### Module: Facility Management

**Interface:** [`IFacilityManagementApiHelper`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.FacilityManagement.Common/Helpers/IFacilityManagementApiHelper.cs)
**Package project:** `SDM.FacilityManagement.Common`

| Property Name | Repository Type | Model Type | Model Defined In |
|---|---|---|---|
| `Facilities` | `IBulkRepository<Facility>` | `Facility` | [`SDM.FacilityManagement.Common/Models/Facility.cs`](https://github.com/SkylineCommunications/SLC-SDM-InfraOps/blob/main/SDM.FacilityManagement.Common/Models/Facility.cs) |

---

## What was checked

| Location | What was searched | Found? |
|---|---|---|
| Solution source `SLC-S-InfraOps` (`**/*.cs`) | `I*ApiHelper.cs` filename | ❌ No |
| `SkylineCommunications/SLC-SDM-InfraOps` → `SDM.AssetManagement.Common/Helpers/` | `IAssetManagementApiHelper.cs` | ✅ Found — 5 repository properties |
| `SkylineCommunications/SLC-SDM-InfraOps` → `SDM.FacilityManagement.Common/Helpers/` | `IFacilityManagementApiHelper.cs` | ✅ Found — 1 repository property |

> **NuGet repo naming convention for InfraOps:** `SLC-SDM-<Module>` (not `SLC-S-<Module>-Nuget`). The devpack repo organises sub-modules as `SDM.<SubModule>.Common/Helpers/I<SubModule>ApiHelper.cs`.

---

> ✅ **6 typed API objects found** across 2 modules (AssetManagement: 5, FacilityManagement: 1).
