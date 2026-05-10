---
title: Create a mobile UI rule
description: Create a mobile UI rule to apply styling or field calculations for your mobile UI elements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile UI Rules, Mobile styles, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a mobile UI rule

Create a mobile UI rule to apply styling or field calculations for your mobile UI elements.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile UI** &gt; **Mobile UI Rules**.

2.  In the **Mobile UI Rules** list, select **New**.

3.  In the **Mobile UI Rule** form, fill in the fields.

<table id="table_r5w_qhw_knb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mobile UI rule.

</td></tr><tr><td>

Active

</td><td>

Whether the mobile UI rule is active.

</td></tr><tr><td>

Condition

</td><td>

Condition under which the mobile UI rule is used. The rule executes if the condition evaluates as true. Mobile UI rules with no condition always evaluate as true.

To use a field in a condition, the field must be displayed on the mobile card, or it must be added to the **Card fields** tab on the card \[sys\_sg\_view\_config\] record for that card. If the field is a reference field, you can also access information in the related record using dot-walking. See [Dot-walking to data in related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_DotWalking.md).

Conditions can also use variables defined in the mobile scratchpad. These variables are created and evaluated using the script in the **Mobile Scratchpad Script** field in the card \[sys\_sg\_view\_config\] record.

![Javascript in the Mobile Scratchpad script field](../image/mobile-scratch-example-2.png)![Mobile UI Rule condition using a scripted condition](../image/mobile-scratch-example-1.png)**Note:** For details on the operators available for your condition, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).

</td></tr><tr><td>

Parent Table

</td><td>

The parent table that the mobile UI rule applies to. Select either:-   **Input Form Screen**
-   **Mobile View**


</td></tr><tr><td>

Parent

</td><td>

The input form screen or mobile view record to which your mobile UI rule is applied.

</td></tr><tr><td>

Triggers

</td><td>

The condition that triggers the mobile UI rule. Select one or both of the following options.-   **onLoad**: The mobile UI rule triggers when the record loads.
-   **onChange**: The mobile UI rule triggers when the record is changed.
-   **onUserAction**: The mobile UI rule triggers when the user performs the specified action.

**Note:** To use the **onUserAction** trigger, a User Action Id must be associated with the UI rule.

</td></tr><tr><td>

User Action Id

</td><td>

A unique value that identifies this action record. It is needed to associate the action with a UI rule.

</td></tr><tr><td>

Order

</td><td>

Order in which the mobile UI rule executes. If there are multiple rules affecting the same element, the rules execute according to this value. Lower numbered rules execute before higher numbered rules.

</td></tr><tr><td>

Reverse If False

</td><td>

When this field is selected, the mobile UI rule actions are reverse if the condition evaluates as false.

 **Important:** When this field is selected for high order mobile UI rules, it inactivates prior rules that address the same target and operation.

</td></tr></tbody>
</table>4.  Select **Submit**


## What to do next

After creating your mobile UI rule, you must create mobile UI rule actions to execute when your rule is used.

