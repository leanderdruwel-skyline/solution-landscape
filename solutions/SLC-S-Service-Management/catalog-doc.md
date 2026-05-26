# Catalog Documentation Check — SLC-S-Service-Management
**Date**: 2026-05-26
**Mode**: report-only

## Pre-Run Discovery
- Existing issue: None
- Existing PR: None

## Findings
| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1 | Required section ## About | PASS | Present in SLC-Service-Management/CatalogInformation/README.md. |
| 2 | Required section ## Key Features and max 5 items | PASS | Present with 4 feature subsections. |
| 3 | Required section ## Use Cases | PASS | Present. |
| 4 | Recommended section ## Prerequisites | PASS | Present. |
| 5 | At least 1 screenshot/image | PASS | Multiple images are embedded in the README. |
| 6 | Forbidden content | ERROR | README contains contact details via 	eam.product.marketing@skyline.be under ## Technical Reference. |
| 7 | Section heading standards | PASS | Required standard headings are used; no non-standard replacement headings detected. |
| 8 | documentation_url in manifest.yml | WARNING | documentation_url is empty. |
| 9 | Manifest tags quality | PASS | Tags are descriptive and do not just repeat the solution name. |

**Result: 1 error(s) · 1 warning(s)**