# SLC-S-InfraOps — API Surface & Storage Modules

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

---

## Storage Modules

The storage inventory below complements the typed API surface above and captures the DOM setup shipped in `SLC-S-InfraOps`.

## Summary

| DOM Module ID | Source | Entity Types | Unique Fields | Has State Machine | C# Wrappers |
|---|---|---|---|---|---|
| (infraops)properties | Setup JSON + C# | 2 | 15 | No | 3 |
| (slc)asset_management | Setup JSON + C# | 11 | 125 | Yes | 19 |
| (slc)cost_billing | C# | — | — | Unknown | — |
| (slc)facility_management | Setup JSON + C# | 9 | 78 | Yes | 9 |
| (slc)instance_properties | Setup JSON reference | — | — | Unknown | — |
| (slc)object_linking | C# | — | — | Unknown | — |
| (slc)people_organizations | Setup JSON reference + C# | — | — | Unknown | 3 |
| (slc)plan_and_build | Setup JSON + C# | 3 | 23 | Yes | 3 |
| (slc)ticketing | C# | — | — | Unknown | — |

## Modules

### `(infraops)properties`

- **Source:** Setup JSON + C#
- **Friendly name:** InfraOps Properties
- **C# wrappers:** `PropertyValueWrapper`, `PropertyValuesWrapper`, `PropertyWrapper`
- **C# references:** `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:16`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:73`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:120`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:149`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:178`; ...
- **Module manifest:** `SLC-S-InfraOps/SetupContent/DOM/(infraops)properties/(infraops)properties.json`
- **DomDefinitions files (2):** `239ed807-3508-4f00-b950-6681cc25a332.json`, `d7e4ecb9-dc79-496e-90c7-310b340a248b.json`
- **SectionDefinitions files (5):** `3ca75450-2b4b-48df-a893-2ca712f521f7.json`, `3f0e4530-8569-4eb6-aac3-8e4306b5d3ff.json`, `98c6c75e-855a-438a-b96a-ad14fafe1db7.json`, `a99ddb61-78b5-42c5-939d-521cd6cdc0ef.json`, `bd33a4c7-9e7b-44f5-9048-6737ab3191e2.json`
- **DomBehaviorDefinitions files (0):** none
- **Cross-module field references:** `(slc)instance_properties`

#### Property

- **DomDefinition file:** `d7e4ecb9-dc79-496e-90c7-310b340a248b.json`
- **Behavior:** none

##### Property Info

- **SectionDefinition file:** `a99ddb61-78b5-42c5-939d-521cd6cdc0ef.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | Yes | Name of the property |
| Property Type | enum | Yes | Type of the property |
| Scope | string | No | Property Scope |
| Default | string | No |  |
| String Size Limit | long | No |  |
| Is Multi Line String | bool | No |  |

##### Discrete

- **SectionDefinition file:** `3ca75450-2b4b-48df-a893-2ca712f521f7.json`
- **Link settings:** optional=Yes, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Option | string | Yes |  |

##### Layout

- **SectionDefinition file:** `bd33a4c7-9e7b-44f5-9048-6737ab3191e2.json`
- **Link settings:** optional=Yes, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Section Name | string | No |  |
| Order | long | No |  |

#### Property Values

- **DomDefinition file:** `239ed807-3508-4f00-b950-6681cc25a332.json`
- **Behavior:** none

##### Property Value Info

- **SectionDefinition file:** `98c6c75e-855a-438a-b96a-ad14fafe1db7.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Linked Object ID | string | Yes | Linked Object |
| Scope | string | No | The scope in which this property value was created |
| Sub ID | string | No | Sub identifier to which these property values are linked. |

##### Property Value

- **SectionDefinition file:** `3f0e4530-8569-4eb6-aac3-8e4306b5d3ff.json`
- **Link settings:** optional=Yes, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Property Name | string | Yes | Property Name |
| Value | string | No | Property Value |
| Property ID | DOM Reference → (slc)instance_properties | No |  |

### `(slc)asset_management`

- **Source:** Setup JSON + C#
- **Friendly name:** Asset Management
- **C# wrappers:** `AssetClassDataPortWrapper`, `AssetClassPowerPortWrapper`, `AssetClassWrapper`, `AssetElementLinkWrapper`, `AssetHistoryWrapper`, `AssetManagerAppSettingsWrapper`, `AssetWrapper`, `CableTypeWrapper`, `CableWrapper`, `ConnectionHistoryWrapper`, `ConnectionWrapper`, `DataPortWrapper`, `DeviceTypeWrapper`, `HistoryWrapper`, `HolderWrapper`, `PortTypeWrapper`, `PowerPortWrapper`, `PropertyValuesHistoryWrapper`, `ReservationWrapper`
- **C# references:** `InfraOps - Export Applications/InfraOps - Export Applications.cs:152`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:236`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:593`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:610`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:639`; ...
- **Module manifest:** `SLC-S-InfraOps/SetupContent/DOM/(slc)asset_management/(slc)asset_management.json`
- **DomDefinitions files (11):** `203aacf0-ad18-4d52-b243-9547fa8b2553.json`, `280b26f8-7245-4b67-85c1-d42bcf3e9c41.json`, `4d4ad8f7-fe8f-48c4-a373-6d36184de4fb.json`, `5372272a-65f3-43e3-9ef4-f7f879de5a26.json`, `9035d110-47f3-412d-ac8a-fde31bd4b00f.json`, `a7844a51-8221-48da-9a0e-7cfa20262715.json`, `b2e24be2-a559-4628-bcfd-e0398644d46a.json`, `d6f9c4c8-9f8d-4e8c-a7e0-1e1500563416.json`, `edfd08fd-ecae-44db-949a-8ca5d17ee22d.json`, `f369e97b-51b2-4cdc-90b4-7a4f86fad82c.json`, `ff930185-a380-46bf-8bfb-8c70f6933c67.json`
- **SectionDefinitions files (33):** `08974346-b8ff-4e00-8cdd-34d401774092.json`, `2ad67f52-0826-4234-ba7e-bbf9ef046fad.json`, `2ad90463-9998-4df9-a068-93a13cfa2e6a.json`, `311b421b-8c62-4fb2-b211-3740a6a17b40.json`, `45368cbd-a605-4930-8bf2-d0f649edeae0.json`, `516210a2-f739-4462-9df8-2a8146c30bf0.json`, `58c1a50e-d1c7-4467-8d19-54a29f985d83.json`, `5b1c5bb2-ec0e-4f65-a195-58f47eb40d61.json`, `67d996e7-d63e-4ab3-8f84-b937af51c1be.json`, `7146ed89-798f-46f9-a534-99ed91d15e29.json`, `73f92de5-317d-41dc-b8c3-2563fcb13e50.json`, `75f703c9-dff8-44ef-9606-49c94a3f2ee4.json`, `7918fb83-c6de-43c7-82d1-e561aefac746.json`, `7b019f7b-024c-46ec-814d-5a65b1e5fabe.json`, `7fc5a856-18a4-46fd-8e34-2bbe4c642982.json`, `7fd5d383-b925-4d93-ac32-85f7453c8f1d.json`, `8f8353b9-5189-468f-881a-5841595548e8.json`, `941488bf-bb5a-46e0-968c-4b96f18fcbf1.json`, `9d0bbc4b-e0be-45e9-8280-6fe36efe12e8.json`, `a22f5492-2021-4eea-8d02-357f778297df.json`, `a4b292f2-f634-4e16-b218-783c7a2baa43.json`, `a8035b4d-f36e-4093-9002-b80238449b14.json`, `affb2069-39ff-4318-868e-f19b298477f1.json`, `bccf76f0-1c97-4e8b-8c78-156a18ec4e2c.json`, `bda370db-b7e1-431b-991d-37044d0b9176.json`, `ca44f3ce-2725-49f1-93f2-8eb53d1d858c.json`, `cae60cfd-5a48-4e6b-8f52-e69e8e468a9c.json`, `cec87feb-30d0-4270-8bf8-7e8282d0513c.json`, `d0b3100f-6a88-4c32-b3fd-4cb7a662c75b.json`, `db82849f-e6da-478b-b295-dd75de94e0b6.json`, `e711b95b-74ea-4e2a-b08a-4f05cb55a8a5.json`, `ea1c78c3-9670-4cf6-8752-29fa9756f275.json`, `f2048e2c-8d4a-4d18-a808-f2bff352905f.json`
- **DomBehaviorDefinitions files (2):** `a3301105-8724-4a36-af03-aa196a6d83df.json`, `e9e2d567-68f4-4c3f-8154-b3862a1b277b.json`
- **Cross-module field references:** `(slc)facility_management`, `(slc)people_organizations`, `(slc)plan_and_build`

#### Asset

- **DomDefinition file:** `9035d110-47f3-412d-ac8a-fde31bd4b00f.json`
- **Behavior:** `Asset_Behavior` (Not Available → Available → Build Plan Ready → Installed → In Service → Disposed → In Planning → In Transit → In Repair)

##### Asset Information

- **SectionDefinition file:** `58c1a50e-d1c7-4467-8d19-54a29f985d83.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Asset Name | string | No |  |
| Serial number | string | No |  |
| Asset Class | DOM Reference → (slc)asset_management | No |  |
| Asset Description | string | No |  |
| FW/OS | string | No |  |
| Asset ID | string | No |  |
| Hardware Version | string | No | The Hw version. |
| Operational Flags | enum[] | No | List of operational flags |

##### Asset Location

- **SectionDefinition file:** `7fd5d383-b925-4d93-ac32-85f7453c8f1d.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Rack Position | long | No | The device position on the rack. |
| Side | enum | No | The device orientation in the rack |
| Rack | DOM Reference → (slc)facility_management | No |  |
| Desk | DOM Reference → (slc)facility_management | No | The desk where the device is. |
| Container | DOM Reference → (slc)facility_management | No | The warehouse where the device is stored |
| Room | DOM Reference → (slc)facility_management | No |  |
| Power Supply Rack Position | long | No | Position on the rack for the power supply assets |
| Parent Asset | DOM Reference → (slc)asset_management | No |  |
| Holder Number | long | No | Number of the holder slot |

##### Asset Location Destination

- **SectionDefinition file:** `a4b292f2-f634-4e16-b218-783c7a2baa43.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Rack Position | long | No | The device position on the rack. |
| Side | enum | No | The device orientation in the rack |
| Rack | DOM Reference → (slc)facility_management | No |  |
| Desk | DOM Reference → (slc)facility_management | No | The desk where the device is. |
| Container | DOM Reference → (slc)facility_management | No | The warehouse where the device is stored |
| Room | DOM Reference → (slc)facility_management | No |  |
| Power Supply Rack Position | long | No | Position on the rack for the power supply assets |
| Parent Asset | DOM Reference → (slc)asset_management | No |  |
| Holder Number | long | No | Number of the holder slot |

##### Asset Lifecycle

- **SectionDefinition file:** `8f8353b9-5189-468f-881a-5841595548e8.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Purchase date | datetime | No | Date of purchase of the asset |
| First-use date | datetime | No |  |
| End of warranty date | datetime | No |  |
| Installation Date | datetime | No |  |
| Installation User | DOM Reference → (slc)people_organizations | No |  |
| Modification Date | datetime | No |  |
| Modification User | DOM Reference → (slc)people_organizations | No |  |
| End of Life | datetime | No | Expected date of the end of life of the asset |

##### Asset Ownership

- **SectionDefinition file:** `7fc5a856-18a4-46fd-8e34-2bbe4c642982.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Organization | DOM Reference → (slc)people_organizations | No |  |
| Contact person | DOM Reference → (slc)people_organizations | No |  |
| Contact person role | DOM Reference → (slc)people_organizations | No |  |
| Team | DOM Reference → (slc)people_organizations | No |  |

##### Asset Custody

- **SectionDefinition file:** `db82849f-e6da-478b-b295-dd75de94e0b6.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| From | datetime | No |  |
| Till | datetime | No |  |
| Contact person | DOM Reference → (slc)people_organizations | No |  |
| Team | DOM Reference → (slc)people_organizations | No |  |
| Organization | DOM Reference → (slc)people_organizations | No |  |
| Contact person role | DOM Reference → (slc)people_organizations | No |  |

##### Holders

- **SectionDefinition file:** `f2048e2c-8d4a-4d18-a808-f2bff352905f.json`
- **Link settings:** optional=No, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Slot Number | long | Yes | Slot number of the holder |
| Hierarchy Role | enum | Yes | Component Type allowed on the slot |
| Label | string | No | Label of the holder |

##### Element Link

- **SectionDefinition file:** `e711b95b-74ea-4e2a-b08a-4f05cb55a8a5.json`
- **Link settings:** optional=No, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Element ID | string | No |  |
| Is Primary | bool | No |  |

##### Asset Network Details

- **SectionDefinition file:** `67d996e7-d63e-4ab3-8f84-b937af51c1be.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| MAC Address | string | No | The MAC Address |

#### Asset Class

- **DomDefinition file:** `d6f9c4c8-9f8d-4e8c-a7e0-1e1500563416.json`
- **Behavior:** `Asset_Class_Behavior` (Draft → Active → Deprecated)

##### Asset Class Info

- **SectionDefinition file:** `311b421b-8c62-4fb2-b211-3740a6a17b40.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No |  |
| Device Type | DOM Reference → (slc)asset_management | Yes | Device type of the asset class |
| Description | string | No |  |
| Manufacturer | DOM Reference → (slc)people_organizations | No |  |
| Height | double | No | Height in cm. |
| Depth | double | No | Depth in cm. |
| Width | double | No | Width in cm |
| Height (U) | double | No |  |
| Weight | double | No | Weigh in kg. |
| Maximum Power Consumption | double | No | The maximum power consumption in kW. |
| Typical Power Consumption | double | No | The typical power consumption in kW. |
| Front Image | string | No |  |
| Back Image | string | No |  |
| Power Supply | enum | No | Type of the power supply. Only applicable for device types of power strip and fuse panel |
| CIType | string | No |  |

##### Asset Class Lifecycle Information

- **SectionDefinition file:** `7146ed89-798f-46f9-a534-99ed91d15e29.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| EOL Date | datetime | No |  |
| EOS Date | datetime | No |  |
| Nominal Lifetime | timespan | No |  |

##### Holders

- **SectionDefinition file:** `f2048e2c-8d4a-4d18-a808-f2bff352905f.json`
- **Link settings:** optional=No, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Slot Number | long | Yes | Slot number of the holder |
| Hierarchy Role | enum | Yes | Component Type allowed on the slot |
| Label | string | No | Label of the holder |

##### Data Port Info

- **SectionDefinition file:** `7918fb83-c6de-43c7-82d1-e561aefac746.json`
- **Link settings:** optional=Yes, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Port Number | long | Yes |  |
| Port Name | string | No |  |
| Port Exposure | enum | No | Define if port is exposed on the back or on the front |
| Output Type | enum | Yes |  |
| Port Type | DOM Reference → (slc)asset_management | No |  |
| Label | string | No | Label of the port |

##### Power Port Info

- **SectionDefinition file:** `75f703c9-dff8-44ef-9606-49c94a3f2ee4.json`
- **Link settings:** optional=Yes, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Port Number | long | Yes |  |
| Port Name | string | No |  |
| Port Exposure | enum | No | Define if port is exposed on the back or on the front |
| Output Type | enum | Yes |  |
| Port Type | DOM Reference → (slc)asset_management | No |  |
| Label | string | No | Label of the port |

#### Asset Manager App Settings

- **DomDefinition file:** `5372272a-65f3-43e3-9ef4-f7f879de5a26.json`
- **Behavior:** none

##### App Settings

- **SectionDefinition file:** `941488bf-bb5a-46e0-968c-4b96f18fcbf1.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Enable Asset History | bool | Yes | Flag to enable the creation of an asset history entry whenever an asset is created, change or deleted. |
| Plan and Build Job Prompt | enum | Yes | Which action to execute after creating/editing or remove an asset regarding the creating of a job. |
| Enable Connection History | bool | Yes | Flag to enable the creation of an asset history entry whenever an asset is created, change or deleted. |
| History TTL | timespan | No | Time to live per history entry |
| History Limit | long | No | Max amount of history entries. |

#### Cable Type

- **DomDefinition file:** `b2e24be2-a559-4628-bcfd-e0398644d46a.json`
- **Behavior:** none

##### Cable Type Information

- **SectionDefinition file:** `08974346-b8ff-4e00-8cdd-34d401774092.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | Yes | Name of the cable type |
| Description | string | No | Description of the cable type |

##### Category Link

- **SectionDefinition file:** `bda370db-b7e1-431b-991d-37044d0b9176.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Categories | enum[] | No |  |

#### Connections

- **DomDefinition file:** `a7844a51-8221-48da-9a0e-7cfa20262715.json`
- **Behavior:** none

##### Connection Info

- **SectionDefinition file:** `a8035b4d-f36e-4093-9002-b80238449b14.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Notes | string | No | Notes. |
| Description | string | No | the description. |
| Connection Type | enum | No |  |

##### Cable Information

- **SectionDefinition file:** `d0b3100f-6a88-4c32-b3fd-4cb7a662c75b.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Cable Length | double | No | The cable length in metters. |
| Cable Type | DOM Reference → (slc)asset_management | No | Type of Cable |

##### Source Info

- **SectionDefinition file:** `ea1c78c3-9670-4cf6-8752-29fa9756f275.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Cable Source Tag | string | No | Tag of the cable source |
| Source Port | DOM Reference → (slc)asset_management | No |  |
| Source Port Type | DOM Reference → (slc)asset_management | No | Port type of the source port |

##### Destination Info

- **SectionDefinition file:** `cae60cfd-5a48-4e6b-8f52-e69e8e468a9c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Cable Destination Tag | string | No | Tag of the cable destination |
| Destination Port | DOM Reference → (slc)asset_management | No |  |
| Destination Port Type | DOM Reference → (slc)asset_management | No | Port type of the destination port |

#### Data Port

- **DomDefinition file:** `280b26f8-7245-4b67-85c1-d42bcf3e9c41.json`
- **Behavior:** none

##### Data Port Info

- **SectionDefinition file:** `7918fb83-c6de-43c7-82d1-e561aefac746.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Port Number | long | Yes |  |
| Port Name | string | No |  |
| Port Exposure | enum | No | Define if port is exposed on the back or on the front |
| Output Type | enum | Yes |  |
| Port Type | DOM Reference → (slc)asset_management | No |  |
| Label | string | No | Label of the port |

##### Address Info

- **SectionDefinition file:** `73f92de5-317d-41dc-b8c3-2563fcb13e50.json`
- **Link settings:** optional=Yes, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| IPV4 Address | string | No | Ipv4 address |
| IPV6 Address | string | No | IPV6 Address |
| Hostname | string | No | Hostname |
| DNS | bool | No | Flag to represent if DNS is enabled or disabled. |

##### Asset

- **SectionDefinition file:** `45368cbd-a605-4930-8bf2-d0f649edeae0.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Asset ID | DOM Reference → (slc)asset_management | No | Link to parent asset |

##### Primary Port Relation

- **SectionDefinition file:** `2ad90463-9998-4df9-a068-93a13cfa2e6a.json`
- **Link settings:** optional=Yes, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| IsPrimaryIpv4 | bool | No | If this port is used as primary ipv4 |
| IsPrimaryIpv6 | bool | No |  |

#### Device Type

- **DomDefinition file:** `f369e97b-51b2-4cdc-90b4-7a4f86fad82c.json`
- **Behavior:** none

##### Device Type Information

- **SectionDefinition file:** `516210a2-f739-4462-9df8-2a8146c30bf0.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | Yes | Name of the type of device |
| Description | string | No | Description of this type of devices |

##### Tags Info

- **SectionDefinition file:** `9d0bbc4b-e0be-45e9-8280-6fe36efe12e8.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Tags | enum[] | No |  |

##### Hierarchy Info

- **SectionDefinition file:** `ca44f3ce-2725-49f1-93f2-8eb53d1d858c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Hierarchy Role | enum | No | Component Type of the Device TYpe |

#### History

- **DomDefinition file:** `4d4ad8f7-fe8f-48c4-a373-6d36184de4fb.json`
- **Behavior:** none

##### History Info

- **SectionDefinition file:** `cec87feb-30d0-4270-8bf8-7e8282d0513c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Description | string | No | Description of the change that was made |
| Job | DOM Reference → (slc)plan_and_build | No | Job linked to the change |
| User ID | DOM Reference → (slc)people_organizations | No | ID of the user in the PnO app, that made the change |
| Instance Definition ID | string | Yes | Definition ID of the instance changed |
| Instance ID | string | No | ID of the instance that was changed |
| Extra Info | string | No | Extra Info about the history entry |
| Type of History | enum | No | Type of history |

#### Port Type

- **DomDefinition file:** `ff930185-a380-46bf-8bfb-8c70f6933c67.json`
- **Behavior:** none

##### Port Type Information

- **SectionDefinition file:** `7b019f7b-024c-46ec-814d-5a65b1e5fabe.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | Yes | Name of the port type |
| Description | string | No | Description of the port type |

##### Category Link

- **SectionDefinition file:** `bda370db-b7e1-431b-991d-37044d0b9176.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Categories | enum[] | No |  |

##### Cable Compatibility

- **SectionDefinition file:** `bccf76f0-1c97-4e8b-8c78-156a18ec4e2c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Cable Types | DOM Reference[] → (slc)asset_management | No | Cables compatible with port type |

#### Power Port

- **DomDefinition file:** `edfd08fd-ecae-44db-949a-8ca5d17ee22d.json`
- **Behavior:** none

##### Power Port Info

- **SectionDefinition file:** `75f703c9-dff8-44ef-9606-49c94a3f2ee4.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Port Number | long | Yes |  |
| Port Name | string | No |  |
| Port Exposure | enum | No | Define if port is exposed on the back or on the front |
| Output Type | enum | Yes |  |
| Port Type | DOM Reference → (slc)asset_management | No |  |
| Label | string | No | Label of the port |

##### Asset

- **SectionDefinition file:** `45368cbd-a605-4930-8bf2-d0f649edeae0.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Asset ID | DOM Reference → (slc)asset_management | No | Link to parent asset |

##### Primary Port Relation

- **SectionDefinition file:** `2ad90463-9998-4df9-a068-93a13cfa2e6a.json`
- **Link settings:** optional=Yes, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| IsPrimaryIpv4 | bool | No | If this port is used as primary ipv4 |
| IsPrimaryIpv6 | bool | No |  |

#### Reservations

- **DomDefinition file:** `203aacf0-ad18-4d52-b243-9547fa8b2553.json`
- **Behavior:** none

##### Reservation Info

- **SectionDefinition file:** `2ad67f52-0826-4234-ba7e-bbf9ef046fad.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Description | string | Yes | A description of the reservation |

##### Reservation Rack

- **SectionDefinition file:** `5b1c5bb2-ec0e-4f65-a195-58f47eb40d61.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Rack | DOM Reference → (slc)facility_management | No |  |

##### Reserved Positions

- **SectionDefinition file:** `a22f5492-2021-4eea-8d02-357f778297df.json`
- **Link settings:** optional=No, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Reserved Positions Lower Bound | long | Yes | Lower limit of the slots reserved on a rack |
| Reserved Positions Upper Bound | long | Yes | Upper limit of the slots reserved |

##### Linked Job

- **SectionDefinition file:** `affb2069-39ff-4318-868e-f19b298477f1.json`
- **Link settings:** optional=Yes, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Job | DOM Reference → (slc)plan_and_build | Yes | Link to the job responsible for the reservation |

### `(slc)cost_billing`

- **Source:** C#
- **Friendly name:** Cost & Billing
- **C# wrappers:** none found
- **C# references:** `People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:73`
- **SetupContent/DOM folder:** not present in repository

Reference snippets:

- `People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:73` — `private const string _costBillingModuleName = "(slc)cost_billing";`

### `(slc)facility_management`

- **Source:** Setup JSON + C#
- **Friendly name:** Facility Management
- **C# wrappers:** `DeskWrapper`, `FacilityManagerAppSettingsWrapper`, `FacilityWrapper`, `FloorWrapper`, `RackWrapper`, `RoomWrapper`, `RowWrapper`, `SiteWrapper`, `ZoneWrapper`
- **C# references:** `InfraOps - Export Applications/InfraOps - Export Applications.cs:153`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:2352`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:2514`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:2537`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:2554`; ...
- **Module manifest:** `SLC-S-InfraOps/SetupContent/DOM/(slc)facility_management/(slc)facility_management.json`
- **DomDefinitions files (9):** `29eef06e-ed52-4a26-95da-fd35cc4433df.json`, `4576240b-b3da-4739-89d1-c3c5e79a26d9.json`, `5320914d-ffec-486a-9950-b69276b6c13f.json`, `9af0e791-b171-4b92-86e7-79dbb8282f66.json`, `9bbb18c2-8284-4e12-a1d1-f2ebb7e2c1fc.json`, `a07a6f21-b919-4903-ae76-c8442fd97f54.json`, `a09ef2ae-78b6-435a-a5b6-f4b91b3ba14f.json`, `c7877685-0295-40b2-acb1-9aea5d7d9c21.json`, `dab0442b-b092-4dbf-a249-19dd421c69db.json`
- **SectionDefinitions files (20):** `05207b85-724c-4b96-8e50-e8419bb32696.json`, `125d4f2c-4d9f-4efe-9af6-1e6a5d4bcaab.json`, `12edb830-c667-4e93-9f9b-94e6992a3bf6.json`, `136914bb-3580-450f-ad38-3bb709ddc68f.json`, `20bcc5d1-5065-4091-a5b0-82a09ecb9ddb.json`, `2f8f34af-8405-4a7e-b996-da6b9d97e61c.json`, `3ee83337-fe05-417e-b328-08a7931da62f.json`, `45f3a9f1-93ca-486b-99f2-70c00f8f80ec.json`, `67ba4303-7c6b-4c2c-bb8b-0fb2fb4d970d.json`, `67f72a06-cb71-4a21-9973-0ba04e966be9.json`, `785e2397-0f0e-4b82-ace6-9e372a208bf6.json`, `790bcbea-9659-4340-91ff-46dc8c37b251.json`, `8a81a86b-7372-4c83-bde7-680004bb3eb4.json`, `8d225b1a-d69c-4efa-86c3-7f45d6ea7e92.json`, `92517859-4d32-471f-93d6-2a41de0d94ce.json`, `9a6552d4-c538-45be-93fd-a879587d25cc.json`, `9f0aade4-5dc5-4d88-b350-15bd8fafed28.json`, `b082f391-0fdd-4eda-b4dc-f246c5e0063f.json`, `cdbc1f3d-70c8-49e3-a3a3-b310d20b4b6e.json`, `f3b701eb-5ae6-4cb3-8207-b11c7801e136.json`
- **DomBehaviorDefinitions files (8):** `4139c312-2b0f-40f3-b875-26cf5066b705.json`, `558627ea-71eb-4ac6-a655-dedce737649d.json`, `843615ba-3f5d-46a7-91d8-504ddabcdad4.json`, `903a2ba4-5467-4e8e-b728-8f3cd1ff0e72.json`, `98f2c20b-c4a6-4297-9d57-291915d298c5.json`, `c620b4a2-2139-4f15-ac6f-c8235f669296.json`, `cce8f754-26c5-4e5e-97fb-0e474afbec5c.json`, `fa64f66c-35a8-4b32-8a68-0b0b1341886d.json`
- **Cross-module field references:** `(slc)people_organizations`

#### Desk

- **DomDefinition file:** `9af0e791-b171-4b92-86e7-79dbb8282f66.json`
- **Behavior:** `Desk_Behaviour` (Draft → Active → Deprecated)

##### Desk Information

- **SectionDefinition file:** `20bcc5d1-5065-4091-a5b0-82a09ecb9ddb.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No | Name of the desk |
| Plan | string | No | Path to the image of the plan of the room |
| Description | string | No |  |
| Desk ID | string | No |  |

##### Room

- **SectionDefinition file:** `3ee83337-fe05-417e-b328-08a7931da62f.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Room | DOM Reference → (slc)facility_management | No |  |

##### Resource

- **SectionDefinition file:** `2f8f34af-8405-4a7e-b996-da6b9d97e61c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Linked Resource | DOM Reference | No | Resource |

#### Facility

- **DomDefinition file:** `dab0442b-b092-4dbf-a249-19dd421c69db.json`
- **Behavior:** `Facility_Behaviour` (Draft → Deprecated → Active)

##### Facility Information

- **SectionDefinition file:** `125d4f2c-4d9f-4efe-9af6-1e6a5d4bcaab.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No |  |
| Facility Type | enum | No | Type of facility |
| Description | string | No |  |
| Address | string | No |  |
| City | string | No |  |
| Zip Code | string | No |  |
| Country | string | No |  |
| Latitude | double | No | Latitude of the facility |
| Longitude | double | No | Longitude of the facility |
| Facility ID | string | No |  |

##### Site

- **SectionDefinition file:** `9a6552d4-c538-45be-93fd-a879587d25cc.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Site | DOM Reference → (slc)facility_management | No |  |

#### Facility Manager App Settings

- **DomDefinition file:** `a07a6f21-b919-4903-ae76-c8442fd97f54.json`
- **Behavior:** none

##### App Settings

- **SectionDefinition file:** `67ba4303-7c6b-4c2c-bb8b-0fb2fb4d970d.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Google Maps API Key | string | No | Google API Key to be able to use the Maps component. |

#### Floor

- **DomDefinition file:** `9bbb18c2-8284-4e12-a1d1-f2ebb7e2c1fc.json`
- **Behavior:** `Floor_Behaviour` (Draft → Active → Deprecated)

##### Floor Information

- **SectionDefinition file:** `f3b701eb-5ae6-4cb3-8207-b11c7801e136.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No | Name of the floor |
| Plan | string | No | Path to the image with the plan of the floor |
| Description | string | No |  |
| Floor ID | string | No |  |

##### Facility

- **SectionDefinition file:** `9f0aade4-5dc5-4d88-b350-15bd8fafed28.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Facility | DOM Reference → (slc)facility_management | No |  |

#### Rack

- **DomDefinition file:** `c7877685-0295-40b2-acb1-9aea5d7d9c21.json`
- **Behavior:** `Rack_Behaviour` (Draft → Active → Deprecated)

##### Rack Information

- **SectionDefinition file:** `05207b85-724c-4b96-8e50-e8419bb32696.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No | Name of the Rack |
| Model | string | No | Model of the rack |
| Position | enum | No | Defines if the rack is on Top or Bottom |
| Width | double | No | Width of the rack (cm) |
| Depth | double | No | Depth of the rack (cm) |
| Height | double | No | Heigh of the rack (cm) |
| Description | string | No |  |
| Bookable | bool | No |  |
| Cooling Flow | enum | No | Direction of the cooling flow |
| X | double | No | X-axis positioning of the rack in the room |
| Y | double | No | Y-axis positioning of the rack in the room. |
| Label | string | No | Rack label to be displayed in the room view. |
| Color | string | No | Hexadecimal color to display the rack in the room viewer. (Ex. '#f4f4f4') |
| Placement Orientation | enum | No | Placement orientation of the rack in the room. |
| Rack ID | string | No |  |

##### Rack Capacity

- **SectionDefinition file:** `790bcbea-9659-4340-91ff-46dc8c37b251.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Maximum Rack Capacity | double | No | Maximum rack capacity (RU) |
| Maximum Power Capacity | double | No | Maximum Power Capacity (kW) |

##### Row

- **SectionDefinition file:** `8a81a86b-7372-4c83-bde7-680004bb3eb4.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Row | DOM Reference → (slc)facility_management | No |  |

##### Zone

- **SectionDefinition file:** `785e2397-0f0e-4b82-ace6-9e372a208bf6.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Zone | DOM Reference → (slc)facility_management | No |  |

##### Resource

- **SectionDefinition file:** `2f8f34af-8405-4a7e-b996-da6b9d97e61c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Linked Resource | DOM Reference | No | Resource |

##### Image Info

- **SectionDefinition file:** `67f72a06-cb71-4a21-9973-0ba04e966be9.json`
- **Link settings:** optional=No, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Image Filepath | string | No | The image filepath |
| Upload Timestamp | datetime | No | Upload Timestamp |

#### Room

- **DomDefinition file:** `a09ef2ae-78b6-435a-a5b6-f4b91b3ba14f.json`
- **Behavior:** `Room_Behaviour` (Draft → Active → Deprecated)

##### Room Information

- **SectionDefinition file:** `45f3a9f1-93ca-486b-99f2-70c00f8f80ec.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No | Name of the room |
| Plan | string | No | Path to the image containing the plan of the room |
| Description | string | No |  |
| Width | long | No | Width of the room in cm. |
| Depth | long | No | Depth of the room in cm. |
| Room ID | string | No |  |

##### Room Ownership

- **SectionDefinition file:** `92517859-4d32-471f-93d6-2a41de0d94ce.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Team | DOM Reference → (slc)people_organizations | No |  |
| Owner | DOM Reference → (slc)people_organizations | No |  |

##### Floor

- **SectionDefinition file:** `cdbc1f3d-70c8-49e3-a3a3-b310d20b4b6e.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Floor | DOM Reference → (slc)facility_management | No |  |

##### Resource

- **SectionDefinition file:** `2f8f34af-8405-4a7e-b996-da6b9d97e61c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Linked Resource | DOM Reference | No | Resource |

#### Row

- **DomDefinition file:** `29eef06e-ed52-4a26-95da-fd35cc4433df.json`
- **Behavior:** `Row_Behaviour` (Draft → Active → Deprecated)

##### Row Information

- **SectionDefinition file:** `12edb830-c667-4e93-9f9b-94e6992a3bf6.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No | Name of the row |
| Row Plan | string | No | Path to the image of the row plan |
| Row Description | string | No |  |
| Y | double | No | Y-axis poisitioning of the row. |
| Label | string | No | Label of the row to be displayed in the room view. |
| Row ID | string | No |  |

##### Room

- **SectionDefinition file:** `3ee83337-fe05-417e-b328-08a7931da62f.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Room | DOM Reference → (slc)facility_management | No |  |

##### Resource

- **SectionDefinition file:** `2f8f34af-8405-4a7e-b996-da6b9d97e61c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Linked Resource | DOM Reference | No | Resource |

#### Site

- **DomDefinition file:** `5320914d-ffec-486a-9950-b69276b6c13f.json`
- **Behavior:** `Site_Behaviour` (Draft → Deprecated → Active)

##### Site Information

- **SectionDefinition file:** `b082f391-0fdd-4eda-b4dc-f246c5e0063f.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No |  |
| Description | string | No |  |
| Address | string | No |  |
| City | string | No |  |
| Zip Code | string | No |  |
| Country | string | No |  |
| Latitude | double | No | Latitude of the facility |
| Longitude | double | No | Longitude of the facility |
| Site ID | string | No |  |

#### Zone

- **DomDefinition file:** `4576240b-b3da-4739-89d1-c3c5e79a26d9.json`
- **Behavior:** `Zone_Behaviour` (Draft → Active → Deprecated)

##### Zone Information

- **SectionDefinition file:** `8d225b1a-d69c-4efa-86c3-7f45d6ea7e92.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | No | Name of the zone |
| Plan | string | No | Path to the image with the plan of the zone |
| Description | string | No |  |
| Thermal Type | enum | No |  |
| X | double | No | X-axis positioning in the room. |
| Y | double | No | Y-axis positioning in the room. |
| Width | double | No | Width of the zone in the room. |
| Depth | double | No | Depth of the zone in the room. |
| Zone ID | string | No |  |

##### Zone Capacity

- **SectionDefinition file:** `136914bb-3580-450f-ad38-3bb709ddc68f.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Cooling Capacity | double | No | Cooling capacity of the zone (kW) |

##### Room

- **SectionDefinition file:** `3ee83337-fe05-417e-b328-08a7931da62f.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Room | DOM Reference → (slc)facility_management | No |  |

##### Resource

- **SectionDefinition file:** `2f8f34af-8405-4a7e-b996-da6b9d97e61c.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Linked Resource | DOM Reference | No | Resource |

### `(slc)instance_properties`

- **Source:** Setup JSON reference
- **Friendly name:** Instance Properties
- **C# wrappers:** none found
- **C# references:** none found
- **SetupContent/DOM folder:** not present in repository

### `(slc)object_linking`

- **Source:** C#
- **Friendly name:** Object Linking
- **C# wrappers:** none found
- **C# references:** `InfraOps.GQI.AssetManager/Data Sources/Asset Manager - GQI - Ad Hoc - Get Assets.cs:119`
- **SetupContent/DOM folder:** not present in repository

Reference snippets:

- `InfraOps.GQI.AssetManager/Data Sources/Asset Manager - GQI - Ad Hoc - Get Assets.cs:119` — `if(Helper.IsDomModuleInstalled(dms.GetConnection(), "(slc)object_linking") && Helper.IsDomModuleInstalled(dms.GetConnection(), "(slc)ticketing"))`

### `(slc)people_organizations`

- **Source:** Setup JSON reference + C#
- **Friendly name:** People & Organizations
- **C# wrappers:** `OrganizationWrapper`, `PeopleWrapper`, `TeamWrapper`
- **C# references:** `People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:72`; `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:17`; `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:230`; `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:247`; `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:264`; ...
- **SetupContent/DOM folder:** not present in repository
- **Inferred entity types from wrappers:** `Organization`, `People`, `Team`

Reference snippets:

- `People and Organizations InfraOps - Tool - Populate/People and Organizations InfraOps - Tool - Populate.cs:72` — `private const string _moduleName = "(slc)people_organizations";`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:17` — `public const string ModuleId = "(slc)people_organizations";`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:230` — `{ ModuleId = "(slc)people_organizations" };`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:247` — `{ ModuleId = "(slc)people_organizations" };`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:264` — `{ ModuleId = "(slc)people_organizations" };`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:281` — `{ ModuleId = "(slc)people_organizations" };`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:298` — `{ ModuleId = "(slc)people_organizations" };`
- `MediaOpsShared/DOM/Applications/GeneratedDomIds.cs:345` — `{ ModuleId = "(slc)people_organizations" };`

### `(slc)plan_and_build`

- **Source:** Setup JSON + C#
- **Friendly name:** Plan and Build
- **C# wrappers:** `AppSettingsWrapper`, `JobTypeWrapper`, `JobWrapper`
- **C# references:** `InfraOps - Export Applications/InfraOps - Export Applications.cs:154`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:4284`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:4668`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:4691`; `InfraOpsShared/DOM Classes/DOM/Applications/DomIds.cs:4768`; ...
- **Module manifest:** `SLC-S-InfraOps/SetupContent/DOM/(slc)plan_and_build/(slc)plan_and_build.json`
- **DomDefinitions files (3):** `01bfa461-bdcb-442a-b624-93658d570c9a.json`, `447da12d-a9bc-471b-bb90-f33f140851ee.json`, `529f8806-4f41-44fb-afa7-8df6e40dd509.json`
- **SectionDefinitions files (5):** `520a7dac-97ab-42bf-9177-32aeb7b8b9e8.json`, `b28ce9cf-96a1-45bf-8e3d-0f3d1ddc586d.json`, `c4c6de12-bbc6-4e61-b818-f7c538369235.json`, `c708731e-b09b-4eed-9a96-27fcc0116db6.json`, `eba2120c-77d0-43c9-a63a-86abd42be359.json`
- **DomBehaviorDefinitions files (1):** `f66fbbcb-70c8-46ad-acbb-04f8e4b469e9.json`
- **Cross-module field references:** `(slc)asset_management`, `(slc)facility_management`, `(slc)people_organizations`

#### App Settings

- **DomDefinition file:** `529f8806-4f41-44fb-afa7-8df6e40dd509.json`
- **Behavior:** none

##### Job Settings

- **SectionDefinition file:** `c4c6de12-bbc6-4e61-b818-f7c538369235.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Job ID prefix | string | No | The prefix is a string that will be prepended to each Job ID. |
| Job ID next sequence | long | No |  |
| Job ID increment | long | No | An integer defining the increment by which the auto-generated ID increases |
| Job ID starting seed | long | No | Provides the \"starting seed\" when first configuring the job IDs |
| Job ID minimum digits | long | No | Defines the minimum number of digits in the auto-generated value, which must be between 1 and 20 |

#### Job

- **DomDefinition file:** `01bfa461-bdcb-442a-b624-93658d570c9a.json`
- **Behavior:** `Job_Behavior` (New → Active → Assigned → Canceled → Review → Resolved)

##### Job Information

- **SectionDefinition file:** `b28ce9cf-96a1-45bf-8e3d-0f3d1ddc586d.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Job ID | string | No | A human-readable ID for a job, auto-generated for each job instance |
| Job Name | string | No | The job name. |
| Start | datetime | No | The job start time. |
| Job Type | enum | No | The job type: Add, Update, Remove |
| End | datetime | No | The job end time. |
| Job Description | string | No | The job description |
| Remarks | string | No | Remarks concerning the job. |
| Priority | enum | No | The job priotity: Critical, Hight, Normal or Low |
| Sub State | enum | No | The job sub state. |
| Locations | DOM Reference[] → (slc)facility_management | No | It can be Facility, Floor, Room, Zone, Row, Desk and Rack. |
| Type | DOM Reference → (slc)plan_and_build | No | Type of job |

##### Job Ownership

- **SectionDefinition file:** `520a7dac-97ab-42bf-9177-32aeb7b8b9e8.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Assigned To | DOM Reference → (slc)people_organizations | No | person to whom this job is assigned |
| Assignment Group | DOM Reference → (slc)people_organizations | No | The team responsible for this job. |

##### Assets Used

- **SectionDefinition file:** `c708731e-b09b-4eed-9a96-27fcc0116db6.json`
- **Link settings:** optional=No, multiple=Yes

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Asset ID | DOM Reference → (slc)asset_management | Yes | Foreign key identifier for the asset. |
| Action | enum | Yes | Type of the item used |

#### Job Type

- **DomDefinition file:** `447da12d-a9bc-471b-bb90-f33f140851ee.json`
- **Behavior:** none

##### Job Type Info

- **SectionDefinition file:** `eba2120c-77d0-43c9-a63a-86abd42be359.json`
- **Link settings:** optional=No, multiple=No

| Field | Type | Required | Tooltip |
|---|---|---|---|
| Name | string | Yes | Name of the job type |
| Description | string | No | Brief description of this job type |
| Icon | string | No | Icon representing the job type |

### `(slc)ticketing`

- **Source:** C#
- **Friendly name:** Ticketing
- **C# wrappers:** none found
- **C# references:** `InfraOps.GQI.AssetManager/Data Sources/Asset Manager - GQI - Ad Hoc - Get Assets.cs:119`
- **SetupContent/DOM folder:** not present in repository

Reference snippets:

- `InfraOps.GQI.AssetManager/Data Sources/Asset Manager - GQI - Ad Hoc - Get Assets.cs:119` — `if(Helper.IsDomModuleInstalled(dms.GetConnection(), "(slc)object_linking") && Helper.IsDomModuleInstalled(dms.GetConnection(), "(slc)ticketing"))`

## What Was Checked

- `SLC-S-InfraOps/SetupContent/DOM/*` for primary JSON-backed DOM modules.
- `SLC-S-InfraOps-WithDependencies/SetupContent/DOM/*` to confirm the duplicate setup tree exposes the same four module folders.
- C# searches for `[SdmDomStorage("...")]`, `new ModuleId("...")`, quoted DOM module IDs, `*Wrapper.cs`, `DomIds.cs`, `new DomHelper(`, and `IDomCrudHelper<`.
- Wrapper inventory under `InfraOpsShared/DOM Classes/DOM/Applications/**/Wrappers`.

## Parse Warnings

- `SLC-S-InfraOps` contains four first-party setup modules; `cost_billing`, `instance_properties`, `object_linking`, `people_organizations`, and `ticketing` are only referenced from code and/or DOM reference fields, so their full JSON structure is not present here.
- No `[SdmDomStorage(...)]`, `new ModuleId(...)`, or `IDomCrudHelper<>` matches were found in `.cs` files; module discovery therefore relied on setup content, quoted module-ID literals, wrappers, `DomIds.cs`, and `DomHelper` usage.
- Field type mapping follows the requested simplification (`string`, `double`, `long`, `bool`, `datetime`, `DOM Reference`) and keeps extra types (`guid`, `enum`, `timespan`) where they occur in the JSON.
