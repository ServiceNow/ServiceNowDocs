---
title: New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the new record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying new record menu items for migrations, and the migration process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the new record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying new record menu items for migrations, and the migration process.

## System property

`sys_property: sn_sow_migration.itsm_aw_migration_tables`

Records corresponding to only these tables are migrated from ITSM Agent Workspace to Service Operations Workspace.

## Table used for migration

New Record Menu Item \[sys\_aw\_new\_menu\_item\]: Contains the active records to migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM.

## How the migration utility identifies new record menu items for migration

The Service Operations Workspace migration utility identifies the new record menu items to migrate based on the following information:

-   Active records of ITSM Agent Workspace table specified by the New Record Menu Item \[sys\_aw\_new\_menu\_item\] table.
-   The records of a table already mentioned in the new record menu item configuration for Service Operations Workspace aren’t migrated to avoid duplicates.

The utility migrates only a copy of an active record if duplicate active records are specified in the New Record Menu Item \[sys\_aw\_new\_menu\_item\] table.

## How the migration works

The Service Operations Workspace migration utility uses the following sequence to migrate new record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the utility.

1.  Searches for the current new record menu item configuration for Service Operations Workspace.

    Queries the UX Page Property \[sys\_ux\_page\_property\] table for the following:

    -   Service Operations Workspace page \(**aa881cad73c4301045216238edf6a716** is the **sysId** for Service Operations Workspace page record\).
    -   **chrome\_tab** \(Name for UX page property record that stores a new record menu item for Service Operations Workspace\)
2.  Uses the record obtained from Step 1 to search for tables that are already part of the new record menu item for Service Operations Workspace.
3.  Ignores the existing tables during migration to avoid duplicates.
4.  Searches the records of the New Record Menu Item \[sys\_aw\_new\_menu\_item\] table whose field values are set as follows:

    -   **active** is **true**
    -   **workspace** is **Agent Workspace**
    -   **table** is one of **sn\_sow\_migration.itsm\_aw\_migration\_tables**.
    For each record, if the table name isn’t a part of existing tables and if the same table name isn’t processed earlier, then the migration utility creates a JSON object.

5.  Creates a JSON object that contains data corresponding to each record as follows:

    ```
    { 
                        "label": { 
                            "translatable": true, 
                            "message": "New " + tableLabel 
                        }, 
                        "routeInfo": { 
                            "route": "record", 
                            "fields": { 
                                "table": table, 
                                "sysId": "-1" 
                            }, 
                            "multiInstField": "sysId" 
                        }, 
                        "condition": { 
                            "tableDescription": { 
                                "table": table, 
                                "canCreate": true 
                            } 
                        } 
    };
    ```

6.  Adds the code to the existing **chrome\_tab** JSON value for the new record menu.

-   **[Perform post-migration tasks for new records](../task/verify-migration-status-new-records.md)**  
Verify that the new record menus in Service Operations Workspace \(SOW\) are consistent with the new record menus in ITSM Agent Workspace \(ITSM AW\) and they are ready for use in SOW. You can update the migrated new record menu settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

