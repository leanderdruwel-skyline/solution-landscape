# SLC-S-InfraOps — API Surface

**Solution:** InfraOps (Infrastructure Operations)
**Repository:** [SkylineCommunications/SLC-S-InfraOps](https://github.com/SkylineCommunications/SLC-S-InfraOps)
**Analysed version:** 1.0.0 (assembly 2026.0506.1232.30588)
**Analysed on:** 2026-05-22

---

## Result: Typed API Objects Found — 7 objects across 2 packages

No `I*ApiHelper.cs` was found in the InfraOps solution source itself. The typed API surface is entirely provided through two NuGet packages referenced by `InfraOps.Common`.

---

## API Objects

### Package: `Skyline.DataMiner.SDM.Ticketing` v1.0.2

**Interface:** [`ITicketingApiHelper`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/ITicketingApiHelper.cs)
**GitHub source:** [SkylineCommunications/SLC-S-Ticketing-Nuget](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget)

| Property Name | Repository Type | Model Type | Model Defined In |
|---|---|---|---|
| `Tickets` | `IObservableRepository<Ticket>` | `Ticket` | [`API.Common/Models/Ticket.cs`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/Models/Ticket.cs) |
| `TicketTypes` | `IObservableRepository<TicketType>` | `TicketType` | [`API.Common/Models/TicketType.cs`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/Models/TicketType.cs) |
| `Attachments` | `IObservableRepository<TicketAttachment>` | `TicketAttachment` | [`API.Common/Models/TicketAttachment.cs`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/Models/TicketAttachment.cs) |
| `AffectedResources` | `IObservableRepository<TicketAffectedResource>` | `TicketAffectedResource` | [`API.Common/Models/TicketAffectedResource.cs`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/Models/TicketAffectedResource.cs) |
| `Notes` | `IObservableRepository<TicketNote>` | `TicketNote` | [`API.Common/Models/TicketNote.cs`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/Models/TicketNote.cs) |
| `ExternalOwners` | `IObservableRepository<ExternalOwner>` | `ExternalOwner` | [`API.Common/Models/ExternalOwner.cs`](https://github.com/SkylineCommunications/SLC-S-Ticketing-Nuget/blob/main/API.Common/Models/ExternalOwner.cs) |

---

### Package: `Skyline.DataMiner.SDM.ObjectLinking.Common` v2.0.1

**Entry point:** [`ObjectLinker`](https://github.com/SkylineCommunications/SLC-SDM-ObjectLinking/blob/main/API.Common/ObjectLinker.cs) (concrete class — no `I*ApiHelper` interface)
**GitHub source:** [SkylineCommunications/SLC-SDM-ObjectLinking](https://github.com/SkylineCommunications/SLC-SDM-ObjectLinking)

| Property Name | Repository Type | Model Type | Model Defined In |
|---|---|---|---|
| `Links` | `IBulkRepository<Link>` | `Link` | [`API.Common/Models/Link.cs`](https://github.com/SkylineCommunications/SLC-SDM-ObjectLinking/blob/main/API.Common/Models/Link.cs) |

> **Note:** `ObjectLinker` is a concrete class, not an interface matching the `I*ApiHelper` pattern. It still qualifies as a typed API surface as `Links` is a public `IBulkRepository<Link>` property.

---

## What was checked

| Location | What was searched | Found? |
|---|---|---|
| Solution source (`**/*.cs`) | `I*ApiHelper.cs` filename | ❌ No |
| Solution source (`**/*.cs`) | `IRepository<T>` / `IBulkRepository<T>` / `IObservableRepository<T>` usage | ❌ No |
| `~/.nuget/packages/skyline.dataminer.sdm.ticketing/` | NuGet XML docs for `I*Api`/`I*ApiHelper` | ❌ Not in local cache |
| `~/.nuget/packages/skyline.dataminer.sdm.objectlinking.common/` | NuGet XML docs for `I*Api`/`I*ApiHelper` | ❌ Not in local cache |
| `SkylineCommunications/SLC-S-Ticketing-Nuget` → `API.Common/` | `ITicketingApiHelper.cs` | ✅ Found — 6 repository properties |
| `SkylineCommunications/SLC-SDM-ObjectLinking` → `API.Common/` | `ObjectLinker.cs` | ✅ Found — 1 repository property (concrete class) |

## DOM-managed objects (out of scope, for reference)

InfraOps manages its own domain objects via DOM modules:

| Module | Entities |
|---|---|
| `asset-management` | Asset, AssetClass, Port, Connection, DeviceType, CableType, PortType |
| `facility-management` | Site, Facility, Floor, Room, Row, Rack, Zone, Desk |
| `field-operations` | (field-op assets and transfers) |
| `plan-and-build` | Job, JobType |
| `people-organizations` | (people, organizations, cost & billing) |

These are accessed via `DomHelper` directly and are out of scope for the typed API landscape.

---

> ✅ **7 typed API objects found** across 2 packages (`Ticketing`: 6, `ObjectLinking`: 1).
