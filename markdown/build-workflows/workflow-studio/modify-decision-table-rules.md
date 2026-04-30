---
title: Modify decision table rules in Workflow Studio
description: Evolve with your business logic by modifying the rows, default result values, or content of your decision table in Workflow Studio.Account for changing business logic by defining default result values in your decision tables in Workflow Studio. Defining a default result accounts for scenarios when no decision rules are met by the input data.Modify conditions and results to update decision rules in a decision table in Workflow Studio.Save time and effort creating decision rules by strategically duplicating rows in a decision table in Workflow Studio. Determine or change the sequence in which your decision rules are evaluated by reordering the rows in a decision table in Workflow Studio. Enter a different number for your row in the Rank column to quickly reorder rows in large tables.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using decision tables, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Modify decision table rules in Workflow Studio

Evolve with your business logic by modifying the rows, default result values, or content of your decision table in Workflow Studio.

**Parent Topic:**[Using decision tables](using-decision-builder.md)

## Define default result values

Account for changing business logic by defining default result values in your decision tables in Workflow Studio. Defining a default result accounts for scenarios when no decision rules are met by the input data.

### Before you begin

Role required: admin

### About this task

If no values are defined in the Default result row or you have cleared values from the row, no default results are returned.

**Note:** You can set default results for decision tables created prior to Decision Builder version 4, but no values are set automatically. The Default result row is compatible with any decision tables created outside of Decision Builder with a default answer specified. If you have the decision\_result\_editor role, you need an admin or user with higher level permissions to set the initial default result for any decision tables created in an earlier version of Decision Builder.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Define at least one Result column in the decision table.

    With a result column defined, the Default result row appears at the bottom of the table.

5.  Define a default result for any columns that need one.

    **Note:** If any column has a default result value, and there are other result columns with the currency or true/false result types, those result columns automatically specify a default result. You can clear all default result values using the ellipsis menu on the row. However, if you add a default value in another column, currency and true/false result type columns auto-populate with a default value.

6.  Select **Save**.


## Modify a decision rule in a decision table

Modify conditions and results to update decision rules in a decision table in Workflow Studio.

### Before you begin

Role required: admin, decision\_table\_admin, or delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-dev-workflow&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Select the cell that you want to edit.

    -   Modify a condition in one of the following ways.
        -   Select the operator and replace it with another operator.
        -   Select the condition value and provide a new value.
        -   Update both the operator and the condition value.
    -   To modify a result, select the result value and provide a new value.
5.  To modify a decision table condition in Decision rule view, select the Decision rule row menu options icon \(![Decision rule row menu options.](../image/ellipses.png)\) to the left of the row number, and then select **Open in Decision rule view**.

    Decision rule view supports complex conditions that may not fit into the table structure.

    ![Decision rule view.](../image/decision-rule-view.png "Decision rule view")

    **Note:** Using Decision rule view can result in creating complex conditions. Tables with advanced rows can be edited in Excel but advanced rows are read-only. For more information, see [Manage decision tables in Excel](manage-decision-tables-ms-excel.md). Where possible, split complex decisions into multiple simplified decision rule rows.

    1.  Edit the condition as needed.

    2.  Select **Done** to commit your changes.

6.  Select **Save**.


## Duplicate rows in a decision table

Save time and effort creating decision rules by strategically duplicating rows in a decision table in Workflow Studio.

### Before you begin

Role required: admin, decision\_table\_admin, or decision\_rule\_author

### About this task

Plan the best way to duplicate rows to maximize efficiency and save time creating your decision table. For example, if you have five rows that have the same first condition, fill in the condition in the first row, and then duplicate the rows. Rows can be duplicated at any time and any point in their completeness.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Open a decision table.

4.  On the far left side of the row you want to duplicate, select the Duplicate decision row below this row icon \(![](../image/db-duplicate-row.png)\).


## Reorder decision rows in a decision table

Determine or change the sequence in which your decision rules are evaluated by reordering the rows in a decision table in Workflow Studio.Enter a different number for your row in the **Rank** column to quickly reorder rows in large tables.

### Before you begin

Role required: admin, decision\_table\_admin, or delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-dev-workflow&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Reorder the rows using either of the following methods.

<table id="choicetable_zvf_qr5_sbc"><tbody><tr><td id="d155299e563">

**Reorder by changing the Rank number**

</td><td>

1.  In the **Rank** column, double-click a number to edit it.
2.  Enter a new value for the row and press **Enter**.
 **Note:** If you change the number but don't press **Enter**, the rank does not change.

 This method is most effective for reordering rows in large decision tables.

</td></tr><tr><td id="d155299e596">

**Reorder by dragging and dropping a row**

</td><td>

1.  Point to a decision row and select the Row drag and drop gripper icon \(![Row drag and drop gripper icon](../image/Drag.png)\) in the far left.
2.  Reorder the rows by dragging the row to a new location.
 This method is most effective for reordering rows in smaller decision tables, as you can only see 20 rows at a time.

</td></tr></tbody>
</table>5.  Select **Save**.


