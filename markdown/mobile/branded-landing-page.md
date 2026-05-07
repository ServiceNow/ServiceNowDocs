---
title: Branded landing page for a single instance
description: A branded landing page is a public web page displayed to users before they log in to their  ServiceNow mobile app. This pre-login page contains a login button in the header or a deep link that navigates users to a specified area of a  ServiceNow mobile app, bypassing the need to select an instance. The login button can be in the header of the mobile app, an integral part of the web page or both. The login button can either be in the header of the mobile app or an integral part of the web page.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 2
breadcrumb: [Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Branded landing page for a single instance

A branded landing page is a public web page displayed to users before they log in to their  ServiceNow mobile app. This pre-login page contains a login button in the header or a deep link that navigates users to a specified area of a  ServiceNow mobile app, bypassing the need to select an instance. The login button can be in the header of the mobile app, an integral part of the web page or both. The login button can either be in the header of the mobile app or an integral part of the web page.

**Note:** Branded landing pages are available only when working with a single instance.

The auto-login behavior for single instances is not supported for Microsoft Intune MDM builds using the iOS operating system. For more information regarding Microsoft Intune, see [Intune mobile device management \(MDM\)](intune-mdm.md).

Branded landing pages enable you to create a customized page that provides navigation to the user to specific areas on your Now Mobile and Mobile Agent apps. Select whether to have the same or different landing pages for each of the mobile apps, based on the specific needs of your users.

![Landing page with a customized sign in button in the mobile app header.](../image/branded-landing-page.png "Branded landing page displaying the customized Sign in button in the header")

## Use case

A municipality home page contains a button to create a ticket, which navigates the user to complete a record in the  Now Mobile app. As this feature only works with a single instance, the system bypasses the need to select an instance and navigates the user directly to the login page. After logging in, the page to create a ticket displays.

Other examples of actions users can take after logging in include: sending a request, accessing personal information, or viewing a specific screen.

## Customize your mobile app login screen

By default, when a user logs in to a ServiceNow mobile app, the standard mobile app login screen displays. This login screen can be customized by using mobile publishing and mobile theming. For more information, see [Publish mobile apps with custom branding](mobile-publishing.md) and [Next Experience theming for mobile](explore-ne-theming.md).

![Default mobile app login screen.](../image/mobile-app-login.png "Default mobile app login screen")

