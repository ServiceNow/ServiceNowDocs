---
title: Install and enable offline capabilities
description: Configure the offline mode for your mobile app to control how and when users access data without connectivity. Users can download the cache manually, or receive it automatically based on schedules you configure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/enable-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-05-31"
reading_time_minutes: 2
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Install and enable offline capabilities

Configure the offline mode for your mobile app to control how and when users access data without connectivity. Users can download the cache manually, or receive it automatically based on schedules you configure.

This mandatory setup option step describes how to request and install the offline mode plugin. Installing the plugin makes available for flags, properties, jobs, and UI elements used throughout the rest of this setup.

## Activation of mobile offline

To activate offline mode, the following actions and outcomes occur:

1.  Request and install the Offline Mode plugin \(`com.glide.sg.offline`\). For more information, see, [Request offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/sg-request-work-offline.md).

    **Note:** This plugin is automatically included when the Field Service Mobile plugin is installed.

2.  Once the plugin is installed, the following occurs:
    1.  Offline capabilities are enabled by default for all users.
    2.  Configure which mobile apps and flows within the mobile app are available for use in offline mode. For more information, see [Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md).
3.  An **Offline mode** section displays in the **Settings** tab of the ServiceNow mobile apps. From this section, users can download the offline cache when required.

    **Note:** After the cache is successfully downloaded, the app automatically switches to offline mode when connectivity is lost, or users can manually switch to offline mode before entering areas with limited or no network access.

4.  Deactivation of mobile offline: If offline mode is no longer required for your mobile applications, you can disable it. This will turn off all offline mode functionality across your instance for all the users.

-   **[Request offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/sg-request-work-offline.md)**  
Activate offline mode for mobile by requesting the activation of the SG Offline support plugin \(com.glide.sg.offline\).
-   **[Deactivate offline mode on your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/deactivate-offline.md)**  
Deactivate the offline mode by creating the property glide.sg.offline.enabled and setting the property to false.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md)

