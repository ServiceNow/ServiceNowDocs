---
title: Business rules installed with Field Service Management
description: Business rules are added with Field Service Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Components installed, Reference, Field Service Management]
---

# Business rules installed with Field Service Management

Business rules are added with Field Service Management.

<table id="table_BusinessRules"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Automatically moves a task from the **Assigned** state to **Accepted** if the **Accept/Reject** option is selected in Field Service Configuration.

</td></tr><tr><td>

Assigned

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Sets a task in the **Draft** state to the **Assigned** state if the **Assigned to** field is populated. This business rule is associated with the "Assigned \(Draft to Assigned\)" State flow.

</td></tr><tr><td>

Assigned\(state flow business rule\)

</td><td>

Work Order\[wm\_order\]

</td><td>

Automatically moves an order to the **Assigned** state if the **Assignment group** or **Assigned to** are populated. ServiceNow recommends not editing this business rule.

</td></tr><tr><td>

Auto close Deliver and Receive Tasks

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Automatically moves a transfer order line task to **Closed Complete** state whenever the part is received and delivered within the agent stockroom.

</td></tr><tr><td>

Cancel Work Task

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Cancels any transfer orders for a work order task, via State Flows, when a task is cancelled.

</td></tr><tr><td>

Create First Work Order Task

</td><td>

Work Order\[wm\_order\]

</td><td>

Creates the first task for a newly qualified work order.

</td></tr><tr><td>

Field Service Automation Group Types

</td><td>

Group\[sys\_user\_group\]

</td><td>

Ensures data integrity for dispatch group coverage information.

</td></tr><tr><td>

Field Service Automation Qualification

</td><td>

System Property\[sys\_properties\]

</td><td>

Turns off the qualification stage whenever the **work.management.qualification** system property is set to **No**. This business rule turns on the qualification stage when the property is set to **Yes**.

</td></tr><tr><td>

Populate Skills - Update Child Tasks

</td><td>

Work Order\[wm\_order\]

</td><td>

When the CI is changed, updates the skills required in tasks for the order to contain those skills.

</td></tr><tr><td>

Populate Work Order from Template

</td><td>

Work Order\[wm\_order\]

</td><td>

Populates a new work order from the work order model selected as a template.

</td></tr><tr><td>

Populate Window End Based On SLA

</td><td>

Task SLA\[task\_sla\]

</td><td>

Populates latest Task SLA breach date from the parent work order. Default value: Inactive

</td></tr><tr><td>

Populate Window End Based On SLA

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Populates latest Task SLA breach date from the parent work order. Default value: Inactive

</td></tr><tr><td>

Ready for Qualification \(approval off qu\)

</td><td>

Work Order\[wm\_order\]

</td><td>

Automatically moves a work order from the **Draft** state to **Ready for Qualification** when the **Template** field is populated.

</td></tr><tr><td>

Reassign

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Prevents task reassignment if the task has part requirements that are in a state of **In transit**.

</td></tr><tr><td>

RFD \(approval qual both off\)

</td><td>

Work Order\[wm\_order\]

</td><td>

Automatically moves a work order from the **Draft** state to **Ready** when the **Assigned to** or **Template** field is populated.

</td></tr><tr><td>

Roll Up Changes

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Updates the work order status based on changes to the work order task. This business rule rolls up the state changes that occur in tasks to the parent work order.If you don’t want the state changes that occur in tasks to roll up to the parent work order, implement a condition on this business rule.

Example condition: `current.sys_class_name != 'wm_task' && current.sys_class_name != 'wm_order'`

</td></tr><tr><td>

Start Work

</td><td>

Work Order\[wm\_order\]

</td><td>

Automatically moves a work order from the **Ready** state to **Work In Progress**.

</td></tr><tr><td>

Start Work\(state flow business rule\)

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Automatically moves a task to the **Work in process** state if the **Actual Start Work** field is populated.

</td></tr><tr><td>

State Change - After - Deprecated

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Ensures that the field service life cycle is followed. ServiceNow recommends not editing this business rule. This business rule is deprecated and is marked inactive for instances that are upgraded. This business rule is not installed for new instances.

</td></tr><tr><td>

State Change - Before

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Ensures that the field service life cycle is followed. ServiceNow recommends not editing this business rule. This business rule is deprecated and is marked inactive for instances that are upgraded. This business rule is not installed for new instances.

</td></tr><tr><td>

Sync up Delivery Time with WOT

</td><td>

Transfer Order\[alm\_transfer\_order\]

</td><td>

Synchronizes the delivery time with the work orders. Default value: Inactive

</td></tr><tr><td>

Transition - Cancel

</td><td>

Work Order\[wm\_order\]

</td><td>

Ensures that the field service life cycle is followed. ServiceNow recommends not editing this business rule.

</td></tr><tr><td>

Transition - PendingDispatchToAssign

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Ensures that the field service life cycle is followed.

</td></tr><tr><td>

Transition - StateChange - Deprecated

</td><td>

Work Order\[wm\_order\]

</td><td>

Ensures that the field service life cycle is followed. ServiceNow recommends not editing this business rule. This business rule is deprecated and is marked inactive for instances that are upgraded. This business rule is not installed for new instances.

</td></tr><tr><td>

Update questionnaires state to complete

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Closes all the pending optional questionnaires, when the work order task moves to Terminal state.

</td></tr><tr><td>

check active questionnaires

</td><td>

Work Order\[wm\_order\]

</td><td>

Blocks subsequent state updates on work order record, when there are pending mandatory questionnaires that need to be completed.

</td></tr><tr><td>

Check active questionnaires

</td><td>

Work Order Task\[wm\_task\]

</td><td>

Blocks subsequent state updates on work order task record, when there are pending mandatory questionnaires that need completed.

</td></tr><tr><td>

Work order task query rules

</td><td>

Work Order Task\[wm\_task\]

</td><td>

When set to active, the query rules on the underlying table will be used to filter the records based on territory of the logged-in user.

</td></tr><tr><td>

Work order query rules

</td><td>

Work Order\[wm\_order\]

</td><td>

When set to active, the query rules on the underlying table will be used to filter the records based on territory of the logged-in user.

</td></tr><tr><td>

Default record - Validation

</td><td>

Resource Schedule Attribute \[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

Ensures that an agent has only one default record for schedule attributes.

</td></tr><tr><td>

Record Validations

</td><td>

Resource Schedule Attribute \[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

Validates the records in the **Resource Schedule Attribute** table.-   Schedule attribute records for a resource shouldn’t have the same rank within the specified date range.
-   The date entered in the **From** should be earlier than the date entered in **To** field.

</td></tr><tr><td>

Restrict negative values

</td><td>

Resource Schedule Attribute \[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

 

</td></tr><tr><td>

Restrict the deletion of default records

</td><td>

Resource Schedule Attribute \[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

Prevents the deletion of the default schedule attribute record for a resource.

</td></tr><tr><td>

Validate Fields

</td><td>

Resource Schedule Attribute \[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

Validates the values for the fields. -   Maximum travel radius can’t be negative
-   Rank should be a whole number
-   Maximum part search radius can’t be negative

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Field Service Management](r_InstalledWithFSM.md)

