---
title: Configuring locations
description: Territory management determines, by geographical location, the individual or group best positioned to execute a service call.Location represents a geographical area that helps administrators to create different groups and assign tasks to those groups based on the location.Location represents a geographical area that helps administrator to create different groups and assign tasks to those groups based on the location.Territory management allows field service management administrators to assign locations to users.Territory management allows field service management administrators to assign locations to groups of users.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set up workforce, Configure, Field Service Management]
---

# Configuring locations

Territory management determines, by geographical location, the individual or group best positioned to execute a service call.

Territory management allows the assignment of a set of geographical locations to an individual or group. This assignment creates a territory. Territory management is based on a hierarchy where all locations are attached to a parent location. Top-level locations do not have a parent location. Territory Management is activated automatically with Field Service Management.

## Configuration overview

The steps for configuring locations are:

1.  [Adding locations](c_TerritoryManagement.md#)

    You can add locations individually or you can perform a bulk import using a CSV, XLS, or XML file.

2.  [Assign locations to users and user groups](c_TerritoryManagement.md#)

    Territory management allows Field Service Management administrators to assign locations to users and user groups.


**Related topics**  


[Assign a location to a user](c_TerritoryManagement.md#)

[Assign a location to a group](c_TerritoryManagement.md#)

## Adding locations

Location represents a geographical area that helps administrators to create different groups and assign tasks to those groups based on the location.

Locations are used to calculate distances and travel times and are used to determine which agent is closest to a task assignment. Define the home locations of all Field Service technicians and the current locations of assets in the field. Define the locations that will be covered by Field Service dispatchers and technicians in your organization. You can configure different levels of locations in a parent-child hierarchy. You can add locations individually or you can perform a bulk import using a CSV, XLS, or XML file. For more information about adding locations to user groups, see [Assign a location to a group](c_TerritoryManagement.md#).

**Related topics**  


[Assign a location to a user](c_TerritoryManagement.md#)

[Assign a location to a group](c_TerritoryManagement.md#)

## Locations in Field Service Management

Location represents a geographical area that helps administrator to create different groups and assign tasks to those groups based on the location.

### Work locations

Field Service Management relies on defined locations for qualifying work orders and tasks, and assigning dispatchers and agents. As part of setting up the application, you will define your locations. You can then create qualification, dispatch, and assignment groups based on those locations.

**Related topics**  


[Configuring locations](c_TerritoryManagement.md#)

### Assign a location to a user

Territory management allows field service management administrators to assign locations to users.

#### Before you begin

Role required: admin

#### About this task

This creates a territory, or set of locations covered by a given user. The association helps the system to determine which users can fix problems in particular locations.

#### Procedure

1.  Navigate to **All** &gt; **Territories** &gt; **Users**.

2.  Open a user record.

3.  In the **Locations Covered** related list:

    -   Click **Edit** to add an existing location to the user.
    -   Click **New** to create a new location to associate to the user.
    Territory management at the user level is not used for automations.


### Assign a location to a group

Territory management allows field service management administrators to assign locations to groups of users.

#### Before you begin

Role required: admin

#### About this task

This creates a territory, or set of locations covered by a given group. The association helps the system to determine which groups can fix problems in particular locations.

#### Procedure

1.  Navigate to **All** &gt; **Territories** &gt; **Groups**.

2.  Open a group record.

3.  In the **Locations Covered** related list:

    -   Click **Edit** to add an existing location to the group.
    -   Click **New** to create a new location to associate to the group.
    **Note:** To determine which group covers a given location, the system checks the location hierarchy to see if there are any groups assigned to the location. If not, the system checks the upper level of hierarchy.


