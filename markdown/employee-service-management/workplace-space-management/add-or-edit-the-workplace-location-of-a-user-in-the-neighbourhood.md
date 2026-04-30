---
title: Add or edit the workplace location of a user in the neighborhood
description: Add a workplace location to a user assignment or update the existing workplace location of the user assignment.
locale: en-US
release: xanadu
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing Neighborhoods, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Add or edit the workplace location of a user in the neighborhood

Add a workplace location to a user assignment or update the existing workplace location of the user assignment.

## Before you begin

If you’re using Workplace Space Management version 1.11.1 or later, you can also edit the workplace location of a user from their workplace profile directly. Refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md).

**Important:** From Workplace Space Management version 1.11.1, the **Neighbourhood User Assignments** table is no longer available. Instead, the user assignment can be performed on a workplace profile directly using the **Workplace Profile Location Assignment** table \(displayed a related list on the form\) in the Workplace Core application. The **Workplace Profile Location Assignment** in the Workplace Core is configured with additional fields such as **Profile type**, **Neighborhood**, and **Source** where all the data is saved. This table helps a space manager to perform scenario planning and save any user assignment-related changes performed on a neighborhood directly on the workplace profile.

On a neighborhood, when you configure a user assignment rule, the neighborhood assignment changes on the workplace profile are automatically saved on the user's workplace profile. On the user's workplace profile, you can know the type of assignment from the **Profile type** field.

If you’re an existing customer, on upgrading, the entities in the **Neighbourhood User assignments** table are automatically migrated to the **Workplace Profile Location Assignment** of the user's workplace profile.

Role required: sn\_wsd\_spcmgmt.admin, sn\_wsd\_spcmgmt.space\_planner

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **All**.

2.  Select the neighborhood that you want to update.

3.  If you’re using Workplace Space Management version 1.10.0 or below, to edit a user, do the following:

    1.  On the form, select the User Assignments Related list.

    2.  Double-click the workplace location of the workplace profile to add or edit the location.

    3.  Search and select the location.

        **Note:** You can only select a floor, area, or a space as the workplace location.

    4.  Select **Save**.

        The workplace location of the user is updated.

4.  If you’re using Workplace Space Management version1.11.1 or later, to edit a user, do the following:

    1.  On the form, select the Workplace Profile Location Assignment related list.

    2.  Double-click the workplace location of the workplace profile to add or edit the location.

    3.  Search and select the location.

        **Note:** You can only select a floor, area, or a space as the workplace location.

    4.  Select **Save**.

5.  Select **Update**.

    The workplace location is updated and the workplace profile of the user is updated with the changes.


## Result

The workplace location is updated for the selected workplace profile. You can also make neighborhood-related changes on the workplace profile directly. Refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md). Neighborhood assignments are applicable if Neighborhood is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.

