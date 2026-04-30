---
title: Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying the eligible UI actions and layout records for migrations, and the migration process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying the eligible UI actions and layout records for migrations, and the migration process.

## UI actions

UI actions appear either as form buttons or as list items in the UI action menu.

The form header shows a group of UI actions under a single menu button or a split button.

To group UI actions, a layout is required, which acts as a container to the group.

## Tables used for migration

|Table name|Description|
|----------|-----------|
|UI Action \[sys\_ui\_action\]|Contains UI action and layouts configurations to migrate.|
|UI Action Layout \[sys\_aw\_form\_uiaction\_layout\]|Contains a set of records \(base system or custom\) associated with the agent workspace. The migration utility considers these records as eligible for migration. All the group UI actions specified in such UI Action Layout \[sys\_aw\_form\_uiaction\_layout\] record are migrated.|

## How the migration utility identifies UI actions and layouts for migration

The Service Operations Workspace migration utility identifies the eligible set of UI actions to migrate based on the following:

-   UI Action \[sys\_ui\_action\] table records that are mapped to the UX Form Actions \[sys\_ux\_form\_action\] table records.
-   UX Form Actions Layout Item \[sys\_ux\_form\_action\_layout\_item\] table records that are mapped to UX Form Actions \[sys\_ux\_form\_action\] table records.
-   UX Form Actions Layout \[sys\_ux\_form\_action\_layout\] table records that are mapped to the input table.

## How the migration works

The Service Operations Workspace migration utility uses the following sequence to migrate the UI actions from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the utility.

1.  Searches for UI Action Layout \[sys\_aw\_form\_uiaction\_layout\] table records that are mapped to UI Action Group \[sys\_aw\_form\_uiaction\_group\] records.
2.  Searches for UX Form Actions Layout Group \[sys\_ux\_form\_action\_layout\_group\] table records that are mapped to UI Action Layout \[sys\_aw\_form\_uiaction\_layout\] table records. The set of UI actions and the type of grouping must be the same for these records.
3.  If a record isn’t found, creates a UX Form Actions Layout Group \[sys\_ux\_form\_action\_layout\_group\] table record.

The Service Operations Workspace migration utility uses the following sequence to migrate the layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the system.

1.  Searches for UI Action Group \[sys\_ux\_form\_action\_layout\_group\] table records that are mapped to UX Form Actions Layout Group \[sys\_ux\_form\_action\_layout\_item\] table records.
2.  If a record isn’t found, creates a UX Form Actions Layout Group \[sys\_ux\_form\_action\_layout\_item\] table record and maps it to the UI Action Group \[sys\_ux\_form\_action\_layout\_group\] table record.

The Service Operations Workspace migration utility uses the following sequence to migrate input tables from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the system.

1.  Searches for a UX Form Actions Layout \[sys\_ux\_form\_action\_layout\] table record.
2.  If a UX Form Actions Layout \[sys\_ux\_form\_action\_layout\] table record isn’t found, completes the migration and shows grouped UI actions in the record page as ungrouped UI actions.

    **Note:** UI actions are grouped only if a UX Form Actions Layout \[sys\_ux\_form\_action\_layout\] table record is found.

3.  If a record is found, performs the migration using the following sequence:
    1.  Checks if the UX Form Actions Layout \[sys\_ux\_form\_action\_layout\] table record is unified.

        For unified records, the **use\_layout\_items\_only** field is selected.

    2.  Completes the migration if the record isn’t unified.
    3.  Searches for Sys Ux M2m Action Layout Item \[sys\_ux\_m2m\_action\_layout\_item\] table records that are mapped to the UX Form Actions Layout \[sys\_ux\_form\_action\_layout\] table record.
    4.  If a mapped record isn’t found, creates a Sys Ux M2m Action Layout Item \[sys\_ux\_m2m\_action\_layout\_item\] table record.

-   **[Perform post-migration tasks for UI actions and layouts](../task/verify-migration-status-ui-actions-layouts.md)**  
Verify that the UI actions and layouts in Service Operations Workspace \(SOW\) are consistent with UI actions and layouts in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated UI actions and layouts settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

