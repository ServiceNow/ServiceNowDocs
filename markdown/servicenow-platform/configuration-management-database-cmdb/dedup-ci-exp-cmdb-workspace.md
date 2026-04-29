---
title: CI de-duplication experience in CMDB Workspace and in Service Graph Workspace
description: Create libraries of de-duplication templates in CMDB Workspace or in Service Graph Workspace, to process de-duplication tasks which remediate duplicate CIs, in a consistent manner and in bulk. De-duplication templates are pre-configured with all necessary settings for remediating duplicate CIs in de-duplication tasks, per class.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI de-duplication experience in CMDB Workspaceand in Service Graph Workspace

Create libraries of de-duplication templates in CMDB Workspaceor in Service Graph Workspace, to process de-duplication tasks which remediate duplicate CIs, in a consistent manner and in bulk. De-duplication templates are pre-configured with all necessary settings for remediating duplicate CIs in de-duplication tasks, per class.

Use the De-duplication dashboard in [CMDB Workspace](cmdb-workspace.md) or in [Service Graph Workspace](sg-workspace.md) to see an overview and insights about duplicate CIs in your CMDB. The De-duplication dashboard lets you create de-duplication templates and organize these templates into libraries. You can also examine de-duplication tasks and then run a preconfigured template to remedy duplicate CIs in multiple de-duplication tasks in a single operation.

More information:

-   To learn about general duplicate CI remediation concepts, restrictions, and special cases such as remediations that involve a large number of duplicate CIs, see [Duplicate CIs remediation](de-duplication-tasks.md).
-   To process a single de-duplication task manualy, using the Duplicate CI Remediator, see [Remediate a de-duplication task \(manual\)](../task/reconcile-dup-task.md).
-   To learn about Identification and Reconciliation \(IRE\) processes that detect duplicate CIs and other concepts related to duplication CI, see [Detecting duplicate CIs](id-detect-dup-ci.md).

## Access

1.  Access either workspace:
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the Service Graph Workspace navigation panel.
2.  In the Manage group in Management tools, select either of the following links:
    -   **De-duplication Dashboard**
    -   **De-duplication Template Library**

Role required:

-   To access the [Management view in CMDB Workspace](cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks: sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor or sn\_cmdb\_admin
-   To perform de-duplication tasks, cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## De-duplication templates and libraries

Use a de-duplication template to apply a consistent remediation to multiple, similar, de-duplication tasks, in a single action. A de-duplication template contains the settings that are required to processing de-duplication tasks for a class. For example, how to choose the main CI, which method to use to consolidate attributes, and what to do with the duplicate CIs \(aside from the main CI\) after remediation. A de-duplication template also contains conditions that de-duplication tasks are matched on. When you run a de-duplication template, the remediation settings in the template are applied to all de-duplication tasks that match the template conditions.

To be able to run a de-duplication template, the template must be in a published state \(a template is initially in a draft state\).When published, you can create a schedule for a de-duplication template so it will automatically run on a recurring time interval. When necessary, you can unpublish a published template so it is temporarily unavailable for use until you republish it.

Organize your de-duplication templates into libraries to group templates by categories that are meaningful in your organization and to help locate a template. For example, you can create several de-duplication templates, all of which for the same CMDB class such as **cmdb\_ci\_win\_server**. Then, add all those templates to the 'De-duplication templates for cmdb\_ci\_win\_server' library for easy access.

## De-duplication Dashboard

The De-duplication dashboard is a central location for remediating de-duplication tasks. Use the dashboard to:

-   See all de-duplication templates on a set of cards. Each card shows details about a template. On a template card, you can select **Assign task** to assign de-duplication tasks to the template, and run the template to process its associated de-duplication tasks.You can also create a recurring schedule for a template such as daily and monthly.
-   Select **Run all** to run all templates, each template remediating its assigned and matching de-duplication tasks.
-   Select **View de-duplication tasks** to access a list view of de-duplication tasks with details such as the de-duplication template assignment. In the list view, you can select **Only show tasks that do NOT match any template conditions** to show only those de-duplication tasks that are unassigned or unmatched to any template class.
-   Select **View template libraries** to create and manage de-duplication templates and libraries.
-   Select the **Running** tab to track templates that are currently running.
-   Select the **Completed** tab to check the status and details about the final state of a run, such as Completed, Cancelled, or Completed with errors.

## De-duplication insights pane

The De-duplication insights pane on the right side of the De-duplication dashboard provides counts and insights related to the on-going de-duplication processes in your organization. This pane provides the following cards and links to help you resolve issues:

-   Total count of de-duplication tasks that were processed in the past week.
-   De-duplication tasks that have completed with various types of errors and therefore need your attention. Provides the **View de-duplication tasks that need your attention** link to access a list view of the associated de-duplication tasks. You can examine error messages and drill down tasks for further troubleshooting details.
-   De-duplication tasks that don't match the conditions in any template and therefore can't be assigned for remediation by a template. Provides the **View de-duplication tasks that don't match** link to access a list view of the associated de-duplication tasks. You can drill down tasks for further details.

Review the de-duplication templates and ensure that they're properly configured for remediating the on-going duplicate CIs that are being generated in the CMDB by newly added data.

## Manage duplicate CIs skill

You can use the manage duplicate CIs skill that Now Assist for CMDB provides to get step-by-step guidance through the de-duplication process. The manage duplicate CIs skill guides you through reviewing de-duplication templates, assigning tasks to the templates, and then running the templates. The manage duplicate CIs skill presents you with relevant options for your next step, as you go, until you complete the remediation.

For more information, see [Now Assist for Configuration Management Database \(CMDB\)](now-assist-landing-cmdb.md).

-   **[Create a de-duplication template](../task/workspc-dedup-create-template.md)**  
Create a de-duplication template that you can then run to apply pre-configured and consistent remediation to de-duplication tasks, in bulk. Organize your templates in libraries that make sense in your organization.
-   **[Run a template to process de-duplication tasks](../task/workspc-dedup-run-template.md)**  
Run a de-duplication template to run de-duplication tasks that remediate duplicate CIs, in bulk. A de-duplication template is pre-configured with remediation settings per class. Running a de-duplication template, processes its assigned de-duplication tasks, consistently, according to the template settings.
-   **[Remediate a single de-duplication task](../task/workspc-dedup-remediate-single-task.md)**  
Remediate a single de-duplilcation task using a de-duplication template in CMDB Workspace,in Service Graph Workspace, or manually, using the Duplicate CI Remediator.
-   **[Publish or unpublish a de-duplication template](../task/workspc-dedup-unpublish-template.md)**  
After creating a de-duplication template, you must publish the draft template to make it available to run. You might also need to unpublish a published de-duplication template so it's temporarily unavailable for de-duplication remediation, until you republish it again.
-   **[Schedule a de-duplication template](../task/workspc-dedup-schedule-template.md)**  
Create a schedule, such as a monthly schedule, for a published de-duplication template so it will automatically run on a recurring interval.
-   **[Retire a de-duplication template](../task/workspc-dedup-retire-template.md)**  
Retire a template that is no longer needed for processing its de-duplication tasks which remediate duplicate CIs.

**Parent Topic:**[Duplicate CIs remediation](de-duplication-tasks.md)

