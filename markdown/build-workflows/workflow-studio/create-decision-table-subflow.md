---
title: Create a decision table in a subflow
description: Create a decision table structure while you author your flow in Workflow Studio. Use data from the subflow to create inputs, conditions, and results for the decision table, all in a convenient modal.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Building subflows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a decision table in a subflow

Create a decision table structure while you author your flow in Workflow Studio. Use data from the subflow to create inputs, conditions, and results for the decision table, all in a convenient modal.

## Before you begin

Role required: admin, decision\_table\_admin, flow\_designer, or delegated developer permissions

## About this task

Creating a decision table in-line in a subflow only creates the structure of the table with inputs, conditions, and results. To complete the table by adding the actual decision rules, you must open and edit the decision table in its own tab.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  Select a subflow.

4.  Set **Subflow Inputs &amp; Outputs** for your subflows.

5.  Under Actions, select **Flow Logic**.

6.  Select **Make a Decision**.

7.  In the **Decision Label** field, enter a unique label for the decision.

8.  In the **Decision Table** field, select the Create new record \(![Create new record icon.](../images/add-record-button.png)\) button.

    In the Create decision table modal, on the Set Properties page, two editable fields are populated from your subflow.

    |Field|Description|
    |-----|-----------|
    |Decision table name|Unique name for the table. This name is populated from the **Decision Label**.|
    |Application|Application where the decision table lives. The application is populated based on the application that the subflow is in.|

    ![set properties](../../workflow-studio/images/set-properties.png)

9.  Select **Next**.

10. Select **Add input** to add inputs to the decision table.

    Inputs are the variables that define the type of data the decision table looks for making decisions. When creating a decision table in a subflow, you can add inputs directly from the data in the subflow. For more information about the types of inputs you can add, see [Create decision tables in Workflow Studio](../../decision-table/task/create-decision-table-in-decision-designer.md).

    **Note:** Some inputs must be added or adjusted when you open the decision table to populate its values.

    -   If you want to add inputs of type Reference to this decision table, you must do that when you open the decision table in its own tab.
    -   If you want to add inputs of type Choice in this modal, the choices themselves don’t appear when you begin editing the decision table on its own. You must add them manually, because choice options are based on the scope you're in. For example, if you add a **Priority** field with **Choice** as the type, the options for priority \(Low, Medium, High, and so on\) aren’t added automatically. You can add them when you open the decision table to populate its values.
11. Select **Next**.

12. Select **Add Result Column** to begin adding the result columns to your table.

    Results are the outputs your decision table returns when certain conditions are met.

13. Add any additional configurations required for the result type that you selected.

14. Select **Create and Open**.

    The decision table opens in its own integrated tab within Workflow Studio. You can edit any part of the table here, including adding Reference type filters to the inputs or results.

    Condition columns are added to the decision table based on corresponding input fields.

15. Complete the decision table by adding decision rules to the condition columns and result values.

16. Select **Save**.

17. In your original subflow, review and test the decision to make sure it produces the expected results.

18. Select **Done**.


**Parent Topic:**[Building subflows](../concept/subflows.md)

