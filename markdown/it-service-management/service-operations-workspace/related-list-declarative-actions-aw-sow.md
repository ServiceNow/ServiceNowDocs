---
title: Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the related list declarative actions from ITSM Agent Workspace to Service Operations Workspace that includes identifying the tables and the migration process.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the related list declarative actions from ITSM Agent Workspace to Service Operations Workspace that includes identifying the tables and the migration process.

The Declarative Action framework is used to integrate Core UI behaviors such as client actions or server scripts into Workspace forms, fields, lists, and related lists without the need to edit code.

## Tables used for migration

Action Assignment \[sys\_declarative\_action\_assignment\]: Contains all declarative settings.

## Conditions for migration

```
Conditions: 
Action model = Related List 
workspace = Agent Workspace 
table = {sys_id of the supported ITSM tables: 600f5e889f320210db9f618dfa0a1cbd and <global table>} 
//We support records which are mapped to ITSM tables and Global table. The mapping the related list to ITSM table can be found in sys_ui_related_list_entry.
view != sow and sow_new_record
//(Considering that sow related view isn't customized in ITSM Agent Workspace)
```

## How the migration works

The SOW migration utility uses the following to migrate the related list declarative actions along with type available in ITSM Agent Workspace to SOW:

-   Client Script
-   Server Script
-   Client Action
-   UI Component

-   **[Migrate the client script from ITSM Agent Workspace to Service Operations Workspace](../task/migrate-related-list-client-script-aw-sow.md)**  
Configure the client script to migrate the related list declarative actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Migrate the server script from ITSM Agent Workspace to Service Operations Workspace](../task/migrate-related-list-server-script-aw-sow.md)**  
Configure the server script to migrate related list declarative actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Migrate the client action from ITSM Agent Workspace to Service Operations Workspace](../task/migrate-related-list-client-action-aw-sow.md)**  
Configure the client actions to migrate related list declarative actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace](../task/migrate-related-list-ui-component-aw-sow.md)**  
Configure the UI component to migrate related list declarative actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Perform post-migration tasks for related list declarative form actions](../task/verify-migration-status-related-actions-aw-sow.md)**  
Verify that the related list declarative form actions in Service Operations Workspace \(SOW\) are consistent with the related list declarative form actions in ITSM Agent Workspace \(ITSM AW\) and they’re ready for use in SOW. You can update the migrated related list declarative form actions settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

