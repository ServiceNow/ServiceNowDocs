---
title: Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying the view rules for migrations, and the migration process.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying the view rules for migrations, and the migration process.

## View rules

For information about view rules, see [https://www.servicenow.com/community/developer-blog/servicenow-view-and-view-rule-servicenow-tutorial-to-understand/ba-p/2333469](https://www.servicenow.com/community/developer-blog/servicenow-view-and-view-rule-servicenow-tutorial-to-understand/ba-p/2333469).

For information about creating a view rule, see [Create a view rule](https://www.servicenow.com/docs/access?context=t_CreateAViewRule&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Tables used for migration

|Table name|Description|
|----------|-----------|
|View Rule \[sysrule\_view\_workspace\]|Contains all view rules.|
|UX View Rules Configuration \[sys\_ux\_view\_rules\_configuration\]|Contains the view rule configuration that is mapped to the specified configurable workspace. The migration utility uses the Service Operations Workspace view rules configuration.|
|Sys Ux M2m Workspace View Rule Ux View Rule Config \[sys\_ux\_m2m\_workspace\_view\_rule\_ux\_view\_rule\_config\]|Contains mapping information between view rules and the view rule configuration. This information helps define and identify rules that are applicable for a workspace.|

## How the migration utility identifies view rules for migration

The migration utility for Service Operations Workspace identifies the set of view rules to migrate by using the following information:

-   View Rule \[sysrule\_view\_workspace\] table records for which **workspace** is ITSM Agent Workspace.
-   All view rules specified by the View Rule \[sysrule\_view\_workspace\] table in the ITSM Agent Workspace.

## How the migration works

The migration utility uses the following sequence to migrate the UI actions from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the utility.

1.  Filters records from View Rule \[sysrule\_view\_workspace\] table for which **workspace** is ITSM Agent Workspace.
2.  Imports all view rules specified by the View Rule \[sysrule\_view\_workspace\] table in the ITSM Agent Workspace.
3.  Filters view rules that aren’t mapped to any view rules configuration.
4.  Creates an m2m mapping between filtered view rules and Service Operations Workspace view rules configurations so that the view rules are applied in Service Operations Workspace.
5.  Creates a fallback view rule with the following field values while migrating view rules for the specified table.

    -   **view** is **workspace**.
    -   **order** is **99999999**.
    **Note:** The fallback view rule is created because, in the ITSM Agent Workspace, the default view for all tables is workspace

    If a view rule isn’t configured for a table, the Service Operations Workspace view rule that is consistent with the ITSM Agent Workspace is migrated.


-   **[Perform post-migration tasks for view rules](../task/verify-migration-status-view-rules.md)**  
Verify that the view rules in Service Operations Workspace \(SOW\) are consistent with the view rules in ITSM Agent Workspace and are ready for use in SOW. You can update the view rules settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](search-config-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

