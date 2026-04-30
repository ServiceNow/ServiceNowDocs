---
title: Create a decision table in a flow
description: Create the structure for a decision table while you author your flow in Workflow Studio. Use data from the flow to create inputs, conditions, and results for the decision table, all in a convenient modal. For example: You can store the logic for incident assignments in a Decision Table, and then use that Decision Table within a flow.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a flow, Building flows, Use, Workflow Studio, Build workflows]
---

# Create a decision table in a flow

Create the structure for a decision table while you author your flow in Workflow Studio. Use data from the flow to create inputs, conditions, and results for the decision table, all in a convenient modal. For example: You can store the logic for incident assignments in a Decision Table, and then use that Decision Table within a flow.

## Before you begin

Role required: admin, decision\_table\_admin, flow\_designer, or delegated developer permissions

## About this task

Creating a decision table in-line in a flow creates only the structure of the table with inputs, conditions, and results. To complete the table by adding the actual decision rules, you must open and edit the decision table in its own tab.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Flows**.

3.  Select a flow.

4.  Under Actions, select **Flow Logic**.

5.  Select **Make a Decision**.

6.  In the **Decision Label** field, enter a unique label for the decision.

7.  In the **Decision Table** field, select the Create new record \(![Create new record icon](../images/create-new-record-icon.png)\) icon.

    In the Create decision table modal, on the Set Properties page, two editable fields are populated from your flow.

    |Field|Description|
    |-----|-----------|
    |Decision table name|Unique name for the table. This name is populated from the **Decision Label**.|
    |Application|Application where the decision table lives. The application is populated based on the application that the flow is in.|

8.  Select **Next**.

9.  Select **Add input** to add inputs to the decision table.

    Inputs are the variables that define the type of data the decision table looks for to make decisions. When creating a decision table in a flow, you can add inputs directly from the data in the flow. For more information about the types of inputs you can add, see [Create decision tables in Workflow Studio](../../decision-table/task/create-decision-table-in-decision-designer.md).

    **Note:** Some inputs must be added or adjusted when you open the decision table to populate its values.

    -   If you want to add inputs of type Reference to this decision table, you must do that when you open the decision table in its own tab.
    -   If you want to add inputs of type Choice in this modal, the choices themselves don’t appear when you begin editing the decision table on its own. You must add them manually, because choice options are based on the scope you're in. For example, if you add a **Priority** field with **Choice** as the type, the options for priority \(Low, Medium, High, etc.\) are not added automatically. You can add them when you open the decision table to populate its values.
10. Select **Next**.

11. Select **Add Result Column** to begin adding the result columns to your table.

    Results are the outputs your decision table returns when certain conditions are met.

12. Add any additional configurations required for the result type that you selected.

13. Select **Create and Open**.

    The decision table opens in its own integrated tab within Workflow Studio. You can edit any part of the table here, including adding Reference type filters to the inputs or results.

    Condition columns are added to the decision table based on corresponding input fields.

14. Complete the decision table by adding decision rules to the condition columns and result values.

15. Select **Save**.

16. In your original flow, review and test the decision to make sure it produces the expected results.

17. Select **Done**.


**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

