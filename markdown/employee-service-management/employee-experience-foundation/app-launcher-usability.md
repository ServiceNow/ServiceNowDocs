---
title: Cross-channel favorites
description: Cross-channel favorites capability provides quick access to the content the employees use frequently and offers extensibility for BUs.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-04-15"
reading_time_minutes: 2
breadcrumb: [Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Cross-channel favorites

Cross-channel **favorites** capability provides quick access to the content the employees use frequently and offers extensibility for BUs.

Employees can view and access their favorite content directly from the **My Favorites** widget on the Employee Center home page or from the **My Favorites** link on the global navigation bar.​

By default, favorites \(sp\_favorite\) are enabled for Employee Center and MESP portals​ for **Requests**, **Articles**, and **Applications** content types.

**Note:** The **Favorites** option for **Applications** is available to only EC pro customers as **App launcher** is an EC Pro feature.

Employees can see the favorites icon on the following types of pages or sections:

-   Topic page
-   Catalog page detail view
-   Knowledge page detail view
-   Service catalog page
-   My applications page
-   My applications widget
-   Recommended for you widget

You can set up the favorite card details and use the default favorite icon ![default favorite icon default without selection](../images/myfav-no-selection.jpg) to bookmark content as your favorites. When your employees mark content as favorites, the favorite icon appearance changes to ![default favorite icon default with selection](../images/myfav-selection.jpg).

**Note:** To change the icon, go to **Service Portal** &gt; **Portals** &gt; **Employee Center** &gt; **Quick start configuration**, and update the icon.

## My Favorites

You can access all your favorite items on the widget from **My Favorites** of the Employee Center home page header.​ Browse the list of your favorites, sort by date or recently, and see card view and list view.

The **My Favorites** widget appears only when you mark some content as your favorite. However, you can show the empty favorites widget on the home page when you select **Show empty state** from the instance options.

**Note:** The my **Favorites** widget syncs instantly with other widgets in real-time on the web. However, when adding favorites items across devices \(example: mobile to the web\), a manual refresh is required to reflect the latest changes — **Reload the page** on web or **Pull to refresh** on mobile.

## Favorites sorting

You can configure the sort order of the favorite items using instance options. On configuration, your employees can sort the favorites from the favorites section in one of the following ways:

-   **Recently Accessed**
-   **Date Added \(newest\)**
-   **Date Added \(oldest\)**

To fix issues with alphabetical sort order of favorites, see [KB1348001](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1348001).

## Favorites and topic security

You can configure user permissions such as **Available for** and **Not Available for**. When the favorite topic is not marked available for the user, the topic isn't visible from **My Favorites** and on the favorites widget.

For more information, see [Enable user criteria for topics](../task/enable-user-criteria-topics.md).

## Favorites troubleshooting

Follow these steps to troubleshoot issues with **Favorites**:

-   For upgrades, you can see the RCAs related to favorites.
-   Confirm you install and update the latest plugins.
-   On the sp\_portal table, set **Enable favorite** value to **True**.
-   Remember, any customizations may impact the display and functionality of the favorites.
-   Favorite applications cannot be viewed from Now Mobile.

**Related topics**  


[Configure favorites option](../task/web-configure-favorites-admin.md)

[Manage favorites](../task/web-configure-favorites-employee.md)

