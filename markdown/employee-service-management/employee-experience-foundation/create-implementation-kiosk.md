---
title: Customize data display in Kiosks
description: Create implementations to customize the display of data in the Schedule and Time off tabs based on your location or any other criterion according to your organizational requirement.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Schedule in Employee Center Pro Kiosk, Configure Employee Center Pro Kiosk, Employee Center Pro Kiosk, Configure, Employee Center, Employee Service Management]
---

# Customize data display in Kiosks

Create implementations to customize the display of data in the **Schedule** and **Time off** tabs based on your location or any other criterion according to your organizational requirement.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

    The names of the two API methods for the **Schedule** tab and the **Time off** tab are:

    -   sn\_ex\_sp\_pro\_kiosk.RetrieveEXKioskEmpSchedule
    -   sn\_ex\_sp\_pro\_kiosk.EXKioskEmployeeTimeOffBalance
2.  From the Extension Points list, select any of the API methods mentioned in step 1.

3.  In the sn\_ex\_sp\_pro\_kiosk.RetrieveEXKioskEmpSchedule method page, select **Create implementation** from the Related Links section.

4.  In the Script Include page, add the unique location sys\_id in the `this.LOCATIONS` array in **Script**.

    -   For more information on location tracking, see [Enabling and selecting location tracking options](https://www.servicenow.com/docs/access?context=location-tracking-enable&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).
    -   For more information on script include customizations, see [Script includes and customization](https://www.servicenow.com/docs/access?context=customize-script-includes-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).
    1.  The location sys\_id enables a `fixed_match`. The `fixed_match` enables you to show location-based data to your users.
    2.  If `fixed_match` isn’t available, then the data available is for a `global_match`. The data remains the same regardless of location.
    3.  If it’s a `no_match`, there isn't a **Schedule** or **Time off** tab visible.

## Result

You can view data on the **Schedule** and **Time off** tabs based on your location or any other user criterion you've set.

**Parent Topic:**[Schedule in Employee Center Pro Kiosk](../concept/shift-time-kiosk-ec.md)

