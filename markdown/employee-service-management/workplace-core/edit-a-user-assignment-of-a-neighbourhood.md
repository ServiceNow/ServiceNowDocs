---
title: Edit a user assignment of a neighborhood
description: Edit an existing user's workplace profile assigned to the neighborhood.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing Neighborhoods, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Edit a user assignment of a neighborhood

Edit an existing user's workplace profile assigned to the neighborhood.

## Before you begin

If you’re using Workplace Space Management version 1.11.1 or later, you can also edit or remove a user from a neighborhood from their workplace profile directly. Refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md).

**Important:** From Workplace Space Management version 1.11.1, the **Neighbourhood User Assignments** table is no longer available. Instead, the user assignment can be performed on a workplace profile directly using the **Workplace Profile Location Assignment** table \(displayed a related list on the form\) in the Workplace Core application. The **Workplace Profile Location Assignment** in the Workplace Core is now configured with additional fields such as **Profile type**, **Neighborhood**, and **Source** where all the data is saved. This table helps a space manager to perform scenario planning and save any user assignment-related changes performed on a neighborhood directly on the workplace profile.

On a neighborhood, when you configure a user assignment rule, the neighborhood assignment changes on the workplace profile are automatically saved on the user's workplace profile. On the user's workplace profile, you can know the type of assignment from the **Profile type** field.

If you’re an existing customer, on upgrading, the entities in the **Neighbourhood User assignments** table are automatically migrated to the **Workplace Profile Location Assignment** of the user's workplace profile.

Role required: sn\_wsd\_core.admin, sn\_wsd\_core.workplace\_manager, sn\_wsd\_spcmgmt.space\_planner

## About this task

You can add only users with workplace profiles to a neighborhood. Perform the following steps to edit user assignments that have workplace profiles.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **All**.

2.  Select the neighborhood in which you want to edit the user assignment.

3.  If you’re using Workplace Space Management version 1.10.0 or below, to edit a user, do the following:

    1.  On the form, select the User Assignments Related list.

    2.  Select **Edit...**.

    3.  On the Edit members form, add or remove users between **Collections** and **User Assignments list**.

    4.  Select **Save**.

        The user assignment is updated.

4.  If you’re using Workplace Space Management version 1.11.1 or later, to edit a user, do the following:

    1.  On the form, select the Workplace Profile Location Assignment related list.

    2.  Edit the details of the user directly from the list view or select the Preview icon \(![Preview icon.](../../safe-workplace-dashboard/image/icon-preview.png)\).

        Select **Open Record**.

    3.  On the Workplace Profile Location Assignment form of the user, change the fields that you want to edit.

    4.  Select **Update**.

        The user assignment is updated and the workplace profile of the user is updated with the changes.

5.  Select **Update**.


## Result

The user assignment is updated. Neighborhood assignments are applicable if **Neighborhood** is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.

**Parent Topic:**[Managing Neighborhoods](../concept/neighborhoods.md)

