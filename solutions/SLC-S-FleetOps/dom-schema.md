# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-29
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules accessed**: 3 (1 installed by this solution, 2 not installed here)

---

## Module: `(slc)fleet_ops` _(installed by this solution)_ — _schema from install JSON + code scan_

### Sections accessed

#### `ChargingData`

| Field | Type | Source |
|-------|------|--------|
| Address | String | install JSON + code |
| ChargingBookingId | String | install JSON + code |
| ChargingSpeed | Double | install JSON + code |
| ConnectionFee | — | ⚠️ code only (not in install JSON) |
| Cost | Double | install JSON + code |
| EndSoc | Double | install JSON + code |
| EndTime | DateTime | install JSON + code |
| Energy | Double | install JSON + code |
| EnergyCost | — | ⚠️ code only (not in install JSON) |
| EnergyInBattery | Double | install JSON + code |
| Latitude | Double | install JSON + code |
| Longitude | Double | install JSON + code |
| Mileage | Double | install JSON + code |
| PriceFromApp | Boolean | install JSON + code |
| Reimbursement | Boolean | install JSON + code |
| Source | String | install JSON + code |
| StartSoc | Double | install JSON + code |
| StartTime | DateTime | install JSON + code |
| TimeFee | — | ⚠️ code only (not in install JSON) |
| Type | Int32 | install JSON + code |

#### `Contract info`

| Field | Type | Source |
|-------|------|--------|
| Driver | Guid | install JSON + code |
| End date | DateTime | install JSON + code |
| Start date | DateTime | install JSON + code |

#### `Financial info`

| Field | Type | Source |
|-------|------|--------|
| BIK | Double | install JSON + code |
| CO2 tax | Double | install JSON + code |
| Fiscal value | Double | install JSON + code |
| Lease cost | Double | install JSON + code |
| Tax deductibility | Double | install JSON + code |

#### `Monitoring info`

| Field | Type | Source |
|-------|------|--------|
| Clearance id | String | install JSON + code |
| Monitoring level | Int32 | install JSON + code |
| Monitoring state | Int32 | install JSON + code |

#### `Pricing`

| Field | Type | Source |
|-------|------|--------|
| Address | String | install JSON only |
| Charging Type | Int32 | install JSON only |
| Cost | Double | install JSON only |
| End | DateTime | install JSON only |
| Reimbursement | Boolean | install JSON only |
| Start | DateTime | install JSON only |
| Type | Int32 | install JSON only |
| User | Guid | install JSON only |

#### `Vehicle info`

| Field | Type | Source |
|-------|------|--------|
| License plate | String | install JSON + code |
| Make | Int32 | install JSON + code |
| Status | Int32 | install JSON + code |
| VIN | String | install JSON + code |

#### `VehicleId`

| Field | Type | Source |
|-------|------|--------|
| Id | String | install JSON + code |

---

## Module: `(slc)people_organizations` _(not installed by this solution)_ — _fields from code scan only_

### Sections accessed

#### `Contact info`

| Field | Type |
|-------|------|
| Email | — |

#### `People information`

| Field | Type |
|-------|------|
| Full name | — |

#### `Team`

| Field | Type |
|-------|------|
| Team | Guid |

---

## Module: `(slc)workflow` _(not installed by this solution)_ — _fields from code scan only_

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
