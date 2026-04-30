---
title: Enable expense type on resource assignments
description: Resource assignments have the same expense type as the project or demand for which they’re created. Enabling expense type on resource assignments helps you to accurately expense different type of expenses for your work.
locale: en-US
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure financials for Project Workspace, Configure, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Enable expense type on resource assignments

Resource assignments have the same expense type as the project or demand for which they’re created. Enabling expense type on resource assignments helps you to accurately expense different type of expenses for your work.

## Before you begin

Role required: admin

## Procedure

1.  Active and execute the scheduled job.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
    2.  Filter the name field to locate and open **Update task type planning attributes on resource assignments**.
    3.  Select the **Active** option to activate the schedule job.
    4.  Edit the fields on the Scheduled Script Execution form to customize the job and meet your requirements.

        For more information about the field description and scripts, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US#t_ScheduleScriptExecution).

    5.  Select **Execute Now** to execute the scheduled job or select **Update** to save your changes.
2.  Enable expense type on resource assignments.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
    2.  Filter the name field to locate and open the **sn\_plng\_att\_core\_resource\_assignment** table for resource assignments.
    3.  Select the **Show List** related link.
    4.  Select the **Personalize List** \(![Gear icon to personalize the list view.](../../alignment-planner-workspace/images/personalize-icon-product-idea.png)\) icon.
    5.  In the Personalize List Column, add **Expense type** from the Available list to the Selected list.
    6.  Select OK.

## Result

**Expense type** field is enabled on resource assignments for the projects and demands. You can expense different expense types to record different work types such as Capex or OpEx.

**Parent Topic:**[Configure financials for Project Workspace](../concept/config-fin-pws.md)

