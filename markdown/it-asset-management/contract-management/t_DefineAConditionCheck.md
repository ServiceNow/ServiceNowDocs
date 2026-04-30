---
title: Define a condition check
description: You can define a condition check to change values in a contract when the Contract Compliance Checks scheduled job runs each night.
locale: en-US
release: yokohama
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-01-20"
reading_time_minutes: 1
breadcrumb: [Condition check definitions, Contract Management, IT Asset Management]
---

# Define a condition check

You can define a condition check to change values in a contract when the **Contract Compliance Checks** scheduled job runs each night.

## Before you begin

Role required:

-   admin/contract\_manager/contract\_system\_admin: Read access
-   admin: Write access

## Procedure

1.  Navigate to **All** &gt; **Contract** &gt; **Administration** &gt; **Condition Check Definitions**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Table|The table to which the condition applies. For a contract check definition, select **Contract \[ast.contract\]**.|
    |Category|The category for the condition check. Select **Contract** or **None**. The category is used for organizing information and reporting.|
    |Condition field|The field to be updated, typically **Expiration level** or **State**.|
    |Event name|The name for the event to be fired when this condition changes the value of the field. Create a name using this syntax: &lt;table\_name&gt;.&lt;condition\_field&gt;, for example, `contract.validation`.|
    |Order|The order in which the conditions are evaluated.|

4.  Right-click the header bar and click **Save**.

    The **Conditions** related list appears.

5.  In the **Conditions** related list, click **New**.

6.  Complete the form.

<table id="table_f2d_ntr_gr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The value the field is set to, if the expiration conditions are met.

</td></tr><tr><td>

Condition check

</td><td>

The associated condition check.

</td></tr><tr><td>

Table

</td><td>

The table associated with the condition check.

</td></tr><tr><td>

Event name

</td><td>

The name of the event this condition triggers.

</td></tr><tr><td>

Expiration Condition

</td><td>

The condition that must be true for the **Condition check** field to be set to this value \(the **Name**\).Add as many conditions as are needed.

</td></tr><tr><td>

Compliant state

</td><td>

System field. Do not use.

</td></tr><tr><td>

Order

</td><td>

The order in which the conditions are evaluated. The first condition that is found to match, where the Expiration Condition is true, is used, and no others are checked.

</td></tr></tbody>
</table>7.  Click **Submit.**

    The Condition Checks form reopens with the new condition listed in the related list.

8.  Continue adding conditions as needed, following the steps above.


**Parent Topic:**[Condition check definitions](../concept/c_UseConditionCheckDefinitions.md)

