---
title: Report an incident
description: Create an Operational Technology \(OT\) incident record to report a deviation from an expected standard of operation.
locale: en-US
release: xanadu
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Incident Management, Operational Technology]
---

# Report an incident

Create an Operational Technology \(OT\) incident record to report a deviation from an expected standard of operation.

## Before you begin

Role required: sn\_ot\_incident\_write

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select an device record or an equipment model entity record.

    **Note:** You can also raise an OT incident on the OT Incidents list module.

3.  Select the **OT Incidents** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

    If you selected an device record, the Site and OT device fields are automatically filled in. If you selected an equipment model entity record, the Site and Equipment model entity fields are automatically filled in. If the OT incident is raised from the OT Incidents list module, then none of these fields are automatically filled in.

    **Note:** Your organization has configured the incident form and its fields to adhere to its incident management process. The following table describes the typical OT incident form fields.

<table id="table_jbh_xzy_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the incident.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation of the incident.

</td></tr><tr><td>

Number

</td><td>

Unique system-generated incident number that is prefixed with Operational Technology Incident \(OTINC\).

</td></tr><tr><td>

Caller

</td><td>

User who contacted the OT engineer with an issue.

</td></tr><tr><td>

Impact

</td><td>

Measure of the effect that an incident has on industrial processes.

</td></tr><tr><td>

Urgency

</td><td>

Measure of how long the resolution can be delayed until an incident has a significant business impact.

</td></tr><tr><td>

State

</td><td>

State of the OT incident. The state moves and tracks incidents through several stages of resolution.

</td></tr><tr><td>

Category

</td><td>

Type of issue. After selecting the category, select the subcategory if applicable.

</td></tr><tr><td>

Subcategory

</td><td>

Type of issue within the selected category.

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this incident when comments are added.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications about this incident when work notes are added.

</td></tr><tr><td>

Site

</td><td>

Site where the issue happened.

</td></tr><tr><td>

OT device

</td><td>

Affected OT device at the site.

</td></tr><tr><td>

Equipment model entity

</td><td>

Affected equipment model equipment model entity at the site.

</td></tr><tr><td>

Business impact

</td><td>

More information about the business impact of the OT incident.

</td></tr><tr><td>

Assignment group

</td><td>

Assigned group that works on the incident. The assignment group can be any group with the type OT.

</td></tr><tr><td>

Assigned to

</td><td>

User who works on this incident. If the assignment group changes, the **Assigned to** field is cleared.You can only select the users that are included in the **Assignment group** field and have the **sn\_ot\_incident\_write** role. If the Assignment group field is empty, then any site user with the sn\_ot\_incident\_write role can be selected.

</td></tr><tr><td>

Parent incident

</td><td>

Unique number of the parent incident for this incident record.

</td></tr><tr><td>

Additional comments

</td><td>

More information about the issue as needed. All users that can view incidents can see the additional comments.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the incident or the steps taken to resolve it, if applicable.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

Now, the assignment group and assignee are aware that there's an OT incident that needs to be addressed.

**Parent Topic:**[Using Operational Technology Incident Management](../concept/using-operational-technology-incident-mgt.md)

