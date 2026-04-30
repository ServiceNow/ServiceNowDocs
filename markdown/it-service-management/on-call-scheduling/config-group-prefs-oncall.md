---
title: Configure preferences for a user group
description: Specify the On-Call preferences for a user group.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Configure preferences for a user group

Specify the On-Call preferences for a user group.

## Before you begin

Role required: admin, rota\_admin, or rota\_manager.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Group Preferences** and then set the values as needed.

<table id="table_tys_kyb_wfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group

</td><td>

User group for which the On-Call preferences should apply.

</td></tr><tr><td>

Shift managers

</td><td>

Users who can manage the shift in addition to group managers, shift administrator \[rota\_admin\], and delegated shift managers. You can also select the current group members.

</td></tr><tr><td>

Allow Shift Schedule Overlap

</td><td>

Specifies if overlapping schedules are allowed for shifts within the group. When set to `Default`, the value selected for the **Configuration to control whether to allow overlapping Shift schedules** \(**com.snc.on\_call\_rotation.allow\_rota\_overlap**\) property is applied.**Note:** Shift overlap is required to have a hand-off period between shifts. With this, multiple shifts can be on-call for the same duration. On-call members from multiple shifts can be contacted.

</td></tr><tr><td>

Escalation rule on Shift overlap

</td><td>

Escalation rule that applies when there is a shift overlap. When set to `Default`, the value selected for the **Escalation rule which applies when Shifts overlap** \(**com.snc.on\_call\_rotation.escalation\_rule\_rota\_over**\) property is applied.

</td></tr><tr><td>

PTO approval preferences

</td><td>

Specifies if an On-Call member in the group can create time-off request \(PTO\). When set to **Default**, the value selected for the sys property **com.snc.on\_call\_rotation.pto.configuration** \(**This property governs if an On-Call user \(Not "admin, rota\_manager, group manager or rota\_admin"\) is allowed to create PTO**\) is applied.

</td></tr><tr><td>

First Day of the Week

</td><td>

Select a preferred start day of the week for the selected group

</td></tr></tbody>
</table>2.  To view On-Call property settings, click **View Global Settings**.

3.  Click **Submit** to configure the settings or **Delete** to delete the preference.


**Parent Topic:**[Managing schedules and shifts](../../user-administration/concept/manage-schedules-and-shifts.md)

