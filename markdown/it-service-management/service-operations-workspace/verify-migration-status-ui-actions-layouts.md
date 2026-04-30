---
title: Perform post-migration tasks for UI actions and layouts
description: Verify that the UI actions and layouts in Service Operations Workspace \(SOW\) are consistent with UI actions and layouts in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated UI actions and layouts settings in SOW based on your requirements.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for UI actions and layouts

Verify that the UI actions and layouts in Service Operations Workspace \(SOW\) are consistent with UI actions and layouts in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated UI actions and layouts settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **UI actions and layouts** option for ITSM Agent Workspace features. For example, the **UI actions and layouts** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Open a record in SOW that is corresponding to a table for which UI actions and layouts are migrated.

        For example: If you want to verify the UI actions and layouts migration status for an incident, navigate to **List** &gt; **Incident** &gt; **All** and then select any incident record.

    3.  Review the UI actions and the layout that are migrated from ITSM Agent Workspace to SOW.

    4.  If you want to rearrange the order of the UI actions layout, navigate to **All** &gt; **sys\_ux\_form\_action\_layout.list**

    5.  Search and select the table for which the UI actions and layout order must be changed.

        For example, Incident.

    6.  Edit the record.

    7.  Check whether the sys\_ux\_form\_action\_layout record is unified for the specified table.

        If the sys\_ux\_form\_action\_layout record is unified, **Unify action** button is not visible. If the sys\_ux\_form\_action\_layout record is not unified, select the **Unify action** option to unify the record. After the UI actions are unified, all the UI actions are displayed under UX Form Action Layout Items related list.

    8.  On the UX Form Action Layout Items related list, change the order of the UI actions as required to rearrange the layout on the record of the targeted table.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the Go to system logs icon \(![Error](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/ui-actions-layouts-migration-itsm-aw-sow.md#section_emh_j23_ccc) section.


**Parent Topic:**[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/ui-actions-layouts-migration-itsm-aw-sow.md)

