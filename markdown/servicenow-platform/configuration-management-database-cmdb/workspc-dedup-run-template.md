---
title: Run a template to process de-duplication tasks
description: Run a de-duplication template to run de-duplication tasks that remediate duplicate CIs, in bulk. A de-duplication template is pre-configured with remediation settings per class. Running a de-duplication template, processes its assigned de-duplication tasks, consistently, according to the template settings.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CI de-duplication experience in a workspace, Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Run a template to process de-duplication tasks

Run a de-duplication template to run de-duplication tasks that remediate duplicate CIs, in bulk. A de-duplication template is pre-configured with remediation settings per class. Running a de-duplication template, processes its assigned de-duplication tasks, consistently, according to the template settings.

## Before you begin

Role required:

-   To access the [Management view in CMDB Workspace](../concept/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks: sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](../concept/sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor or sn\_cmdb\_admin
-   To perform this task: cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## About this task

You can run a single template to process its associated de-duplication tasks, or run all published templates at once, each remediating duplicate CIs in its associated tasks. Before running any templates, ensure that those templates are properly configured with their remediation settings and are properly assigned with de-duplication tasks. De-duplication tasks can be automatically assigned to a template based on the template conditions. You can also manually assign additional de-duplication tasks to a template.

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the navigation panel.
2.  Select the **De-duplication Dashboard** link in Management tools, in the Manage section.

3.  Select a template library in the **Ready** tab, or select **All libraries** in the libraries drop-down list \(set to **All libraries** by default\).

    The set of cards is filtered to show only the templates from the selected library, or to show all templates from all libraries if you select **All libraries** from the drop-down list.

4.  On the De-duplication templates page, select **Run all** to run all de-duplication templates on their assigned de-duplication tasks.

    To assign de-duplication tasks to a template or to run a single template, continue with the following steps.

5.  On the De-duplication templates page, locate the card with the template that you want to run and select **Assign tasks** in that card.

6.  Select the tasks in the Available de-duplication tasks list that you want to process using the selected de-duplication template. Then select **Add Selected** to assign the selected tasks to the current template.

    Available de-duplication tasks lists all open de-duplication tasks, some of which can be non-compatible with the template. If you try to associate a non-compatible task, an error appears. Some of the tasks in the list might be assigned to another template, and you can reassign those to the current template.

    The Assigned de-duplication tasks pane on the right contains two tabs:

    -   **All matching tasks**: Shows de-duplication tasks that match the condition of the selected template.
    -   **Your selected tasks**: Shows the tasks that you’ve assigning to the template for remediation.
    The selected tasks are added to the list in the **Your selected tasks** tab in the Assigned de-duplication tasks pane on the right. The template will run for all tasks in the **Your selected tasks** list and any tasks in the **All matching tasks** list that aren't assigned to another template.

7.  Select **Run template**.

    The selected template is added to the running queue.


## What to do next

-   Select the **Running** tab to track the progress and details of templates that you added to the running queue and are currently running. General counts for the template run appear when those counts become available. The templates are sorted by their start time, with the template with the most recent start time at the top of the list.

    -   Select **Details** \(accessible only after all de-duplication tasks have been calculated\) to show further details about this run and to drill down to de-duplication tasks.
    -   Select **Cancel** to stop a template's run. The details for the cancelled template are added in the **Completed** tab with the state of Cancel Requested. Upon completing the cancellation, the state changes to Cancelled.
    After a template run completes, its details no longer appear under the **Running** tab, but are available in the **Completed** tab. Also, the completed template is available again for running in the **Ready** tab.

-   Select the **Completed** tab to view general counts per template, such as erroneous and skipped tasks, and general run time. The templates are sorted by their completion time, with the template that completed most recently at the top of the list. Select **Details** for a template to access a list view of the template's assigned de-duplication tasks. This list view shows details for each de-duplication task, such as its state \(color coded\) and error message if applicable. You can drill down a de-duplication task for further details.
-   Select **View de-duplication tasks that need your attention** in the De-duplication tasks completed with errors card in the De-duplication insights pane on the right. The De-duplication tasks with errors list view shows de-duplication tasks that didn't complete successfully along with an error message. You can drill down de-duplication tasks in the list for more details.
-   [Schedule a de-duplication template](workspc-dedup-schedule-template.md).

**Parent Topic:**[CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md)

