---
title: Perform post-migration tasks for search configurations
description: Verify that the search configurations in Service Operations Workspace \(SOW\) are consistent with the search configurations in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated search configurations settings in SOW based on your requirements.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for search configurations

Verify that the search configurations in Service Operations Workspace \(SOW\) are consistent with the search configurations in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated search configurations settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **Workspace search configurations** option for ITSM Agent Workspace other features. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md). ![Workspace search configurations migration](../image/mu-workspace-search-config-checkbox.png)

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

When migrating the search configuration from ITSM Agent Workspace to SOW, the **globalSearchDataConfigId** SOW page property is updated with SOW context config record sys\_id that is available in the base system.

## Procedure

1.  If the migration is successful, perform the following steps to verify the migration data.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Use the Global search on the SOW landing \(Home\) page to search all the record types such as Incident, User, or Knowledge.

        The search result displays the records in the order specified in the SOW search config table that contains all the application search sources along with the order value, migrated from ITSM Agent Workspace.![Search using global search in SOW](../image/mu-search-config-sow-home.png)

        You can also navigate to **All** &gt; **sow\_search\_config.list** to compare the application search sources and the order value in the Service Operations Workspace Search Config table with the Agent Workspace Search Config table to understand if migration is successful. The following screenshots depict both application search sources on the Service Operations Workspace Search Config table and the Agent Workspace Search Config table.

        The following screenshot depics the application search sources on the Service Operations Workspace Search Config table. ![Application search sources on the Service Operations Workspace Search Config table](../image/mu-search-app-config-sow.png)

        The following screenshot depicts the application search sources on the Agent Workspace Search Config table. ![Application search sources on the Agent Workspace Search Config table](../image/mu-search-app-config-aw.png)

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![Error](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/search-config-migration-itsm-aw-sow.md#section_s4z_14j_dcc) section.


**Parent Topic:**[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/search-config-migration-itsm-aw-sow.md)

