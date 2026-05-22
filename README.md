# DataMiner Standard Solutions Landscape

## 📊 Live Matrix Dashboard

**➡️ [leanderdruwel-skyline.github.io/solution-landscape](https://leanderdruwel-skyline.github.io/solution-landscape/)**

Traffic-light matrix showing the status of all `standard-solution` repos across **22 checks** in 6 categories.

---

## Check Categories

| Category | Checks | Active Agents |
|---|---|---|
| 📄 Documentation | Catalog Doc, Source README, Release Notes | `catalog-doc-checker`, `readme-writer`, `rn-write` |
| 🏗 Architecture | SDM Compliance, Storage/DOM Objects, SRM Resources*, Inter-Solution Refs* | `sdm-compliance-checker`, `sdm-api-objects` |
| 🔌 API Surface | Typed API Objects, GQI/UDAPI*, NuGet Devpack*, Component Privacy | `solution-api-surface-mapper`, `component-privacy-checker` |
| 🧪 Quality | Naming Convention, Tests*, CI/CD*, Dependency Health*, Health & Freshness* | `naming-convention-check` |
| 🖥 UX & Experience | Low-Code App*, Demo Mode*, LCA UX Audit | `dataminer-ux-audit` |
| ⚙️ Process | Product Owner*, Active Backlog, Catalog Published* | `issue-triage` |

`*` = agent planned, not yet built

---

## Data Format

Agent results are written to [`matrix-data.json`](./matrix-data.json). To update a check result:

```json
{
  "solutions": [{
    "id": "SLC-S-<Name>",
    "checks": {
      "<check-id>": {
        "status": "pass | partial | fail | unknown",
        "note": "Human-readable finding",
        "prUrl": "https://github.com/.../pull/N",
        "issueUrl": "https://github.com/.../issues/N",
        "reportUrl": "https://github.com/.../blob/main/solutions/...",
        "updatedAt": "YYYY-MM-DD"
      }
    }
  }]
}
```

---

## Solutions

| Solution | Repository | API Surface Report |
|---|---|---|
| InfraOps | [SLC-S-InfraOps](https://github.com/SkylineCommunications/SLC-S-InfraOps) | *(report coming)* |
| SatOps | [SLC-S-SatOps](https://github.com/SkylineCommunications/SLC-S-SatOps) | [SLC-S-SatOps.md](./solutions/SLC-S-SatOps.md) |
| MediaOps Plan | [SLC-S-MediaOps.Plan](https://github.com/SkylineCommunications/SLC-S-MediaOps.Plan) | — |
| MediaOps Live | [SLC-S-MediaOps.Live](https://github.com/SkylineCommunications/SLC-S-MediaOps.Live) | — |
| Ticketing | [SLC-S-Ticketing](https://github.com/SkylineCommunications/SLC-S-Ticketing) | — |
| IP Network Explorer | [SLC-S-IpNetworkExplorer](https://github.com/SkylineCommunications/SLC-S-IpNetworkExplorer) | — |
| DocumentHub | [SLC-S-DocumentHub](https://github.com/SkylineCommunications/SLC-S-DocumentHub) | — |
| Service Management | [SLC-S-Service-Management](https://github.com/SkylineCommunications/SLC-S-Service-Management) | — |
| FleetOps | [SLC-S-FleetOps](https://github.com/SkylineCommunications/SLC-S-FleetOps) | — |
| Relationships | [SLC-S-Relationships](https://github.com/SkylineCommunications/SLC-S-Relationships) | — |