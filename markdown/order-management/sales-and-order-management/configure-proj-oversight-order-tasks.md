---
title: Configure project oversight for order tasks
description: Specify the conditions and decision rules that qualify order tasks for project oversight. You also specify the project template task used by Order Management to create the project for order tasks. The project template task defines the project tasks for the order tasks.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up project oversight conditions and decision rules, Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Configure project oversight for order tasks

Specify the conditions and decision rules that qualify order tasks for project oversight. You also specify the project template task used by Order Management to create the project for order tasks. The project template task defines the project tasks for the order tasks.

## Before you begin

Role required: admin

## About this task

Use the Project Management Oversight for Order Task Decision Builder to add or change the conditions and decision rules that an order task must meet to be tracked as a project. For example, if you want projects to be created for order tasks for a particular request type, you can add a condition column for **Type**.

## Procedure

1.  Navigate to **All** &gt; **Decision Management** &gt; **Decision Builder**.

2.  Select the **Project Management Oversight for Domain Order** decision table.

    The Order Task item is displayed in the **Inputs** and the **Project Template Task** column in the **Results**.

3.  Add a condition that a domain order must match.

    1.  Select **Add Condition column**.

    2.  On the form, fill in the fields.

<table id="table_uky_vvw_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition column label

</td><td>

Label for the column.

</td></tr><tr><td>

Description

</td><td>

Brief overview of the condition.

</td></tr><tr><td>

Input

</td><td>

Input linked to the condition column.To evaluate multiple fields, you can add multiple conditions with the Reference input type.

</td></tr><tr><td>

Table

</td><td>

If the data type is Reference, the name of the reference table is displayed.For domain items, the table is Order Task \[sn\_ind\_tmt\_orm\_order\_task\].

</td></tr><tr><td>

Data to evaluate

</td><td>

For condition columns with the input type of Reference, specifies whether the condition column evaluates the reference record or a field on the reference table.To evaluate a particular field, select **Field** and choose a field from the Order Task table, such as **Request Type** \(Order Task.request\_type\) to specify a request type.

</td></tr><tr><td>

Condition type

</td><td>

Data type selected for the condition column.

</td></tr><tr><td>

Default operator

</td><td>

How every row in the condition column evaluates a user-specified value. A default operator is required for all input data types except for True or False.

</td></tr></tbody>
</table>    3.  Select **Save**.

    4.  Repeat steps 3a through 3c for each condition to be added.

4.  Enter a decision rule by selecting **Add new decision row**.

    1.  Select the **Add** action and enter the conditions and project template task to be used.

        **Note:** If there are duplicate project template tasks that have the same **Short description**, it may be difficult to identify and select the appropriate project template task. For details on differentiating between similar project template tasks, see [Choosing a project template task when duplicates exist](../concept/Determining-correct-project-task-template.md).

    2.  Select **Save**.

    3.  Repeat steps 4a through 4c for each decision rule to be added.


## Result

The system uses the specified project template task to create projects for order tasks that match the conditions and decisions rules defined in the Project Oversight for Order Task decision table.

