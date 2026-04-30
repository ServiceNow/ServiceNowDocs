---
title: Location tracking for mobile
description: Location tracking enables you to track the activity and positioning of agents while they perform tasks. You can also use the feature to make sure your agents are safe and can be easily located.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Location tracking for mobile

Location tracking enables you to track the activity and positioning of agents while they perform tasks. You can also use the feature to make sure your agents are safe and can be easily located.

## Location tracking options

There are two options available for location tracking. You can either select one option for users or you can make both options available to users who then must select a location tracking option. The location tracking option that you select applies to the instance.

The two location tracking options are:

-   Manual tracking – This option enables users to select whether to start location tracking for a defined period or for users ￼￼to be continuously tracked. This type of location tracking is only supported on the Mobile Agent app. For information about the manual tracking option, see [Configuring manual location tracking](../task/location-tracking-manual-config.md).
-   Action-based tracking – You can use this option to configure functions to start or stop location tracking, based on actions a user performs. This type of location tracking is supported on both the Mobile Agent app and the Now Mobile app. For information about the action-based tracking option, see [Configuring action-based location tracking](../task/location-tracking-action-config.md).

## Activating plugins

As an administrator, you must activate geolocation tracking for your  users by installing the Geolocation plugin \(com.snc.geolocation\). This plugin enables the manual tracking option. To enable action-based location tracking, the Mobile Location Tracking plugin \(com.glide.sg.location.tracking\) must be installed.

**Note:** To install the Mobile Location Tracking plugin \(com.glide.sg.location.tracking\), you must first install the Geolocation plugin \(com.snc.geolocation\).

For details on plugin activation, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Location tracking and your users

After activating the plugins and performing the various configurations, you must enable location tracking for users. For more information, see [Enabling location tracking for users](../task/location-tracking-add-user.md).

On the users-side, after configuring the location tracking options, users will see the geolocation location tracking settings in the  **Settings**  tab of their mobile devices. Users can enable or disable location tracking on their device. For more information, see [Using location tracking for mobile](mobile-location.md).

## Location tracking in offline

Location tracking is supported in offline. While offline, the user’s location and activity is collected and stored in the device. When the user goes back online, all the collected tracking data is synchronized to their instance.

-   **[Enabling and selecting location tracking options](../task/location-tracking-enable.md)**  
Learn how to enable location tracking for the Mobile Agent and select the location tracking option best suited for your users.
-   **[Enabling location tracking for users](../task/location-tracking-add-user.md)**  
Enable location tracking for specified users. The same tracking location settings apply to all the selected users on the instance.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

