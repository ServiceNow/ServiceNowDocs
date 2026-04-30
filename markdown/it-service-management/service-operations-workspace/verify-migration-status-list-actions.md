---
title: Perform post-migration tasks for list actions
description: Verify that the list actions in Service Operations Workspace \(SOW\) are consistent with the list actions in ITSM Agent Workspace \(ITSM AW\) and they’re ready for use in SOW. You can update the migrated list actions settings in SOW based on your requirements.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for list actions

Verify that the list actions in Service Operations Workspace \(SOW\) are consistent with the list actions in ITSM Agent Workspace \(ITSM AW\) and they’re ready for use in SOW. You can update the migrated list actions settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **List actions** option for ITSM Agent Workspace features. For example, the **List actions** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Open the forms in ITSM Agent Workspace and SOW.

        The migrated list actions are shown on the forms.

        Duplicate list actions might be displayed on the form when you don't migrate the view rule. So, SOW field declarative actions still show up even after migration if the view isn't changed.

        If the migration is successfully completed and not visible in the UI or not working properly the cross-check the conditions in Advance view.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![System logs icon](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-actions-migration-itsm-aw-sow.md) section.


**Parent Topic:**[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-actions-migration-itsm-aw-sow.md)

