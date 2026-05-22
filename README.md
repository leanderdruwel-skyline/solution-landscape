# DataMiner Standard Solutions Landscape

## 📊 Live Matrix Dashboard

**➡️ [leanderdruwel-skyline.github.io/solution-landscape](https://leanderdruwel-skyline.github.io/solution-landscape/)**

Traffic-light matrix showing the quality status of all `standard-solution` repositories across a growing set of checks.

---

## How to get results displayed

Results are written to [`matrix-data.json`](./matrix-data.json) by Copilot agents. The dashboard fetches this file live on every page load — **no build step needed, just refresh the browser after an agent run**.

### Step 1 — Run a checker agent on a solution repo

In GitHub Copilot (CLI or chat), ask:

```
Run the catalog-doc-checker on SLC-S-MediaOps
```

By default agents run in **report-only mode**: they validate the solution repo (read-only), write a findings report here, and update the matrix. No issues or PRs are created in the solution repo unless you explicitly ask for assist mode:

```
Run the catalog-doc-checker on SLC-S-MediaOps in assist mode
```

### Step 2 — Refresh the dashboard

Open (or refresh) the [live dashboard](https://leanderdruwel-skyline.github.io/solution-landscape/). The new traffic-light cell appears immediately.

### Step 3 — Drill down

Click any cell in the matrix to open the detail panel — it shows the agent's full findings report and links to any issues or PRs that were created.

---

## Available agents

### Checker agents (produce traffic-light status)

These live in [`SkylineCommunications/_ReusableAgenticWorkflows/agents/`](https://github.com/SkylineCommunications/_ReusableAgenticWorkflows/tree/main/agents).

| Agent | What it checks | Matrix check ID |
|---|---|---|
| `catalog-doc-checker` | Quality of `CatalogInformation/README.md` | `catalog-doc` |
| `sdm-compliance-checker` | 3-tier SDM architecture (Foundational / Encapsulated / Federated) | `sdm-compliance` |
| `naming-convention-check` | Script, app, and dashboard naming conventions | `naming-convention` |
| `component-privacy-checker` | Sub-package catalog visibility (private vs public) | `component-privacy` |
| `api-objects-checker` | API object completeness (interface, CRUD, GQI, UDAPI, tests) | `api-objects` |

All checker agents support two modes:

| Mode | How to invoke | What happens |
|---|---|---|
| `report-only` *(default)* | Just run the agent | Writes report + updates matrix. Nothing touches the solution repo. |
| `assist` | Ask explicitly: *"… in assist mode"* | Same as above, plus creates/updates issues (and PRs where applicable) in the solution repo. |

### Mapper agents (discovery — no traffic light)

These live in [`leanderdruwel-skyline/_ReusableAgenticWorkflows/agents/`](https://github.com/leanderdruwel-skyline/_ReusableAgenticWorkflows/tree/main/agents). Mappers always write their output — there is no report-only/assist distinction.

| Agent | What it discovers | Output file |
|---|---|---|
| `solution-api-surface-mapper` | Typed API objects and helper interfaces | `solutions/<repo>/api-surface.md` |
| `solution-storage-mapper` | DOM modules and storage objects | `solutions/<repo>/storage-objects.md` |

Run the mapper first, then the `api-objects-checker` — the checker reuses the mapper's output rather than re-scanning from scratch.

---

## Report structure

Each agent run produces a Markdown report under `solutions/<REPO_NAME>/`:

```
solutions/
  SLC-S-InfraOps/
    api-surface.md          ← solution-api-surface-mapper
    api-objects.md          ← api-objects-checker
    catalog-doc.md          ← catalog-doc-checker
    component-privacy.md    ← component-privacy-checker
    naming-convention.md    ← naming-convention-check
    sdm-compliance.md       ← sdm-compliance-checker
```

Matrix status is stored in [`matrix-data.json`](./matrix-data.json). To manually set or correct a result:

```json
{
  "solutions": [{
    "id": "SLC-S-InfraOps",
    "checks": {
      "catalog-doc": {
        "status": "pass | partial | fail | unknown",
        "note": "One-line summary of key finding",
        "issueUrl": "https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/N",
        "reportUrl": "https://github.com/leanderdruwel-skyline/solution-landscape/blob/main/solutions/SLC-S-InfraOps/catalog-doc.md",
        "updatedAt": "YYYY-MM-DD"
      }
    }
  }]
}
```

---

## Future direction

> **This repo is intentionally transitional.**
>
> Today it serves a dual purpose: aggregated matrix view *and* storage for per-solution check reports. As the practice matures, the detailed findings for each solution (the `solutions/<repo>/` reports and agent outputs) will move into the solution repositories themselves — closer to the code and the team that owns it.
>
> When that happens, this repo becomes a **pure aggregation layer**: `matrix-data.json` remains here as the source of truth for the dashboard, but agents will write their detailed reports to the solution repo and only push the resulting status (`pass/partial/fail`) back here. The `Report Target` block in each agent controls exactly this — it is the only thing that needs updating when the switch happens.

---

## Solutions

| Solution | Repository |
|---|---|
| InfraOps | [SLC-S-InfraOps](https://github.com/SkylineCommunications/SLC-S-InfraOps) |
| SatOps | [SLC-S-SatOps](https://github.com/SkylineCommunications/SLC-S-SatOps) |
| MediaOps Plan | [SLC-S-MediaOps.Plan](https://github.com/SkylineCommunications/SLC-S-MediaOps.Plan) |
| MediaOps Live | [SLC-S-MediaOps.Live](https://github.com/SkylineCommunications/SLC-S-MediaOps.Live) |
| Ticketing | [SLC-S-Ticketing](https://github.com/SkylineCommunications/SLC-S-Ticketing) |
| IP Network Explorer | [SLC-S-IpNetworkExplorer](https://github.com/SkylineCommunications/SLC-S-IpNetworkExplorer) |
| DocumentHub | [SLC-S-DocumentHub](https://github.com/SkylineCommunications/SLC-S-DocumentHub) |
| Service Management | [SLC-S-Service-Management](https://github.com/SkylineCommunications/SLC-S-Service-Management) |
| FleetOps | [SLC-S-FleetOps](https://github.com/SkylineCommunications/SLC-S-FleetOps) |
| Relationships | [SLC-S-Relationships](https://github.com/SkylineCommunications/SLC-S-Relationships) |
