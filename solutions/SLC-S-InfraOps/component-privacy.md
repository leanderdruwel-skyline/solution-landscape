# Component Privacy Check — SLC-S-InfraOps
**Date**: 2026-05-22
**Mode**: report-only

## Pre-Run Discovery
- Existing issue: https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/73
- Existing PR: https://github.com/SkylineCommunications/SLC-S-InfraOps/pull/64

## Repository Visibility
Private GitHub repository (`private: true`).

## Manifests Found
| Manifest Path | Type | Classification | isHidden | Status |
|---------------|------|----------------|----------|--------|
| `SLC-S-InfraOps/CatalogInformation/manifest.yml` | `Standard Solution` | Main solution package | not set | [PASS] |
| `SLC-S-InfraOps-CleanSystem/CatalogInformation/manifest.yml` | `Custom Solution` | Sub-component solution package | not set | [ERROR] |
| `SLC-S-InfraOps-Demo-Data/CatalogInformation/manifest.yml` | `Custom Solution` | Sub-component solution package | not set | [ERROR] |
| `SLC-S-InfraOps-FieldOperations-AddOns/CatalogInformation/manifest.yml` | `Custom Solution` | Sub-component solution package | not set | [ERROR] |
| `SLC-S-InfraOps-RT/CatalogInformation/manifest.yml` | `Custom Solution` | Sub-component solution package | not set | [ERROR] |
| `SLC-S-InfraOps-Vodafone-AddOns/CatalogInformation/manifest.yml` | `Custom Solution` | Sub-component solution package | not set | [ERROR] |
| `SLC-S-InfraOps-WithDependencies/CatalogInformation/manifest.yml` | `Custom Solution` | Sub-component solution package | not set | [ERROR] |

## Findings
| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1 | Repository visibility | [INFO] | The GitHub repository is private, but Catalog visibility is still controlled per manifest. |
| 2 | Main solution manifest | [PASS] | `SLC-S-InfraOps/CatalogInformation/manifest.yml` is the main package and is not hidden. |
| 3 | CleanSystem privacy | [ERROR] | `SLC-S-InfraOps-CleanSystem/CatalogInformation/manifest.yml` does not set `registrationOptions.isHidden: true`. |
| 4 | Demo Data privacy | [ERROR] | `SLC-S-InfraOps-Demo-Data/CatalogInformation/manifest.yml` does not set `registrationOptions.isHidden: true`. |
| 5 | FieldOperations AddOns privacy | [ERROR] | `SLC-S-InfraOps-FieldOperations-AddOns/CatalogInformation/manifest.yml` does not set `registrationOptions.isHidden: true`. |
| 6 | RT privacy | [ERROR] | `SLC-S-InfraOps-RT/CatalogInformation/manifest.yml` does not set `registrationOptions.isHidden: true`. |
| 7 | Vodafone AddOns privacy | [ERROR] | `SLC-S-InfraOps-Vodafone-AddOns/CatalogInformation/manifest.yml` does not set `registrationOptions.isHidden: true`. |
| 8 | WithDependencies privacy | [ERROR] | `SLC-S-InfraOps-WithDependencies/CatalogInformation/manifest.yml` does not set `registrationOptions.isHidden: true`. |
| 9 | Existing privacy issue | [INFO] | Open issue already exists: https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/73 |
| 10 | Existing keyword-matching PR | [WARNING] | Open PR matched the pre-run keyword search: https://github.com/SkylineCommunications/SLC-S-InfraOps/pull/64 |

**Result: 6 error(s) · 1 warning(s)**