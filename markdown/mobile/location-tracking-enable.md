---
title: Enabling and selecting location tracking options
description: Learn how to enable location tracking for the Mobile Agent and select the location tracking option best suited for your users.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Location tracking for mobile, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enabling and selecting location tracking options

Learn how to enable location tracking for the Mobile Agent and select the location tracking option best suited for your users.

## Before you begin

Enable geolocation features on your instance by activating the Geolocation plugin \[com.snc.geolocation\]. The Geolocation plugin gives you access to the manual tracking option. You must purchase a subscription before activating the plugin. For details on plugin activation, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). For more details, see [ServiceNow plugins](https://www.servicenow.com/docs/access?context=c_ServiceNowPlugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

To enable the action-based location tracking option, ensure that you have the Mobile Location Tracking plugin \[com.glide.sg.location.tracking\] installed. For more information about action-based location tracking and its settings, see [Configuring action-based location tracking](location-tracking-action-config.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Branding** &gt; **Mobile App Configs**.

2.  Select Mobile Agent.

3.  In the Mobile app config form, under the Location Tracking area, select the **Geolocation enabled** field.

4.  Select the lock icon \(![Lock icon.](../image/lock-icon.png)\) in the **Location Tracking Options** field to edit the field, and select from the following location tracking options.

<table id="choicetable_dn4_2vy_2wb"><thead><tr><th align="left" id="d41846e121">

Tracking options

</th><th align="left" id="d41846e124">

Behavior in the Mobile Agent

</th></tr></thead><tbody><tr><td id="d41846e133">

**Manual tracking**

</td><td>

Displays the manual location tracking option to the user.**Note:** Manual location tracking contains configurable properties. For more information, see [Configuring manual location tracking](location-tracking-manual-config.md).

 ![Manual tracking option.](../image/location-tracking-manual.png)

</td></tr><tr><td id="d41846e158">

**Action-based tracking**

</td><td>

Displays the action-based location tracking option.**Note:** Action-based location tracking contains configurable properties. For more information, see [Configuring action-based location tracking](location-tracking-action-config.md).

 ![Action-based tracking option.](../image/location-tracking-action.png)

</td></tr><tr><td id="d41846e183">

**Action-based and manual tracking option**

</td><td>

Displays both the manual and action-based tracking options in the Agent Mobile app. The user selects which option to use.![Action-based and manual tracking selection screen.](../image/location-tracking-both.png)

</td></tr></tbody>
</table>5.  Select the unlock icon \(![Unlock icon.](../image/unlock-icon.png)\) in the **Location Tracking Options** field to save the location tracking option.

6.  Right-click in the header and select **Save**.


-   **[Configuring manual location tracking](location-tracking-manual-config.md)**  
Configure manual location tracking system properties to control how location tracking registers the activity of your users, while performing their tasks.
-   **[Configuring action-based location tracking](location-tracking-action-config.md)**  
Configure action-based tracking location properties. This tracking option starts and stops tracking based on the actions a user performs.

**Parent Topic:**[Location tracking for mobile](../concept/mobile-location-tracking.md)

