# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-28
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules accessed**: 3 (1 owned, 2 cross-solution reference)

---

## Module: `(slc)fleet_ops` _(owned)_ — _schema from install JSON_

### Sections accessed

#### `ChargingData`

| Field | Type |
|-------|------|
| Address | String |
| ChargingBookingId | String |
| ChargingSpeed | Double |
| Cost | Double |
| EndSoc | Double |
| EndTime | DateTime |
| Energy | Double |
| EnergyInBattery | Double |
| Latitude | Double |
| Longitude | Double |
| Mileage | Double |
| PriceFromApp | Boolean |
| Reimbursement | Boolean |
| Source | String |
| StartSoc | Double |
| StartTime | DateTime |
| Type | Int32 |

#### `Contract info`

| Field | Type |
|-------|------|
| Driver | Guid |
| End date | DateTime |
| Start date | DateTime |

#### `Financial info`

| Field | Type |
|-------|------|
| BIK | Double |
| CO2 tax | Double |
| Fiscal value | Double |
| Lease cost | Double |
| Tax deductibility | Double |

#### `Monitoring info`

| Field | Type |
|-------|------|
| Clearance id | String |
| Monitoring level | Int32 |
| Monitoring state | Int32 |

#### `Pricing`

| Field | Type |
|-------|------|
| Address | String |
| Charging Type | Int32 |
| Cost | Double |
| End | DateTime |
| Reimbursement | Boolean |
| Start | DateTime |
| Type | Int32 |
| User | Guid |

#### `Vehicle info`

| Field | Type |
|-------|------|
| License plate | String |
| Make | Int32 |
| Status | Int32 |
| VIN | String |

#### `VehicleId`

| Field | Type |
|-------|------|
| Id | String |

---

## Module: `(slc)people_organizations` _(cross-solution reference)_ — _fields from code scan_

### Sections accessed

#### `Contract info`

| Field | Type |
|-------|------|
| Driver | — |

#### `Vehicle info`

| Field | Type |
|-------|------|
| VIN | — |

---

## Module: `(slc)workflow` _(cross-solution reference)_ — _fields from code scan_

### Sections accessed

#### `Job info`

| Field | Type |
|-------|------|
| Job end | DateTime |
| Job name | String |
| Job start | DateTime |

---

## Direct DOM access from Low-Code App

> ⚠️ **These queries bypass the solution API and access DOM storage directly from the UI.**  
> Prefer reading data through UDAPI/GQI data sources exposed by the solution.

| Query name | Module | DOM Definition |
|------------|--------|---------------|
| Fleet - Vehicle Info | `(slc)fleet_ops` | Vehicles |
| Pricing - Table View | `(slc)fleet_ops` | Pricing |
| Get DOM Instances | `(slc)fleet_ops` | Vehicles |
| Debug - ChargingData | `(slc)fleet_ops` | ChargingData |

## Scanner notes

- **Owned module schema** (`(slc)fleet_ops`): sourced from install JSON (`DOM.zip`) — complete.
- **Cross-solution modules**: sourced from code scan of DomCache/DomHelper variable assignments.
  Field types are not available for cross-solution modules (not in this repo's install JSON).
- **Limitation**: calls through higher-level helper objects (e.g. `fleetOpsHelper.GetFieldValue(...)`) 
  are not traced when the helper wraps a DomCache internally. These are covered by the install JSON for owned modules.
