---
title: Define default style rules
description: Define style rules from the Default Style Rules module to apply them to all change schedules rather than to a specific application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/def-stl-rules-from-stl-rules-table.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Style rules definition, Change schedules, Configure, Change Management, IT Service Management]
---

# Define default style rules

Define style rules from the Default Style Rules module to apply them to all change schedules rather than to a specific application.

## Before you begin

Role required: itil, sn\_chg\_soc.change\_soc\_admin, sn\_change\_role, sn\_change\_write, or admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Schedule** &gt; **Default Style Rules**.

2.  On the Style Rule page, select **New**.

3.  On the form, fill in the fields.

<table id="table_p1x_5tf_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the style rule.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that determine when the style rule applies. For example, show a red span when **Risk** is **High**.

</td></tr><tr><td>

Active

</td><td>

Check box that, when selected, makes the style rule active.

</td></tr><tr><td class="sub-head" colspan="2">

Styling

</td></tr><tr><td>

Advanced

</td><td>

Check box that, when selected, lets you write a script to set the label color, label weight, and event color.If you do not select the check box, the **Label color**, **Label weight**, and the **Event color** fields appear.

</td></tr><tr><td>

Label color

</td><td>

Color of the text that is displayed for each record on the timeline that matches the style rule.

</td></tr><tr><td>

Label weight

</td><td>

Thickness of the label, such as normal or bold.

</td></tr><tr><td>

Event color

</td><td>

Color of the schedule span displayed for each record on the timeline that matches the style rule.

</td></tr></tbody>
</table>4.  Select **Save**.


**Parent Topic:**[Style rules definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/style-rules-definition.md)

**Related topics**  


[Define style rules from Change Schedule Definitions]()

[Define style rules from the change schedules view]()

