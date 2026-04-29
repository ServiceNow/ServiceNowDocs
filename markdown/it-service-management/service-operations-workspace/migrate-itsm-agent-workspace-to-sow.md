---
title: Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Through a set of simple steps, quickly migrate your ITSM Agent Workspace features including configurations and customizations to Service Operations Workspace for ITSM.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
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
        -   Only after you create the basic authentication configuration, create an update set to record any changes that are made to Service Operations Workspace for ITSM in your non-production instance during the migration. See [Create and select an update set as the current set](https://www.servicenow.com/docs/access?context=create-select-update-set&version=australia&pubname=australia-application-development&ft:locale=en-US).
    2.  From the **Select a basic auth configuration** drop-down, select the required configuration.

    3.  Select **Test the configuration**.

    4.  Review the mentioned guidelines.

    5.  Select **Start migration**.

    **Note:** In case your previous migration task is partially complete, you can select **Continue migration** on this page to resume the migration process.

3.  On the Features to migrate from Agent Workspace page, for each feature, select the configurations and customizations to migrate.

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

