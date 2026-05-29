# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-29
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules accessed**: 3 (1 installed by this solution, 2 not installed here)

---

## Module: `(slc)fleet_ops`
**Created by**: JSON — _schema from install JSON + code scan_

### Sections accessed

#### `ChargingData`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Address | String | Backend | JSON |
| ChargingBookingId | String | Backend | JSON |
| ChargingSpeed | Double | Backend | JSON |
| ConnectionFee | — | Backend | ⚠️ not in install package |
| Cost | Double | Backend | JSON |
| EndSoc | Double | Backend | JSON |
| EndTime | DateTime | Backend | JSON |
| Energy | Double | Backend | JSON |
| EnergyCost | — | Backend | ⚠️ not in install package |
| EnergyInBattery | Double | Backend | JSON |
| Latitude | Double | Backend | JSON |
| Longitude | Double | Backend | JSON |
| Mileage | Double | Backend | JSON |
| PriceFromApp | Boolean | Backend | JSON |
| Reimbursement | Boolean | Backend | JSON |
| Source | String | Backend | JSON |
| StartSoc | Double | Backend | JSON |
| StartTime | DateTime | Backend | JSON |
| TimeFee | — | Backend | ⚠️ not in install package |
| Type | Int32 | Backend | JSON |

#### `Contract info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Driver | Guid | Backend | JSON |
| End date | DateTime | Backend | JSON |
| Start date | DateTime | Backend | JSON |

#### `Financial info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| BIK | Double | Backend | JSON |
| CO2 tax | Double | Backend | JSON |
| Fiscal value | Double | Backend | JSON |
| Lease cost | Double | Backend | JSON |
| Tax deductibility | Double | Backend | JSON |

#### `Monitoring info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Clearance id | String | Backend | JSON |
| Monitoring level | Int32 | Backend | JSON |
| Monitoring state | Int32 | Backend | JSON |

#### `Pricing`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Address | String | None | JSON |
| Charging Type | Int32 | None | JSON |
| Cost | Double | None | JSON |
| End | DateTime | None | JSON |
| Reimbursement | Boolean | None | JSON |
| Start | DateTime | None | JSON |
| Type | Int32 | None | JSON |
| User | Guid | None | JSON |

#### `Vehicle info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| License plate | String | Backend | JSON |
| Make | Int32 | Backend | JSON |
| Status | Int32 | Backend | JSON |
| VIN | String | Backend | JSON |

#### `VehicleId`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Id | String | Backend | JSON |

---

## Module: `(slc)people_organizations`
**Created by**: not installed here — _fields from code scan only_

### Sections accessed

#### `Contact info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Email | — | Backend | None |

#### `People information`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Full name | — | Backend | None |

#### `Team`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Team | Guid | Backend | None |

---

## Module: `(slc)workflow`
**Created by**: not installed here — _fields from code scan only_

### Sections accessed

#### `Job info`

| Field | Type | Direct access | Created by |
|-------|------|---------------|------------|
| Job end | DateTime | Backend | None |
| Job name | String | Backend | None |
| Job start | DateTime | Backend | None |

---

## Direct DOM access from Low-Code App

> ⚠️ **These queries bypass the solution API and access DOM storage directly from the UI.**  
> Prefer reading data through UDAPI/GQI data sources exposed by the solution.

| Query name | Module | Definitions | Columns selected | Join module | Join definitions | Join columns |
|------------|--------|-------------|-----------------|-------------|-----------------|--------------|
| Fleet - Vehicle Info | `(slc)fleet_ops` | Vehicles | (fd:c8257ec1…), Name, (fd:02e0ad14…), (fd:fda2373c…), (fd:61771564…), ID, (fd:4c4508c2…), (fd:5f6ddb66…), Connectivity, Request, Consumption | — | — | — |
| Pricing - Table View | `(slc)fleet_ops` | Pricing | Name, (fd:39ffda91…), (fd:5f95f666…), (fd:90073dd0…), (fd:1ec670dc…), (fd:0acb352e…), (fd:e99e83e1…), (fd:1621fd7d…), (fd:a48a361c…) | — | — | — |
| Get DOM Instances | `(slc)fleet_ops` | Vehicles | (all) | — | — | — |
| Debug - ChargingData | `(slc)fleet_ops` | ChargingData | (all) | — | — | — |

## Scanner notes

- **Modules installed by this solution** (`(slc)fleet_ops`): schema sourced from install JSON (`DOM.zip`) merged with code scan.
  Fields in code but not in install JSON are flagged as `⚠️ code only`.
- **Modules not installed here**: sourced from code scan only (DomCache/DomHelper variable assignments).
  Module IDs resolved from string literals, `const string` references, and class property initializers.
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
