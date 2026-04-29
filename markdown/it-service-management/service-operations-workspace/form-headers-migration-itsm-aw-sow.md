---
title: Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the form headers from ITSM Agent Workspace to Service Operations Workspace \(SOW\) include identifying the required tables, eligible form header records for migrations and the migration process. Form headers provide an overview of the record.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the form headers from ITSM Agent Workspace to Service Operations Workspace \(SOW\) include identifying the required tables, eligible form header records for migrations and the migration process. Form headers provide an overview of the record.

## Tables used for migration

|Table Name|Description|
|----------|-----------|
|sys\_aw\_form\_header|Table that contains all the form headers.|
|sys\_ux\_header\_config|Table that contains all the form header configurations mapped to a particular configurable workspace such as SOW Header Configuration.|
|sys\_ux\_m2m\_workspace\_header\_ux\_header\_config|Table which contains the mapping information that exist between sys\_aw\_form\_header and sys\_ux\_header\_config tables. This enables you to define and identify which form headers are applicable to a particular workspace.|

## How the migration utility identifies form headers for migration

The SOW migration utility identifies the eligible set of form headers to be migrated based on the following sequence:

1.  Filters all the form header records that have **Workspace** set to **Agent Workspace** from the sys\_aw\_form\_header table.
2.  Filters all the form header records that are mapped to the SOW Header Configuration record from the sys\_ux\_m2m\_workspace\_header\_ux\_header\_config table.
3.  Based on the above filtered records, all form header records that have **Workspace** set to **Agent Workspace** and are not mapped to SOW Header Configuration record is identified eligible for migration.

## How the migration works

The SOW migration utility uses the following sequence to migrate the form headers from ITSM Agent Workspace to SOW:

1.  Creates a mapping between the filtered form header records and the SOW Header Configuration record in the sys\_ux\_m2m\_workspace\_header\_ux\_header\_config table.
2.  Searches the form header with **Workspace** set as **Agent Workspace** and that has the least order value. The form header with the least order value is applied at the ITSM Agent Workspace runtime.
3.  Searches the form header which is mapped to the SOW Header Configuration record and that has the least order value.
4.  If order value of the form header that is mapped to SOW Header Configuration record is less than the order value of the form header with **Workspace** set as **Agent Workspace**, update the order value of the form header mapped with SOW Header Configuration record with a lesser order value \(Example: Reduce the order value by 10\).

    This ensures that the form header which is already applicable to ITSM Agent Workspace during runtime is applied to SOW as well.


-   **[Perform post-migration tasks for form headers](../task/verify-migration-status-form-headers-sow.md)**  
Verify that the form header in Service Operations Workspace \(SOW\) are consistent with the form header in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated form header settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

