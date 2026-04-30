---
title: Create a knowledge article for a work order template
description: You can add knowledge articles and guides \(such as installation guides, maintenance procedures, and checklists\) to the default knowledge base for hardware, software, and consumable templates.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring work order templates, Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Create a knowledge article for a work order template

You can add knowledge articles and guides \(such as installation guides, maintenance procedures, and checklists\) to the default knowledge base for hardware, software, and consumable templates.

## Before you begin

Role required: wm\_admin or model\_manager

## Procedure

1.  Navigate to one of the following:

    -   **Product Catalog** &gt; **Templates** &gt; **Work Order Templates**
    -   **Field Service** &gt; **Catalog &amp; Knowledge** &gt; **Work Order Templates**
2.  Click **New**.

3.  Fill in the fields on the Work Order Template form, as appropriate.

<table id="table_nlm_5zm_mr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Request information

</td></tr><tr><td>

Name

</td><td>

\[Required\] Unique and descriptive name for this template.

</td></tr><tr><td>

Short description

</td><td>

\[Required\] Content that is copied into the **Short description** field of a work order when this work order template is used. The exception to this is a work order created from an incident, problem, or change request, which always uses the short description of the source task, even when a template is applied.

</td></tr><tr><td>

Description

</td><td>

More in-depth description of the purpose of the template.

</td></tr><tr><td>

Checklist template

</td><td>

Select a checklist template to add a checklist to the work orders created from this work order template. For information on checklists, see [Checklists](https://www.servicenow.com/docs/access?context=c_Checklists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Workflow

</td><td>

The workflow for work orders created from this template.

</td></tr><tr><td>

Qualification group

</td><td>

The qualification group for work orders created from this template.

</td></tr><tr><td class="sub-head" colspan="2">

Task information

</td></tr><tr><td>

Work configuration

</td><td>

The Work configuration for this task. Selecting a work configuration will automatically populate the **Task type** and **Work type** fields. Work configurations must be configured for this field to appear. For more information, see [Configuring Field Service Work Configurations](../../field-service-management/concept/configuring-work-configs.md).

</td></tr><tr><td>

Task type

</td><td>

The type of task to create. The default is **Work Order Task**.

</td></tr><tr><td>

Name

</td><td>

Unique and descriptive name for this task. As you start to type the description of the task, fields for your next task appear.

</td></tr><tr><td>

Description

</td><td>

A description of this task.

</td></tr><tr><td>

Task skills

</td><td>

Skills required by an agent to work on the task.**Note:** Select the **Mandatory** check box to indicate that this skill is required to perform the work order task.

</td></tr><tr><td>

Parts and quantities

</td><td>

Parts requirements and quantities, as needed. If you selected **Part requirements are not needed by agents** on the Field Service Configuration screen, the **Parts and quantities** fields are not displayed. **Note:** Select the **Mandatory** check box in front of all the parts that are required to perform the work order task.

</td></tr><tr><td>

Dispatch group

</td><td>

The dispatch group used to select the individuals who will fulfill the task. By default, ServiceNow filters the list of available dispatch groups by their proximity to the work order task location. When the **work.management.limit.location** property is set to **false**, the system displays all dispatch groups for selection, without any consideration of location. If only one dispatch group is available for a work order task in any location, ServiceNow automatically enters that group in this field. If the **Field Service will not use the dispatch queue** option is selected in the Field Service Configuration screen, this field is not displayed.

</td></tr><tr><td>

Depends on

</td><td>

Identifies the task of tasks that must be completed before this task can be performed. You cannot make an entry in the first task until you have created subsequent tasks.

</td></tr><tr><td>

Checklist template

</td><td>

Select a checklist template to add a checklist to the tasks created from this work order template.

</td></tr><tr><td>

Work Type

</td><td>

The type of work to be performed by an agent or crew to complete the task. -   Break Fix
-   Install
-   Planned Maintenance
 For more information, see [Create work types for a work order task](../../field-service-management/task/create-work-type-fsm.md).

</td></tr><tr><td>

Needs Crew

</td><td>

Indicator of work type associated with work order tasks that requires a group of agents to work on it. Administrator or Initiator can select or clear this option.

</td></tr></tbody>
</table>    Any hardware, software, and consumable assets you create and assign to the new template are displayed in the **Knowledge** related list on the template record.


