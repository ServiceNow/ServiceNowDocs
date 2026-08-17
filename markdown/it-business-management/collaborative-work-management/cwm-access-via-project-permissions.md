---
title: Project task access in CWM
description: Learn how project users and CWM users can access project tasks and CWM tasks within the Collaborative Work Management workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/cwm-access-via-project-permissions.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 1
keywords: [access control, ACL, project permissions, project task]
breadcrumb: [Reference, Collaborative Work Management, Strategic Portfolio Management]
---

# Project task access in CWM

Learn how project users and CWM users can access project tasks and CWM tasks within the Collaborative Work Management workspace.

## Access to CWM tasks for project users

Access to a CWM task is granted through either of the following paths:

-   Being a member in the Space that contains the Board where the task lives. This requires the sn\_cwm.cwm\_user role and is the typical CWM access path. For more information about roles for team members, see [Team member role access permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/cwm-team-member-role-permissions.md).
-   Read or write access to the project task referenced by the **Project task** field on the CWM task, along with the sn\_cwm.cwm\_user role.

Either path allows access and the project user can perform the corresponding action on the CWM task.

## Access matrix

<table id="table_project_access_matrix"><thead><tr><th>

Access to project task in Project Workspace

</th><th>

Access in CWM

</th><th>

Effective access of project task in CWM

</th></tr></thead><tbody><tr><td>

Read

</td><td>

-   sn\_cwm.cwm\_user
-   No Space access

</td><td>

View in My Work

</td></tr><tr><td>

Write

</td><td>

-   sn\_cwm.cwm\_user
-   No Space access

</td><td>

View and edit in My Work

</td></tr><tr><td>

Read

</td><td>

Viewer access to the CWM Space

</td><td>

View project task in My Work and CWM Board

</td></tr><tr><td>

Write

</td><td>

Editor access to the CWM Space

</td><td>

-   View and edit project task in My Work and CWM Board
-   Create child CWM tasks for the project task

</td></tr><tr><td>

None

</td><td>

-   sn\_cwm.cwm\_user
-   Viewer access to Space

</td><td>

No access

</td></tr><tr><td>

None

</td><td>

None

</td><td>

No access

</td></tr></tbody>
</table>**Parent Topic:**[Collaborative Work Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/reference-cwm.md)

**Related topics**  


[CWM integration with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/connect-project-workspace-cwm.md)

[Team member role access permissions in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/cwm-team-member-role-permissions.md)

