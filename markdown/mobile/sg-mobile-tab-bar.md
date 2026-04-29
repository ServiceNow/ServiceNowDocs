---
title: Navigation bar
description: User the navigation bar in your mobile apps to access launcher screens, screens, settings, and notifications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile app components, Building mobile apps, Mobile Platform]
---

# Navigation bar

User the navigation bar in your mobile apps to access launcher screens, screens, settings, and notifications.

<table id="table_pll_qnn_rhb"><tbody><tr><td>

![Navigation bar component hierarchy.](../image/navigation-bar-image.png "Navigation bar component hierarchy")

</td><td>

The navigation bar consists of these components:

-   Navigation bar
-   Navigation bar tabs
-   Screen tab
-   Launcher tab
-   Saved tab
-   Notification tab
-   Settings tab

</td></tr><tr><td>

![Navigation bar tabs with More tab](../image/nav-bar-tabs.png)

</td><td>

The navigation bar appears at the bottom of each mobile app. You can create navigation bar tabs in the navigation bar. Users can access launcher screens and regular screens within the navigation bar.

 **Note:** The navigation bar in each mobile app is preconfigured with **Notifications** and **Settings** navigation bar tabs. For more information about the content of these tabs, see [Mobile app structure](mobile-layout.md). There is also a saved tab, which displays a page showing the user's saved records.

</td></tr><tr><td>

![List displayed after a user taps the More tab](../image/nav-bar-more-tab.png)

</td><td>

When you add more than five tabs to the navigation bar, a **More** \(![More icon](../image/more-icon.png)\) tab displays. Tap the **More** tab to open a list view showing the additional tabs.

</td></tr></tbody>
</table>## Screen tabs and launcher screen tabs

<table id="table_gn5_dlk_llb"><tbody><tr><td>

![Screen navigation tab](../image/applet-nav-tab.png "Screen navigation tab")

</td><td>

Use a screen tab to enable access directly to a calendar, custom map, list, map, or mobile web screen.

</td></tr><tr><td>

![Launcher screen navigation tab](../image/applet-launcher-nav-tab.png "Launcher screen navigation tab")

</td><td>

Use a launcher screen tab to enable users to access elements in a screen launcher.

 Launcher screens are dashboards. They provide shortcuts to other screens and information. Shortcuts can be added with icons, cards, media sections, or score counts.

</td></tr></tbody>
</table>## General guidelines for the navigation bar

Consider these general guidelines when configuring your navigation bar.

-   **Number of tabs**
    -   The navigation bar displays up to five tabs. When there are more than five tabs an overflow tab, known as the more tab, \(![More icon.](../image/more-icon.png)\) is added.
    -   Try to limit your navigation bar to five tabs, so that all the tabs are visible at all times.
-   **Tab types**
    -   By default, the navigation bar contains Settings and Notification tabs. Removing these tabs is possible, but might prevent your users from accessing important information and features of the app.
    -   Rather than removing the Setting and Notification tabs, consider changing the order in which they appear in the navigation bar.
    -   The Settings, Notifications, and Saved tabs navigate to specific pages, so only one of each tab is required. You can use multiple screen and launcher screen tabs, however it's suggested that you use no more than five tabs.
-   **Display specific tabs to specified users**
    -   Apply user criteria permissions, so users only view tabs relevant to their work. For more information, see [User criteria permissions in mobile apps](user-criteria-permissions.md).
    -   You should have the Settings and Navigation tabs available to users.
-   **Tab names**
    -   Give your navigation tabs a descriptive name that provides context. Avoid generic names like Home or Apps.
    -   Use capital letters for your titles to make them stand out. For example, Open Tasks.
-   **Length of tab names**
    -   Limit the length of your titles so they aren't cut off when displayed in the navigation bar.
    -   If you support multiple languages, consider the length of titles in each of the languages you support.
    -   When testing your application, look out for titles that don't fully display in the navigation bar.
-   **Icon composition**
    -   The navigation bar icon color is determined by your application’s theme.
    -   Select icons that are visually consistent and best represent the functions or information presented in that part of your application.
    -   Avoid using the same icon for more than one navigation tab, so users can quickly find what they need.
-   **Ordering**

    The order of the tabs should be listed in the level of importance. This order varies for left-to-right languages and right-to-left languages.


