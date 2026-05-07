---
title: Modify decision table structure in Workflow Studio
description: Evolve with your business logic by modifying the inputs or columns of your decision table in Workflow Studio.Modify an input by changing the label, modifying the type and associated properties, and changing the mandatory toggle.Narrow down the list of results to only information that you need to see for Reference type input and result fields in decision tables in Workflow Studio.Make changes to an existing filter on Reference type inputs or results in decision tables in Workflow Studio.Delete inputs that are no longer necessary from your decision table in Workflow Studio. Deleting an input also deletes any related condition columns.Modify a condition column by renaming the label, editing the description, or updating the input type or default operator of your decision table in Workflow Studio.Change the data that a decision evaluates by changing the source table for that decision table in Workflow Studio.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using decision tables, Decision tables, Workflow Studio, Build workflows]
---

# Modify decision table structure in Workflow Studio

Evolve with your business logic by modifying the inputs or columns of your decision table in Workflow Studio.

**Parent Topic:**[Using decision tables](using-decision-builder.md)

## Modify an input for a decision table

Modify an input by changing the label, modifying the type and associated properties, and changing the mandatory toggle.

### Before you begin

Role required: admin, decision\_table\_admin, or delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-dev-workflow&version=australia&pubname=australia-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Choose the input that you want to modify.

5.  Modify the input.

    -   To modify the label, select the label, provide a new name, and press **Enter**.
    -   To change the input type, choose a different input type from the Type list.

        **Note:** The input type can be modified only if the input is not linked to a condition column.

    -   To modify the input type properties, select the property field and update the value.
6.  Select **Save**.


## Filter reference inputs and results in a decision table

Narrow down the list of results to only information that you need to see for Reference type input and result fields in decision tables in Workflow Studio.

### Before you begin

Role required: admin or decision\_table\_admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Create a filter for an input or result.

<table id="choicetable_mgh_hb1_cyb"><thead><tr><th align="left" id="d50270e271">

Action

</th><th align="left" id="d50270e274">

Description

</th></tr></thead><tbody><tr><td id="d50270e280">

**Create a filter for a Reference type input**

</td><td>

1.  Select **Add an input**.
2.  In the **Label** field, add a label for the input. For example, `Reference input`.
3.  In the **Type** field, select **Reference**.

The **Reference** column appears and displays the Reference table.

4.  In the **Table** field, select the table you want to reference. For example, `sys_user`.


</td></tr><tr><td id="d50270e330">

**Create a filter for a Reference type result**

</td><td>

1.  Select **Add result column**.
2.  In the **Result column label** field, enter a name for the field.
3.  In the **Result type** field, select **Reference**.
4.  Select the table that you want to reference in the **Result table** field.


</td></tr></tbody>
</table>5.  Select **Add reference filter**.

6.  Build a filter by adding conditions that contain a field, operator, and value.

    You can build a more complex filter by selecting **New condition set** and adding more conditions with **or** or **and** to string them together.

7.  Select **Done**.

8.  Add a linked reference condition column with the filters you've created applied by selecting **Add condition column** in the Reference input row.

9.  In the **Data to evaluate** section, select **Reference record**.

    A filtered input filters the list of records in linked condition column cells where the data to evaluate is **Reference record**. A filtered result column filters the list of records in the corresponding result column cells.

10. Select **Save**.


## Update an existing reference filter

Make changes to an existing filter on Reference type inputs or results in decision tables in Workflow Studio.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Select an input or result that you want to modify.

5.  Point to the result column header, and select the Edit column properties icon \(![Edit column properties icon](../image/Pencil.png)\).

6.  Select **Modify reference filter**.

7.  Make your changes and select **Done**.

8.  Select **Save**.


## Delete an input from a decision table

Delete inputs that are no longer necessary from your decision table in Workflow Studio. Deleting an input also deletes any related condition columns.

### Before you begin

Deleting an input from a decision table can break a flow, playbook, or script passing data through the input. Because of this possibility, you should know where the decision table is used before deleting anything from it.

Role required: admin, decision\_table\_admin, or delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-dev-workflow&version=australia&pubname=australia-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  At the end of the input row, select the Input menu options icon \(![Input menu options icon.](../image/ellipses.png)\), and select **Delete**.

5.  Select **Save**.


## Modify a decision table condition column

Modify a condition column by renaming the label, editing the description, or updating the input type or default operator of your decision table in Workflow Studio.

### Before you begin

Role required: admin, decision\_table\_admin, or delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-dev-workflow&version=australia&pubname=australia-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Point to the condition column header and select the Edit column properties icon \(![Edit icon.](../image/Pencil.png)\).

5.  Make your changes and select **Done**.

    **Note:** If you have an input of the type *Choice*, and you switch the input type to any other type, that action deletes all values from the condition column.

6.  Select **Save**.


## Modify a decision table result column

Change the data that a decision evaluates by changing the source table for that decision table in Workflow Studio.

### Before you begin

Role required: admin, decision\_table\_admin, delegated developer permissions. For more information, see [Delegate developers using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-dev-workflow&version=australia&pubname=australia-application-development&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a decision table.

4.  Point to the results column header and select the Edit column properties icon \(![Edit icon.](../image/Pencil.png)\).

5.  Replace the existing result table with a new source table.

    **Note:** Changing the result table deletes the current decision table results values.

6.  Select **Done**.

7.  Select **Save**.


