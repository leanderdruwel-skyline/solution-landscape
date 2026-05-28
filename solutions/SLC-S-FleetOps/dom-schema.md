# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-28
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules accessed**: 3 (1 owned, 2 cross-solution reference)

---

## Module: `(slc)fleet_ops` _(owned)_

### Sections accessed

#### `ChargingData`

| Field | Type |
|-------|------|
| Address | String |
| ChargingBookingId | String |
| ChargingSpeed | Double |
| ConnectionFee | — |
| Cost | Double |
| EndSoc | Double |
| EndTime | DateTime |
| Energy | Double |
| EnergyCost | — |
| EnergyInBattery | Double |
| Latitude | Double |
| Longitude | Double |
| Mileage | Double |
| PriceFromApp | Boolean |
| Reimbursement | Boolean |
| Source | String |
| StartSoc | Double |
| StartTime | DateTime |
| TimeFee | — |
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
| _(section accessed, no individual fields captured)_ | — |

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

## Module: `(slc)people_organizations` _(cross-solution reference)_

### Sections accessed

#### `Contact info`

| Field | Type |
|-------|------|
| Email | — |

#### `Job info`

| Field | Type |
|-------|------|
| _(section accessed, no individual fields captured)_ | — |

#### `People information`

| Field | Type |
|-------|------|
| Full name | — |

#### `Team`

| Field | Type |
|-------|------|
| _(section accessed, no individual fields captured)_ | — |

---

## Module: `(slc)workflow` _(cross-solution reference)_

### Sections accessed

#### `Contact info`

| Field | Type |
|-------|------|
| Email | — |

#### `Job info`

| Field | Type |
|-------|------|
| _(section accessed, no individual fields captured)_ | — |

#### `People information`

| Field | Type |
|-------|------|
| Full name | — |

#### `Team`

| Field | Type |
|-------|------|
| _(section accessed, no individual fields captured)_ | — |

---
