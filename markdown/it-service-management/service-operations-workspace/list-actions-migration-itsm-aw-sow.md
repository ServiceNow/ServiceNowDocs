---
title: List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the tables and the migration process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the tables and the migration process.

## List declarative actions

The declarative action framework integrates core UI behaviors such as client actions or server scripts into workspace forms, fields, lists, and lists without editing the code.

For more information about types of declarative actions and how to create these actions, see [https://www.servicenow.com/community/next-experience-articles/introduction-to-declarative-actions/ta-p/2332003](https://www.servicenow.com/community/next-experience-articles/introduction-to-declarative-actions/ta-p/2332003) and [https://www.servicenow.com/community/developer-blog/declarative-actions-in-servicenow-the-complete-guide/ba-p/2781607](https://www.servicenow.com/community/developer-blog/declarative-actions-in-servicenow-the-complete-guide/ba-p/2781607).

## Table used for migration

Action Assignment \[sys\_declarative\_action\_assignment\]: Contains all list action settings.

## Conditions for migration

```
Conditions: 
Action model = List 
workspace = Agent Workspace 
table = ITSM tables {ys_id of the supported ITSM tables: 600f5e889f320210db9f618dfa0a1cbd} and Global table
view != sow and sow_new_record (As we are assuming sow related view isn't customized in ITSM Agent Workspace)
```

## How the migration works

The following are the list actions available in ITSM Agent Workspace:

-   Client script
-   Server script
-   Client action
-   UI component

-   **[Migrate the client script from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/migrate-list-client-script-aw-to-sow.md)**  
Configure the client script to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.
-   **[Migrate the server script from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/migrate-list-server-script-aw-sow.md)**  
Configure the server script to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.
-   **[Migrate the client action from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/migrate-list-client-action-aw-to-sow.md)**  
Configure the client actions to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.
-   **[Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/migrate-list-ui-component-from-aw-to-sow.md)**  
Configure the UI component to migrate list actions from ITSM Agent Workspace to Service Operations Workspace \(SOW\) for ITSM.
-   **[Perform post-migration tasks for list actions](../task/verify-migration-status-list-actions.md)**  
Verify that the list actions in Service Operations Workspace \(SOW\) are consistent with the list actions in ITSM Agent Workspace \(ITSM AW\) and they’re ready for use in SOW. You can update the migrated list actions settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

