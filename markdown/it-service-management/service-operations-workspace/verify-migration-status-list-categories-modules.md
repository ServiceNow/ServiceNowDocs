---
title: Perform post-migration tasks for list categories and modules
description: Verify that the list categories and modules in Service Operations Workspace \(SOW\) are consistent with the list categories and modules in ITSM Agent Workspace \(ITSM AW\) and the list categories and modules are ready for use in SOW. You can update the migrated list categories and modules settings in SOW based on your requirements.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for list categories and modules

Verify that the list categories and modules in Service Operations Workspace \(SOW\) are consistent with the list categories and modules in ITSM Agent Workspace \(ITSM AW\) and the list categories and modules are ready for use in SOW. You can update the migrated list categories and modules settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **List categories and modules** option for ITSM Agent Workspace features. For example, the **List categories and modules** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps to verify list categories and modules are similar in ITSM Agent Workspace and Service Operations Workspace.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Compare the list categories and modules in ITSM Agent Workspace and SOW.

        Ensure that the columnar layout and list applicabilities are correctly applied.

        The existing SOW list categories must be updated, and new categories must be created if ITSM Agent Workspace contains additional categories. The migration utility does not delete any existing or out-of-the-box categories from Service Operations Workspace.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![System logs icon](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-categories-modules-migration-itsm-aw-sow.md) section.


**Parent Topic:**[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-categories-modules-migration-itsm-aw-sow.md)

