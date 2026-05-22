# DataMiner Solution API Landscape

This repository maps the **typed API surfaces** exposed by DataMiner solutions — objects available through a compiled API helper (DLL, NuGet devpack, or web API), **not** via raw DOM storage reads.

Solutions that expose data exclusively through DOM are tracked separately; they are not listed here until a typed `I<Module>ApiHelper` is introduced.

## Purpose

Build a full landscape of inter-solution object dependencies, eventually feeding into a central **Solution Registration** element on a DataMiner system.

## Structure

```
solutions/
  <repo-name>.md    # One file per analysed solution
```

## Solutions

| Solution | Repository | Typed API Objects | Status |
|----------|-----------|-------------------|--------|
| SLC-S-SatOps | [SkylineCommunications/SLC-S-SatOps](https://github.com/SkylineCommunications/SLC-S-SatOps) | — | ⚠️ DOM-only, no typed API yet |
