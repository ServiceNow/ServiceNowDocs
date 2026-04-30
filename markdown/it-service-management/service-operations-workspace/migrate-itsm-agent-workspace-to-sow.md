---
title: Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Through a set of simple steps, quickly migrate your ITSM Agent Workspace features including configurations and customizations to Service Operations Workspace for ITSM.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM

Through a set of simple steps, quickly migrate your ITSM Agent Workspace features including configurations and customizations to Service Operations Workspace for ITSM.

## Before you begin

Ensure that the scope is set to Service Operations Workspace Core.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview** &gt; **Initial Setup** &gt; **Migrate from ITSM Agent Workspace to SOW** if you're upgrading from AW 2.0 or higher.

    If you're installing the latest migration utility, navigate to **All** &gt; **Service Operations Workspace** &gt; **Migrate from ITSM Agent Workspace to SOW**.

2.  On the Migration from ITSM Agent Workspace to SOW page, perform the following steps.

    1.  If required, create a basic authentication configuration with existing or new user credentials by selecting **Create basic authentication configurations**.

        **Important:**

        -   This configuration must contain the credentials of the user who is logged in and has the admin role.
        -   Only after you create the basic authentication configuration, create an update set to record any changes that are made to Service Operations Workspace for ITSM in your non-production instance during the migration. See [Create and select an update set as the current set](https://www.servicenow.com/docs/access?context=create-select-update-set&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
    2.  From the **Select a basic auth configuration** drop-down, select the required configuration.

    3.  Select **Test the configuration**.

    4.  Review the mentioned guidelines.

    5.  Select **Start migration**.

    **Note:** In case your previous migration task is partially complete, you can select **Continue migration** on this page to resume the migration process.

3.  On the Features to migrate from Agent Workspace page, for each feature, select the configurations and customizations to migrate.

    Apart from the pre-defined features or application and sub features within the features that correspond to specific tables, you can also configure to add custom tables or multiple tables to the features for migration from ITSM Agent Workspace to SOW using the **ITSM Agent Workspace migration grp tables** \[**sn\_sow\_migration.itsm\_aw\_migration\_grp\_tables**\] system property. This includes the tables that you created or modified in ITSM Agent Workspace.

    On the Features to migrate from Agent Workspace page, the banner displays a notification message with the link to the system property. You can select the link to access the system property page. On the system property page, you can modify the json string in the **Value** field to add custom tables or multiple tables to the features for migration. When editing the json string, you must ensure the following points to avoid errors during migration process:

    -   Maintain the format and structure of the json string as is and ensure that the json string is valid.
    -   Add multiple or custom tables that correspond to the features such as **Incident Management** or **Change Management**.
    -   Avoid duplicate entry of the same custom table under multiple features except for **List** and **Other features**.
    -   As the **List** and **Other features** does not correspond to a specific table, it contains multiple tables from other features or applications in ITSM.
    -   If you want to run the migration for the custom table in **List** and **Other features**, then add the custom table to the existing pre-defined features as well as in List and Other features section of the json string.
    -   In case, if any custom table does not correspond to any pre-defined features or application or categories, you can add the custom table in Custom Table Migration section of the json string.
    For information about configurations and customizations that can be migrated, see [Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md).

4.  Select **Next**.

5.  From the Migration confirmation page, review the selected features and select **Confirm the migration**.

    The migration can be fully or partially successful.

    -   Full successful migration: All configurations and customizations of selected features are successfully migrated to Service Operations Workspace for ITSM and captured in the specified update sets in the non-production instance.
    -   Partial migration: All successfully migrated configurations and customizations of selected features are captured in the specified update sets in Service Operations Workspace for ITSM in the non-production instance.
6.  Select **View migration details** to review the migration information.


## What to do next

Complete the post-migration tasks for each configuration or customization that you have migrated. For more information, see the following topics.

-   [Perform post-migration tasks for UI actions and layouts](verify-migration-status-ui-actions-layouts.md)
-   [Perform post-migration tasks for ribbons](verify-migration-status-ribbons.md)
-   [Perform post-migration tasks for view rules](verify-migration-status-view-rules.md)
-   [Perform post-migration tasks for new records](verify-migration-status-new-records.md)
-   [Perform post-migration tasks for highlighted fields in list and forms](verify-migration-status-highlighted-fields-lists-forms.md)
-   [Perform post-migration tasks for list actions](verify-migration-status-list-actions.md)
-   [Perform post-migration tasks for list categories and modules](verify-migration-status-list-categories-modules.md)
-   [Perform post-migration tasks for form headers](verify-migration-status-form-headers-sow.md)
-   [Perform post-migration tasks for search configurations](verify-migration-status-search-config.md)
-   [Perform post-migration tasks for Agent assist configuration](verify-migration-status-agent-assist.md)
-   [Perform post-migration tasks for related list declarative form actions](verify-migration-status-related-actions-aw-sow.md)
-   [Perform post-migration tasks for field decorators form actions](verify-migration-status-field-declarative-actions-aw-sow.md)

-   **[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)**  
Several configurations and customizations related to various ITSM Agent Workspace features that can be migrated to SOW for ITSM.

**Parent Topic:**[Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../concept/migration-from-itsm-aw-sow.md)

