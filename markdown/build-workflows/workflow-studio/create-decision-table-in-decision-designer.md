---
title: Create decision tables in Workflow Studio
description: Create decision tables in Workflow Studio to embed business logic into a series of if-then decision rules. Use decision tables when business logic is complex or may be reused in multiple places.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using decision tables, Decision tables, Workflow Studio, Build workflows]
---

# Create decision tables in Workflow Studio

Create decision tables in Workflow Studio to embed business logic into a series of if-then decision rules. Use decision tables when business logic is complex or may be reused in multiple places.

## Before you begin

Role required: admin, decision\_table\_admin, or delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-app-dev-workflow.md).

## About this task

You can create decision tables for use in flows, subflows,playbooks, and scripts. Create your decision table and then reference it from one of those objects, or anywhere else on the platform that you write code. As of the Xanadu release, you can also create the structure of a decision table directly in a flow or playbook, and populate the table afterwards.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **New**.

3.  Select **Decision table**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Decision table name|Name for the decision table.|
    |Description|Description of the decision table.|
    |Application|Application scope for the decision table.|
    |Accessible from|Scopes that can use the decision table. Available values are **Application scope only**or **All application scopes**.|
    |Enable draft authoring|Option to author decision tables in draft mode before publishing to make them available for use. This function also enables you to change a decision table in draft mode after it has been published and republish with changes.|

5.  Select **Build decision table**.

6.  Select **Add an input**.

    **Note:** Note that adding more then 30 inputs to your table can adversely affect the performance of the application while you create the table.

7.  On the form, fill in the fields.

<table id="table_bm2_jzd_qqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Header for the input.

</td></tr><tr><td>

Type

</td><td>

Type of data used for the input.When the input type is **Reference**, a new column titled **Reference** appears in the input section and displays the reference table. This input type enables you to add multiple condition columns to a decision table.

The available input types are:

-   Choice
-   Currency
-   Date
-   Date/Time
-   Decimal
-   Due Date
-   Integer
-   Long
-   Reference
-   String
-   String \(Full UTF-8\)
-   True/False


</td></tr><tr><td>

Mandatory

</td><td>

Option for making an input field required when using the table.

</td></tr><tr><td>

Add reference filter

</td><td>

Option to filter the list of reference records in a linked condition column where the input type is **Reference** and the Data to evaluate is **Reference record**. Use this field to build a filter condition statement. For more information, see [Filter reference inputs and results in a decision table](../concept/format-decision-table-in-decision-designer.md#).

</td></tr></tbody>
</table>    **Note:** For the Choice input type, the ability to select an existing choice list depends on the choice list living on a table in the same application scope as the decision table. For example, if you create a decision table in the Global scope, you can use any existing choice list on tables in the Global scope. But, if you create a decision table in a custom scope, you can only use existing choice lists from tables in the same custom scope.

8.  Select **Add condition column**.

9.  On the form, fill in the fields.

<table id="table_dzj_sc2_qqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition column label

</td><td>

Label for the condition column.

</td></tr><tr><td>

Description

</td><td>

Brief overview of the condition column.

</td></tr><tr><td>

Input

</td><td>

Input linked to the condition column.To evaluate multiple fields, you can add multiple conditions with the Reference input type.

</td></tr><tr><td>

Table

</td><td>

If the data type is Reference, the name of the reference table is displayed.

</td></tr><tr><td>

Data to evaluate

</td><td>

For condition columns with the input type of Reference, specifies whether the condition column evaluates the reference record or a field on the reference table.

</td></tr><tr><td>

Condition type

</td><td>

Data type selected for the condition column.

</td></tr><tr><td>

Default operator

</td><td>

How every row in the condition column evaluates a user-specified value. A default operator is required for all input data types except for True or False.For more information about operators, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).

</td></tr></tbody>
</table>10. Select **Done**.

11. Add more condition columns.

    1.  Navigate to the last condition column, select the plus icon \(+\), and select **Add condition column**.

    2.  Point to a condition column and select the plus icon \(+\).

    3.  Select the **Add condition column** button to the right of an input.

12. Select **Add result column**.

13. On the form, fill in the fields.

<table id="table_ppp_pzm_vsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Result column label

</td><td>

Label for the result column.

</td></tr><tr><td>

Description

</td><td>

Brief overview of the result column.

</td></tr><tr><td>

Result type

</td><td>

Type of data used for the result column.The available result types are:

-   Choice
-   Currency
-   Date
-   Date/Time
-   Decimal
-   Due Date
-   Duration
-   Integer
-   Long
-   Reference
-   String
-   String \(Full UTF-8\)
-   True/False


</td></tr><tr><td>

Add reference filter

</td><td>

Option to filter the list of reference records in the result column when the result type is Reference. Use this field to build a filter condition statement. For more information, see [Filter reference inputs and results in a decision table](../concept/format-decision-table-in-decision-designer.md#).

</td></tr></tbody>
</table>    **Note:** The Currency and True/False result types have several important exceptions.

    -   If no alternate result is specified \(0.00 for currency, false for true/false\), cells in currency and true/false type result columns return a default value.
    -   For instances using multi-currency mode, you can specify currency results using any available instance currency. However, result values are always converted to the session currency on saving.
    -   For instances using single-currency mode, you can only specify currency results using the single instance currency.
14. Select **Done**.

15. Enable multiple results in a decision table by adding more result columns using one of the following methods.

    -   Navigate to the first result column, select the plus icon \(+\), and select **Add result column**.
    -   Navigate to the last result column and select the plus icon \(+\).
    -   Point to a result column and select the plus icon \(+\).
16. For each condition, click into the empty box in the condition column to select an operator and enter a value.

    ![Decision table with empty cells](../image/populate-decision-table.png)

    For more information about operators, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).

17. To modify a decision table condition in Decision rule view, select the Decision rule row menu options icon \(![](../image/ellipses.png)\) to the left of the row number, and then select **Open in Decision rule view**.

    Decision rule view supports complex conditions that may not fit into the table structure.

    ![Decision rule view.](../image/decision-rule-view.png "Decision rule view")

    **Note:** Using Decision rule view can result in creating complex conditions. Tables with advanced rows can be edited in Excel but advanced rows are read-only. For more information, see [Manage decision tables in Excel](../concept/manage-decision-tables-ms-excel.md). Where possible, split complex decisions into multiple simplified decision rule rows.

    1.  Edit the condition as needed.

    2.  Select **Done** to commit your changes.

18. For each result, click into the empty box in the result column and enter a result value.

    ![Empty decision table, adding results](../image/populate-decision-table-results.png)

19. Add more decision rules by selecting **Add new decision row** and entering conditions and desired results.

20. Select **Save**.

21. Select **Publish**.

    A modal appears asking if you’re sure you want to publish. If you want to make edits to this table after it's published, you must create a draft of the table. For more information about editing a published decision table, see [Edit decision tables using draft authoring](edit-decision-tables-using-draft-authoring.md).

22. Select **Publish**.


**Parent Topic:**[Using decision tables](../concept/using-decision-builder.md)

