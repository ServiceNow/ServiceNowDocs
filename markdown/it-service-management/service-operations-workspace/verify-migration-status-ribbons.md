---
title: Perform post-migration tasks for ribbons
description: Verify that the ribbons in Service Operations Workspace \(SOW\) are consistent with the ribbons in ITSM Agent Workspace and the ribbons are ready for use in SOW. You can update the migrated ribbon settings in SOW based on your requirements.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for ribbons

Verify that the ribbons in Service Operations Workspace \(SOW\) are consistent with the ribbons in ITSM Agent Workspace and the ribbons are ready for use in SOW. You can update the migrated ribbon settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **Ribbons in the record form** option for ITSM Agent Workspace features. For example, the **Ribbons in the record form** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to confirm successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Select **Lists** from the navigation pane to open the **Lists** window in SOW and ITSM Agent Workspace.

    3.  Open a record from the available lists to compare in both workspaces.

        For example, select an incident by navigating to the **Incidents** list in both workspaces.

    4.  Compare the ribbons for that record in SOW and ITSM Agent Workspace records.

    5.  To modify any ribbon settings in SOW to match settings in **All** &gt; **sys\_ux\_ribbon\_config\_setting.list**.

        **Note:** Preconfigured ribbon settings for SOW might get turned off after the migration.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![System logs icon](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/ribbons-migration-itsm-aw-sow.md#section_irt_kq3_ccc) section.


**Parent Topic:**[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/ribbons-migration-itsm-aw-sow.md)

