---
title: Create a Change approval policy using decision builder
description: Create a change approval policy using the Change approval policy decision builder to define the approvals that should be generated for your change.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating change approval policies, Use, Change Management, IT Service Management]
---

# Create a Change approval policy using decision builder

Create a change approval policy using the Change approval policy decision builder to define the approvals that should be generated for your change.

## Before you begin

The Decision Builder \[sn\_decision\_design\] plugin must be installed.

A change approval policy can be applied to a change request. An approval policy can contain multiple decisions allowing a single policy to handle every approval required for a change type. When a decision condition matches, the related approval definition is evaluated.

Role required: admin or change\_manager

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Policy** &gt; ****.

2.  Select **Create new change approval policy**.

3.  Enter the name of the policy.

4.  In the **Execution** field, select an option to determine the approach to implement your decision.

<table id="choicetable_dsq_35w_f5b"><tbody><tr><td id="d110743e102">

**First decision that matches**

</td><td>

Uses the first matching decision in ascending order of the value defined in the **Order** column of the **Decisions** list. The associated approval definition is applied.

</td></tr><tr><td id="d110743e120">

**Run all decisions that match**

</td><td>

Uses all matching decisions and applies the associated approval definition.

</td></tr></tbody>
</table>5.  Select **Create &amp; Continue**.

6.  Select **Add an input**.

7.  On the form, fill in the fields.

<table id="table_opv_p5w_f5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Header of the input.

</td></tr><tr><td>

Type

</td><td>

Type of data used for the input.

 When the data type is **Reference**, a new column titled Reference appears in the form. The reference is the table associated with the input.

 The available input types are:

 -   Choice
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


</td></tr></tbody>
</table>8.  Add a condition by selecting **Add Condition Column**.

9.  On the form, fill in the fields.

<table id="table_lgc_z5w_f5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition column label

</td><td>

Label for the condition.

</td></tr><tr><td>

Description

</td><td>

Brief overview of the condition.

</td></tr><tr><td>

Input

</td><td>

Input linked to the condition column.

 To evaluate multiple fields, you can add multiple conditions with the Reference input type.

</td></tr><tr><td>

Table

</td><td>

If the data type is **Reference**, this field is automatically set to the name of the reference table.

</td></tr><tr><td>

Data to evaluate

</td><td>

If the input type is **Reference**, specifies whether the condition evaluates a reference record or a field from the reference table.

</td></tr><tr><td>

Condition type

</td><td>

Data type selected for the input.

</td></tr><tr><td>

Default operator

</td><td>

Operator used to evaluate a user-specified value. A default operator is required for all input data types except for True or False.

</td></tr></tbody>
</table>10. Add more conditions by navigating to the last condition column and the plus icon \(+\) or by pointing to a condition column and clicking the plus icon \(+\).

11. For each condition cell, select an operator and enter a value.

    For example, if you wanted to evaluate the change approval policy only for hardware issues, you could set the condition **\[Assignment group\]\[is\]\[Hardware\]**.

12. Select the result column, and then select a desired Change approval definition from the list.

13. In the form header, click **Save**.


## Result

A change approval policy is created and is evaluated on a change request that matches the defined condition.

**Parent Topic:**[Creating change approval policies](../concept/using-change-approval-policies-cf.md)

