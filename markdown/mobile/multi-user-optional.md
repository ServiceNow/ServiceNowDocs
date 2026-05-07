---
title: Optional settings for multi-user configuration
description: Use optional settings on a shared device to define how long users are allowed to remain inactive before being required to reenter their PIN. The default is 300 seconds. You also have the option define the maximum number of users permitted on a shared device. The default is 15 users.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Multiple users on a shared device, Configuring the Mobile Platform, Mobile Platform]
---

# Optional settings for multi-user configuration

Use optional settings on a shared device to define how long users are allowed to remain inactive before being required to reenter their PIN. The default is 300 seconds. You also have the option define the maximum number of users permitted on a shared device. The default is 15 users.

## Before you begin

Role required: mobile\_admin, admin

## About this task

There are three optional settings that can be used when working with the multi-user configuration on a shared device.

-   Set the maximum number of users on a shared device. The default is 15 users the maximum is 30 users.

    **Note:** If the maximum number of users has been reached and an additional user tries to add themselves, they are given the option to remove the user who has been inactive on the device the longest.

-   Enable the **EnablePushNotificationinSharedDeviceMode** property. By default, push notifications in a shared device are not enabled. Only use this property and set to true if you want to display push notifications to the active user.

    **Note:** When enabling push notifications on a shared device, be aware that other users using the device may be able to view other users’ notifications and banners.

-   Set the maximum idle time before users are prompted to re-enter their PIN. The default is 300 seconds. This feature is described in the topic [PIN timeout](pin-timeout.md).

## Procedure

1.  Set the number of users on a shared device.

    1.  Navigate to **All** &gt; **All &gt; sys\_sg\_properties.list**. The Mobile Properties form displays.
    2.  In the Mobile Properties list, select  **New**.
    3.  Type the mobile property name **MaxUsersPerSharedDevice** in the name field.
    4.  Select **Integer** in the **Type** field.
    5.  Enter a number between 2 and 30 in the **Value** field.

        **Note:** The value must be between 2 and 30. Any entry outside of this range defaults to 15.

    6.  Select **Update**.
2.  Set **EnablePushNotificationinSharedDeviceMode** to `true` to allow notifications and banners to be displayed to the active user on the shared device.

    1.  Navigate to **All** &gt; **All &gt; sys\_sg\_properties.list**. The Mobile Properties form displays.
    2.  Search for the property **EnablePushNotificationinSharedDeviceMode** and select it or add the property if it does not already exist.
    3.  Select **True/False** is in the **Type** field and enter `true` in the **Value** field.

        **Note:** If this parameter is set to `true` and the device is in shared mode, push notifications are only sent to the currently active user. This means that another user may receive notifications that were not intended for them.

    4.  Select **Update**.

