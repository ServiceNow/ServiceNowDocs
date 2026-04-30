---
title: Configure Zero Trust Access for mobile
description: Configure Zero Trust Access \(ZTA\) on mobile to reduce end-user access based on factors such as IP address, location, and identity provider attributes.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Zero Trust Access, Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Configure Zero Trust Access for mobile

Configure Zero Trust Access \(ZTA\) on mobile to reduce end-user access based on factors such as IP address, location, and identity provider attributes.

## Before you begin

Role required: security-admin

## Procedure

1.  Navigate to **All** &gt; **Zero Trust Access** &gt; **Properties**.

2.  Select the following properties to enable them:

    1.  **zero trust session access**

    2.  **zero trust access for Mobile apps**

3.  Under the mobile client application to which you want to add Zero Trust Access, ensure that **Enable Zero Trust Access** is selected under **Application Registries**.


## Result

If Zero Trust Access is enabled on mobile, the following scenarios trigger a check against the security policy:

-   When the user logs in to the mobile app
-   When the mobile access token has expired and the instance makes a request to get the refresh token

If the session access state changes, the user is informed with a banner and the app refreshes to the home tab. If session access privilege is reduced while the user is impersonating, the session isrelegated and ends the impersonation mode.

To turn off the banner display on mobile app screens when the connection state changes, set the **disableZTABanner** mobile property to `True`. For more information, see [Turn off the Zero Trust Access banner on mobile apps](turn-off-zta-banner.md).

**Note:**

This feature is not yet fully supported with mobile offline capability. Mobile offline and ZTA are both opt-in features. If an offline mobile customer wants to enable ZTA on mobile, the following scenarios can occur:

-   When the cache is downloaded either manually or scheduled, the cache always downloads with full access even if the user downloads it from a relegated session.
-   If the user is offline and performed an action that is pending to be synced, the sync may fail when the user comes online and the user session gets relegated.

Typically, users should not to opt in for mobile offline and ZTA together. However, if users want both then they should create a group of users to whom the ZTA policy should not be applied. This group of users would contain mobile offline users, and if ZTA is enabled, the access policies can be defined to exclude ZTA offline users.

**Parent Topic:**[Securing your ServiceNow mobile instance with Zero Trust Access](zero-trust-access-for-mobile.md)

