# Naming Convention Check â€” SLC-S-InfraOps
**Date**: 2026-05-22
**Mode**: report-only

## Pre-Run Discovery
- Existing issue: https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/74
- Existing PR: None

## Discovered SOLCODE
No explicit 3-letter SOLCODE was documented in the repository root or README. The repo consistently uses the human-readable name `InfraOps` and module names like `Asset Manager` / `Facility Manager`. For this report I treated `IOP` as the most likely candidate abbreviation derived from `InfraOps`, but validation was based primarily on the names that actually exist in the repository.

Root-level folders discovered via `gh api /repos/SkylineCommunications/SLC-S-InfraOps/contents`: **207**

## Findings by Component Type
### Automation Scripts
| Component | Expected Pattern | Actual | Status |
|-----------|-----------------|--------|--------|
| Asset Manager - IDP - Interactive - Network Discovery | {ModuleName} - {Type} - {SubFunction} | Asset Manager - IDP - Interactive - Network Discovery | WARNING â€” extra non-standard token IDP |
| Asset Manager - ImportExport - Asset - Default | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - Asset - Default | OK |
| Asset Manager - ImportExport - Asset - Json | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - Asset - Json | OK |
| Asset Manager - ImportExport - Asset - PhysicalDevice | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - Asset - PhysicalDevice | OK |
| Asset Manager - ImportExport - Asset - Simple Patch Template | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - Asset - Simple Patch Template | OK |
| Asset Manager - ImportExport - AssetClass - Default | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - AssetClass - Default | OK |
| Asset Manager - ImportExport - AssetClass - Json | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - AssetClass - Json | OK |
| Asset Manager - ImportExport - Port - IPHostAddress | {ModuleName} - {Type} - {SubFunction} | Asset Manager - ImportExport - Port - IPHostAddress | OK |
| Asset Manager - Interactive - Assign Asset To Rack | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Assign Asset To Rack | OK |
| Asset Manager - Interactive - Assign Rack to Row | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Assign Rack to Row | OK |
| Asset Manager - Interactive - Choose Racks to Compare | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Choose Racks to Compare | OK |
| Asset Manager - Interactive - Config App Settings | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Config App Settings | OK |
| Asset Manager - Interactive - Create Asset | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Asset | OK |
| Asset Manager - Interactive - Create Asset Class | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Asset Class | OK |
| Asset Manager - Interactive - Create Data Connection | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Data Connection | OK |
| Asset Manager - Interactive - Create Data Ports | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Data Ports | OK |
| Asset Manager - Interactive - Create Holders | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Holders | OK |
| Asset Manager - Interactive - Create Power Connection | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Power Connection | OK |
| Asset Manager - Interactive - Create Power Ports | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Power Ports | OK |
| Asset Manager - Interactive - Create Reservation | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create Reservation | OK |
| Asset Manager - Interactive - Create or Edit Cable Types | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create or Edit Cable Types | OK |
| Asset Manager - Interactive - Create or Edit Device Types | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create or Edit Device Types | OK |
| Asset Manager - Interactive - Create or Edit Port Types | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Create or Edit Port Types | OK |
| Asset Manager - Interactive - Duplicate Asset | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Duplicate Asset | OK |
| Asset Manager - Interactive - Edit Asset Class Information | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Class Information | OK |
| Asset Manager - Interactive - Edit Asset Class Lifecycle | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Class Lifecycle | OK |
| Asset Manager - Interactive - Edit Asset Custody | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Custody | OK |
| Asset Manager - Interactive - Edit Asset Information | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Information | OK |
| Asset Manager - Interactive - Edit Asset Lifecycle | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Lifecycle | OK |
| Asset Manager - Interactive - Edit Asset Location | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Location | OK |
| Asset Manager - Interactive - Edit Asset Ownership | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Asset Ownership | OK |
| Asset Manager - Interactive - Edit Connection | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Connection | OK |
| Asset Manager - Interactive - Edit Network Details | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit Network Details | OK |
| Asset Manager - Interactive - Edit or Delete Data Ports | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit or Delete Data Ports | OK |
| Asset Manager - Interactive - Edit or Delete Holder | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit or Delete Holder | OK |
| Asset Manager - Interactive - Edit or Delete Power Ports | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Edit or Delete Power Ports | OK |
| Asset Manager - Interactive - Install Asset | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Install Asset | OK |
| Asset Manager - Interactive - Link Asset With Elements | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Link Asset With Elements | OK |
| Asset Manager - Interactive - Query Filters for Ad Hoc | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Query Filters for Ad Hoc | OK |
| Asset Manager - Interactive - Remove Asset From Rack | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Remove Asset From Rack | OK |
| Asset Manager - Interactive - Remove Reservation | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Remove Reservation | OK |
| Asset Manager - Interactive - Toggle Operational Flags | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Interactive - Toggle Operational Flags | OK |
| Asset Manager - Script - Cleanup History Entries | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Script - Cleanup History Entries | OK |
| Asset Manager - Script - Delete Instances | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Script - Delete Instances | OK |
| Asset Manager - Script - Export Connection Panel Connections | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Script - Export Connection Panel Connections | OK |
| Asset Manager - Script - Linked Elements Operations | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Script - Linked Elements Operations | OK |
| Asset Manager - Script - Set Asset Class Image | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Script - Set Asset Class Image | OK |
| Asset Manager - Scripts - Delete Multiple Instances | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Scripts - Delete Multiple Instances | WARNING â€” non-standard type token Scripts |
| Asset Manager - Tool - AppSettings Setup | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Tool - AppSettings Setup | OK |
| Asset Manager - Tool - Import Export | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Tool - Import Export | OK |
| Asset Manager - Tool - Populate | {ModuleName} - {Type} - {SubFunction} | Asset Manager - Tool - Populate | OK |
| Facility Manager - Interactive - Assign Rack To Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Assign Rack To Room | OK |
| Facility Manager - Interactive - Assign Row to Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Assign Row to Room | OK |
| Facility Manager - Interactive - Assign Zone to Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Assign Zone to Room | OK |
| Facility Manager - Interactive - Config App Settings | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Config App Settings | OK |
| Facility Manager - Interactive - Create Desk | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Desk | OK |
| Facility Manager - Interactive - Create Facility | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Facility | OK |
| Facility Manager - Interactive - Create Floor | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Floor | OK |
| Facility Manager - Interactive - Create Rack | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Rack | OK |
| Facility Manager - Interactive - Create Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Room | OK |
| Facility Manager - Interactive - Create Row | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Row | OK |
| Facility Manager - Interactive - Create Site | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Site | OK |
| Facility Manager - Interactive - Create Zone | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Create Zone | OK |
| Facility Manager - Interactive - Edit Desk | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Desk | OK |
| Facility Manager - Interactive - Edit Facility Information | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Facility Information | OK |
| Facility Manager - Interactive - Edit Floor | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Floor | OK |
| Facility Manager - Interactive - Edit Rack | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Rack | OK |
| Facility Manager - Interactive - Edit Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Room | OK |
| Facility Manager - Interactive - Edit Row | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Row | OK |
| Facility Manager - Interactive - Edit Site Information | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Site Information | OK |
| Facility Manager - Interactive - Edit Zone | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Edit Zone | OK |
| Facility Manager - Interactive - Generate Initial Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Generate Initial Room | OK |
| Facility Manager - Interactive - Remove Rack from Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Remove Rack from Room | OK |
| Facility Manager - Interactive - Remove Row from Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Remove Row from Room | OK |
| Facility Manager - Interactive - Remove Zone from Room | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Interactive - Remove Zone from Room | OK |
| Facility Manager - Script - Add Or Remove Rack Image | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Script - Add Or Remove Rack Image | OK |
| Facility Manager - Script - Delete Instance | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Script - Delete Instance | OK |
| Facility Manager - Script - Manage Site Facility Link | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Script - Manage Site Facility Link | OK |
| Facility Manager - Script - Set Plan Image | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Script - Set Plan Image | OK |
| Facility Manager - Script - Update New States | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Script - Update New States | OK |
| Facility Manager - Tool - AppSettings Setup | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Tool - AppSettings Setup | OK |
| Facility Manager - Tool - Populate | {ModuleName} - {Type} - {SubFunction} | Facility Manager - Tool - Populate | OK |
| Field Operations - Interactive - Remove Selected Asset | {ModuleName} - {Type} - {SubFunction} | Field Operations - Interactive - Remove Selected Asset | OK |
| Field Operations - Interactive - Save Asset | {ModuleName} - {Type} - {SubFunction} | Field Operations - Interactive - Save Asset | OK |
| Field Operations - Interactive - Submit Transfer | {ModuleName} - {Type} - {SubFunction} | Field Operations - Interactive - Submit Transfer | OK |
| InfraOps - DEBUG - Check DB Consistency | {ModuleName} - {Type} - {SubFunction} | InfraOps - DEBUG - Check DB Consistency | WARNING â€” non-standard type token DEBUG |
| InfraOps - Export Applications | {ModuleName} - {Type} - {SubFunction} | InfraOps - Export Applications | ERROR â€” missing standard type segment |
| InfraOps - Generate Default Data | {ModuleName} - {Type} - {SubFunction} | InfraOps - Generate Default Data | ERROR â€” missing standard type segment |
| InfraOps - Merge Themes | {ModuleName} - {Type} - {SubFunction} | InfraOps - Merge Themes | ERROR â€” missing standard type segment |
| InfraOps - Register Solutions | {ModuleName} - {Type} - {SubFunction} | InfraOps - Register Solutions | ERROR â€” missing standard type segment |
| InfraOps - Transition States ALL | {ModuleName} - {Type} - {SubFunction} | InfraOps - Transition States ALL | ERROR â€” missing standard type segment |
| InfraOps Generate Demo Data | {ModuleName} - {Type} - {SubFunction} | InfraOps Generate Demo Data | ERROR â€” missing expected hyphenated structure |
| InfraOps Generate Demo Data From Scratch | {ModuleName} - {Type} - {SubFunction} | InfraOps Generate Demo Data From Scratch | ERROR â€” missing expected hyphenated structure |
| InfraOps Properties - IAS - Property EditValues | {ModuleName} - {Type} - {SubFunction} | InfraOps Properties - IAS - Property EditValues | WARNING â€” non-standard type token IAS |
| InfraOps Properties - IAS - Property Editor | {ModuleName} - {Type} - {SubFunction} | InfraOps Properties - IAS - Property Editor | WARNING â€” non-standard type token IAS |
| InfraOps Properties - Script - Delete Property | {ModuleName} - {Type} - {SubFunction} | InfraOps Properties - Script - Delete Property | OK |
| InfraOps_Scalability_Finalize | {ModuleName} - {Type} - {SubFunction} | InfraOps_Scalability_Finalize | ERROR â€” missing expected hyphenated structure |
| InfraOps_Scalability_Initialize | {ModuleName} - {Type} - {SubFunction} | InfraOps_Scalability_Initialize | ERROR â€” missing expected hyphenated structure |
| NetBox - Read Device Type Library | {ModuleName} - {Type} - {SubFunction} | NetBox - Read Device Type Library | ERROR â€” missing standard type segment |
| People and Organizations - Tools - Cost and Billing DOM Classes | {ModuleName} - {Type} - {SubFunction} | People and Organizations - Tools - Cost and Billing DOM Classes | WARNING â€” non-standard type token Tools |
| People and Organizations InfraOps - Tool - Populate | {ModuleName} - {Type} - {SubFunction} | People and Organizations InfraOps - Tool - Populate | OK |
| Plan And Build - General Setup | {ModuleName} - {Type} - {SubFunction} | Plan And Build - General Setup | ERROR â€” missing standard type segment |
| Plan And Build - ImportExport - Jobs - Default | {ModuleName} - {Type} - {SubFunction} | Plan And Build - ImportExport - Jobs - Default | OK |
| Plan And Build - Interactive - Assign Job | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Assign Job | OK |
| Plan And Build - Interactive - Config Job ID | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Config Job ID | OK |
| Plan And Build - Interactive - Create Job | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Create Job | OK |
| Plan And Build - Interactive - Create Job Type | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Create Job Type | OK |
| Plan And Build - Interactive - Delete Job Type | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Delete Job Type | OK |
| Plan And Build - Interactive - Edit Job | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Edit Job | OK |
| Plan And Build - Interactive - Edit Job Type | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Edit Job Type | OK |
| Plan And Build - Interactive - Set Job To Review | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Interactive - Set Job To Review | OK |
| Plan And Build - Script - Bulk Delete | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Script - Bulk Delete | OK |
| Plan And Build - Script - Convert Old Job Types To New Job Types | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Script - Convert Old Job Types To New Job Types | OK |
| Plan And Build - Script - Delete Instance | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Script - Delete Instance | OK |
| Plan And Build - Script - Export Job Cabling Plans | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Script - Export Job Cabling Plans | OK |
| Plan And Build - Tool - Demo Setup Jobs | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Tool - Demo Setup Jobs | OK |
| Plan And Build - Tools - Default Data | {ModuleName} - {Type} - {SubFunction} | Plan And Build - Tools - Default Data | WARNING â€” non-standard type token Tools |
| QA Portal - GQI - Ad Hoc - Get Scalability Results | {ModuleName} - {Type} - {SubFunction} | QA Portal - GQI - Ad Hoc - Get Scalability Results | WARNING â€” non-standard type token GQI |
| Scalability_CleanUp | {ModuleName} - {Type} - {SubFunction} | Scalability_CleanUp | ERROR â€” missing expected hyphenated structure |
| SetPortAsPrimary | {ModuleName} - {Type} - {SubFunction} | SetPortAsPrimary | ERROR â€” missing expected hyphenated structure |

### GQI Projects
| Component | Expected Pattern | Actual | Status |
|-----------|-----------------|--------|--------|
| InfraOps.GQI.AssetManager | InfraOps.GQI.{ObjectName} or InfraOps GQI {ObjectName} | InfraOps.GQI.AssetManager | OK |
| InfraOps.GQI.Common | InfraOps.GQI.{ObjectName} or InfraOps GQI {ObjectName} | InfraOps.GQI.Common | OK |
| InfraOps.GQI.FacilityManager | InfraOps.GQI.{ObjectName} or InfraOps GQI {ObjectName} | InfraOps.GQI.FacilityManager | OK |
| InfraOps.GQI.FieldOperations | InfraOps.GQI.{ObjectName} or InfraOps GQI {ObjectName} | InfraOps.GQI.FieldOperations | OK |
| InfraOps.GQI.PlanAndBuild | InfraOps.GQI.{ObjectName} or InfraOps GQI {ObjectName} | InfraOps.GQI.PlanAndBuild | OK |

### DOM Buttons
| Component | Expected Pattern | Actual | Status |
|-----------|-----------------|--------|--------|
| AssetManagement_AssetClass_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | AssetManagement_AssetClass_DOM Button | OK |
| AssetManagement_Asset_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | AssetManagement_Asset_DOM Button | OK |
| FacilityManagement_Desk_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Desk_DOM Button | OK |
| FacilityManagement_Facility_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Facility_DOM Button | OK |
| FacilityManagement_Floor_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Floor_DOM Button | OK |
| FacilityManagement_Rack_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Rack_DOM Button | OK |
| FacilityManagement_Room_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Room_DOM Button | OK |
| FacilityManagement_Row_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Row_DOM Button | OK |
| FacilityManagement_Site_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Site_DOM Button | OK |
| FacilityManagement_Zone_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | FacilityManagement_Zone_DOM Button | OK |
| PlanAndBuild_Job_DOM Button | {DomModuleName}_{ObjectType}_DOM Button | PlanAndBuild_Job_DOM Button | OK |

### Packages / Main Solution
| Component | Expected Pattern | Actual | Status |
|-----------|-----------------|--------|--------|
| SLC-S-InfraOps | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps | OK |
| SLC-S-InfraOps-CleanSystem | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps-CleanSystem | WARNING â€” suffix added to base solution package name |
| SLC-S-InfraOps-Demo-Data | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps-Demo-Data | WARNING â€” suffix added to base solution package name |
| SLC-S-InfraOps-FieldOperations-AddOns | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps-FieldOperations-AddOns | WARNING â€” suffix added to base solution package name |
| SLC-S-InfraOps-RT | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps-RT | WARNING â€” suffix added to base solution package name |
| SLC-S-InfraOps-Vodafone-AddOns | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps-Vodafone-AddOns | WARNING â€” suffix added to base solution package name |
| SLC-S-InfraOps-WithDependencies | InfraOps or SLC-S-InfraOps | SLC-S-InfraOps-WithDependencies | WARNING â€” suffix added to base solution package name |

## Summary
| # | Check | Status | Notes |
|---|-------|--------|-------|
| 1 | Pre-run discovery | OK | Open naming issue: https://github.com/SkylineCommunications/SLC-S-InfraOps/issues/74; open naming PR: None |
| 2 | Automation scripts | FAIL | 99 OK, 8 warning(s), 13 error(s) |
| 3 | GQI projects | PASS | 5 OK, 0 warning(s), 0 error(s) |
| 4 | DOM buttons | PASS | 11 OK, 0 warning(s), 0 error(s) |
| 5 | Packages / main solution | PARTIAL | 1 OK, 6 warning(s), 0 error(s) |
| 6 | Skipped root folders | INFO | 64 internal/test/library folders were skipped: .github, CommonInfraOpsSharedTests, DOM Classes, Dlls, InfraOps.Common, InfraOpsInteractiveAutomationCommon, InfraOpsShared, Internal, MediaOps.Common, MediaOpsShared, RT_AssetManager_AssignAssetToRack, RT_AssetManager_CreateAsset, RT_AssetManager_CreateAssetClass, RT_AssetManager_CreateAssetFromFullAssetClass, RT_AssetManager_CreateCableType, RT_AssetManager_CreateDataConnection, RT_AssetManager_CreateDeviceType, RT_AssetManager_CreateOrEditPorts, RT_AssetManager_CreatePortType, RT_AssetManager_CreatePowerPorts, RT_AssetManager_DuplicateAsset, RT_AssetManager_EditAssetClassInformation, RT_AssetManager_EditAssetClassLifecycle, RT_AssetManager_EditAssetCustody, RT_AssetManager_EditAssetInformation, RT_AssetManager_EditAssetLocation, RT_AssetManager_EditAssetNetworkDetails, RT_AssetManager_EditAssetOwnership, RT_AssetManager_EditOrDeleteDataPorts, RT_AssetManager_EditOrDeletePowerPorts, RT_AssetManager_GetAllAssets, RT_AssetManager_ImportExport, RT_AssetManager_ImportExport_AssetClasses, RT_AssetManager_Scalability_ConnectionUseCases, RT_AssetManager_Scalability_UseCases, RT_Asset_Manager_CreateReservations, RT_FacilityManager_AssignRackToRoom, RT_FacilityManager_CreateDesk, RT_FacilityManager_CreateFacility, RT_FacilityManager_CreateFloor, RT_FacilityManager_CreateRack, RT_FacilityManager_CreateRoom, RT_FacilityManager_CreateRow, RT_FacilityManager_CreateZone, RT_FacilityManager_DeleteInstances, RT_FacilityManager_EditDesk, RT_FacilityManager_EditFacility, RT_FacilityManager_EditFloor, RT_FacilityManager_EditRack, RT_FacilityManager_EditRoom, RT_FacilityManager_EditRow, RT_FacilityManager_EditZone, RT_FacilityManager_GenerateInitialRoom, RT_InventoryManager_Execute, RT_InventoryManager_Playwright, RT_InventoryManager_ScaleUp_AssetManager, RT_InventoryManager_Setup, RT_PlanAndBuildSetJobToReview, RT_PlanAndBuild_CompleteJob, RT_PlanAndBuild_ConfigJobID, RT_PlanAndBuild_CreateJob, RT_PlanAndBuild_CreateJobType, SolutionInstallerTools, TestingLibrary |

**Result: 13 error(s) Â· 14 warning(s)**