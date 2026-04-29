---
title: Perform post-migration tasks for view rules
description: Verify that the view rules in Service Operations Workspace \(SOW\) are consistent with the view rules in ITSM Agent Workspace and are ready for use in SOW. You can update the view rules settings in SOW based on your requirements.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for view rules

Verify that the view rules in Service Operations Workspace \(SOW\) are consistent with the view rules in ITSM Agent Workspace and are ready for use in SOW. You can update the view rules settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **Workspace views \(form and related list\) and view rules** option for ITSM Agent Workspace features. For example, the **Workspace views \(form and related list\) and view rules** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to confirm successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps.

    1.  Open SOW and for ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open for ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Select **Lists** from the navigation pane to open the **Lists** window in SOW and for ITSM Agent Workspace.

    3.  Open a record from the available lists to compare in both workspaces.

        For example, select an incident by navigating to the **Incidents** list in both workspaces.

    4.  Compare the view of the record, form layout, related lists, and related lists layout SOW and ITSM Agent Workspace records.

    5.  Check that user interface \(UI\) policies and client scripts of the ITSM Agent Workspace record are working in the SOW record.

        -   UI policies and client scripts that are applicable for the for ITSM Agent Workspace record also work in the SOW record after the migration of views and view rules.
        -   SOW records open in the same view as ITSM Agent Workspace records.
    6.  To modify any view rule in SOW to match settings in **All** &gt; **sysrule\_view\_workspace.list**.

        For more information about configuring view rules, see [Create a view rule](https://www.servicenow.com/docs/access?context=t_CreateAViewRule&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

        **Note:** Preconfigured view rules for SOW might get turned off after the migration.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![System logs icon](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/ribbons-migration-itsm-aw-sow.md#section_irt_kq3_ccc) section.


**Parent Topic:**[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/view-rules-migration-itsm-aw-sow.md)

