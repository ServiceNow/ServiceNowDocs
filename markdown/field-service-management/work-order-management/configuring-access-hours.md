---
title: Configuring the auto-population of access hours in a work order task
description: Defining default access hours for a work order task based on customer preferences such as account, location, or asset, enables the auto-population of the access hours for the task.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Configuring the auto-population of access hours in a work order task

Defining default access hours for a work order task based on customer preferences such as account, location, or asset, enables the auto-population of the access hours for the task.

An administrator can set up access hours preferred by the customers such as account, location, asset, or a combination. The system evaluates these levels based on their order to determine the appropriate default access hours for the task.

Access hour levels define different attributes of work order tasks as matching criteria. These attributes should match the task for which you’re determining the access hours. Assigning an order to each level helps the system to evaluate the attributes of a task based on their priority. An ordering rule sorts the levels in descending order. You can then set preferences for these access hour levels by assigning a value to each attribute, and providing an access hour schedule, such as 8-5 weekdays, 24x7.

When a work order task is created, the system searches for any active access hour levels based on the assigned order and then identifies whether the attributes on the task match the access hour preferences. If the attributes match, the system auto-populates the corresponding access hour preferences. Note that administrators or dispatchers can also manually override the default access hours if the estimated time duration for the task falls outside the defined access hours.

The following example shows the access hour preferences for an account at two different locations and the information that the system might return.

-   **Access hour level: Account Location, Matching criteria: Account and Location, Account preferences: Boxeo, Location preferences: San Francisco and Florida**

    The Boxeo account at the San Francisco location has 19:00 - 21:00 access hours, whereas the Boxeo account at the Florida location has 18:00 - 21:00 access hours.


## Configuration overview

The steps for setting up the auto-population of access hours are:

1.  [Activate Field Service Management Access Hours Management](../task/install-access-hour-fsm.md)

    Activate the Field Service Management Access Hours Management plugin \(com.snc.fsm\_access\_hours\) for Field Service Management if you have the admin role.

2.  [Define access hour preferences for a work order task](../task/define-access-hour-preferences.md)

    Define the access hours to set the times that a location is available for an agent to go to and complete work.


