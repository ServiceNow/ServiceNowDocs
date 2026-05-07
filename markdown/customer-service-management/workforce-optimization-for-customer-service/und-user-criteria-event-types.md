---
title: Managing user criteria for event types in Workforce Optimization for Customer Service
description: Manage user access for any event type such as meeting, training, and time-off requests in the team calendar.Add a user criteria record to specify which users, roles, and groups can access event types in Workforce Optimization for Customer Service.Add or remove access to users for any event type so that they can view event types that are relevant only to them.​Check what create, read, update, and delete rights your groups or your team members have for events to make sure that they have the correct permissions that they need.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Managing user criteria for event types in Workforce Optimization for Customer Service

Manage user access for any event type such as meeting, training, and time-off requests in the team calendar.

You can include or exclude Create, Read, Write or Update, and Delete \(CRUD\) rights for event types using the inclusion and exclusion user criteria access. You can perform the CRUD operations for users, groups, or roles.

**Note:** By default, team members don’t have read-access to events of type **Actual work**.

For additional flexibility around managing the CRUD access, you can set the user criteria for each event type. For example, if team members don't have access to edit their work shifts using their role-based access, you can set that access using user criteria. You can set this access for specific team members or for the whole group.

![The flow diagram diaplying the logic on how inclusion and exclusion user criteria access work for event types.](../image/inclusion-exclusion-criteria-event-types.svg "Inclusion and exclusion logic for event types")

**How inclusion and exclusion user criteria access works**

When the user criteria rules get evaluated, it's done in the following order:

1.  The system first evaluates the exclusion access for each criteria.
    -   If the exclusion access for a CRUD operation is set to **true**, then the system evaluates the user criteria.
        1.  If the user doesn’t have access based on their role, then the user is denied access for the specific CRUD operation.
        2.  If the user isn’t denied access, then the system evaluates the inclusion criteria.
    -   If the exclusion access for a CRUD operation is set to **false**, then the system evaluates the inclusion criteria.
2.  For the inclusion access, for a specific CRUD operation such as Create, the system checks if at least one of the inclusion user criteria is set to **true**. If yes, then the system evaluates the user criteria based on the user's role access.
    -   If the user:
        -   Has access for the CRUD operation based on their user role, then the user can perform that action. For example, if the event type is training and the CRUD operation is **Create** then the user can create the training event types.
        -   Doesn’t have access for the CRUD operation based on their user role, then the user can’t perform that action.
    -   If at least one of the inclusion criteria isn’t set to **true**, the user doesn’t have access to the specific CRUD operation. In this example, the user can’t create the training event types.

**Note:** The exclusion access always takes precedence over the inclusion access. If no inclusion or exclusion access is set, then the role-based access is used for managing event types.

**Parent Topic:**[Using Workforce Optimization for Customer Service](use-configurable-wfo-cs.md)

## Create user criteria for event types in Workforce Optimization for Customer Service

Add a user criteria record to specify which users, roles, and groups can access event types in Workforce Optimization for Customer Service.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **User Criteria**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the user criteria|
    |Users|Users who can access event types.|
    |Groups|Groups who can access event types.|
    |Roles|Roles who can access event types when you apply the user criteria.|
    |Advanced|Option to create a script for the user criteria.|
    |Active|Enabling the check box makes the user criteria available.|
    |Companies|Companies who can access event types.|
    |Location|Locations that can access event types.|
    |Departments|Departments that can access event types.|
    |Match All|Option to make every condition that is set required when the user criteria are applied.|

4.  Select **Submit**.


## Include or exclude user access for event types​

Add or remove access to users for any event type so that they can view event types that are relevant only to them.​

### Before you begin

Role required: sn\_shift\_planning.admin​

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for CSM** &gt; **Scheduling** &gt; **Event Configuration**.

2.  Select an event.

3.  Exclude or Include specific CRUD access for users to events.

<table id="choicetable_s5n_mmr_pwb"><thead><tr><th align="left" id="d234160e442">

To

</th><th align="left" id="d234160e445">

Do this

</th></tr></thead><tbody><tr><td id="d234160e451">

**Exclude users for which you do not want to enable specific access to event types.__Important:__ For exclusion, a __Create__ access will deny the user from creating events because it excludes that access for the user. The same principle applies to any of the CRUD operations.

**

</td><td>

1.  Select the **Evaluate access for exclusion** tab.

**Note:** You can set the CRUD access for each user criteria where you would exclude the user from specific CRUD operations.

2.  To create a new **Event Exclusion User Criteria**, select **New**.
3.  In the **Name** field, enter a name, which is an entity of users that is evaluated for the exclusion user criteria for the selected event type. This entity identifies and associates the user criteria to the event type..
4.  In the **User criteria** field, select the user criteria record for which you want to set exclusion CRUD operations.
5.  Select the CRUD operations for which you do not want to give access.
6.  Select **Submit**.


</td></tr><tr><td id="d234160e508">

**Include users for which you want to enable specific access to event types.__Important:__

For inclusion, for specific CRUD operation such as __Create__, the system evaluates if at least one of the inclusion user criteria is set to __true__:

-   If any of the criteria is set to true, then the system checks if the user satisfies the criteria.
    -   If the user satisfies the criteria, then they have access for the specific CRUD operation.
    -   If the user does not satisfy the criteria, then they don't have access to the CRUD operation.
-   If none of the criteria is set to true, the user has access to the specific CRUD operation. This is based on the default behavior where all users have access based on their roles before they're added to the user criteria.
**

</td><td>

1.  Select the **Evaluate access for inclusion** tab.
2.  To create a new **Event Inclusion User Criteria**, select **New**.
3.  In the **Name** field, enter a name for the event inclusion user criteria.
4.  In the **User criteria** field, select the user criteria record for which you want to set inclusion user criteria access.
5.  Select the CRUD operations for which you want to give access.
6.  Select **Submit**.


</td></tr></tbody>
</table>4.  Click **Update**.


## Verify access criteria for a group or a team member in Workforce Optimization for Customer Service

Check what create, read, update, and delete rights your groups or your team members have for events to make sure that they have the correct permissions that they need.

### Before you begin

Role required: sn\_shift\_planning.admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  In the lists module, go to **Scheduling** &gt; **Event type**.

3.  Select an event for which you want to verify user access.

4.  Select the **User access** tab.

5.  Do any of the following.

<table id="choicetable_oxp_qm1_xwb"><thead><tr><th align="left" id="d234160e696">

To

</th><th align="left" id="d234160e699">

Do this

</th></tr></thead><tbody><tr><td id="d234160e705">

**Verify user access for all your groups**

</td><td>

Select **All my groups**.

</td></tr><tr><td id="d234160e717">

**Specific groups and team members**

</td><td>

1.  Select **Specific groups and team members**.
2.  In the **Specific groups** field, enter the groups for which you want to verify user access.
3.  In the **Team members** field, select the members of your team for which you want to verify the access.
4.  Select **Check user access**.


</td></tr></tbody>
</table>    The screen displays the create, read, write, and delete columns as **true** for each team member that has access to the specific type of access to the selected event.


