# API Surface Check — SLC-S-InfraOps
**Date**: 2026-05-22
**Mode**: report-only

## Pre-Run Discovery
- Existing issue: https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/65, https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/73
- Existing PR: https://github.com/SkylineCommunications/SLC-S-InfraOps/pull/13

## Discovered API Objects
Asset, AssetClass, CableType, Connection, DataPort, DeviceType, History, Holder, PortType, PowerPort, Reservation, Desk, Facility, Floor, Rack, Room, Row, Site, Zone, Job, JobType

Utility-only GQI sources excluded from the object matrix: VersionInfo, StateActions, Statistics, AppSettings, cable-length/placement/ratio helpers.

## GQI Projects
- **InfraOps.GQI.AssetManager** — Asset, AssetClass, CableType, Connection, DeviceType, History, Holder, PortType, DataPort, PowerPort, plus utility sources.
- **InfraOps.GQI.Common** — VersionInfo only.
- **InfraOps.GQI.FacilityManager** — Facility, Rack, Zone, plus utility sources (room ratio, placements, statistics, app settings, cable length).
- **InfraOps.GQI.FieldOperations** — Asset (filtered/selected assets).
- **InfraOps.GQI.PlanAndBuild** — Job, plus utility sources (statistics, state actions, job-location operator).

## Per-Object Status
| Object | Typed Model | IApiHelper | GQI Source | UDAPI | Tests |
|--------|-------------|------------|------------|-------|-------|
| Asset | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| AssetClass | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| CableType | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| Connection | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| DataPort | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| DeviceType | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| History | ✅ | ⚠️ | ✅ | ❌ | ⚠️ |
| Holder | ✅ | ⚠️ | ✅ | ❌ | ⚠️ |
| PortType | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| PowerPort | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| Reservation | ✅ | ⚠️ | ⚠️ | ❌ | ✅ |
| Desk | ✅ | ⚠️ | ⚠️ | ❌ | ✅ |
| Facility | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| Floor | ✅ | ⚠️ | ⚠️ | ❌ | ✅ |
| Rack | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| Room | ✅ | ⚠️ | ⚠️ | ❌ | ✅ |
| Row | ✅ | ⚠️ | ⚠️ | ❌ | ✅ |
| Site | ✅ | ⚠️ | ⚠️ | ❌ | ⚠️ |
| Zone | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| Job | ✅ | ⚠️ | ✅ | ❌ | ✅ |
| JobType | ✅ | ⚠️ | ⚠️ | ❌ | ✅ |

## Findings
| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1 | Pre-run discovery | INFO | Open search hits: issues #65 and #73, plus PR #13. |
| 2 | Typed models | PASS | Found strongly typed definitions/wrappers for 21 domain objects in `InfraOpsShared`. |
| 3 | CRUD wrapper layer | PASS | Representative wrappers (`AssetWrapper`, `RackWrapper`, `JobWrapper`, `JobTypeWrapper`) inherit `DomInstanceWrapper`; `DomInstanceWrapper` provides `Save()`, and wrappers expose `HandlerCRUD`. |
| 4 | IApiHelper abstraction | WARNING | No repo-local `IApiHelper` interface or typed repository properties were found; only unrelated `UserDefinableApiHelper` / `ITicketingApiHelper` references appear. |
| 5 | GQI coverage | WARNING | No dedicated object-level GQI source was found for Reservation, Desk, Floor, Room, Row, Site, or JobType. |
| 6 | UDAPI coverage | INFO | No `[UDApiObject]` attribute or other UDAPI registration was found anywhere in the repository. |
| 7 | Unit tests | WARNING | No direct API-focused coverage was found for History, Holder, or Site. |
| 8 | GQI project alignment | WARNING | `InfraOps.GQI.AssetManager`, `InfraOps.GQI.FieldOperations`, and `InfraOps.GQI.PlanAndBuild` align with the wrapper layer; `InfraOps.GQI.FacilityManager` only directly exposes Facility/Rack/Zone while several facility-domain objects remain utility-only or uncovered. |

**Result: 0 error(s) · 31 warning(s)**
