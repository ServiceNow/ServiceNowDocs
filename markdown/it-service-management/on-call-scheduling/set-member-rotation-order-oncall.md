---
title: Modify the order of a member in a roster
description: You can modify the order number for a member without affecting the past shift schedule.
locale: en-US
release: zurich
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing roster members, Configure or update an On-Call shift, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Modify the order of a member in a roster

You can modify the order number for a member without affecting the past shift schedule.

## Before you begin

Role required: rota\_admin, rota\_manager, or admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **My Group Schedules**.

2.  Open the required shift form.

3.  In the Rosters related list, click the information icon \( ![Information icon.](../image/icon-information.png) \) for the roster in which you want to modify the order of a member.

4.  Click **Open Record**.

5.  On the Roster form, click **Move** in the Members related list.

6.  On the form, fill in the fields.

<table id="table_pv1_k3l_xv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From date

</td><td>

Date from when the order change applies to the member.**Note:** The member's order will be active on the roster in the next rotation.

</td></tr><tr><td>

Member

</td><td>

Name of the member to update the order.

</td></tr><tr><td>

Current roster

</td><td>

Roster from which you navigated to the form.

</td></tr><tr><td>

Shift

</td><td>

Name of the shift.

</td></tr><tr><td>

Move type

</td><td>

Type of move.-   **Move after**: Moves the order of the member after the target member.
-   **Swap**: Swaps the order of the member with the target member.


</td></tr><tr><td>

Target member

</td><td>

Name of the member with whom the order is swapped or after whom the member will be in the execution order.

</td></tr><tr><td>

Rosters

</td><td>

Rosters affected after modifying the order of a member. This field is auto-populated by comparing the members in the rosters. If a member exists in more than one roster, both the rosters are auto-populated to avoid conflicts in schedule.

</td></tr></tbody>
</table>7.  Click **Submit**.

    The member appears in the new order. The original record has a **To** date for the end of validity and the new record has the current date as the **From** date for the start of validity.


**Parent Topic:**[Managing roster members](../concept/managing-roster-members.md)

