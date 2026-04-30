---
title: Assigning On-Call Scheduling roles
description: Admins can assign On-Call Scheduling roles to user groups and to individual users based on user activities and responsibilities.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Define escalation process, On-Call Scheduling, IT Service Management]
---

# Assigning On-Call Scheduling roles

Admins can assign On-Call Scheduling roles to user groups and to individual users based on user activities and responsibilities.

## On-Call Scheduling roles tasks and access permissions

<table id="table_wfq_5hf_xlb"><thead><tr><th>

Role

</th><th>

Tasks and access permissions

</th></tr></thead><tbody><tr><td>

Shift administrator \[rota\_admin\]

</td><td>

A user with the rota\_admin role can create, read, update, and delete shifts. The rota\_admin can create shifts using the [Create new schedule wizard](../task/create-update-schedule-oncall.md), modify shifts and rosters, and maintain coverage and time off on the [Manage shifts from the Calendar view](../task/customize-calendar-view-oncall.md).

 The rota\_admin role contains the platform assignment\_rule\_admin role.

</td></tr><tr><td>

Shift manager \[rota\_manager\]

</td><td>

The Shift manager role is for the manager of a group. The purpose of the role is to distinguish a member that has been delegated the role of managing shifts of a group. The role cannot be used to manage all groups on the instance.

 The role can be delegated to the members of a group. See [Delegating roles](https://www.servicenow.com/docs/access?context=c_DelegateRoles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) .

 A user with the Shift manager role that meets any of the following requirements can manage shifts for their group:

 -   The user is the manager of the group.
-   The user was delegated the rota\_manager role. For information on delegating the shift manager role, see [Delegate the shift manager \[rota\_admin\] role](../task/delegate-shift-mgr-role-oncall.md). For information on role delegation, see [Delegate roles](https://www.servicenow.com/docs/access?context=c_DelegateRoles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) .

**Note:** When a user is delegated a role on behalf of a group, the user can manage the shifts only for that group.

-   The user is configured as a shift manager for a group. For information on configuring group preferences, see [Configure preferences for a user group](../task/config-group-prefs-oncall.md).

</td></tr><tr><td>

itil

</td><td>

A user with the itil role can view the [Manage shifts from the Calendar view](../task/customize-calendar-view-oncall.md), on-call commitments on reports, and has general read-only access to their group's shifts.

</td></tr><tr><td>

Premium Dashboard user \[rota\_prem\_dashboard\_user\]

</td><td>

Access to the On-Call Premium dashboard. The Premium dashboard displays performance metrics across groups. See [Legacy: Viewing the Performance reports for escalations](viewing-performance-report-oncall.md).

</td></tr><tr><td>

DEPRECATED: roster\_admin

</td><td>

**Warning:** Do not use this role for new users. This deprecated legacy role exists only to support customers that still use the role.

</td></tr></tbody>
</table>**Parent Topic:**[Defining On-Call Scheduling escalation process](../../user-administration/concept/defining-escalation-process-and-template.md)

**Related topics**  


[System roles](https://www.servicenow.com/docs/access?context=base-system-roles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Base system Roles](https://www.servicenow.com/docs/access?context=r_BaseSystemRoles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

