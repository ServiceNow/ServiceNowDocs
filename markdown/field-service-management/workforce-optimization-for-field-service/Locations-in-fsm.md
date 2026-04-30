---
title: Locations in Field Service Management
description: Location represents a geographical area that helps administrators to create different groups and assign tasks to those groups based on the location.Territory management allows Field Service Management administrators to assign locations to users.Territory management allows Field Service Management administrators to assign locations to groups of users.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring locations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Locations in Field Service Management

Location represents a geographical area that helps administrators to create different groups and assign tasks to those groups based on the location.

## Work locations

Field Service Management relies on defined locations for qualifying work orders and tasks, and assigning dispatchers and agents. As part of setting up the application, you define your locations. You can then create qualification, dispatch, and assignment groups based on those locations.

**Related topics**  


[Configuring locations](../../work-management/concept/c_TerritoryManagement.md)

## Assign a location to a user

Territory management allows Field Service Management administrators to assign locations to users.

### Before you begin

Role required: admin

### About this task

This creates a territory, or set of locations covered by a given user. The association helps the system to determine which users can fix problems in particular locations.

### Procedure

1.  Navigate to **All** &gt; **Territories** &gt; **Users**.

2.  Open a user record.

3.  In the **Locations Covered** related list:

    -   Click **Edit** to add an existing location to the user.
    -   Click **New** to create a new location to associate to the user.
    Territory management at the user level is not used for automations.


## Assign a location to a group

Territory management allows Field Service Management administrators to assign locations to groups of users.

### Before you begin

Role required: admin

### About this task

This creates a territory, or set of locations covered by a given group. The association helps the system to determine which groups can fix problems in particular locations.

### Procedure

1.  Navigate to **All** &gt; **Territories** &gt; **Groups**.

2.  Open a group record.

3.  In the **Locations Covered** related list:

    -   Click **Edit** to add an existing location to the group.
    -   Click **New** to create a new location to associate to the group.
    **Note:** To determine which group covers a given location, the system checks the location hierarchy to see if there are any groups assigned to the location. If not, the system checks the upper level of hierarchy.


