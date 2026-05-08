---
title: Insight rule form
description: Use the Insight rule form to create an insight rule from Automation Center.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Automation Center, Workflow Data Fabric]
---

# Insight rule form

Use the Insight rule form to create an insight rule from Automation Center.

<table id="id_psp_l3j_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the insight rule.

</td></tr><tr><td>

Active

</td><td>

Option to verify the usability of the insight rule.On clearing this option, the notifications won’t be generated from this insight rule.

</td></tr><tr><td>

Application

</td><td>

Field that indicates which applications can use this insight rule.

</td></tr><tr><td>

Severity

</td><td>

Priority of the insight rule:-   **Urgent**
-   **High**
-   **Moderate**
-   **Low**

 The default value is set to **Moderate**.

</td></tr><tr><td>

Type

</td><td>

Level of insight rule:-   **Info**
-   **Warning**
-   **Error**

</td></tr><tr><td>

Message

</td><td>

Custom message that describes the insight.For example, `Time to Cleanup Automation Tasks. The count is {0}.`

 To configure the variable, such as \{0\}, see [Write a script for an automation message variable](../task/create-message-variable-auto-center.md).

 **Note:** To enable localization of this message string, create the sys\_ui\_message update record. For more information, see Custom translations.

</td></tr><tr><td>

Applies to

</td><td>

Table that the insight rule is applied on.For example, Automation Request \[sn\_ac\_automation\_request\].

</td></tr><tr><td>

When

</td><td>

Conditions at which the insights are triggered.Select a table from the Applies to list before modifying this field.

 This field appears only when an entry is selected from the Threshold type list.

 Select the **Set Condition** field to add a trigger condition. For example, you might want to generate an insight rule when the state of an automation request isn't published. In that case, select **State** from the field list, **is not** from the operator list, and **Published** from the value list.

 You can use **or** or **and** next to the condition.

 To add more conditions, select **New condition set**.

</td></tr><tr><td>

Threshold type

</td><td>

Type of threshold:-   **Count**
-   **Percentage**

</td></tr><tr><td class="sub-head" colspan="2">

Threshold Count**Note:** This tab appears only when **Count** is selected from the Threshold type list.

</td></tr><tr><td>

Operator

</td><td>

Qualifier to trigger insights:-   **is**
-   **less than**
-   **greater than**
-   **less than or is**
-   **greater than or is**

 This field appears only when **Count** is selected from the Threshold type list.

</td></tr><tr><td>

Value

</td><td>

Value to determine if an insight rule must be triggered based on the qualifier that is selected in the **Operator** field.For example, an insight rule is triggered if a few automation requests get rejected in a day. To set a condition, select **Count** in the Threshold type list, **greater than** in the Operator list, and **10** in the Value list.

 This field appears only when **Count** is selected from the Threshold type list.

</td></tr><tr><td class="sub-head" colspan="2">

Threshold Percentage**Note:** This tab appears only when **Percentage** is selected from the Threshold type list.

</td></tr><tr><td>

Percentage of

</td><td>

Denominator value for the resulted rule value.

</td></tr><tr><td>

Operator

</td><td>

Qualifier to trigger insights:-   **is**
-   **less than**
-   **greater than**
-   **less than or is**
-   **greater than or is**

 This field appears only when **Percentage** is selected from the Threshold type list.

</td></tr><tr><td>

Value

</td><td>

Value to determine if an insight rule must be triggered based on the qualifier that is selected in the **Operator** field.For example, an insight rule is triggered if a few automation requests get rejected in a day. To set a condition, select **Percentage** in the Threshold type list, **greater than** in the Operator list, and **10%** in the Value list.

 This field appears only when **Percentage** is selected from the Threshold type list.

</td></tr></tbody>
</table>**Parent Topic:**[Automation Center reference](../concept/automation-center-reference.md)

