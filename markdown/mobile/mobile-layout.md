---
title: Mobile app structure
description: Learn how components and settings are organized within ServiceNow mobile apps to understand how to find the tools and data you're looking for.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Using the mobile apps, Mobile Platform]
---

# Mobile app structure

Learn how components and settings are organized within ServiceNow® mobile apps to understand how to find the tools and data you're looking for.

## Components of a ServiceNow app

![Mobile diagram placeholder image.](../image/mobile-components-large.png)

## App Icons

<table id="table_mj1_gtk_cjb"><tbody><tr><td>

Each ServiceNow app has its own icon on your mobile device. You can configure your apps to show a badge indicating the number of unread notifications you have in the app.

 **Note:** If your company has provided you with branded ServiceNow mobile apps, your icons may not match the image shown here.

</td><td>

![Mobile app icons with badges](../image/mobile-app-icons.png)

</td></tr></tbody>
</table>## Navigation bar

<table id="table_o2c_ttk_cjb"><tbody><tr><td>

![Navigation bar tabs with More tab.](../image/nav-bar-tabs.png)

</td><td>

Each ServiceNow app displays a navigation bar along the bottom of the screen. This bar displays icons called tabs, which you can use to access settings, notifications and commonly used screens or launcher screens.

 Your administrator selects which tabs appear in the navigation bar, and the order in which they appear. If a navigation bar has six or more icons, a **More** \(![More icon.](../image/more-icon.png)\) tab displays. Tap the **More** tab to see the additional tabs in a list format.

 For information on navigation bar configuration, see [Navigation bar](sg-mobile-tab-bar.md).

</td></tr></tbody>
</table>## Launcher screens

<table id="table_llw_b5k_cjb"><tbody><tr><td>

Launcher screens serve as a landing page or a home page. Using a launcher screen, you can access other screens in various formats, as well as search, do quick actions, and find user information.

 -   **Header**

The header of the launcher screen defines how the title of the screen appears and what information is shown in the header. For more details on configuring headers, see [Configure a launcher screen header](../task/create-alp-header.md).

-   **Search**

Use global search to search through defined search sources configured on your instance. For more details, see [Global search for mobile](mobile-search-config.md).

-   **UI sections**

UI sections appear as containers within launcher screens. Within sections, you can see other screens, analytics previews, record information, and more. For more details on these sections, see [Launcher screen UI sections](alp-ui-sections.md).

-   **Quick Actions**

Quick actions are a way to access commonly used functions, such as transferring records or using a template in the mobile app. For more details on quick actions, see [Quick actions](../task/sg-config-quick-actions.md).


 For more information on launcher screens configuration, see [Launcher screens](sg-mobile-applet-launcher.md).

</td><td>

![Application launcher in the Mobile Agent app.](../image/applet-launcher-generic.png)

</td></tr></tbody>
</table>## Settings

<table id="table_uzb_rvk_cjb"><tbody><tr><td>

![Mobile navigation bar with notification badge](../image/mobile-settings-screen.png)

</td><td>

Use the settings screen to configure multiple options and review information about the app. The settings page is accessed from the Settings tab on the navigation bar. The following are examples of available options. These options may vary according to the operating system you use.

-   **Header**

The header displays the name of the logged-in user and last login time and date.

-   **Instance**

Tap to view the ServiceNow instance you're currently using, and the instances that are available to you. For more information, see [Working with instances](instances-concept.md).

-   **Location tracking**

Option to enable location tracking. Location tracking keeps a record of your location either for a defined period or while performing actions.

For more information, see [Using location tracking for mobile](mobile-location.md). For information on location tracking configuration, see [Location tracking for mobile](mobile-location-tracking.md).

-   **Offline**

Tap to open the offline mode page. Here you can select to work offline and to download the cache.

For more information about working in offline, see [Offline mode for mobile](offline-end-user.md). For information about offline configuration, see [Offline mode](mobile-offline-mode.md).

-   **Preferences**

Tap to list additional settings. For example, languages, enable push notifications, themes, analytics, and banners.

    -   Language: Tap to display the Language page, where you can select a language for your ServiceNow mobile app. For more information, see [Languages on your mobile device](display-language.md).
    -   Notification: Option to enable push notifications on your mobile device. For more information, see [Enable notification settings for mobile](../task/notification-preference-settings.md).
    -   Security: Tap to display the option to set up an app PIN. For more information, see [App PIN settings for mobile](mobile-app-pin-settings.md).
    -   Theme: Option to enable the dark theme or the default theme on your mobile app. For more information. see [Enable dark theme](../task/enable-dark-theme.md).
    -   Start my week: Option to select which day to allocate as the start of your week.
    -   Analytics: Enable analytics tracking for your mobile app journey. For more information about analytics settings, see [Analytics settings for mobile](mobile-analytics-settings.md).
    -   Banners: Tap to open the Banners page. Within the page, select the number of seconds a banner displays. You can also select whether to group multiple messages. For more information, see [Define notification banner display time](../task/banner-display.md).
    -   Chart accessibility: Select whether to display data analytics views in color or black and white patterns. For more information, see [Change mobile analytics views for accessibility](../task/accessibility-chart-view.md).
    -   Swipe from edge: For Android devices that have the option to swipe a screen from the side of the device.
-   **Legal**

Tap to view the apps legal disclosures and privacy policy.

-   **Give feedback**

Tap to provide feedback on your ServiceNow mobile app experience. For more information, see [Mobile app feedback](feedback-mobile-app.md).

-   **Version**

The version of the mobile app on your mobile device.

-   **Log out**

Tap to log out of the connected ServiceNow instance.


</td></tr></tbody>
</table>## Notifications

<table id="table_jrw_svk_cjb"><tbody><tr><td>

The notifications page is accessed from the **Notifications** tab on the navigation bar. This page displays push notifications sent to you. Tap any notification to view its contents.

 Notifications that are defined by the administrator as critical are flagged with the words Critical Alert. This type of notification helps you to prioritize which ones should be addressed first.

 Unread notifications are marked with a blue dot in the margin and the title is bold. Swipe left to reveal the option to delete the message. Swipe right to reveal the option to mark the message as read/unread.

 You can mark all notifications as read or delete all notifications by tapping on the more menu \(![More icon.](../image/IconAppMenuAndroid.png)\) and selecting the appropriate option.

 For more information on notifications, see [Mobile notifications](mobile-notifications.md), [Handling mobile alerts](../task/mobile-alerts-using.md), and [Enabling critical alerts](../reference/critical-alert-enable.md).

 For information on mobile notification configuration, see [Mobile push notifications](sg-mobile-push-notifications.md).

</td><td>

![Application launcher in the Mobile Agent app.](../image/mobile-notif-screen.png)

</td></tr></tbody>
</table>## Screens

Examples of screen types that you can view on your mobile device.

![Mobile screen examples.](../image/mobile-applet-examples.png)

Screens within your mobile apps are designed for specific tasks. The template may include other optional screens that you can access for additional information. All screens display information that is based on records in a data item.

-   **Segments**

    Screens can contain one or more segments, which display information from a specific data item. If a screen has more than one segment, you're able to switch between segments using a tabbed interface.

-   **Embedded screens**

    Within a record screen, you might see one or many embedded screens. An embedded screen could be a details screen, an activity stream screen, a related list screen, or an embedded list screen.

-   **Functions**

    Screens can be associated with one or more functions. Access these functions through the top menu or swipe actions. Use functions to perform tasks relating to the current record, or navigate to another screens, launcher screens, or external resources.


For more information on screens and how to configure them, see [Mobile screen types](sg-mobile-applet.md).

**Related topics**  


[Mobile hierarchy](mobile-hierarchy.md)

[Navigation bar](sg-mobile-tab-bar.md)

[Launcher screens](sg-mobile-applet-launcher.md)

[Mobile screen types](sg-mobile-applet.md)

