---
title: Mobile application management \(MAM\) integration
description: Use Microsoft Intune or BlackBerry Dynamics to secure and protect sensitive information in mobile applications, even in cases where customers use their own mobile devices.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile application management \(MAM\) integration

Use Microsoft Intune or BlackBerry Dynamics to secure and protect sensitive information in mobile applications, even in cases where customers use their own mobile devices.

Use Microsoft Intune or BlackBerry Dynamics mobile management tools to control, secure, and enforce policies for ServiceNow mobile apps. These tools provide a central point of control for securing your data on mobile apps, even in scenarios where you are not the owner of the mobile device.

These apps are available in the Apple App store, Google Play, and BlackBerry marketplace stores. Get started right away using these publicly available apps, or request custom branded versions of these apps with your unique company identity.

<table id="table_ezv_ksx_qlb"><thead><tr><th>

MAM Platform

</th><th>

Mobile Agent

 Availability

</th><th>

Now Mobile

 Availability

</th></tr></thead><tbody><tr><td>

Microsoft Intune

</td><td>

Available in Madrid and later releases.

</td><td>

Available in New York and later releases.

</td></tr><tr><td>

BlackBerry Dynamics

</td><td>

Available in Madrid and later releases.

</td><td>

Available in New York and later releases.

</td></tr></tbody>
</table>## Microsoft Intune

**Important:**

Microsoft requires iOS Intune apps to be registered with Microsoft Entra ID \(formerly Microsoft Entra ID\) in the second half of the calendar year 2024. Apps that are not registered will fail the Microsoft Intune login flow.

What this means for publicly distributed and privately distributed iOS Intune apps:

-   Publicly distributed iOS apps must be registered in your Microsoft tenant after the build is created and before distribution of the app.
-   Privately distributed iOS apps must get your Microsoft Entra ID administrator's consent. This can be done at any point in the app build process, but must be done before distribution of the app.

For more information, see the following resources:

-   [Microsoft website explaining the requirement and the timeline](https://learn.microsoft.com/en-us/mem/intune/fundamentals/whats-new#wrapped-ios-apps-and-ios-apps-using-the-intune-app-sdk-will-require-azure-ad-app-registration).
-   [Microsoft Entra ID App Registration Mandate for iOS Intune Mobile Apps - Mobile Publishing \(KB1640759\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1640759). \(You must have an account and log in to view this ServiceNow KB.\)

Take advantage of the policy enforcement and management features of Microsoft Intune for your ServiceNow mobile apps.

ServiceNow provides versions of the Mobile Agent and Now Mobile apps designed to integrate with your Microsoft Intune mobility management tools.

![App logos for ServiceNow mobile apps for Microsoft Intune.](../image/ms-intune-app-logos.png "App logos for ServiceNow mobile apps for Microsoft Intune")

Using these apps, you can set and manage policies for each app using your organizations Intune administration portal. The following mobile application management features are supported:

-   App protection without device enrollment​​
-   Restrict copy/paste
-   Attachment Control
-   Remote wipe
-   MSFT conditional access

## BlackBerry Dynamics

Manage your ServiceNow mobile apps using your organization's BlackBerry Dynamics mobility management tools.

ServiceNow provides versions of the Mobile Agent and Now Mobile apps designed to integrate with your BlackBerry Dynamics mobility management tools. BlackBerry versions of ServiceNow are available in the BlackBerry marketplace store.

![App logos for ServiceNow mobile apps for BlackBerry Dynamics.](../image/bb-dynm-app-logos.png "App logos for ServiceNow mobile apps for BlackBerry Dynamics")

Using these apps, you can set and manage policies for each app using the BlackBerry Dynamics SDK. The following mobile application management features are supported:

Your branded apps are integrated with the BlackBerry Dynamics SDK to help manage policy enforcement and employee access to your data. The following mobile application management features are supported:

-   App protection without device enrollment
-   Restrict copy/paste
-   Attachment Control
-   Remote wipe
-   Dynamic VPN

## Package and Bundle IDs

To enforce app policies your mobile application management software may require the bundle or package ID associated with the mobile apps. For information on these IDs see [Bundle and Package IDs for ServiceNow mobile apps](../reference/sg-mobile-package-ids.md).

