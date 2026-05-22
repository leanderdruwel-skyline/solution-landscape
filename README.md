# DataMiner Solution Landscape

This repository maps DataMiner solution integration surfaces, including **typed APIs** and **DOM storage structures** when no typed API helper exists.

## Purpose

Build a full landscape of inter-solution object dependencies, eventually feeding into a central **Solution Registration** element on a DataMiner system.

## Structure

```
solutions/
  <repo-name>.md    # One file per analysed solution
```

## Solutions

| Solution | Repository | Coverage | Status |
|----------|-----------|----------|--------|
| SLC-S-SatOps | [SkylineCommunications/SLC-S-SatOps](https://github.com/SkylineCommunications/SLC-S-SatOps) | API scan only | ⚠️ No typed API found; DOM-only storage noted |
| SLC-S-InfraOps | [SkylineCommunications/SLC-S-InfraOps](https://github.com/SkylineCommunications/SLC-S-InfraOps) | Typed API + DOM storage map | ✅ 6 typed API objects; 4 setup modules mapped (+5 referenced modules) |
