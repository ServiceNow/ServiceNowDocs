---
title: Configure Task templates and Task template groups
description: Create task templates and task template groups to save individual tasks or groups of tasks for reuse. Add templates to new plans or insert them into existing ones.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-task-temp-temp-groups.html
release: australia
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [Configuring plan template, Setup for a BCP, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure Task templates and Task template groups

Create task templates and task template groups to save individual tasks or groups of tasks for reuse. Add templates to new plans or insert them into existing ones.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **Plan configuration** &gt; **Task templates**.

2.  To create a recovery task template, open the Recovery task templates section in the workspace and select **New** to create template.

3.  Enter a name and description for the template and add the required fields and task details.

4.  Save the template.

5.  To inspect a recovery task template, open it from the **Recovery task templates** list.

    The template form exposes the same recovery task fields as a non-template task, including Dependencies, Phase, Task classification, Tag, Configuration item, Asset recovery level, Tag assets, and Include task in. The **Plan templates**, **Loss scenarios**, and **Recovery strategies** related lists show every parent the template is currently attached to. For field-level details, see [Task template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/task-template-form.md).

    \[Omitted image "recovery-task-template-form.png"\] Alt text: Recovery task template form with related lists for Plan templates, Loss scenarios, and Recovery strategies.

6.  To create a Template group, select New in the Template Groups section.

    1.  Enter a group name.

    2.  Add individual task templates and set task dependencies as needed.

    3.  Set **Applicable to element definitions** to **All element definitions** or **Specific element definitions**, and select the element definitions that the group applies to.

        When the group is applied from a loss scenario whose element definition does not match, the group is hidden from the **Select task template groups** dialog.

    4.  Save the template group.

    The template group record includes tabs for **Task templates**, **Plan templates**, **Loss scenarios**, and **Recovery strategies**. Use the **Loss scenarios** tab to associate the group with specific loss scenarios such as Loss of Datacenters, so that tasks are automatically scoped when the group is applied to a plan.

    \[Omitted image "task-temp-group-tg1.png"\] Alt text: Task template group TG1 record showing the Loss scenarios tab with Loss of Datacenters listed as an associated scenario.

    \[Omitted image "task-template-groups-list.png"\] Alt text: Task template groups list showing Applicable to element definitions and Active columns.

    For field-level details, see [Task template group form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/task-template-group-form.md).


-   **[Task template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/task-template-form.md)**  
Use the Task template form to define a reusable recovery task or event task that can be inserted into plans, loss scenarios, recovery strategies, exercise events, crisis events, or activated plans.
-   **[Task template group form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/task-template-group-form.md)**  
Use the Task template group form to bundle related task templates and define dependencies between them. Apply the group from a plan, loss scenario, recovery strategy, exercise event, crisis event, or activated plan to create the underlying tasks in bulk.

**Parent Topic:**[Configuring plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-admin-plan-templates.md)

