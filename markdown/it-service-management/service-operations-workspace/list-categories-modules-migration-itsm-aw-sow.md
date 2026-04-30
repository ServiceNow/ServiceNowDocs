---
title: List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration from ITSM Agent Workspace to Service Operations Workspace \(SOW\) for ITSM includes identifying the required tables, highlighted field records for migrations, and the migration process.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration from ITSM Agent Workspace to Service Operations Workspace \(SOW\) for ITSM includes identifying the required tables, highlighted field records for migrations, and the migration process.

## Associated system property

If ITSM Agent Workspace contains list modules that use group-based list applicabilities, then only enable the **glide.ux.user\_criteria\_enabled** property mentioned in the System Property \[sys\_properties\] table.

## How the migration utility identifies list categories and modules for migration

The Migration utility for SOW identifies the list categories and modules to migrate based on the type of migration.

Mapping list categories and modules

The migration utility maintains a mapping between base system ITSM Agent Workspace list categories and list modules and their corresponding records in the Service Operations Workspace. It identifies the mapping by checking the tables, conditions, and intuitiveness in names for similarity.

Migration criteria

The migration utility uses different fields and values depending on the type of migration \(list categories, list modules, list layout, list applicabilities, and list attributes\).

-   List categories using the Workspace List Category \[sys\_aw\_list\_category\] and UX List Category \[sys\_ux\_list\_category\] table records.
-   List items and modules within each category using the Workspace List \[sys\_aw\_list\] and UX List \[sys\_ux\_list\] table records.
-   Columnar layout of list modules
-   List applicabilities
-   List attributes

## How the migration works

The migration utility uses different fields, values, and migration steps depending on the type of migration. All these actions are done by the utility.

Mapping and verification

1.  Creates and verifies a comprehensive mapping between ITSM Agent Workspace list categories or modules and Service Operations Workspace list categories or modules.
2.  Verifies the mapping based on table, conditions, and intuitiveness in the name of the base system list categories and modules in ITSM Agent Workspace and Service Operations Workspace.

Migrating list categories

1.  Iterates over the Workspace List Category \[sys\_aw\_list\_category\] table with filter condition of `workspace` = `Agent Workspace`.
2.  Check for the mapping between ITSM Agent Workspace and Service Operations Workspace for each list item.
3.  If a mapping is found, update the list categories by copying the following fields from the current ITSM Agent Workspace Workspace List Category \[sys\_aw\_list\_category\] table record to the mapped Service Operations Workspace UX List Category \[sys\_ux\_list\_category\] table record:
    -   active
    -   description
    -   order
    -   active
4.  If a mapping isn’t found, createss a record in the UX List Category \[sys\_ux\_list\_category\] table.

    If the mapping isn’t found, it means that the specified category exists in ITSM Agent Workspace but the category is missing in Service Operations Workspace \(new category created by the user\).


Migrating list items or modules for each category

1.  Iterates over the Workspace List \[sys\_aw\_list\] table with the filter condition of the current list item or module and `workspace` = `Agent Workspace`.
2.  Checks for the mapping between ITSM Agent Workspace and Service Operations Workspace for each list item.
3.  If a mapping is found, updates the list items by copying the following fields from the current ITSM Agent Workspace Workspace List \[sys\_aw\_list\] record to the mapped Service Operations Workspace UX List \[sys\_ux\_list\] record:
    -   title
    -   order
    -   active
    -   condition
4.  If a mapping isn’t found, creates a record in the UX List \[sys\_ux\_list\] table.

    If the mapping isn’t found, it means that the list item exists in ITSM Agent Workspace, but the list item is missing in Service Operations Workspace. For such cases, the migration utility creates a record in the UX List \[sys\_ux\_list\] table by setting the following fields from the current ITSM Agent Workspace list record and \(`category = current iterating category, configuration = Default – SOW, and view = sow`\):

    -   title
    -   order
    -   active
    -   condition
5.  Performs the following migration after the list item is migrated \(if the mapping is found\) or created \(if the mapping isn’t found\):
    1.  Migrates list applicability for the migrated or created list item:

        1.  Creates a list applicability using the List Applicability \[sys\_ux\_applicability\_m2m\_list\] table and user criteria \(if groups are specified in the list item\) with the corresponding ITSM Agent Workspace list module, roles, and groups.
        2.  Attaches this newly created list applicability with the migrated or created Service Operations Workspace list item.
        The migration utility doesn’t delete any existing list applicability associated with the migrated list.

    2.  Migrates columnar layout for migrated or created list item:
        1.  Unifies the columnar layout in Service Operations Workspace based on the layout of the list module with a lower-order list item in the specified ITSM Agent Workspace table.
        2.  Search for records with the following conditions in the List \[sys\_ui\_list\] table for setting columnar layout in Service Operations Workspace:

            -   `conditions = table` \(with which this list item is associated\)
            -   `parent list =null`
            For this record, the migration utility updates the List Element \[sys\_ui\_list\_element\] table to insert or update the correct order and columns.

    3.  Migrates list attributes for migrated or created list items:

        ITSM Agent Workspace uses **Omit Count** and **Disable Highlighted Values** list attributes. These attributes are associated with the Workspace List Attribute \[sys\_aw\_list\_attribute\] table. For the current list item record, the migration utility:

        1.  Iterates over the Workspace List Attribute \[sys\_aw\_list\_attribute\_list\] table to identify list attributes that are associated with the specified record.
        2.  Sets the corresponding attributes in the UX List \[sys\_ux\_list\] table.

-   **[Perform post-migration tasks for list categories and modules](../task/verify-migration-status-list-categories-modules.md)**  
Verify that the list categories and modules in Service Operations Workspace \(SOW\) are consistent with the list categories and modules in ITSM Agent Workspace \(ITSM AW\) and the list categories and modules are ready for use in SOW. You can update the migrated list categories and modules settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

