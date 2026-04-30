---
title: Add questions or instructions to a decision input
description: Create decision inputs for each decision node. Decision inputs appear in the form of questions in a workspace for service agents to answer.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add questions or instructions to a decision input

Create decision inputs for each decision node. Decision inputs appear in the form of questions in a workspace for service agents to answer.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

Create a decision path first. A decision node is automatically created with the same name as the decision path.

## About this task

Decision nodes can have one or multiple questions with different answer types.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select the start node or any decision node.

4.  Select **Create Input**.

5.  In the **Type** field, select the type of a decision input.

    **Note:** In the **Type** field, you have access to many input types. Select only one of the recommended input types listed the following table.

<table id="table_ugg_fft_qwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choice

</td><td>

A list of choices**Choice list specification**: Type of choice list.

You can create a choice list by clicking **New** in the Choices related list.

</td></tr><tr><td>

Date

</td><td>

Date in the format of YYYY-MM-DD

</td></tr><tr><td>

Date/time

</td><td>

Date and time in the format of YYYY-MM-DD HH:MM:SS

</td></tr><tr><td>

Decimal

</td><td>

A number with the decimal points

</td></tr><tr><td>

Integer

</td><td>

A number with no decimal points

</td></tr><tr><td>

Reference

</td><td>

Reference to a field from another table-   **Reference**: Reference table for selecting a field.
-   **Reference qual condition**: Condition to filter the search results.
For example, the Caller field on the Incident table is a reference to the User \[sys\_user\] table.

</td></tr><tr><td>

String

</td><td>

A line of text**Maximum number of characters**: Option to specify the length of the string

</td></tr><tr><td>

True/False

</td><td>

A check box field

</td></tr></tbody>
</table>6.  In the **Label** field, enter a question or instruction for customers.

7.  Select **Submit**.


## What to do next

[Determine the next node in a decision tree](create-decision-paths.md)

