---
title: Major incident assignment
description: A major incident is assigned to a group automatically at the time of proposal and promotion based on the value of the property Major Incident Management Group \(sys\_id\) to whom the Major Incident should be re-assigned on promotion to 'Major Incident' \(sn\_major\_inc\_mgmt.major\_incident\_management\_group\). The assigned group works on the major incident and resolves it.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working on major incident management, Manage major incidents, Incident Management, IT Service Management]
---

# Major incident assignment

A major incident is assigned to a group automatically at the time of proposal and promotion based on the value of the property **Major Incident Management Group \(sys\_id\) to whom the Major Incident should be re-assigned on promotion to 'Major Incident'** \(**sn\_major\_inc\_mgmt.major\_incident\_management\_group**\). The assigned group works on the major incident and resolves it.

The incident is assigned to an individual if the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\) is activated and a shift is defined for the group. The following table illustrates the different conditions under which a major incident is assigned to a group and a user.

<table id="table_nhx_43h_hdb"><thead><tr><th>

Action

</th><th>

Condition

</th><th>

Assignment group

</th><th>

Assigned to

</th></tr></thead><tbody><tr><td rowspan="2">

Incident is proposed as a candidate manually or based on major incident trigger rules

</td><td>

Assignment Group is empty

</td><td>

Group based on the property value

</td><td>

-   If on-call is activated, shift is defined and a user is available on-call then the incident is assigned to the on-call user
-   If on-call is not activated, the **Assigned to** field remains empty

</td></tr><tr><td>

Assignment Group is not empty

</td><td>

No change - incident retains the current value of the assignment group

</td><td>

No change - incident remains with the current value in the **Assigned to** field

</td></tr><tr><td rowspan="2">

Incident is manually promoted to a major incident

</td><td>

Assignment Group is empty

</td><td>

Group based on the property value

</td><td>

The value for the **Assigned to** field is the user who promoted the incident to a major incident

</td></tr><tr><td>

Assignment Group is not empty

</td><td>

-   Incident reassigned to group based on the property value
-   Send a notification to the original Assignment Group members about the latest incident reassignment.

</td><td>

-   **Assigned to** value is overwritten by the user who promoted the major incident candidate
-   Send a notification to the user to whom the major incident was previously assigned

</td></tr><tr><td rowspan="2">

Major incident is created

</td><td>

Assignment Group is empty

</td><td>

Group based on the property value

</td><td>

The value of the **Assigned to** field is the user who has created the major incident

</td></tr><tr><td>

Assignment Group is not empty

</td><td>

No change - incident retains the current value of the assignment group

</td><td>

No change - incident remains with the current value in the **Assigned to** field

</td></tr></tbody>
</table>|Action|Condition|Assignment group|Assigned to|
|------|---------|----------------|-----------|
|Incident communication plan is created with source as major incident|Assignment Group is empty|The value for the **Assignment group** field is copied from the source incident|The value of the **Assigned to** field is copied from the source incident|
|Assignment Group is not empty|No change - incident communication plan retains the current value of the assignment group|No change - incident communication plan retains the current value of the **Assigned to** field|
|Incident communication task is created from incident communication plan whose source is major incident|Assignment Group is empty|The value for the **Assignment group** field is copied from the incident communication plan|The value of the **Assigned to** field is copied from the incident communication plan|
|Assignment Group is not empty|No change - incident communication plan retains the current value of the assignment group|No change - incident communication task retains the current value of the **Assigned to** field|

**Parent Topic:**[Working on major incident management](work-on-mim.md)

