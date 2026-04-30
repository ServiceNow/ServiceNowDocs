---
title: Define style rules from Change Schedule Definitions
description: You can define style rules from change schedule definitions when you want the style rules to be applied to the change schedule related to the change schedule definition.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Style rules definition, Change schedules, Configure, Change Management, IT Service Management]
---

# Define style rules from Change Schedule Definitions

You can define style rules from change schedule definitions when you want the style rules to be applied to the change schedule related to the change schedule definition.

## Before you begin

Role required: itil, sn\_chg\_soc.change\_soc\_admin, sn\_change\_role, sn\_change\_write roles, sn\_change\_write, or admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Schedules** &gt; **Change Schedule Definitions**.

2.  Open the definition for which you want to define or edit a style rule.

3.  Click the Style Rules related list and click **New**.

4.  On the form, fill in the fields.

<table id="table_p1x_5tf_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the style rule.

</td></tr><tr><td>

Conditions

</td><td>

Conditions which dictate the style rule. For example, risk = High = red.

</td></tr><tr><td>

Active

</td><td>

Check box to determine whether the style rule is active.

</td></tr><tr><td class="sub-head" colspan="2">

Styling

</td></tr><tr><td>

Advanced

</td><td>

Check box to write a script to set the value of label color, label weight and event color.If you do not select the check box, the **Label color**, **Label weight**, and the **Event color** fields appear.

</td></tr><tr><td>

Label color

</td><td>

Color of the text that is displayed for each record on the timeline that matches the style rule.

</td></tr><tr><td>

Label weight

</td><td>

Thickness of the label such as normal or bold.

</td></tr><tr><td>

Event color

</td><td>

Color of the schedule span displayed for each record on the timeline that matches the style rule.

</td></tr></tbody>
</table>5.  Click **Save**.

    **Note:** Style rules that you create from a change schedule definition take precedence over the style rules that exist in the base style rule table \[chg\_soc\_style\_rule\].


**Parent Topic:**[Style rules definition](../concept/style-rules-definition.md)

**Related topics**  


[Define default style rules](def-stl-rules-from-stl-rules-table.md)

[Define style rules from Change Schedules View](define-style-rules-from-view.md)

