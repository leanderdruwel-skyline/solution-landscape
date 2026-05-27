# DOM Schema — SLC-S-FleetOps
**Generated**: 2026-05-27
**Repository**: https://github.com/SkylineCommunications/SLC-S-FleetOps
**Modules found**: 1

---

## Module: `(slc)fleet_ops`

> **Source**: `SLC-FleetOps/SetupContent/DOM.zip/module.json`

### DOM Definitions

| Definition | Sections linked |
|------------|----------------|
| ChargingData | ChargingData, VehicleId |
| Pricing | Pricing |
| Vehicles | Vehicle info, Financial info, Contract info, Monitoring info |

### Section Definitions

#### `ChargingData`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| ChargingBookingId | String | — | — |
| Energy | Double | — | — |
| EnergyInBattery | Double | ✅ | — |
| ChargingSpeed | Double | — | — |
| Cost | Double | ✅ | — |
| Type | Int32 | — | — |
| StartTime | DateTime | — | — |
| EndTime | DateTime | — | — |
| Reimbursement | Boolean | — | — |
| PriceFromApp | Boolean | — | — |
| Address | String | ✅ | — |
| Mileage | Double | ✅ | — |
| StartSoc | Double | ✅ | — |
| EndSoc | Double | ✅ | — |
| Latitude | Double | ✅ | — |
| Longitude | Double | ✅ | — |
| Source | String | ✅ | — |

#### `Contract info`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| Driver | Guid | ✅ | — |
| Start date | DateTime | ✅ | — |
| End date | DateTime | ✅ | — |

#### `Financial info`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| CO2 tax | Double | ✅ | — |
| Tax deductibility | Double | ✅ | — |
| BIK | Double | ✅ | — |
| Fiscal value | Double | ✅ | — |
| Lease cost | Double | ✅ | — |

#### `Monitoring info`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| Monitoring state | Int32 | ✅ | — |
| Monitoring level | Int32 | ✅ | — |
| Clearance id | String | ✅ | — |

#### `Pricing`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| Cost | Double | — | — |
| Start | DateTime | — | — |
| End | DateTime | — | — |
| User | Guid | ✅ | — |
| Charging Type | Int32 | — | — |
| Type | Int32 | ✅ | — |
| Reimbursement | Boolean | ✅ | — |
| Address | String | ✅ | — |

#### `Vehicle info`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| VIN | String | — | — |
| Make | Int32 | ✅ | — |
| License plate | String | ✅ | — |
| Status | Int32 | ✅ | — |

#### `VehicleId`

| Field | Type | Optional | Hidden |
|-------|------|----------|--------|
| Id | String | — | — |

---
