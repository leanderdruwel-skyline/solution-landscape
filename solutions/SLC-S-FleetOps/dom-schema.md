# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-29
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules accessed**: 3 (1 owned, 2 cross-solution reference)

---

## Module: `(slc)fleet_ops` _(owned)_ — _schema from install JSON_

### Sections accessed

#### `ChargingData`

| Field | Type | Source |
|-------|------|--------|
| Address | String | JSON only |
| ChargingBookingId | String | JSON only |
| ChargingSpeed | Double | JSON only |
| Cost | Double | JSON only |
| EndSoc | Double | JSON only |
| EndTime | DateTime | JSON + code |
| Energy | Double | JSON only |
| EnergyInBattery | Double | JSON only |
| Latitude | Double | JSON only |
| Longitude | Double | JSON only |
| Mileage | Double | JSON only |
| PriceFromApp | Boolean | JSON only |
| Reimbursement | Boolean | JSON only |
| Source | String | JSON only |
| StartSoc | Double | JSON only |
| StartTime | DateTime | JSON + code |
| Type | Int32 | JSON only |

#### `Contract info`

| Field | Type | Source |
|-------|------|--------|
| Driver | Guid | JSON only |
| End date | DateTime | JSON only |
| Start date | DateTime | JSON only |

#### `Financial info`

| Field | Type | Source |
|-------|------|--------|
| BIK | Double | JSON only |
| CO2 tax | Double | JSON only |
| Fiscal value | Double | JSON only |
| Lease cost | Double | JSON only |
| Tax deductibility | Double | JSON only |

#### `Monitoring info`

| Field | Type | Source |
|-------|------|--------|
| Clearance id | String | JSON only |
| Monitoring level | Int32 | JSON only |
| Monitoring state | Int32 | JSON only |

#### `Pricing`

| Field | Type | Source |
|-------|------|--------|
| Address | String | JSON only |
| Charging Type | Int32 | JSON only |
| Cost | Double | JSON only |
| End | DateTime | JSON only |
| Reimbursement | Boolean | JSON only |
| Start | DateTime | JSON only |
| Type | Int32 | JSON only |
| User | Guid | JSON only |

#### `Vehicle info`

| Field | Type | Source |
|-------|------|--------|
| License plate | String | JSON only |
| Make | Int32 | JSON only |
| Status | Int32 | JSON + code |
| VIN | String | JSON + code |

#### `VehicleId`

| Field | Type | Source |
|-------|------|--------|
| Id | String | JSON only |

---

## Module: `(slc)people_organizations` _(cross-solution reference)_ — _fields from code scan_

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
