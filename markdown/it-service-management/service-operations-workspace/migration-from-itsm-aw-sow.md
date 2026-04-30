---
title: Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: You can easily migrate common customizations and configurations for various features from ITSM Agent Workspace to Service Operations Workspace for ITSM using the on-screen migration utility. With this migration, you won't have to rebuild these features in Service Operations Workspace for ITSM. For these features, you can migrate any specific record types and elements or all of them.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM

You can easily migrate common customizations and configurations for various features from ITSM Agent Workspace to Service Operations Workspace for ITSM using the on-screen migration utility. With this migration, you won't have to rebuild these features in Service Operations Workspace for ITSM. For these features, you can migrate any specific record types and elements or all of them.

## Migration process

**Important:** You should run the migration in your non-production instance. If the migration to SOW for ITSM works as expected in the non-production instance, you can move the migration changes to a production instance using an update set.

Perform the following steps in your non-production instance.

1.  Install the Migration Utility for Service Operations Workspace application. See [Install the Migration Utility for Service Operations Workspace](../task/install-migration-utility-for-sow.md).
2.  If you have any custom ITSM table that should be migrated, specify the table in the **sn\_sow\_migration.itsm\_aw\_migration\_tables** system property for migrating the associated list category and modules, list actions, related list actions and New record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM. See [Configure the migration of a custom ITSM table from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/configure-migration-custom-table-to-sow-itsm.md).
3.  Create a basic authentication configuration \(sys\_auth\_profile\_basic\) to authenticate the Table API that the migration utility uses to perform creation, updating, and deletion of records. See [Create a basic authentication configuration to migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/create-basic-authentication-credential-sow-migration.md).
4.  Create an update set to record any changes that are made to Service Operations Workspace for ITSM during the migration. See [Create and select an update set as the current set](https://www.servicenow.com/docs/access?context=create-select-update-set&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
5.  Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM using the migration utility. See [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/migrate-itsm-agent-workspace-to-sow.md).
6.  If the migration to Service Operations Workspace for ITSM is working as expected in your non-production instance, move your migration changes to a production instance using the update set.

**Note:** The logged in admin user credentials must match the credential used to setup basic authentication to successfully perform the migration from ITSM Agent Workspace to Service Operations Workspace for ITSM.

-   **[Install the Migration Utility for Service Operations Workspace](../task/install-migration-utility-for-sow.md)**  
You can install the Migration Utility for Service Operations Workspace application \(sn\_sow\_migration\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Configure the migration of a custom ITSM table from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/configure-migration-custom-table-to-sow-itsm.md)**  
If you have a custom ITSM table that must be migrated, you must enable the migration of the associated list categories and modules, list actions, related list actions, and New record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM.
-   **[Create a basic authentication configuration to migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/create-basic-authentication-credential-sow-migration.md)**  
Authenticate the Table API that the migration utility uses to perform creation, updating, and deletion of records.
-   **[Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](../task/migrate-itsm-agent-workspace-to-sow.md)**  
Through a set of simple steps, quickly migrate your ITSM Agent Workspace features including configurations and customizations to Service Operations Workspace for ITSM.

**Parent Topic:**[Configuring Service Operations Workspace for ITSM](configure-sow.md)

**Related topics**  


[Getting started with Service Operations Workspace for ITSM](getting-started-sow.md)

[Setting up integrations in Service Operations Workspace for ITSM](setting-up-sow-itsm.md)

[Admin Center in Service Operations Workspace for ITSM](admin-center-sow.md)

[Configuring Service Operations Workspace for ITSM to improve your experience](configuring-sow-to-improve-experience.md)

[Admin Center in Service Operations Workspace for ITSM](admin-center-sow.md)

