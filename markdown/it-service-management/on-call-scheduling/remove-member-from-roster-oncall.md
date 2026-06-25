---
title: Remove a member from a roster
description: You might remove a member from a roster, for example, if they are no longer a member of the organization or of the group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/on-call-scheduling/remove-member-from-roster-oncall.html
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing roster members, Configure or update an On-Call shift, Managing schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Remove a member from a roster

You might remove a member from a roster, for example, if they are no longer a member of the organization or of the group.

## Before you begin

Role required: rota\_manager, rota\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **My Group Schedules**.

2.  Open the required shift form.

3.  In the Rosters related list, click the information icon \( \[Omitted image "icon-information.png"\] Alt text: Information icon. \) for the roster from which you want to remove a member.

4.  Click **Open Record**.

5.  On the Roster form, click **Remove** in the Members related list.

6.  On the form, fill in the fields.

<table id="table_ihs_xj1_npb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From date

</td><td>

Date from when the member is removed.

</td></tr><tr><td>

Rosters

</td><td>

Rosters affected after modifying the order of a member. This field is auto-populated by comparing the members in the rosters. If a member exists in more than one roster, both the rosters are auto-populated to avoid conflicts in schedule.

</td></tr><tr><td>

Delete member

</td><td>

Option to delete the member record.**Warning:** When you enable this option to delete the member record, the deleted member rotation history is removed, and the rotation history of other members is affected.

</td></tr><tr><td>

Member

</td><td>

Name of the member to remove from the roster.

</td></tr><tr><td>

Current roster

</td><td>

Roster from which you navigated to the form.

</td></tr><tr><td>

Shift

</td><td>

Name of the shift.

</td></tr></tbody>
</table>7.  Click **Submit**.


**Parent Topic:**[Managing roster members](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/managing-roster-members.md)

**Related topics**  


[Assigning On-Call Scheduling roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/roles-assigning-oncall.md)

