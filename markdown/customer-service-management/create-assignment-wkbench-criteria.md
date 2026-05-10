---
title: Create assignment workbench matching criteria
description: Create one or more matching criteria that can be used in an assignment workbench configuration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure assignment workbench, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create assignment workbench matching criteria

Create one or more matching criteria that can be used in an assignment workbench configuration.

## Before you begin

Role required: admin

## About this task

The assignment workbench uses configurable matching criteria, such as skills and availability, to evaluate agents in a selected group and provide an overall ranking. The Matching Criteria \[matching\_dimension\] table stores the individual criterion that can be added to a matching rule to create an assignment workbench configuration.

## Procedure

1.  Navigate to **All** &gt; **Routing and Assignment** &gt; **Criteria**.

2.  Click **New**.

3.  Enter a **Name** and a **Description** for the criterion.

4.  Select the **Type** of matching criterion.

<table id="choicetable_at3_1ch_cw"><tbody><tr><td id="d225078e115">

**Simple Match**

</td><td>

Creates a one-to-one match. For example, match the time zone of an agent with the time zone of a task location.

</td></tr><tr><td id="d225078e124">

**Aggregate**

</td><td>

Takes a simple query as an input and provides aggregate results. The query returns a set of users.

</td></tr><tr><td id="d225078e133">

**Scripted**

</td><td>

Includes a scripted query which returns a list of users.

</td></tr></tbody>
</table>5.  To create a **Simple Match** criterion, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Applies to|The type of task that this criterion applies to.|
    |Field|The field from the selected task table that you want to match.|
    |Resource Table|The table that stores the resource to use for this matching criterion.|
    |Resource Matching Field|The field from the resource table that you want to match.|
    |Resource Field|The resource field to be displayed for the task records that match the resource records.|

6.  To create an **Aggregate** criterion, fill in the following fields.

<table id="table_g2m_atw_rx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Aggregate Table

</td><td>

The type of task that this criterion applies to.

</td></tr><tr><td>

Aggregate Filter

</td><td>

Use the condition builder to create a query that returns a set of users from the selected task table. For example, create a query that returns customer service cases with the following states: New, Open, Awaiting info.

</td></tr><tr><td>

Aggregate Field

</td><td>

The field from the selected task table to be displayed for the task records that match the query conditions.

</td></tr></tbody>
</table>7.  To create a **Scripted** criterion, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Script|Create a customized script which returns a list of users. An example script is included. The expected return from a customized script is an array of resource sys\_ids.|
    |Aggregate Field|The field from the selected task table to be displayed for the task records that match the query conditions.|

8.  Enter a **Display Name**.

9.  Enable the **Use Reference** field.

    If you use a reference field, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Reference Table|The table that stores the referenced information.|
    |Reference Filter|Add filter conditions to return the desired reference information.|
    |Reference Field|The field from the selected reference table to be displayed for the records that match the filter conditions.|
    |UI Filter Label|The label for this field that appears on the assignment workbench|

10. Click **Submit**.


**Related topics**  


[Matching criteria for case assignment](../concept/case-assignment-matching-criteria.md)

