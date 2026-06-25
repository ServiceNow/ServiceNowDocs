---
title: Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the field decorators actions from ITSM Agent Workspace to Service Operations Workspace that includes identifying the tables and the migration process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/field-declarative-actions-aw-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the field decorators actions from ITSM Agent Workspace to Service Operations Workspace that includes identifying the tables and the migration process.

The Declarative Action framework is used to integrate Core UI behaviors such as client actions or server scripts into Workspace forms, fields, lists, and related lists without the need to edit code.

## Tables used for migration

Action Assignment \[sys\_declarative\_action\_assignment\]: Contains all declarative settings.

## Conditions for migration

```
Conditions: 
Action model = Field 
workspace = Agent Workspace 
table = {sys_id of the supported ITSM tables: 600f5e889f320210db9f618dfa0a1cbd and <global table>} 
//We support records which are mapped to ITSM tables and Global table. The mapping the related list to ITSM table can be found in sys_ui_related_list_entry.
view != sow and sow_new_record
//(Considering that sow related view isn't customized in ITSM Agent Workspace)
```

## How the migration works

The SOW migration utility uses the following to migrate the field decorator actions along with type available in ITSM Agent Workspace to SOW:

-   Client Script
-   Server Script
-   Client Action
-   UI Component

-   **[Migrate the client script from ITSM Agent Workspace to Service Operations Workspace for field decorators actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/migrate-field-declarative-client-script-aw-sow.md)**  
Configure the client script to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Migrate the server script from ITSM Agent Workspace to Service Operations Workspace for field decorators actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/migrate-field-declarative-server-script-aw-sow.md)**  
Configure the server script to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Migrate the client action from ITSM Agent Workspace to Service Operations Workspace for field decorators actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/migrate-field-declarative-client-action-aw-sow.md)**  
Configure the client actions to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace for field decorators actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/migrate-field-declarative-ui-component-aw-sow.md)**  
Configure the UI component to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.
-   **[Perform post-migration tasks for field decorators form actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/verify-migration-status-field-declarative-actions-aw-sow.md)**  
Verify that the field decorators form actions in Service Operations Workspace \(SOW\) are consistent with the field declarative form actions in ITSM Agent Workspace \(ITSM AW\) and they’re ready for use in SOW. You can update the migrated field declarative form actions settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

