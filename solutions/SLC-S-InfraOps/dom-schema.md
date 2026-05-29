# DOM Schema — SLC-S-InfraOps
**Generated**: 2026-05-29
**Repository**: https://github.com/SkylineCommunications/SLC-S-InfraOps
**Modules accessed**: 5 (5 installed by this solution, 0 not installed here)

---

## Module: `(infraops)properties`
**Created by**: JSON — _schema from install JSON + code scan_

### Sections accessed

#### `Discrete`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Option | String | Back + Frontend | JSON |

#### `Layout`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Order | — | Backend | ⚠️ not in install package |
| SectionName | — | Backend | ⚠️ not in install package |

#### `Property Info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Name | String | Frontend | JSON |
| Property Type | String | Frontend | JSON |
| Scope | String | Frontend | JSON |

#### `Property Value`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Property ID | Guid | None | JSON |
| Property Name | String | None | JSON |
| Value | String | None | JSON |

#### `Property Value Info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Linked Object ID | String | None | JSON |
| Scope | String | Frontend | JSON |
| Sub ID | String | None | JSON |

#### `PropertyInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Default | — | Backend | ⚠️ not in install package |
| IsMultiLineString | — | Backend | ⚠️ not in install package |
| Name | — | Back + Frontend | ⚠️ not in install package |
| PropertyType | — | Backend | ⚠️ not in install package |
| Scope | — | Back + Frontend | ⚠️ not in install package |
| StringSizeLimit | — | Backend | ⚠️ not in install package |

#### `PropertyValue`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| PropertyID | — | Backend | ⚠️ not in install package |
| PropertyName | — | Backend | ⚠️ not in install package |
| Value | — | Backend | ⚠️ not in install package |

#### `PropertyValueInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| LinkedObjectID | — | Backend | ⚠️ not in install package |
| Scope | — | Back + Frontend | ⚠️ not in install package |
| SubID | — | Backend | ⚠️ not in install package |

---

## Module: `(slc)asset_management`
**Created by**: code — _schema from DomIds.cs + code scan_

### Sections accessed

#### `AddressInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| DNS | — | Backend | code |
| Hostname | — | Backend | code |
| IPV4Address | — | Backend | code |
| IPV6Address | — | Backend | code |

#### `AppSettings`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| EnableAssetHistory | — | Backend | code |
| EnableConnectionHistory | — | Backend | code |
| HistoryLimit | — | Backend | code |
| HistoryTTL | — | Backend | code |
| PlanAndBuildJobPrompt | — | Backend | code |

#### `Asset`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| AssetID | — | Backend | code |

#### `AssetClassInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| BackImage | — | Backend | code |
| Citype | — | Backend | code |
| Depth | — | Backend | code |
| Description | — | Backend | code |
| DeviceType | — | Backend | code |
| FrontImage | — | Backend | code |
| Height | — | Backend | code |
| HeightU | — | Backend | code |
| Manufacturer | — | Backend | code |
| MaximumPowerConsumption | — | Backend | code |
| Name | — | Back + Frontend | code |
| PowerSupply | — | Backend | code |
| TypicalPowerConsumption | — | Backend | code |
| Weight | — | Backend | code |
| Width | — | Backend | code |

#### `AssetClassLifecycleInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| EOLDate | — | Backend | code |
| EOSDate | — | Backend | code |
| NominalLifetime | — | Backend | code |

#### `AssetCustody`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ContactPerson | — | Backend | code |
| ContactPersonRole | — | Backend | code |
| From | — | Backend | code |
| Organization | — | Backend | code |
| Team | — | Backend | code |
| Till | — | Backend | code |

#### `AssetInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| AssetClass | — | Backend | code |
| AssetDescription | — | Backend | code |
| AssetID | — | Backend | code |
| AssetName | — | Backend | code |
| FWOS | — | Backend | code |
| HardwareVersion | — | Backend | code |
| OperationalFlags | — | Backend | code |
| SerialNumber | — | Backend | code |

#### `AssetLifecycle`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| EndOfLife | — | Backend | code |
| EndOfWarrantyDate | — | Backend | code |
| FirstUseDate | — | Backend | code |
| InstallationDate | — | Backend | code |
| InstallationUser | — | Backend | code |
| ModificationDate | — | Backend | code |
| ModificationUser | — | Backend | code |
| PurchaseDate | — | Backend | code |

#### `AssetLocation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Container | — | Backend | code |
| Desk | — | Backend | code |
| HolderNumber | — | Backend | code |
| ParentAsset | — | Backend | code |
| PowerSupplyRackPosition | — | Backend | code |
| Rack | — | Backend | code |
| RackPosition | — | Backend | code |
| Room | — | Backend | code |
| Side | — | Backend | code |

#### `AssetLocationDestination`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Container | — | Backend | code |
| Desk | — | Backend | code |
| HolderNumber | — | Backend | code |
| ParentAsset | — | Backend | code |
| PowerSupplyRackPosition | — | Backend | code |
| Rack | — | Backend | code |
| RackPosition | — | Backend | code |
| Room | — | Backend | code |
| Side | — | Backend | code |

#### `AssetNetworkDetails`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| MACAddress | — | Backend | code |

#### `AssetOwnership`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ContactPerson | — | Backend | code |
| ContactPersonRole | — | Backend | code |
| Organization | — | Backend | code |
| Team | — | Backend | code |

#### `CableCompatibility`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| CableTypes | — | Backend | code |

#### `CableInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| CableLength | — | Backend | code |
| CableType | — | Backend | code |

#### `CableTypeInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| Name | — | Back + Frontend | code |

#### `CategoryLink`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Categories | — | Backend | code |

#### `ConnectionInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ConnectionType | — | Backend | code |
| Description | — | Backend | code |
| Notes | — | Backend | code |

#### `DataPortInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Label | — | Backend | code |
| OutputType | — | Backend | code |
| PortExposure | — | Backend | code |
| PortName | — | Backend | code |
| PortNumber | — | Backend | code |
| PortType | — | Backend | code |

#### `DestinationInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| CableDestinationTag | — | Backend | code |
| DestinationPort | — | Backend | code |
| DestinationPortType | — | Backend | code |

#### `DeviceTypeInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| Name | — | Back + Frontend | code |

#### `ElementLink`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ElementID | — | Backend | code |
| IsPrimary | — | Backend | code |

#### `HierarchyInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| HierarchyRole | — | Backend | code |

#### `HistoryInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| ExtraInfo | — | Backend | code |
| InstanceDefinitionID | — | Backend | code |
| InstanceID | — | Backend | code |
| Job | — | Backend | code |
| TypeOfHistory | — | Backend | code |
| UserID | — | Backend | code |

#### `Holders`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| HierarchyRole | — | Backend | code |
| Label | — | Backend | code |
| SlotNumber | — | Backend | code |

#### `LinkedJob`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Job | — | Backend | code |

#### `PortTypeInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| Name | — | Back + Frontend | code |

#### `PowerPortInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Label | — | Backend | code |
| OutputType | — | Backend | code |
| PortExposure | — | Backend | code |
| PortName | — | Backend | code |
| PortNumber | — | Backend | code |
| PortType | — | Backend | code |

#### `PrimaryPortRelation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Isprimaryipv4 | — | Backend | code |
| Isprimaryipv6 | — | Backend | code |

#### `ReservationInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |

#### `ReservationRack`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Rack | — | Backend | code |

#### `ReservedPositions`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ReservedPositionsLowerBound | — | Backend | code |
| ReservedPositionsUpperBound | — | Backend | code |

#### `SourceInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| CableSourceTag | — | Backend | code |
| SourcePort | — | Backend | code |
| SourcePortType | — | Backend | code |

#### `TagsInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Tags | — | Backend | code |

---

## Module: `(slc)facility_management`
**Created by**: code — _schema from DomIds.cs + code scan_

### Sections accessed

#### `AppSettings`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| GoogleMapsAPIKey | — | Backend | code |

#### `DeskInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| DeskID | — | Backend | code |
| Name | — | Back + Frontend | code |
| Plan | — | Backend | code |

#### `Facility`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Facility_fc282509 | — | Backend | code |

#### `FacilityInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Address | — | Backend | code |
| City | — | Backend | code |
| Country | — | Backend | code |
| Description | — | Backend | code |
| FacilityID | — | Backend | code |
| FacilityType | — | Backend | code |
| Latitude | — | Backend | code |
| Longitude | — | Backend | code |
| Name | — | Back + Frontend | code |
| ZipCode | — | Backend | code |

#### `Floor`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Floor_6a3f0eeb | — | Backend | code |

#### `FloorInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| FloorID | — | Backend | code |
| Name | — | Back + Frontend | code |
| Plan | — | Backend | code |

#### `ImageInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ImageFilepath | — | Backend | code |
| UploadTimestamp | — | Backend | code |

#### `RackCapacity`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| MaximumPowerCapacity | — | Backend | code |
| MaximumRackCapacity | — | Backend | code |

#### `RackInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Bookable | — | Backend | code |
| Color | — | Backend | code |
| CoolingFlow | — | Backend | code |
| Depth | — | Backend | code |
| Description | — | Backend | code |
| Height | — | Backend | code |
| Label | — | Backend | code |
| Model | — | Backend | code |
| Name | — | Back + Frontend | code |
| PlacementOrientation | — | Backend | code |
| Position | — | Backend | code |
| RackID | — | Backend | code |
| Width | — | Backend | code |
| X | — | Backend | code |
| Y | — | Backend | code |

#### `Resource`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| LinkedResource | — | Backend | code |

#### `Room`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Room_8d904f8d | — | Backend | code |

#### `RoomInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Depth | — | Backend | code |
| Description | — | Backend | code |
| Name | — | Back + Frontend | code |
| Plan | — | Backend | code |
| RoomID | — | Backend | code |
| Width | — | Backend | code |

#### `RoomOwnership`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Owner | — | Backend | code |
| Team | — | Backend | code |

#### `Row`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Row_5d2f9bb3 | — | Backend | code |

#### `RowInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Label | — | Backend | code |
| Name | — | Back + Frontend | code |
| RowDescription | — | Backend | code |
| RowID | — | Backend | code |
| RowPlan | — | Backend | code |
| Y | — | Backend | code |

#### `Site`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Site_f08b42c7 | — | Backend | code |

#### `SiteInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Address | — | Backend | code |
| City | — | Backend | code |
| Country | — | Backend | code |
| Description | — | Backend | code |
| Latitude | — | Backend | code |
| Longitude | — | Backend | code |
| Name | — | Back + Frontend | code |
| SiteID | — | Backend | code |
| ZipCode | — | Backend | code |

#### `Zone`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Zone_45922fd2 | — | Backend | code |

#### `ZoneCapacity`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| CoolingCapacity | — | Backend | code |

#### `ZoneInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Depth | — | Backend | code |
| Description | — | Backend | code |
| Name | — | Back + Frontend | code |
| Plan | — | Backend | code |
| ThermalType | — | Backend | code |
| Width | — | Backend | code |
| X | — | Backend | code |
| Y | — | Backend | code |
| ZoneID | — | Backend | code |

---

## Module: `(slc)people_organizations`
**Created by**: code — _schema from DomIds.cs + code scan_

### Sections accessed

#### `Billing`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| City | — | None | code |
| Country | — | None | code |
| Email | — | None | code |
| Phone | — | None | code |
| StreetAddress | — | None | code |
| Zip | — | None | code |

#### `CategoryInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Category | — | None | code |

#### `ContactInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| City | — | Backend | code |
| Country | — | Backend | code |
| Email | — | Backend | code |
| Phone | — | Backend | code |
| StreetAddress | — | Backend | code |
| ZIP | — | Backend | code |

#### `Contracts`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Contract | — | Backend | code |

#### `ExperienceInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Experience | — | None | code |

#### `Organization`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Organization_57695f03 | — | Backend | code |

#### `OrganizationInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Category | — | None | code |
| Icon | — | None | code |
| OrganizationName | — | Backend | code |

#### `PeopleInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| ExperienceLevel | — | None | code |
| FullName | — | Backend | code |
| PersonalSkills | — | Backend | code |
| ProfileImage | — | None | code |

#### `Resource`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| LinkedResource | — | Backend | code |

#### `ResourcePool`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| LinkedResourcePool | — | Backend | code |

#### `RoleInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Role | — | None | code |

#### `Team`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| TeamRole | — | Backend | code |
| Team_144d3379 | — | Backend | code |

#### `TeamInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Bookable | — | Backend | code |
| Icon | — | None | code |
| TeamDescription | — | Backend | code |
| TeamEmail | — | Backend | code |
| TeamName | — | Backend | code |
| TeamSkills | — | Backend | code |

---

## Module: `(slc)plan_and_build`
**Created by**: code — _schema from DomIds.cs + code scan_

### Sections accessed

#### `AssetsUsed`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Action | — | Backend | code |
| AssetID | — | Backend | code |

#### `JobInformation`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| End | — | Backend | code |
| JobDescription | — | Backend | code |
| JobID | — | Backend | code |
| JobName | — | Backend | code |
| JobType | — | Backend | code |
| Locations | — | Backend | code |
| Priority | — | Backend | code |
| Remarks | — | Backend | code |
| Start | — | Backend | code |
| SubState | — | Backend | code |
| Type | — | Backend | code |

#### `JobOwnership`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| AssignedTo | — | Backend | code |
| AssignmentGroup | — | Backend | code |

#### `JobSettings`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| JobIDIncrement | — | Backend | code |
| JobIDMinimumDigits | — | Backend | code |
| JobIDNextSequence | — | Backend | code |
| JobIDPrefix | — | Backend | code |
| JobIDStartingSeed | — | Backend | code |

#### `JobTypeInfo`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Description | — | Backend | code |
| Icon | — | Backend | code |
| Name | — | Back + Frontend | code |

---

## Direct DOM access from Low-Code App

> ⚠️ **These queries bypass the solution API and access DOM storage directly from the UI.**  
> Prefer reading data through UDAPI/GQI data sources exposed by the solution.

| Query name | Module | Definitions | Columns selected | Join module | Join definitions | Join columns |
|------------|--------|-------------|-----------------|-------------|-----------------|--------------|
| Get assets | `(slc)asset_management` | (guid:f369e97b…) | Name, (fd:fa9a8c23…), ID | `(slc)asset_management` | (guid:d6f9c4c8…) | Name, (fd:e7661d39…), ID |
| Get Racks | `(slc)facility_management` | (guid:c7877685…) | Name, State, (fd:be8b9be1…), (fd:fead1e27…), (fd:fb2f13e8…), ID | — | — | — |
| Get Asset Classes | `(slc)asset_management` | (guid:d6f9c4c8…) | Name, State, (fd:e7661d39…), (fd:065a0dde…), (fd:535dedd7…), (fd:7a38322c…), (fd:c518fadb…), (fd:84820351…), (fd:14a1b2f6…), (fd:481f1010…), (fd:df1cd95b…) | — | — | — |
| Get Asset Class Details | `(slc)asset_management` | (guid:d6f9c4c8…) | Name, (fd:7a38322c…), (fd:535dedd7…), (fd:c518fadb…), (fd:64e8da13…), (fd:e7661d39…), (fd:b8adb2c5…), (fd:065a0dde…), (fd:84820351…), (fd:14a1b2f6…), State, (fd:481f1010…), (fd:c6493f31…), (fd:df1cd95b…), (fd:23edd575…), (fd:2183802a…), (fd:28427166…), (fd:9c01fc26…), (fd:cebfc16b…) | — | — | — |
| Asset Classes grouped by Device Type | `(slc)asset_management` | (guid:d6f9c4c8…) | Name, ID | — | — | — |
| Asset Classes grouped by State | `(slc)asset_management` | (guid:d6f9c4c8…) | ID, State | — | — | — |
| Assets per rack top 10 | `(slc)facility_management` | (guid:c7877685…) | Name, ID | — | — | — |
| Total assets | `(slc)asset_management` | (guid:9035d110…) | (all) | — | — | — |
| Total Asset Classes | `(slc)asset_management` | (guid:d6f9c4c8…) | (all) | — | — | — |
| Total racks | `(slc)facility_management` | (guid:c7877685…) | (all) | — | — | — |
| Assets grouped by Asset class | `(slc)asset_management` | (guid:d6f9c4c8…) | Name, ID | — | — | — |
| Get All Facilities Dropdown | `(slc)facility_management` | (guid:dab0442b…) | Name, ID | — | — | — |
| Get Floors Dropdown | `(slc)facility_management` | (guid:9bbb18c2…) | Name, (fd:fc282509…), ID | — | — | — |
| Get Rooms Dropdown | `(slc)facility_management` | (guid:a09ef2ae…) | Name, (fd:6a3f0eeb…), ID | — | — | — |
| Get Rows By Room Dropdown | `(slc)facility_management` | (guid:29eef06e…) | Name, (fd:8d904f8d…), ID | — | — | — |
| Get Racks by Rows Dropdown | `(slc)facility_management` | (guid:c7877685…) | Name, (fd:5d2f9bb3…), ID | — | — | — |
| Get Facility Names | `(slc)facility_management` | (guid:dab0442b…) | Name, ID | — | — | — |
| Get Floor Names Filtered By Facility | `(slc)facility_management` | (guid:9bbb18c2…) | Name, (fd:fc282509…), ID | — | — | — |
| Get Room Names Filtered By Floor | `(slc)facility_management` | (guid:a09ef2ae…) | Name, (fd:6a3f0eeb…), ID | — | — | — |
| Get Rack Names Filtered by Room | `(slc)facility_management` | (guid:c7877685…) | Name, ID, (fd:5d2f9bb3…) | — | — | — |
| Get Rows | `(slc)facility_management` | (guid:29eef06e…) | Name, (fd:12ee587f…), (fd:335719a3…), (fd:73b46987…), (fd:3c56aa07…), (fd:ca234e07…), (fd:8d904f8d…), (fd:af0981cf…) | — | — | — |
| Get All Rooms | `(slc)facility_management` | (guid:a09ef2ae…) | Name, ID | — | — | — |
| Get Floors Dropdown Row Viewer | `(slc)facility_management` | (guid:9bbb18c2…) | Name, (fd:fc282509…), ID | — | — | — |
| Get Rooms Dropdown Row Viewer | `(slc)facility_management` | (guid:a09ef2ae…) | Name, (fd:6a3f0eeb…), ID | — | — | — |
| Get Rows By Room Dropdown Row Viewer | `(slc)facility_management` | (guid:29eef06e…) | Name, (fd:8d904f8d…), ID | — | — | — |
| Get App Settings | `(slc)asset_management` | (guid:5372272a…) | (fd:9555c359…), (fd:be7d9f39…), (fd:62a7768a…), (fd:c540fb2a…), (fd:ca9c44c6…), History Entries TTL | — | — | — |
| Get Jobs for asset | `(slc)people_organizations` | (guid:1624a01d…) | Name, ID | `(slc)people_organizations` | (guid:5150bc87…) | Name, ID |
| Get Jobs for asset | `(slc)people_organizations` | (guid:1624a01d…) | Name, ID | `(slc)plan_and_build` | (guid:01bfa461…) | (fd:124ee700…), Name, (fd:ae07a73c…), (fd:a92163d0…), (fd:27b85f20…), State, (fd:2cf0ad38…), (fd:f73d9198…), (fd:30deab28…), (fd:e90b9377…), ID |
| Get Asset Properties | `(infraops)properties` | Property | Name, (fd:9936899d…), CreatedBy | — | — | — |
| Get Facilities | `(slc)facility_management` | (guid:dab0442b…) | Name, State, (fd:def40fd7…), (fd:872360fb…), (fd:37dbb06b…), ID | — | — | — |
| Get Floors By Facilities | `(slc)facility_management` | (guid:9bbb18c2…) | Name, State, (fd:1d3a2787…), ID | — | — | — |
| Get Rooms By Floor | `(slc)facility_management` | (guid:a09ef2ae…) | Name, State, Concatenate, Concatenate, Concatenate, Concatenate, (fd:bcdd4b85…), ID | — | — | — |
| Get All Rooms | `(slc)facility_management` | (guid:a09ef2ae…) | Name, State, (fd:6a3f0eeb…), (fd:371b8e3c…), (fd:8ca723ed…) | — | — | — |
| Get Row By Room | `(slc)facility_management` | (guid:29eef06e…) | Name, State, (fd:335719a3…), (fd:8d904f8d…) | — | — | — |
| Get Desks By Room | `(slc)facility_management` | (guid:9af0e791…) | Name, State, (fd:ef68805b…), (fd:8d904f8d…) | — | — | — |
| Get All Racks | `(slc)facility_management` | (guid:c7877685…) | Name, State, (fd:be8b9be1…), (fd:fead1e27…), (fd:fb2f13e8…), (fd:cd193a69…), (fd:c4bc0a18…), (fd:32ec429c…), (fd:c499cb89…), (fd:45922fd2…), (fd:5d2f9bb3…) | — | — | — |
| Get Facilities Drafts | `(slc)facility_management` | (guid:dab0442b…) | Name, (fd:def40fd7…), (fd:872360fb…), (fd:37dbb06b…) | — | — | — |
| Get selected floor | `(slc)facility_management` | (guid:9bbb18c2…) | Name, (fd:1d3a2787…), Concatenate, ID, LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, State, (fd:37dbb06b…), (fd:eea022dd…), (fd:3b996c01…) | — | — | — |
| Get Selected Facility | `(slc)facility_management` | (guid:dab0442b…) | (fd:37dbb06b…), (fd:370f8d27…), (fd:def40fd7…), (fd:872360fb…), LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:fd4dbb48…), (fd:4fa9677f…), (fd:91359fc6…), (fd:613d7d84…), Name, (fd:4ca5dc9c…), (fd:f08b42c7…) | — | — | — |
| Get selected room | `(slc)facility_management` | (guid:a09ef2ae…) | Name, (fd:bcdd4b85…), (fd:371b8e3c…), (fd:8ca723ed…), Name, State, LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:4c12f63d…), (fd:31249cdc…), (fd:11dede73…), (fd:16beb7ef…) | — | — | — |
| Get selected room (Room page) | `(slc)facility_management` | (guid:a09ef2ae…) | Name, (fd:bcdd4b85…), State, Concatenate, Concatenate, Concatenate, LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:4c12f63d…), (fd:16beb7ef…) | — | — | — |
| Get selected row | `(slc)facility_management` | (guid:29eef06e…) | Name, (fd:335719a3…), Name, State, LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:73b46987…), (fd:12ee587f…), (fd:808a94ba…) | — | — | — |
| Get selected desk | `(slc)facility_management` | (guid:9af0e791…) | Name, (fd:ef68805b…), Name, State, LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:2291fc00…), ID, (fd:488edf47…) | — | — | — |
| Get selected rack | `(slc)facility_management` | (guid:c7877685…) | Name, State, (fd:be8b9be1…), (fd:fead1e27…), (fd:fb2f13e8…), (fd:cd193a69…), (fd:c4bc0a18…), (fd:32ec429c…), (fd:c499cb89…), LastModified, LastModifiedBy, CreatedAt, CreatedBy, (fd:5d2f9bb3…), (fd:45922fd2…), (fd:0fce02b2…), (fd:94fddd93…), (fd:5a337cca…) | — | — | — |
| Get Facilities selected map | `(slc)facility_management` | (guid:dab0442b…) | Name, State, (fd:37dbb06b…), ID, (fd:f08b42c7…) | — | — | — |
| Get Facilities Grouped by Type | `(slc)facility_management` | (guid:dab0442b…) | (all) | — | — | — |
| Facilities Count | `(slc)facility_management` | (guid:dab0442b…) | (all) | — | — | — |
| Floors Count per facility | `(slc)facility_management` | (guid:9bbb18c2…) | (all) | — | — | — |
| Room Count per facility | `(slc)facility_management` | (guid:a09ef2ae…) | (all) | — | — | — |
| Rows Count per facility | `(slc)facility_management` | (guid:29eef06e…) | (fd:8d904f8d…), ID | — | — | — |
| Zone Count per facility | `(slc)facility_management` | (guid:4576240b…) | (fd:8d904f8d…), ID | — | — | — |
| Desk Count per facility | `(slc)facility_management` | (guid:9af0e791…) | (fd:8d904f8d…), ID | — | — | — |
| Rack Count per facility | `(slc)facility_management` | (guid:c7877685…) | ID, (fd:5d2f9bb3…) | — | — | — |
| Top 10 floors per facility | `(slc)facility_management` | (guid:9bbb18c2…) | (all) | — | — | — |
| Facilities grouped by state | `(slc)facility_management` | (guid:dab0442b…) | (all) | — | — | — |
| Top 10 rooms per facility | `(slc)facility_management` | (guid:a09ef2ae…) | (fd:6a3f0eeb…), ID, State | — | — | — |
| Get All Rooms With ID | `(slc)facility_management` | (guid:a09ef2ae…) | Name, ID | — | — | — |
| Get Assets on Rack with KPIs | `(slc)asset_management` | (guid:9035d110…) | Name, (fd:71a78231…), (fd:cad2081d…), (fd:7c36827c…), (fd:bd1fdb19…), (fd:1b894f9c…), (fd:a5ca6c86…), (fd:b267553c…), (fd:4ce12068…) | — | — | — |
| Get All Floors | `(slc)facility_management` | (guid:9bbb18c2…) | Name, State, (fd:fc282509…), ID | — | — | — |
| Get Sites | `(slc)facility_management` | (guid:5320914d…) | Name, State, (fd:e9485c2b…), ID, (fd:fd3feeaf…), (fd:3f7b64ea…) | — | — | — |
| Get Selected Site | `(slc)facility_management` | (guid:5320914d…) | LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, Name, (fd:199e9b2a…), (fd:54866065…), (fd:a5871ad2…), (fd:22ea6e74…), (fd:0b43ef7a…), (fd:fd3feeaf…), (fd:3f7b64ea…), (fd:e9485c2b…) | — | — | — |
| Get All Non Site Facilities | `(slc)facility_management` | (guid:dab0442b…) | Name, (fd:f08b42c7…), (fd:259e31ed…), (fd:37dbb06b…), (fd:fd4dbb48…), (fd:370f8d27…), (fd:4fa9677f…), (fd:91359fc6…), (fd:613d7d84…), (fd:def40fd7…), Is Empty, State | — | — | — |
| Get Site Facilities | `(slc)facility_management` | (guid:dab0442b…) | Name, (fd:f08b42c7…), (fd:259e31ed…), (fd:37dbb06b…), (fd:fd4dbb48…), (fd:370f8d27…), (fd:4fa9677f…), (fd:91359fc6…), (fd:613d7d84…), (fd:def40fd7…), State | — | — | — |
| Get Sites selected Map | `(slc)facility_management` | (guid:5320914d…) | Name, State, (fd:e9485c2b…), ID, (fd:fd3feeaf…), (fd:3f7b64ea…) | — | — | — |
| P&B - Jobs - Base | `(slc)plan_and_build` | (guid:01bfa461…) | Name, (fd:e90b9377…), (fd:30deab28…), (fd:124ee700…), (fd:c2f4bfb8…), (fd:ae07a73c…), (fd:a92163d0…), (fd:fe73ef98…), (fd:5176adad…), Location, ID, LastModified, LastModifiedBy, CreatedAt, CreatedBy, DefinitionID, State, (fd:f73d9198…), (fd:2cf0ad38…), (fd:50ff0baa…) | — | — | — |
| P&B - Jobs - All - Table | `(slc)plan_and_build` | (guid:447da12d…) | Name, (fd:aee7d6e1…), ID | — | — | — |
| PO - People - Base | `(slc)people_organizations` | (guid:1624a01d…) | Name, ID | — | — | — |
| PO - Teams - Base | `(slc)people_organizations` | (guid:5150bc87…) | Name, ID | — | — | — |
| P&B - Jobs - Details - Job | `(slc)plan_and_build` | (guid:01bfa461…) | Name, (fd:e90b9377…), (fd:30deab28…), (fd:c2f4bfb8…), (fd:ae07a73c…), (fd:a92163d0…), (fd:fe73ef98…), (fd:5176adad…), LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:f73d9198…), (fd:2cf0ad38…), (fd:124ee700…), (fd:50ff0baa…) | — | — | — |
| P&B - Jobs - Most recent jobs | `(slc)plan_and_build` | (guid:01bfa461…) | Name, (fd:ae07a73c…), (fd:27b85f20…), (fd:a92163d0…), (fd:fe73ef98…), (fd:f73d9198…), ID, State, (fd:2cf0ad38…) | — | — | — |
| P&B - Jobs - Starting jobs | `(slc)plan_and_build` | (guid:01bfa461…) | Name, (fd:ae07a73c…), (fd:27b85f20…), (fd:a92163d0…), (fd:fe73ef98…), (fd:f73d9198…), ID, State, (fd:2cf0ad38…) | — | — | — |
| P&B - Jobs - Details - Job (1) Timeline | `(slc)plan_and_build` | (guid:01bfa461…) | Name, (fd:e90b9377…), (fd:30deab28…), (fd:124ee700…), (fd:c2f4bfb8…), (fd:ae07a73c…), (fd:27b85f20…), (fd:a92163d0…), (fd:fe73ef98…), (fd:5176adad…), LastModified, LastModifiedBy, CreatedAt, CreatedBy, State, (fd:f73d9198…), (fd:2cf0ad38…) | — | — | — |
| Get Locations | `(slc)facility_management` | (guid:a09ef2ae…), (guid:dab0442b…), (guid:9bbb18c2…) | ID, Name | — | — | — |
| P&B - Get All Job Types | `(slc)plan_and_build` | (guid:447da12d…) | Name, (fd:0da5e09c…), (fd:aee7d6e1…) | — | — | — |

## Scanner notes

- **Pattern A (FleetOps-style)**: modules resolved from `new DomCache/DomHelper(..., "moduleId")` in code.
  Fields via `GetSectionDefinitionByName` / `GetFieldDescriptorByName` / `GetFieldValue<T>`.
- **Pattern B (InfraOps-style)**: modules + schema from `DomIds.cs` / `GeneratedDomIds.cs`.
  Access via `ModuleClass.Sections.SectionName.FieldName` typed constants.
- **Pre-filter**: only .cs files containing DOM-related keywords are deep-scanned.
- **Direct access**: Backend = accessed in C# code; Frontend = queried by LCA GQI; None = defined but not accessed.
- **Created by**: JSON = in install JSON; code = in DomIds.cs or code-create patterns; ⚠️ = code-accessed but not in install package.
- **LCA field mapping**: fields from all sections linked to the queried definition are marked Frontend.
  For typed-pattern modules without JSON section links, all fields of the module are considered reachable.
