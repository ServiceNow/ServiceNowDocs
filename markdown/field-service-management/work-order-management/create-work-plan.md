---
title: Create a work plan
description: Create a work plan to specify how and when the work should be performed for any activity.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure work plans, Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Create a work plan

Create a work plan to specify how and when the work should be performed for any activity.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin and model\_manager

## About this task

A work plan consists of the effective start and end date that determines the period for which the plan can be scheduled for execution. The plan won’t work beyond the specified end date.

Each work plan must have at least one or more records associated with it for which you want to apply the work plan. You can identify the records that require work by applying the filtering criteria to the selected table in the plan. For example, you can filter the matching records \(containing apple computers\) for a work plan by applying a filtering criteria to the table containing the records of computer that starts with "apple."

**Note:** The filtered assets or activities that require work are called matching records in the work plan.

You can also create a work plan through the Planned Work Management Workspace. Navigate to **All** &gt; **Planned Work Management** &gt; **Workspace**, and then select the **List** icon \(![List icon](../image/ListIcon.png)\).

## Procedure

1.  Navigate to **All** &gt; **Planned Work Management** &gt; **Plans**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_bwx_q3y_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number for the work plan.This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to determine if this work plan is available to use.

</td></tr><tr><td>

Effective start

</td><td>

Effective start date from when the work plan is active.

</td></tr><tr><td>

Effective end

</td><td>

Effective end date until when the work plan is active.

</td></tr><tr><td>

Forecast work orders

</td><td>

Option to specify if this work plan is applicable to estimate and generate the upcoming work orders.**Note:** When you check the check box, **Generate work orders** related list appears and you can generate work orders either from a work plan, a work schedule, or a schedule occurrence.

</td></tr><tr><td>

Enable grouping

</td><td>

Option to enable grouping of work orders based on the criteria like asset, location, or model.For more information on grouping of work orders and adding criteria for grouping, see [Add grouping criteria](add-grouping-criteria.md).

</td></tr><tr><td>

Template type

</td><td>

Specifies the template used for this work plan. The available options are:

-   **Work order template**- The work plan creates work orders and work order tasks based on the linked work order template. By default, Work order template is applied to a work plan.

**Note:** The work orders created for the work plan are automatically linked to their corresponding schedule occurrence. Administrators can configure the form layout of the work order to add the **Schedule occurrence** field.

-   **Task plan template**– The work plan creates tasks like cases and incidents based on the linked task plan template. For more information on the creation and usage of task plans, see [Task Plan Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/task-plan-templates.md).
**Note:**

-   Activate the Task Plan Templates \(com.sn\_task\_plan\_templates\) plugin from the ServiceNow Store and configure the extension point sn\_fsm\_planned\_wm.TaskPlanTemplateOutputTasks to attach task plan templates to the work plan. For more details about the extension point, see [Extension points in Field Service Management](../reference/extension-points-field-service.md).
-   You must update the state of the schedule occurrence when the state of the task changes.
-   You must link the output records \(cases or incidents\) with schedule occurrences because they are not linked automatically. You can link the output records by adding new field in the output record.
-   The **Template type** field is not available by default. The administrator can configure the form layout to add the **Template type** field.
-   You can modify the template type only if there are no templates attached.

To modify the template type, either delete the current attached templates before modifying, or create a new work plan with the preferred template type.

</td></tr><tr><td>

Name

</td><td>

Name of the work plan.

</td></tr><tr><td>

Short description

</td><td>

A short description of the work plan.

</td></tr><tr><td class="sub-head" colspan="2">

Conditions

</td></tr><tr><td>

Type

</td><td>

Type of trigger that determines when work should be performed.-   **Model based:** Base the work plan on a specified model of a CI.
-   **General:** Base the work plan on a table and filter.
-   **Install base:** Base the work plan on specified models of install base items
**Note:**

-   Model-based plans apply only to hardware models, specifically ones that have at least one model category defined.
-   Install base plan type is available only if the Customer Service Install Base Management \(com.snc.install\_base\) plugin is activated.


</td></tr><tr><td>

Model

</td><td>

Select one or more Product catalog items to identify the CIs or Install base that requires maintenance. When you select a model, the associated table appears in the Table field. For example, if you select a specific model of PC, the Table field displays **Computer \[cmdb\_ci\_computer\]**. This field appears if you selected either **Model based**or **Install base** type. For Install base type, The Table field automatically populates an appropriate table based on the selected model.

</td></tr><tr><td>

Table

</td><td>

Table you want to associate with the work plan.If you have selected Model Based in the **Type** field, this field displays the lowest level table that contains all the selected CIs. If you have selected Install base in the **Type** field, this field displays the install base tables.

</td></tr><tr><td>

Filter conditions

</td><td>

Filter conditions to locate the specific assets that you want to work. Only records in the selected table that match the filtering criteria require work.

</td></tr><tr><td>

Category

</td><td>

Determine whether the work plan is applicable for either category original equipment scheduling \(OEM\) or alternative equipment scheduling \(AEM\).

</td></tr><tr><td>

Apply to new matching records

</td><td>

Option to ensure that the schedules defined for this work plan are applied to all records that have been added to the specified table since the last time the plan was executed, also meet the conditions specified in the Filter conditions.

</td></tr><tr><td>

Task creation policy

</td><td>

Specify what to do when a work plan runs based on a schedule occurrence that is already in progress.-   **Leave alone:** Don’t allow the creation of new tasks or the deletion of existing ones.
-   **Cancel existing:** Allow the deletion of existing tasks associated with the plan and the creation of new tasks to replace them.
-   **Add to existing:** Allow new tasks to replace the existing active tasks for the specific schedule occurrence of a plan.


</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

-   The work plan is created successfully.
-   Specific activities that require work are identified from the selected table based on the filtering conditions.

## What to do next

After creating a work plan, configure a schedule to the work plan. For more information, see [Configure a work schedule](configure-work-plan.md)

