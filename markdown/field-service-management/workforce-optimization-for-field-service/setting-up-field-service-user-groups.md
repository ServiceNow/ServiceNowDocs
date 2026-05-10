---
title: Setting up Field Service user groups
description: Field Service Management groups are sets of users or agents, who perform specific tasks. Configuring your field service groups efficiently enables you to align the right skills and resources to the right tasks.Set up user groups for agents to execute the dispatched tasks for specific locations with the required parts and skills to work on the assigned task.Create a qualifier user group to review and qualify work orders to ensure that the work order tasks are created.Set up dispatcher user groups to dispatch tasks to agent user groups in order to meet the needs of specific areas.You can set up other types of user groups.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Users, Set up workforce, Configure, Field Service Management]
---

# Setting up Field Service user groups

Field Service Management groups are sets of users or agents, who perform specific tasks. Configuring your field service groups efficiently enables you to align the right skills and resources to the right tasks.

There are several types of user groups that serve different capabilities. The most common types include user groups for agents and dispatchers. These user groups are essential for organizing and managing the tasks and responsibilities of field service agents.

Additionally, you can create optional group types based on your specific needs, including user groups for initiators, managers, territory planners, and more. For example, you can create user groups for qualifiers to implement an additional qualification step to review and approve work orders. By setting up these groups, you can assign the appropriate roles and users to each group. The roles assigned to the group are automatically inherited by the users within that group, so you don’t need to individually assign roles to each user.

For more information about Field Service Roles, see [Roles installed with Field Service Management](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md).

For information about assigning a role to a user group, see [Assign a role to a group](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/roles/task/t_AssignRoleToGroup.html).

Location also plays an important role in configuring field service user groups. It ensures that qualifiers, dispatchers, and agents only engage with tasks that align with their assigned locations and groups.

There are a few good practices when creating groups:

-   Create one group for administrators and assign the admin role to this group only.
-   Create as many groups as needed in your organization. For example, create a staff group for each geographic location, function, skills, and product models, such as building maintenance or building security. Assign the necessary users to those groups, and then assign the staff role to those groups.

Example user group setup.

<table id="table_tdd_kdv_3xb"><thead><tr><th>

User

</th><th>

Locations

</th><th>

User Groups

</th><th>

User Group Roles

</th><th>

Group Relationship

</th></tr></thead><tbody><tr><td>

Agent1

</td><td>

San Diego

</td><td>

SD Agents

</td><td>

wm\_agent

</td><td>

Receives work order tasks from SD Dispatchers

</td></tr><tr><td>

Agent2

</td><td>

Los Angeles

</td><td>

LA Agents

</td><td>

wm\_agent

</td><td>

Receives work order tasks from LA Dispatchers

</td></tr><tr><td>

Agent3

</td><td>

San Jose

</td><td>

SJ Agents

</td><td>

wm\_agent

</td><td>

Receives work order tasks from SJ Dispatchers

</td></tr><tr><td>

Agent4

</td><td>

San Francisco

</td><td>

SF Agents

</td><td>

wm\_agent

</td><td>

Receives work order tasks from SF Dispatchers

</td></tr><tr><td>

Dispatcher1

</td><td>

San Diego

</td><td>

SD Dispatchers

</td><td>

wm\_dispatcher

</td><td>

Assigns work order tasks to SD Agents

</td></tr><tr><td>

Dispatcher2

</td><td>

Los Angeles

</td><td>

LA Dispatchers

</td><td>

wm\_dispatcher

</td><td>

Assigns work order tasks to LA Agents

</td></tr><tr><td>

Dispatcher3

</td><td>

San Jose

</td><td>

SJ Dispatchers

</td><td>

wm\_dispatcher

</td><td>

Assigns work order tasks to SJ Agents

</td></tr><tr><td>

Dispatcher4

</td><td>

San Francisco

</td><td>

SF Dispatchers

</td><td>

wm\_dispatcher

</td><td>

Assigns work order tasks to SF Agents

</td></tr><tr><td>

Qualifier1

</td><td>

San Jose

 San Francisco

</td><td>

NorCal Qualifiers

</td><td>

wm\_qualifier

</td><td>

Qualifies work order tasks for SJ and SF Dispatchers to assign to SJ and SF Agents

</td></tr><tr><td>

Qualifier2

</td><td>

San Diego

 Los Angeles

</td><td>

SoCal Qualifiers

</td><td>

wm\_qualifier

</td><td>

Qualifies work order tasks for SD and LA Dispatchers to assign to SD and LA Agents

</td></tr></tbody>
</table>## Setting up user groups for agents

Set up user groups for agents to execute the dispatched tasks for specific locations with the required parts and skills to work on the assigned task.

### Before you begin

Role required: wm\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Group Management** &gt; **Work Groups**.

2.  Click **New**.

3.  On the form, enter the name for the user group.

4.  Right-click and save.

5.  Use the following tabs to add additional information to the agent user group.

<table><tbody><tr><td id="d107494e429">

**Roles**

</td><td>

Assign one or more roles from the list of available roles to the user group.

 For more information on roles and assigning them to user groups, see [Roles installed with Field Service Management](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md) and [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

</td></tr><tr><td id="d107494e458">

**Group Members**

</td><td>

Assign one or more agents from the list of available agents to the user group.

 For more information on assigning group members, see [Add a user to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AddAUserToAGroup.md).

</td></tr><tr><td id="d107494e477">

**Groups**

</td><td>

Create a child user group.

</td></tr><tr><td id="d107494e486">

**Skills**

</td><td>

Assign one or more skills from the list of available skills to the user group.

 For more information on assigning skills, see [Manage Field Service and Customer Service skills](../reference/field-service-manager-agent-skills.md).

</td></tr><tr><td id="d107494e508">

**Locations Covered**

</td><td>

Assign one or more locations from the list of locations to the user group.

 For more information on assigning locations to a group, see [Assign a location to a group](../../work-management/concept/c_TerritoryManagement.md#).

</td></tr><tr><td id="d107494e531">

**Covered by Dispatch Groups**

</td><td>

If dispatch groups have been created, assign one, or more dispatch groups to the agent user group.

</td></tr><tr><td id="d107494e543">

**Product Models**

</td><td>

Assign the equipment used by the group.

</td></tr></tbody>
</table>6.  Click **Update**.


## Setting up user groups for qualifiers

Create a qualifier user group to review and qualify work orders to ensure that the work order tasks are created.

### Before you begin

Role required: wm\_admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Group Management** &gt; **Qualifier Groups**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  Right-click and save.

5.  Use the following tabs to add additional information to the agent user group.

<table id="choicetable_d42_kbh_3xb"><tbody><tr><td id="d107494e666">

**Roles**

</td><td>

Assign one or more roles from the list of available roles to the user group.

 For more information on roles and assigning them to user groups, see [Roles installed with Field Service Management](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md) and [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).

</td></tr><tr><td id="d107494e695">

**Group Members**

</td><td>

Assign one or more qualifiers from the list of available qualifiers to the user group.

 For more information on assigning group members, see [Add a user to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AddAUserToAGroup.md).

</td></tr><tr><td id="d107494e714">

**Groups**

</td><td>

Create a child user group.

</td></tr><tr><td id="d107494e723">

**Locations Covered**

</td><td>

Assign one or more locations from the list of locations to the qualifier user group.

 For more information on assigning locations to a group, see [Assign a location to a group](../../work-management/concept/c_TerritoryManagement.md#).

</td></tr></tbody>
</table>6.  Click **Update**.


## Setting up user groups for dispatchers

Set up dispatcher user groups to dispatch tasks to agent user groups in order to meet the needs of specific areas.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Group Management** &gt; **Dispatch Groups**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  Right-click and save.

5.  Use the following tabs to add additional information to the agent user group.

    For more information about Field Service Roles, see [Roles installed with Field Service Management](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md).

<table id="choicetable_qrz_byd_hxb"><tbody><tr><td id="d107494e870">

**Roles**

</td><td>

Assign one or more roles from the list of available roles to the user group.

 For more information on roles and assigning them to user groups, see [Roles installed with Field Service Management](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md) and [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md) .

</td></tr><tr><td id="d107494e899">

**Group Members**

</td><td>

Assign one or more dispatchers from the list of available dispatchers to the user group.

 For more information on assigning group members, see [Add a user to a group](https://servicenow.com/docs/bundle/utah-platform-administration/page/administer/users-and-groups/task/t_CreateAGroup.html).

</td></tr><tr><td id="d107494e918">

**Groups**

</td><td>

Create a child user group.

</td></tr><tr><td id="d107494e927">

**Locations Covered**

</td><td>

Assign one or more locations from the list of locations to the dispatcher user group.

 For more information on assigning locations to a group, see [Assign a location to a group](https://servicenow.com/docs/bundle/utah-field-service-management/page/product/work-management/concept/c_TerritoryManagement.html#t_AssignALocationToAGroup).

</td></tr><tr><td id="d107494e946">

**Assignment Groups Covered\|**

</td><td>

Assign one or more agent groups to the dispatch user group.

</td></tr></tbody>
</table>6.  Click **Update**.


## Additional user groups

You can set up other types of user groups.

In addition to setting up Field Service specific user groups, you can set up user groups for managers and initiators. For example, you can set up an initiator user group to create a new work order or you can create a work order from other record types, such as problem, incident, change, or project task. For more information on setting up other types of user groups, see [Create a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/t_CreateAGroup.md).

|User|Locations|User Group|User Group Roles|Manager-Initiator Group Relationship|
|----|---------|----------|----------------|------------------------------------|
|Manager 1|San Diego|SD Managers|wm\_manager|Manages SD Initiators|
|Manager 2|Los Angeles|LA Managers|wm\_manager|Manages LA Initiators|
|Initiator 1|San Diego|SD Initiators|wm\_initiator|Creates work orders for SD Qualifiers|
|Initiator 2|Los Angeles|LA Initiators|wm\_initiator|Creates work orders for LA Qualifiers|

