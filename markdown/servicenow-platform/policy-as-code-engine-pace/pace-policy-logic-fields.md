---
title: Policy logic condition fields
description: Policy logic is a set of conditions that is used for determining whether a policy is compliant or non-compliant. You can use the condition builder to specify conditions for the policy.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create PaCE policy version in low-code, Create PaCE policy versions, Manage PaCE policy versions, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Policy logic condition fields

Policy logic is a set of conditions that is used for determining whether a policy is compliant or non-compliant. You can use the condition builder to specify conditions for the policy.

## Policy logic page

![Policy builder.](../image/pace-low-code-policy-builder-3.jpg)

Select the **or** and **and** button to add multiple rules in the condition set. Select the minus icon ![Minus icon.](../../devops-config/image/pace-output-type-delete.png) to delete a condition.

You can add a condition set by selecting the **New condition set** button.

<table id="table_rfb_gpj_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition description

</td><td>

Description of the field.

</td></tr><tr><td>

Source

</td><td>

Variable of the source for the condition.

</td></tr><tr><td>

Operator

</td><td>

List of operators to filter the source for the condition. The list changes depending on the source selected.

</td></tr><tr><td>

Value

</td><td>

Value to enter text. Select the Data picker icon ![Data pill picker icon.](../image/pace-pill-picker-icon-2.jpg) to concatenate multiple text strings with multiple data pills to select a variable for the log.**Note:** If your Source is choice, the Data pill picker icon is inactive.

</td></tr></tbody>
</table>The **else if** statement enables you to specify a new condition if the first condition is false. The **else** statement enables you to specify a new condition if it does not apply to the **if** statement.

You can add a dependent condition by selecting **or** or **and** next to the condition.

<table id="table_g25_5pj_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logic type

</td><td>

Select the logic type of the policy:-   Decision: Determines if the policy is **Compliant** or **Non-compliant**.
-   Run policy: For nested policies, the parent policy will return the decision of the child policy that has been selected in the builder.

**Note:** PaCE supports nesting policies for decision-making and up to two levels are supported, a child and a grandchild.


</td></tr><tr><td>

Log level

</td><td>

Level of the log.

</td></tr><tr><td>

Log message

</td><td>

Log message field to enter text or select the Data picker icon ![Data pill picker icon.](../image/pace-pill-picker-icon-2.jpg) to concatenate multiple text strings with multiple data pills to select a variable for the log.

</td></tr><tr><td>

Output type

</td><td>

Output type of the log. You can select the plus icon ![Add icon.](../../devops-config/image/pace-output-type-add.png) to add multiple output types or the minus icon ![Minus icon.](../../devops-config/image/pace-output-type-delete.png) to delete the output type.

</td></tr><tr><td>

Data

</td><td>

Data field to enter text. Select the Data picker icon ![Data pill picker icon.](../image/pace-pill-picker-icon-2.jpg) to concatenate multiple text strings with multiple data pills to select a variable for the log.

</td></tr></tbody>
</table>The following images show you are able to use the data pill picker to concatenate data in the fields:

![Selecting data from pill picker.](../image/pace-low-code-data-picker.jpg)

![Data concatenated.](../image/pace-low-code-concatenate-data.jpg)

You can see a list of the data sources under the Data source tab.![Data source tab.](../image/pace-data-source-tab-3.jpg)

You can calculate fields using numeric operators and use these variables to calculate the desired value in a policy logic.

**Note:** This only supports numeric fields.

|Operator|Description|
|--------|-----------|
|Plus \(+\)|Add variables and constants. For example, "Var1 + Var2..."|
|Minus \(-\)|Subtract variables and constants. For example, "Var1 - Var2..."|
|Multiplication \(\*\)|Multiple variables and constants. For example, "Var1 \* Var2..."|
|Division \(/\)|Divide variables and constants. For example, "Var1 / Var2..."|
|Parentheses \(\)|Use parentheses to support the order of operators.|
|calc\[\]|Use the brackets to evaluate an expression.|

You can mix and match between the operators. For example, "Var1 +Var2\*Var3 / Var4".

