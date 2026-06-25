---
title: Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the ribbons from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying ribbons records for migration, and the migration process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/ribbons-migration-itsm-aw-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the ribbons from ITSM Agent Workspace to Service Operations Workspace for ITSM includes identifying the required tables, identifying ribbons records for migration, and the migration process.

## Tables used for migration

|Table name|Description|
|----------|-----------|
|Ribbon Setting \[sys\_aw\_ribbon\_setting\]|Contains all ribbon settings.|
|UX Ribbon Configuration \[sys\_ux\_ribbon\_config\]|Contains the ribbon configuration that is mapped to a configurable workspace. The migration utility uses the Service Operations Workspace ribbon configuration.|
|Ribbon Configuration Setting \[sys\_ux\_ribbon\_config\_setting\]|Contains mapping information between the Ribbon Setting \[sys\_aw\_ribbon\_setting\] and the UX Ribbon Configuration \[sys\_ux\_ribbon\_config\] table records. This information helps define and identify ribbon settings that are applicable for the specified workspace.|

## Limitation

-   The combined width of the ribbon widgets must be equal to or lower than 12 for the specified table and ribbon configuration.
-   A record can’t be created when:
    -   The ribbon widgets are already configured for the specified table and ribbon configuration.
    -   The width of the ribbon setting that is being mapped with the ribbon configuration plus the widths of the existing ribbon settings that are mapped to the same ribbon configuration is greater than 12.

## How the migration utility identifies ribbons for migration

The migration utility searches all ribbon settings for which **workspace** is set to ITSM Agent Workspace in the Ribbon Setting \[sys\_aw\_ribbon\_setting\] table. These ribbon settings are candidates for migration.

## How the migration works

The Service Operations Workspace migration utility uses the following sequence to migrate ribbons from ITSM Agent Workspace to Service Operations Workspace for ITSM. All these actions are done by the utility.

1.  Calculates the total width of existing ribbons that are mapped to Service Operations Workspace Ribbon Config plus ITSM Agent Workspace ribbons that must be migrated.
2.  If the sum of widths is greater than 12, disables all existing ribbons that are mapped to the Service Operations Workspace ribbon configuration.

    **Note:** All ITSM Agent Workspace ribbons are migrated. The aim of the ITSM Agent Workspace migration utility is to prioritize migrating items from ITSM Agent Workspace to Service Operations Workspace for ITSM and so this trade-off is acceptable.

3.  Creates a mapping between filtered ribbon settings and Service Operations Workspace ribbon configuration in the Ribbon Configuration Setting \[sys\_ux\_ribbon\_config\_setting\] table.

-   **[Perform post-migration tasks for ribbons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/verify-migration-status-ribbons.md)**  
Verify that the ribbons in Service Operations Workspace \(SOW\) are consistent with the ribbons in ITSM Agent Workspace and the ribbons are ready for use in SOW. You can update the migrated ribbon settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

