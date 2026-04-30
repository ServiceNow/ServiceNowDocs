---
title: Incident email notifications
description: Use Operational Technology \(OT\) incident email notifications to alert users when changes are made to an incident.
locale: en-US
release: xanadu
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Incident email notifications

Use Operational Technology \(OT\) incident email notifications to alert users when changes are made to an incident.

The notifications are listed in the following table.

<table id="table_wfl_4ms_bwb"><thead><tr><th>

Notification name

</th><th>

When to send

</th><th>

Who receives it

</th><th>

What it contains

</th></tr></thead><tbody><tr><td>

Incident commented

</td><td>

When an extra comment is added

</td><td>

Assigned to, Watch list

</td><td>

Subject: &lt;Incident \#&gt; - comment added

 Body: Comment added

 URL to the incident

</td></tr><tr><td>

Incident opened and unassigned

</td><td>

When the **Assigned to** field changes to empty and **Active** is true

</td><td>

The one who opened the incident

</td><td>

Subject: &lt;Incident \#&gt; - is unassigned

 Body: Please identify someone to work on this incident

 URL to the incident

</td></tr><tr><td>

Incident closed

</td><td>

When the incident is closed

</td><td>

Assignment group

</td><td>

Subject: &lt;Incident \#&gt; - is closed

 Body: Resolution Code and Resolution Notes

</td></tr><tr><td>

Incident priority changed

</td><td>

When triggered

</td><td>

Assigned to, Assignment group, Watch list

</td><td>

Subject: &lt;Incident \#&gt; - priority changed

 Body: New priority: &lt;priority&gt;

</td></tr><tr><td>

Incident resolved

</td><td>

When the incident state changes to **Resolved**

</td><td>

Caller, Watch list

</td><td>

Subject: &lt;Incident \#&gt; - is resolved

 Body: Resolution Code and Resolution Notes

</td></tr><tr><td>

Incident assigned to my group

</td><td>

When the **Assignment Group** field changes

</td><td>

Assignment group, Watch list

</td><td>

Subject: &lt;Incident \#&gt; - is assigned to &lt;assignment group&gt;

 Body: Priority, Short description, Description

 URL to the incident

</td></tr><tr><td>

Incident assigned to me

</td><td>

When the **Assigned to** field changes

</td><td>

Assigned to, Watch list

</td><td>

Subject: &lt;Incident \#&gt; - is assigned to you

 Body: Priority, Short description, Description

 URL to the incident

</td></tr><tr><td>

Incident opened for me

</td><td>

When a new incident is created

</td><td>

Caller

</td><td>

Subject: &lt;Incident \#&gt; - is opened on your request

 Body: Priority, Short description, Description

 URL to the incident

</td></tr><tr><td>

Incident state changed

</td><td>

When the state of the incident changes

</td><td>

Assigned to, Watch list

</td><td>

Subject: &lt;Incident \#&gt; - State changed

 Body: Short description, Old State, New State

 URL to the incident

</td></tr></tbody>
</table>**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

