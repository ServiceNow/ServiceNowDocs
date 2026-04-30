---
title: Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying eligible highlighted field records for migrations, and the migration process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying eligible highlighted field records for migrations, and the migration process.

## Highlighted fields in lists and forms

Use colors to highlight list and form fields to get the attention of an agent or user.

## Table used for migration

The migration utility uses the Highlighted Value \[sys\_highlighted\_value\] table for migration.

## How the migration utility identifies highlighted fields for migration

If the table contains a set of records \(base system or custom\) for the ITSM Agent Workspace, the migration utility considers the Highlighted Value \[sys\_highlighted\_value\] table for migration.

## How the migration works

The Service Operations Workspace migration utility uses the following sequence to migrate the highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the utility.

1.  Searches for records in the Highlighted Value \[sys\_highlighted\_value\] table records that are mapped to Sys Ux M2m Highlighted Value Config \[sys\_ux\_m2m\_highlighted\_value\_config\] table records.
2.  If a Highlighted Value \[sys\_highlighted\_value\] table record isn’t found, creates a Highlighted Value \[sys\_highlighted\_value\] table record.
3.  Maps the Sys Ux M2m Highlighted Value Config \[sys\_ux\_m2m\_highlighted\_value\_config\] table record.

-   **[Perform post-migration tasks for highlighted fields in list and forms](../task/verify-migration-status-highlighted-fields-lists-forms.md)**  
Verify that the highlighted fields in list and forms in Service Operations Workspace \(SOW\) are consistent with the highlighted fields in list and forms in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated highlighted fields in list and forms settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

