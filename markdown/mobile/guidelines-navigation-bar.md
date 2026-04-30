---
title: General guidelines for a navigation bar
description: When creating a navigation bar, keep these general guidelines in mind for usability and a good user experience.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Navigation bar, Mobile app components, Building mobile apps, Mobile Platform]
---

# General guidelines for a navigation bar

When creating a navigation bar, keep these general guidelines in mind for usability and a good user experience.

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


