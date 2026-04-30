---
title: Add a user to the neighborhood
description: Assign one or more users to a neighborhood. Create a workplace profile and add the user directly.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Managing Neighborhoods, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Add a user to the neighborhood

Assign one or more users to a neighborhood. Create a workplace profile and add the user directly.

## Before you begin

If you’re using Workplace Space Management version 1.11.1 or later, you can also add a user to the neighborhood from their workplace profile directly. Refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md).

**Important:** From Workplace Space Management version 1.11.1, the **Neighbourhood User Assignments** table is no longer available. Instead, the user assignment can be performed on a workplace profile directly using the **Workplace Profile Location Assignment** table \(displayed a related list on the form\) in the Workplace Core application. The **Workplace Profile Location Assignment** in the Workplace Core is now configured with additional fields such as **Profile type**, **Neighborhood**, and **Source** where all the data is saved. This table helps a space manager to perform scenario planning and save any user assignment-related changes performed on a neighborhood directly on the workplace profile.

On a neighborhood, when you configure a user assignment rule, the neighborhood assignment changes on the workplace profile are automatically saved on the user's workplace profile. On the user's workplace profile, you can know the type of assignment from the **Profile type** field.

If you’re an existing customer, upon upgrading, the entities in the **Neighbourhood User assignments** table are automatically migrated to the **Workplace Profile Location Assignment** of the user's workplace profile.

Role required: sn\_wsd\_core.admin, sn\_wsd\_core.workplace\_manager, sn\_wsd\_spcmgmt.space\_planner

## About this task

Edit an existing user in a neighborhood or add a user to a neighborhood.

To add a user to the neighborhood, the user must have a workplace profile. If the user doesn’t have a workplace profile created, create a workplace profile and add the user using the following procedure.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **All**.

2.  Select the neighborhood to which you want to assign a user.

3.  If you’re using Workplace Space Management version 1.10.0 or below, to add a user, do the following:

    1.  On the form, select the User Assignments Related list.

    2.  Select **New**.

    3.  On the User Workplace Profile form, do the following:

        1.  Select the **Employee** whom you want to add.
        2.  Select the **Workplace Entity** to which the employee belongs.
        3.  Select **Submit**.

            The workplace profile is created for the user and is also added to the neighborhood.

4.  If you’re using Workplace Space Management version 1.11.1 or later, to add a user, do the following:

    1.  On the form, select the Workplace Profile Location Assignment related list.

    2.  Select **New**.

    3.  On the Workplace Profile Location Assignment, do the following:

        1.  In the **Workplace profile** field, select the user's workplace profile who you want to add.
        2.  Select the **Profile type** as **Neighbourhood assignment**.
        3.  In the **Workplace location** field, select the workplace location in the neighborhood to which you want to assign the user.

            The user is added to the neighborhood. The workplace profile of the user is updated with the neighborhood assignment. You can also make or edit the neighborhood assignment from the workplace profile. For more information, refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md).

5.  Select **Update**.


## Result

The user is added to the neighborhood. The Workplace Profile Location Assignment of the user is updated. The Workplace Profile Location Assignment related list in the Workplace Profile form of the user and the Neighborhood form are updated. Neighborhood assignments are applicable if **Neighborhood** is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.

For more information about the Workplace Profile Location Assignment, see [Workplace Profile Location Assignment form](../../workplace-service-delivery/reference/wsd-location-assignment-form.md).

**Parent Topic:**[Managing Neighborhoods](../concept/neighborhoods.md)

