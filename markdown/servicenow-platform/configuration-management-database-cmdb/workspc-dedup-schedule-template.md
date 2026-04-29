---
title: Schedule a de-duplication template
description: Create a schedule, such as a monthly schedule, for a published de-duplication template so it will automatically run on a recurring interval.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CI de-duplication experience in a workspace, Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Schedule a de-duplication template

Create a schedule, such as a monthly schedule, for a published de-duplication template so it will automatically run on a recurring interval.

## Before you begin

The de-duplication template that you want to create a schedule for, must be in a published state. For information about publishing a template, see [Publish or unpublish a de-duplication template](workspc-dedup-unpublish-template.md).

Role required:

-   To access the [Management view in CMDB Workspace](../concept/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks, sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](../concept/sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor or sn\_cmdb\_admin
-   To perform this task, cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the navigation panel.
2.  Select the **De-duplication Dashboard** link in Management tools, in the Manage section.

3.  On the De-duplication templates pane, select the More options icon for the template that you want to create a schedule, and then select **Create schedule**.

4.  On the Schedule &lt;template&gt; dialog box, fill in the scheduling details.

    Various fields, such as **Time zone** and **Time** appear on the form according to your choice in the **Run** field. If **Run** is **Periodically**, you must set the **Repeat internal \(day\)** or the **Repeat interval \(time\)** fields \(or both\) before you can save the schedule.

5.  Select **Save**.


## Result

The newly created schedule is active by default.

## What to do next

Track the state and details of templates:

-   Select the **Running** tab to track the progress and details of the scheduled templates that are currently running. General counts for the template run appear when those counts become available. The templates are sorted by their start time, with the template with the most recent start time at the top of the list.

    -   Select **Details** \(accessible only after all de-duplication tasks have been calculated\) to show further details about this run and to drill down to de-duplication tasks.
    -   Select **Cancel** to stop a template's run. The details for the cancelled template are added in the **Completed** tab with the state of Cancel Requested. Upon completing the cancellation, the state changes to Cancelled.
    After a template run completes, its details no longer appear under the **Running** tab, but are available in the **Completed** tab. Also, the completed template is available again for running in the **Ready** tab.

-   Select the **Completed** tab to view general counts per template, such as erroneous and skipped tasks, and general run time. The templates are sorted by their completion time, with the template that completed most recently at the top of the list. Select **Details** for a template to access a list view of the template's assigned de-duplication tasks. This list view shows details for each de-duplication task, such as its state \(color coded\) and error message if applicable. You can drill down a de-duplication task for further details.
-   Select **View de-duplication tasks that need your attention** in the De-duplication tasks completed with errors card in the De-duplication insights pane on the right. The De-duplication tasks with errors list view shows de-duplication tasks that didn't complete successfully along with an error message. You can drill down de-duplication tasks in the list for more details.

On the De-duplication templates pane, select the More options icon for a template with a schedule. Some of the following options appear, according to the state of the schedule:

-   Select **Edit schedule** to modify the schedule.
-   Select **Deactivate schedule** to halt temporarily the automatic runs of the template, while preserving the schedule settings.
-   Select **Activate schedule** to resume automatic runs of the template according to the schedule settings.

**Parent Topic:**[CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md)

