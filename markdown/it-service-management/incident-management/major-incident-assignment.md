---
title: Major incident assignment
description: When an incident is proposed as a major incident candidate or promoted to a major incident, it's automatically assigned to the major incident management group that a system property defines. The assigned group works on the major incident and resolves it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/major-incident-assignment.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# Major incident assignment

When an incident is proposed as a major incident candidate or promoted to a major incident, it's automatically assigned to the major incident management group that a system property defines. The assigned group works on the major incident and resolves it.

The **Major Incident Management Group \(sys\_id\) to whom the Major Incident should be re-assigned on promotion to 'Major Incident'** \(**sn\_major\_inc\_mgmt.major\_incident\_management\_group**\) system property defines the assignment group. If the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\) is active and a shift is defined for the group, the incident is also assigned to an individual. The following table describes the conditions under which a major incident is assigned to a group and a user.

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

**Assignment group** is empty

</td><td>

Group based on the property value

</td><td>

-   If on-call scheduling is active, a shift is defined, and a user is on call, the incident is assigned to the on-call user
-   If on-call scheduling isn't active, the **Assigned to** field remains empty

</td></tr><tr><td>

**Assignment group** is not empty

</td><td>

No change—the incident retains the current value of the assignment group

</td><td>

No change—the incident remains with the current value in the **Assigned to** field

</td></tr><tr><td rowspan="2">

Incident is manually promoted to a major incident

</td><td>

**Assignment group** is empty

</td><td>

Group based on the property value

</td><td>

The value for the **Assigned to** field is the user who promoted the incident to a major incident

</td></tr><tr><td>

**Assignment group** is not empty

</td><td>

-   Incident reassigned to group based on the property value
-   Notification sent to the original assignment group members about the reassignment

</td><td>

-   **Assigned to** value is overwritten by the user who promoted the major incident candidate
-   Notification sent to the user to whom the major incident was previously assigned

</td></tr><tr><td rowspan="2">

Major incident is created

</td><td>

**Assignment group** is empty

</td><td>

Group based on the property value

</td><td>

The value of the **Assigned to** field is the user who has created the major incident

</td></tr><tr><td>

**Assignment group** is not empty

</td><td>

No change—the incident retains the current value of the assignment group

</td><td>

No change—the incident remains with the current value in the **Assigned to** field

</td></tr></tbody>
</table>|Action|Condition|Assignment group|Assigned to|
|------|---------|----------------|-----------|
|Incident communication plan is created with source as major incident|**Assignment group** is empty|The value for the **Assignment group** field is copied from the source incident|The value of the **Assigned to** field is copied from the source incident|
|**Assignment group** is not empty|No change—the incident communication plan retains the current value of the assignment group|No change—the incident communication plan retains the current value of the **Assigned to** field|
|Incident communication task is created from incident communication plan whose source is major incident|**Assignment group** is empty|The value for the **Assignment group** field is copied from the incident communication plan|The value of the **Assigned to** field is copied from the incident communication plan|
|**Assignment group** is not empty|No change—the incident communication task retains the current value of the assignment group|No change—the incident communication task retains the current value of the **Assigned to** field|

**Parent Topic:**[Working on major incident management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/work-on-mim.md)

