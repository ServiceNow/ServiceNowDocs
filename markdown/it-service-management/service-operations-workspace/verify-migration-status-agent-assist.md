---
title: Perform post-migration tasks for Agent assist configuration
description: Verify that the Agent assist configurations in Service Operations Workspace \(SOW\) are consistent with the Agent assist configurations in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated Agent assist configuration settings in SOW based on your requirements.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for Agent assist configuration

Verify that the Agent assist configurations in Service Operations Workspace \(SOW\) are consistent with the Agent assist configurations in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated Agent assist configuration settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **Agent Assist Configuration** option for ITSM Agent Workspace features. For example, the **Agent Assist Configuration** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps to verify the Agent assist configuration.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Open a record in SOW that is corresponding to a table for which Agent assist configuration is migrated.

        For example: If you want to verify the Agent assist configuration migration status for an incident, navigate to **List** &gt; **Incident** &gt; **All** and then select any incident record.

    3.  Select the **Agent Assist** \(![agent assist icon](../image/agent-assist-icon.png)\) icon from the Contextual side panel.

    4.  Review the Agent assist side panel to verify that the Agent assist configurations for all selected tables are available in SOW same as in ITSM Agent Workspace.

    5.  Navigate to **All** &gt; **sys\_ux\_screen.list** and ensure that the Macroponent Configuration field and mappings are applied to Agent assist SNC record.

    6.  Perform thorough testing to confirm that all migrated configurations function as expected in SOW.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![Error](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/agent-assist-migration-itsm-aw-sow.md#section_knd_y5j_dcc).


**Parent Topic:**[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/agent-assist-migration-itsm-aw-sow.md)

