---
title: Roles installed with Event Management
description: Roles used by the Event Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/r\_RolesInstalledWithEventMgmt.html
release: brazil
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Roles installed with Event Management

Roles used by the Event Management application.

Event Management adds these roles.

<table id="table_dmp_vhb_mt"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Event Management Administrator\[evt\_mgmt\_admin\]

</td><td>

Has read and write access to all Event Management features to configure Event Management.**Note:** Exercise caution with the evt\_mgmt\_admin role, as it can be elevated to the admin role. A user with the evt\_mgmt\_admin role has the ability to add and modify scripts that run on a global scope. Ensure proper access control. With this role, the user can create and/or update the following scripts:

-   Alert correlation rules
-   Alert management rules
-   Maintenance rules
-   Advanced scripts
-   Event field mapping
-   Pre- and post-binding scripts

</td><td>

-   evt\_mgmt\_user
-   template\_editor\_global

</td></tr><tr><td>

Event Management Operator\[evt\_mgmt\_operator\]

</td><td>

In addition to the evt\_mgmt\_user permissions, can also activate operations on alerts such as acknowledge, close, open incident, and run remediations.

</td><td>

evt\_mgmt\_user

</td></tr><tr><td>

Event Management User\[evt\_mgmt\_user\]

</td><td>

Has read access to all Event Management features. Has the itil role to be able to manage incidents that are created from alerts.

</td><td>

itil

</td></tr><tr><td>

Event Management Integrator\[evt\_mgmt\_integration\]

</td><td>

Has create access to the Event \[em\_event\] and Registered Nodes \[em\_registered\_nodes\] tables to integrate with external event sources.

</td><td>

 

</td></tr><tr><td>

Event Management AIOps Manager\[evt\_aiops\_manager\]

</td><td>

Responsible for overseeing NOC teams performance and can onboard AI Specialists as part of the agentic workforce features in AIOps.

</td><td>

evt\_team\_operator

</td></tr><tr><td>

Event Management Team Operator\[evt\_team\_operator\]

</td><td>

Can create and manage their own integrations, set up their own alert automations, and enhance control over alert management for their teams.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/event-management-reference.md)

