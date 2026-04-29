---
title: Add or modify risk and impact conditions
description: You can define risk calculation rules on which the risk and impact of a change are calculated. Best Practice - Change Risk Calculator is activated by default in the base system.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Risk conditions and calculation, Analyze change request risk and impact, Reference, Change Management, IT Service Management]
---

# Add or modify risk and impact conditions

You can define risk calculation rules on which the risk and impact of a change are calculated. Best Practice - Change Risk Calculator is activated by default in the base system.

## Before you begin

Role required: itil\_admin or admin

## About this task

Risk Conditions are run against the change request based on their **Order** field from lowest to highest. The first Risk Condition that matches the change request record is applied. All subsequent risk conditions are then ignored whether they match or not. A risk calculation rule is defined with two elements.

-   Conditions that can evaluate to *true* or *false*. You can use a condition builder or write a script.
-   **Risk** and **Impact** field value settings when the conditions evaluate to **true**.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Risk Conditions**.

2.  Click **New**, or click the risk condition to modify.

    You can also edit risk conditions from within the Change Request form by opening the form context menu and clicking **Edit Risk Conditions**.

3.  Complete or update the form, as appropriate.

<table id="table_xym_4zl_wy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name for the rule

</td></tr><tr><td>

RiskImpact

</td><td>

Select a value for one of these fields. The selection determines which field to update based on this risk calculation.

</td></tr><tr><td>

Active

</td><td>

Select the check box to use the rule.

</td></tr><tr><td>

Order

</td><td>

Enter the order in which this risk calculation is evaluated. Rules with lower numbers are evaluated first. If there are two or more rules with differing orders, the rule with the lowest order is evaluated and the others are ignored.

</td></tr><tr><td>

Use advanced condition

</td><td>

Select the check box to enter a script instead of using the condition builder.

</td></tr><tr><td>

Use script values

</td><td>

Select the check box to hide the **Risk** and **Impact** fields. The script specifies the risk and impact values.

</td></tr><tr><td>

Description

</td><td>

Enter a description of how this risk calculation is applied.

</td></tr></tbody>
</table>4.  Specify the rule based on your selected rule method.

<table id="choicetable_zdq_xvm_lz"><thead><tr><th align="left" id="d216474e223">

Choice

</th><th align="left" id="d216474e226">

Action

</th></tr></thead><tbody><tr><td id="d216474e232">

**Condition**

</td><td>

Use the condition builder to add conditions. It is hidden if you selected **Use advanced condition**.

</td></tr><tr><td id="d216474e244">

**Use advanced conditions**

</td><td>

Write the script in the **Advanced condition** field using standard business rule syntax. The condition must set the global variable answer to *true* or *false*.

</td></tr><tr><td id="d216474e262">

**Use script values**

</td><td>

Write the script in the **Script values** field. Specify the **Risk** and **Impact** values in the script.The conditions are set using either the condition builder or an advanced condition script.

</td></tr></tbody>
</table>    In the following example, the **Advanced condition** script first determines whether the CI is a business service. If so, the script identifies whether the **Business criticality** value is **1 - most critical** or **2 - somewhat critical**. If it does, it sets the global variable answer to *true*.

    ![Critical business service risk condition](../image/risk-condition-rule.png)

    When the **Advanced condition** script returns *true*, the script in the **Script values** field sets the change request **Impact** and **Risk** values based on the **Business criticality** value.


**Parent Topic:**[Risk conditions and calculation](../concept/change-risk-assess-detect-conflict.md)

**Related topics**  


[Risk Calculator property](../../../script/server-scripting/reference/r_ChangeRiskCalculator.md)

