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

#### `Team`

| Field | Type |
|-------|------|
| _(section accessed; no individual fields captured)_ | — |

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

| Query name | Primary module | Definitions | Join module | Join definitions | Join columns |
|------------|----------------|-------------|-------------|-----------------|--------------|
| Fleet - Vehicle Info | `(slc)fleet_ops` | Vehicles | `(slc)people_organizations` | (guid:1624a01d…) | Name, ID |
| Pricing - Table View | `(slc)fleet_ops` | Pricing | — | — | — |
| Get DOM Instances | `(slc)fleet_ops` | Vehicles | — | — | — |
| Debug - ChargingData | `(slc)fleet_ops` | ChargingData | — | — | — |

## Scanner notes

- **Owned module schema** (`(slc)fleet_ops`): sourced from install JSON (`DOM.zip`) — complete.
- **Cross-solution modules**: sourced from per-file code scan of DomCache/DomHelper variable assignments.
  Module IDs are resolved from both string literals and `const string` references.
- **Field types on cross-solution modules**: inferred from `GetFieldValue<T>` generic parameter.
- **Owned-section filter**: sections whose names match owned-module sections are excluded from
  cross-module attribution (prevents false attribution caused by variable shadowing in method parameters).
- **LCA joins**: the scanner recurses into Join→On sub-queries to capture both sides of a join,
  including column names selected from the joined source.
- **Definition GUID resolution**: definition names can only be resolved for modules installed by this
  solution (`(slc)fleet_ops`). GUIDs from cross-solution modules show as `(guid:…)` because resolving
  them requires reading the owning solution's install JSON.
- **Single-arg `GetFieldDescriptorByName`** (called on a section definition variable, not the DomCache)
  is not captured. Example: `teamSd.GetFieldDescriptorByName("Team")` — section is known (`Team`),
  field name and type require additional regex tracking of section-definition variables.
- **Higher-level wrapper helpers** (e.g. `fleetOpsHelper.GetFieldValue(...)`) cannot be traced via
  variable names alone. These are covered by the owned module install JSON.
