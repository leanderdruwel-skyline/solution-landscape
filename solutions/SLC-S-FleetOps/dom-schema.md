# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-29
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules accessed**: 3 (1 installed by this solution, 2 not installed here)

---

## Module: `(slc)fleet_ops`
**Install method**: JSON — _schema from install JSON + code scan_

### Sections accessed

#### `ChargingData`

| Field | Type | Created by |
|-------|------|------------|
| Address | String | JSON |
| ChargingBookingId | String | JSON |
| ChargingSpeed | Double | JSON |
| ConnectionFee | — | ⚠️ not in install JSON |
| Cost | Double | JSON |
| EndSoc | Double | JSON |
| EndTime | DateTime | JSON |
| Energy | Double | JSON |
| EnergyCost | — | ⚠️ not in install JSON |
| EnergyInBattery | Double | JSON |
| Latitude | Double | JSON |
| Longitude | Double | JSON |
| Mileage | Double | JSON |
| PriceFromApp | Boolean | JSON |
| Reimbursement | Boolean | JSON |
| Source | String | JSON |
| StartSoc | Double | JSON |
| StartTime | DateTime | JSON |
| TimeFee | — | ⚠️ not in install JSON |
| Type | Int32 | JSON |

#### `Contract info`

| Field | Type | Created by |
|-------|------|------------|
| Driver | Guid | JSON |
| End date | DateTime | JSON |
| Start date | DateTime | JSON |

#### `Financial info`

| Field | Type | Created by |
|-------|------|------------|
| BIK | Double | JSON |
| CO2 tax | Double | JSON |
| Fiscal value | Double | JSON |
| Lease cost | Double | JSON |
| Tax deductibility | Double | JSON |

#### `Monitoring info`

| Field | Type | Created by |
|-------|------|------------|
| Clearance id | String | JSON |
| Monitoring level | Int32 | JSON |
| Monitoring state | Int32 | JSON |

#### `Pricing`

| Field | Type | Created by |
|-------|------|------------|
| Address | String | JSON |
| Charging Type | Int32 | JSON |
| Cost | Double | JSON |
| End | DateTime | JSON |
| Reimbursement | Boolean | JSON |
| Start | DateTime | JSON |
| Type | Int32 | JSON |
| User | Guid | JSON |

#### `Vehicle info`

| Field | Type | Created by |
|-------|------|------------|
| License plate | String | JSON |
| Make | Int32 | JSON |
| Status | Int32 | JSON |
| VIN | String | JSON |

#### `VehicleId`

| Field | Type | Created by |
|-------|------|------------|
| Id | String | JSON |

---

## Module: `(slc)people_organizations`
**Install method**: not installed here — _fields from code scan only_

### Sections accessed

#### `Contact info`

| Field | Type | Created by |
|-------|------|------------|
| Email | — | not installed here |

#### `People information`

| Field | Type | Created by |
|-------|------|------------|
| Full name | — | not installed here |

#### `Team`

| Field | Type | Created by |
|-------|------|------------|
| Team | Guid | not installed here |

---

## Module: `(slc)workflow`
**Install method**: not installed here — _fields from code scan only_

### Sections accessed

#### `Job info`

| Field | Type | Created by |
|-------|------|------------|
| Job end | DateTime | not installed here |
| Job name | String | not installed here |
| Job start | DateTime | not installed here |

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
