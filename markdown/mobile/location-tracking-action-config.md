---
title: Configuring action-based location tracking
description: Configure action-based tracking location properties. This tracking option starts and stops tracking based on the actions a user performs.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Enabling/selecting options, Location tracking, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configuring action-based location tracking

Configure action-based tracking location properties. This tracking option starts and stops tracking based on the actions a user performs.

## Before you begin

Enable geolocation features on your instance by activating the Geolocation plugin \[com.snc.geolocation\]. The Geolocation plugin gives you access to the manual tracking option. You must purchase a subscription before activating the plugin. For details on plugin activation, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

To enable the action-based location tracking option, ensure that you have the Mobile Location Tracking plugin \[com.glide.sg.location.tracking\] installed.

You must have a preconfigured action item before you can configure the action-based tracking option. For more information, see [Configure an action item](sg-studio-create-action-item.md).

You need preconfigured action functions for users to tap within their mobile device. For more information, see [Configure an action function](sg-studio-config-action-function.md).

**Note:**

-   Action-based location tracking is supported on both the Mobile Agent app and the Now Mobile app.
-   Only a start action function is needed in a scenario where you want tracking to start for a defined number of hours, after the user taps a button.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Functions**.

2.  Select a preconfigured action function.

3.  Select Action item in the **Type** field.

4.  In the **Action item** field, select the search icon \(![Reference lookup icon.](../image/reference-lookup-icon.png)\) and from the list, select the action item you want to trigger.

5.  In the **Location tracking action** field, select one of the following options of the action item.

<table id="choicetable_tqp_sb1_fwb"><thead><tr><th align="left" id="d123245e154">

Location tracking action

</th><th align="left" id="d123245e157">

Description

</th></tr></thead><tbody><tr><td id="d123245e163">

**None**

</td><td>

This option does not affect any location tracking functionality.

</td></tr><tr><td id="d123245e172">

**Stop**

</td><td>

Ends a location tracking session.

</td></tr><tr><td id="d123245e181">

**Start**

</td><td>

Starts a location tracking session.**Note:** If you select the Start option, the **Tracking properties** field displays and is a required field.

</td></tr></tbody>
</table>6.  Define the location tracking settings that happen after a user initiates the action function.

    This option displays only when you select Start in the **Location tracking action** field.

    1.  In the **Tracking properties** field, select the search icon to open the Location Tracking list.
    2.  Select the **New** button.
    3.  Enter a name for the location tracking settings.
    4.  In the **Duration** field, enter the amount of time the action-based tracking should be active after the user selects the start action item. The range is 1 minute to 24 hours.
    5.  In the **Accuracy** field, define the accuracy of the user’s action location in real time. The approximate settings are:

        1.  High is within about 10 meters of the desired location.
        2.  Medium is within about 100 meters of the desired location.
        3.  Low is within about 1000 meters of the desired location.
        **Note:** Consider that the higher the accuracy the more drain on the battery of the users’ device. Also, higher accuracy values can affect data protection and data privacy for users.

    6.  In the **Proximity** field, define the number of meters that a user moves before a new tracking report is recorded. The range is from 1 meter and above.
    7.  In the **Frequency** field, define how often a new tracking report is recorded. The range is 1 minute to 24 hours.
    8.  Select **Submit**, to save your location tracking record.
    The **Tracking Properties** field is populated with the location tracking record setting that you define.

7.  Right-click in the header and select **Save**, to save your action function settings.


**Parent Topic:**[Enabling and selecting location tracking options](location-tracking-enable.md)

