---
title: Set the primary location of a workplace profile
description: Assign a primary location for the workplace profile if there are multiple locations assigned.
locale: en-US
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mapping employees to their designated workspaces, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Set the primary location of a workplace profile

Assign a primary location for the workplace profile if there are multiple locations assigned.

## Before you begin

**Note:** From Workplace Core version 2.16.1, the workplace user profiles are created in the Workplace Profile Location Assignment \[sn\_wsd\_core\_workplace\_profile\_location\] table. A new field **Is Primary** is added in the table so that you can specify if a location is the primary location when there are multiple locations. In the case of existing user profiles created in the User Workplace Profiles \[sn\_wsd\_core\_workplace\_profile\] table, a fix script runs and automatically considers the latest workplace location added to the profile as the primary workplace location. To set the primary location of a workplace profile, refer to [Set the primary location of a workplace profile](set-prim-location-of-worplace-profile.md).

Role required: admin

## About this task

When there are multiple locations to which as user workplace profile is assigned, you can specify the primary workplace location. The primary workplace location is considered as the main location. The following areas are impacted when you set a primary workplace location:

-   When an employee raises a workplace service request, depending on the user for whom the request is being used, the fields are automatically filled. In the case where a location is required on the form, the application automatically fills it with the specified primary location.
-   When an employee searches for spaces nearby to the user's location to make a reservation, the primary location is considered.

## Procedure

1.  Navigate to **All** &gt; **Workplace core** &gt; **Administration** &gt; **Workplace profiles**.

2.  Select the **Active** field of the workplace profile that you want to modify.

    For example, select **true** in the **Active** column to open the record.

3.  On the form, scroll down to the Workplace Profile Location Assignment related list.

4.  Set the primary location.

    -   To add a new location and then it set it as primary, do the following:
        1.  Select **New**.
        2.  Add the location. Refer to [Map designated workspaces to user profiles](map-employees-to-existing-workplace-locations-wsd.md).
        3.  Ensure that the **Is primary** field is selected.
    -   To set an existing location as primary, do the following:
        1.  Go to the **Is primary** field of the workplace location.
        2.  Set the field to **true**.
5.  Select **Update**.


## Result

The primary workplace location is set. The **Primary Workplace location** field is updated with the location.

**Parent Topic:**[Mapping employees to their designated workspaces](../concept/mapping-employees-to-existing-work-locations-wsd.md)

