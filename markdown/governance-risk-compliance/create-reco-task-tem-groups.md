---
title: Apply Task templates and Task template groups
description: Save individual tasks or groups of tasks for reuse across plans. You can add templates to new plans or inserted into existing ones. You can also generate templates directly from tasks and plans that already exist in the system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-reco-task-tem-groups.html
release: australia
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Apply Task templates and Task template groups

Save individual tasks or groups of tasks for reuse across plans. You can add templates to new plans or inserted into existing ones. You can also generate templates directly from tasks and plans that already exist in the system.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager

## About this task

Key behaviors:

-   You can create templates for a single task or for a group of tasks.
-   Define dependencies between tasks within a task group.
-   Only administrators and plan managers can add tasks to groups. Contributors and planners do not have this permission.
-   Use the **Add groups** and **Add tasks** controls on the **Recovery tasks** tab toolbar to apply a template group or individual task templates to a plan, loss scenario, or recovery strategy.
-   Each template group is scoped by an **Applicable to element definitions** field. Selecting **All element definitions** makes the group available on every plan, loss scenario, and recovery strategy. Selecting **Specific element definitions** restricts the group to loss scenarios \(and their recovery strategies\) whose element definition is in the list.

**Note:** UI action labels use the simplified terms “task template” and “template group” for consistency.

When applying a template group to a plan, use the **Add groups** toolbar control on the **Recovery tasks** tab. The **Select task template groups** dialog lists all active template groups with their name, description, and active status. Selecting a group adds all its task templates to the plan and automatically associates them with the configured loss scenarios and recovery strategies.

\[Omitted image "select-task-templates-groups-list.png"\] Alt text: Select task template groups dialog listing available groups such as TG1 with their description and active status.

**Note:** Verify that Task templates and Task template groups are set up in the application. For more information, see [Configure Task templates and Task template groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-task-temp-temp-groups.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Plan record** &gt; **Recovery tasks**.

2.  To apply a task template or template group to a plan, open the plan and select the **Recovery tasks** tab.

    1.  To apply a template group, select **Add groups** and to apply individual task templates, select **Add tasks**.

    2.  Browse or search for the group or template that you want to use.

    3.  Select the group or template and select **Add**.

        The tasks from the group or template are added to the plan.

3.  To create a template from an existing task \(upgraded customers\), Open the plan that contains the task you want to convert to a template.

    1.  Locate the task in the Recovery tasks list.

    2.  Select the task’s action menu and choose **Save as template**.

    3.  Enter a name for the new template and select **Save**.

        The template is now available for reuse in other plans.


**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

