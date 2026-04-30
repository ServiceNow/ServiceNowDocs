---
title: Roles used by Express List
description: Detailed information on all roles that can access the Express List feature on the Service Operations Workspace.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Express List]
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Roles used by Express List

Detailed information on all roles that can access the Express List feature on the Service Operations Workspace.

<table id="table_jtn_5wp_12c"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Event Management Administrator\[evt\_mgmt\_admin\]

</td><td>

Has read and write access to all Event Management features to configure Event Management.**Note:** Be careful with the evt\_mgmt\_admin role because it can be elevated to the admin role.

</td><td>

-   evt\_mgmt\_user
-   template\_editor\_global

</td></tr><tr><td>

Event Management Operator\[evt\_mgmt\_operator\]

</td><td>

In combination with the evt\_mgmt\_user permissions, can also activate operations on alerts such as acknowledge, close, open incident, and run remediations.

</td><td>

evt\_mgmt\_user

</td></tr><tr><td>

Event Team Operator\[evt\_team\_operator\]

</td><td>

Manages Event Management operations within a specific team as defined in the **Assignment Group** field. This role allows the operator to read and write alerts exclusively for their assigned team. Additionally, the operator can make configuration changes specific to their team, including updates to Alert Automation and Integrations Launchpad.**Note:** The evt\_team\_operator role must be assigned to an assignment group to view and manage alerts for that group. If the role is created but not associated with any groups that have alerts assigned, the operator cannot see any alerts.

</td><td>

 

</td></tr><tr><td>

Event Management User\[evt\_mgmt\_user\]

</td><td>

Has read-only access to all Event Management features. The contained itil role grants access to manage incidents that are created from alerts. Can only view Express List.

</td><td>

itil

</td></tr><tr><td>

Event Management Integrator\[evt\_mgmt\_integration\]

</td><td>

Has create access to the Event \[em\_event\] and Registered Nodes \[em\_registered\_nodes\] tables to integrate with external event sources.

</td><td>

 

</td></tr></tbody>
</table>