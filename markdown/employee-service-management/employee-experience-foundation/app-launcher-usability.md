---
title: Cross-channel favorites
description: Cross-channel favorites capability provides quick access to the content the employees use frequently and offers extensibility for BUs.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Cross-channel favorites

Cross-channel **favorites** capability provides quick access to the content the employees use frequently and offers extensibility for BUs.

Employees can view and access their favorited content directly from the **My Favorites** widget on the Employee Center home page or from the **My Favorites** link on the global navigation bar.​

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

**Note:** To change the icon, go to **Service Portal** &gt; **Portals** &gt; **Employee Center** &gt; **Quick start config**, and update the icon.

## My Favorites

You can access all your favorite items on the widget from **My Favorites** of the Employee Center home page header.​ Browse the list of your favorites, sort by date or recency, and see card view and list view.

The **My Favorites** widget appears only when you mark some content as your favorite. However, you can show the empty favorites widget on the home page when you select **Show empty state** from the instance options.

## Favorites sorting

You can configure the sort order of the favorited items using instance options. On configuration, your employees can sort the favorites from the favorites section in one of the following ways:

-   **Recently Accessed**
-   **Date Added \(newest\)**
-   **Date Added \(oldest\)**

To fix issues with alphabetical sort order of favorites, see [KB1348001](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1348001).

## Favorites and topic security

You can configure user permissions such as **Available for** and **Not Available for**. When the favorited topic is not marked available for the user, the topic isn't visible from **My Favorites** and on the favorites widget.

For more information, see [Enable user criteria for topics](../task/enable-user-criteria-topics.md).

## Favorites troubleshooting

Follow these steps to troubleshoot issues with **Favorites**:

-   For upgrades, you can allow the RCAs related to favorites.
-   Ensure you install and update the latest plugins.
-   On the sp\_portal table, set **Enable favorite** value to **True**.
-   Remember, any customizations may impact the display and functionality of the favorites.
-   Favorite applications cannot be viewed from Now Mobile.

**Related topics**  


[Configure favorites option](../task/web-configure-favorites-admin.md)

[Manage favorites](../task/web-configure-favorites-employee.md)

