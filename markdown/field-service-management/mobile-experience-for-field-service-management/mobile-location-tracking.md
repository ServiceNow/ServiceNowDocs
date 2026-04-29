---
title: Location tracking for mobile
description: Location tracking enables you to track the activity and positioning of agents while they perform tasks. You can also use the feature to make sure your agents are safe and can be easily located.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Now Mobile Agent application, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Location tracking for mobile

Location tracking enables you to track the activity and positioning of agents while they perform tasks. You can also use the feature to make sure your agents are safe and can be easily located.

## Location tracking options

There are two options available for location tracking. You can either select one option for users or you can make both options available to users who then must select a location tracking option. The location tracking option that you select applies to the instance.

The two location tracking options are:

-   Manual tracking – This option enables users to select whether to start location tracking for a defined period or for users ￼￼to be continuously tracked. This type of location tracking is only supported on the Mobile Agent app. For information about the manual tracking option, see [Configuring manual location tracking](https://www.servicenow.com/docs/access?context=location-tracking-manual-config&version=australia&pubname=australia-mobile&ft:locale=en-US).
-   Action-based tracking – You can use this option to configure functions to start or stop location tracking, based on actions a user performs. This type of location tracking is supported on both the Mobile Agent app and the Now Mobile app. For information about the action-based tracking option, see [Configuring action-based location tracking](https://www.servicenow.com/docs/access?context=location-tracking-action-config&version=australia&pubname=australia-mobile&ft:locale=en-US).

## Activating plugins

As an administrator, you must activate geolocation tracking for your  users by installing the Geolocation plugin \(com.snc.geolocation\). This plugin enables the manual tracking option. To enable action-based location tracking, the Mobile Location Tracking plugin \(com.glide.sg.location.tracking\) must be installed.

**Note:** To install the Mobile Location Tracking plugin \(com.glide.sg.location.tracking\), you must first install the Geolocation plugin \(com.snc.geolocation\).

For details on plugin activation, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Location tracking and your users

After activating the plugins and performing the various configurations, you must enable location tracking for users. For more information, see [Enabling location tracking for users](https://www.servicenow.com/docs/access?context=location-tracking-add-user&version=australia&pubname=australia-mobile&ft:locale=en-US).

On the users-side, after configuring the location tracking options, users will see the geolocation location tracking settings in the  **Settings**  tab of their mobile devices. Users can enable or disable location tracking on their device. For more information, see [Using location tracking for mobile](https://www.servicenow.com/docs/access?context=mobile-location&version=australia&pubname=australia-mobile&ft:locale=en-US).

## Location tracking in offline

Location tracking is supported in offline. While offline, the user’s location and activity is collected and stored in the device. When the user goes back online, all the collected tracking data is synchronized to their instance.

