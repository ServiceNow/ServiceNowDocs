---
title: Enabling and selecting location tracking options
description: Learn how to enable location tracking for the Mobile Agent and select the location tracking option best suited for your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/location-tracking-enable.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Location tracking in the Now Mobile Agent app, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Enabling and selecting location tracking options

Learn how to enable location tracking for the Mobile Agent and select the location tracking option best suited for your users.

## Before you begin

Enable geolocation features on your instance by activating the Geolocation plugin \[com.snc.geolocation\]. The Geolocation plugin gives you access to the manual tracking option. You must purchase a subscription before activating the plugin. For details on plugin activation, see Activate a plugin. For more details, see ServiceNow plugins.

To enable the action-based location tracking option, ensure that you have the Mobile Location Tracking plugin \[com.glide.sg.location.tracking\] installed. For more information about action-based location tracking and its settings, see [Configuring action-based location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/location-tracking-action-config.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Branding** &gt; **Mobile App Configs**.

2.  Select Mobile Agent.

3.  In the Mobile app config form, under the Location Tracking area, select the **Geolocation enabled** field.

4.  Select the lock icon \(\[Omitted image "lock-icon.png"\] Alt text: Lock icon.\) in the **Location Tracking Options** field to edit the field, and select from the following location tracking options.

<table id="choicetable_dn4_2vy_2wb"><thead><tr><th align="left" id="d39837e127">

Tracking options

</th><th align="left" id="d39837e130">

Behavior in the Mobile Agent

</th></tr></thead><tbody><tr><td id="d39837e139">

**Manual tracking**

</td><td>

Displays the manual location tracking option to the user.**Note:** Manual location tracking contains configurable properties. For more information, see [Configuring manual location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/location-tracking-manual-config.md).

 \[Omitted image "location-tracking-manual.png"\] Alt text: Manual tracking option.

</td></tr><tr><td id="d39837e164">

**Action-based tracking**

</td><td>

Displays the action-based location tracking option.**Note:** Action-based location tracking contains configurable properties. For more information, see [Configuring action-based location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/location-tracking-action-config.md).

 \[Omitted image "location-tracking-action.png"\] Alt text: Action-based tracking option.

</td></tr><tr><td id="d39837e189">

**Action-based and manual tracking option**

</td><td>

Displays both the manual and action-based tracking options in the Agent Mobile app. The user selects which option to use.\[Omitted image "location-tracking-both.png"\] Alt text: Action-based and manual tracking selection screen.

</td></tr></tbody>
</table>5.  Select the unlock icon \(\[Omitted image "unlock-icon.png"\] Alt text: Unlock icon.\) in the **Location Tracking Options** field to save the location tracking option.

6.  Right-click in the header and select **Save**.


-   **[Configuring manual location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/location-tracking-manual-config.md)**  
Configure manual location tracking system properties to control how location tracking registers the activity of your users, while performing their tasks.
-   **[Configuring action-based location tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/location-tracking-action-config.md)**  
Configure action-based tracking location properties. This tracking option starts and stops tracking based on the actions a user performs.

**Parent Topic:**[Location tracking for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-location-tracking.md)

