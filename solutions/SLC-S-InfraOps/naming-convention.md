# SLC-S-InfraOps -- Naming Convention

**Solution:** InfraOps
**Repository:** [SkylineCommunications/SLC-S-InfraOps](https://github.com/SkylineCommunications/SLC-S-InfraOps)
**Checked on:** 2026-05-22
**Agent:** naming-convention-check.agent.md

---

## Result: Fail -- 1 error, 2 warnings

### catalog / naming-convention-validation

| # | Check | Status | Notes |
|---|---|---|---|
| 1 | SOLCODE/SOLNAME discovery | Compliant | SOLCODE = IFO, SOLNAME = InfraOps |
| 2 | Automation script names | Non-compliant [ERROR] | 192/199 scripts missing SLC-[TYPE]-[name] pattern |
| 3 | Automation script folder placement | Non-compliant [WARNING] | 7 wrapper scripts have no folder metadata |
| 4 | Low-code app names | Non-compliant [WARNING] | Packaged low-code apps not named InfraOps |
| 5 | Dashboard names | N/A | No dashboard definitions found in repo |
| 6 | Ad hoc data source display names | N/A | No ad hoc data sources found |
| 7 | View names | N/A | No view definitions found in repo |
| 8 | Runtime-only components | INFO | Elements, Correlation rules must be validated manually on a live system |

**Result: 1 error, 2 warnings, 3 N/A**

### Priority Actions
1. Rename all Automation scripts to follow IFO-[TYPE]-[name] pattern (192 scripts)
2. Add folder metadata to the 7 wrapper scripts
3. Rename packaged low-code apps to InfraOps

### Issue
[#74 - Component naming convention validation findings](https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/74)
