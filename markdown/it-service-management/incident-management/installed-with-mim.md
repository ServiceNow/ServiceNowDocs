---
title: Components installed with Incident Management - Major Incident Management
description: Several types of components are installed with activation of the Incident Management - Major Incident Management plugin, including tables and user roles.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Incident Management - Major Incident Management, Major Incident Management plugins, Managing major incidents, Incident Management, IT Service Management]
---

# Components installed with Incident Management - Major Incident Management

Several types of components are installed with activation of the Incident Management - Major Incident Management plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Major incident manager\[mim\_manager\]

</td><td>

A major incident manager can:-   Initiate the major incident process by assessing and approving major incident candidates or creating a major incident.
-   Reject a major incident candidate.
-   Demote a major incident after it is accepted so that the incident can be handled as a regular incident.
-   Maintain the ownership and accountability for the life cycle of the incident.
-   Identifies the users and groups to be involved in the resolution activities.
-   Creates adhoc communication plans and tasks.
-   Edits a communication plan that is attached to a major incident.
-   Close a major incident.

</td><td>

This role inherits the ia\_admin role.

</td></tr><tr><td>

Major incident admin\[sn\_mim\_admin\]

</td><td>

Configure all Major Incident Management features including major incident properties and trigger rules.

</td><td>

-   mim\_manager
-   sn\_iam\_admin
-   sn\_sow\_mim.sn\_mim\_sow\_admin

</td></tr><tr><td>

Communications manager\[communication\_manager\]

</td><td>

-   Manages communications for major incidents and is responsible for communicating with all stakeholders.
-   Creates adhoc communication plans and tasks.
-   Edits a communication plan that is attached to a major incident.

</td><td>

This role inherits the ia\_admin role.

</td></tr><tr><td>

Incident Manager \[incident\_manager\]

\(Existing role with added responsibilities\)

</td><td>

-   Manages incident properties and major incident trigger rules.
-   Can create and edit Communication Plan Definitions.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Major Incident Trigger Rules\[major\_incident\_trigger\_rule\]

</td><td>

This table extends the Application File \[sys\_metadata\] table and stores the major incident trigger rules.

</td></tr></tbody>
</table>**Parent Topic:**[Activate Incident Management - Major Incident Management](activate-major-incident-management-plugin.md)

