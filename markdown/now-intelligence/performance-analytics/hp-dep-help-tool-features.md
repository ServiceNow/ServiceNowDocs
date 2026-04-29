---
title: Homepage deprecation help tool
description: Use the Homepage deprecation help tool to find all of your homepages in one place and convert them to dashboards, retire them, and restore retired homepages as dashboards.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Homepage deprecation, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Homepage deprecation help tool

Use the Homepage deprecation help tool to find all of your homepages in one place and convert them to dashboards, retire them, and restore retired homepages as dashboards.

To access the Homepage deprecation dashboard, navigate to **All** &gt; **Homepage deprecation help tool** &gt; **Overview**.

Before you use the homepage deprecation help tool, perform these two steps. A user with the admin role must change the system property. A user with the admin role or a user with both the dashboard\_admin and flow\_designer roles can populate the homepage migration status table.

1.  Disable the creation of new homepages: Set the system property **com.glideapp.home.deprecate\_homepages** to true.

    **Important:** When set to true, this property disables the creation of new homepages and sets the default start page or landing page to Dashboards. Menu items and URLs that open homepages will continue to point to those homepages. Otherwise, homepages are unavailable and should be migrated using this tool.

2.  [Populate the homepage migration status table](../task/hpm-populate-hp-status-table.md).

The Homepage deprecation dashboard has four tabs:

-   **Overview**

    The overview enables you to start the deprecation process and view the general status of the homepages on your instance.

-   **Personal homepages**

    A list of all the homepages that are owned by individuals who are inactive or locked out of the instance. Personal homepages are different than Global homepages, which are accessible to all users.

-   **Menus and Favorites**

    Lists of homepages that appear on configured menus and homepages that are marked as favorites by users. In the first case, you must reconfigure the menu item to point to the converted dashboard. In the second case, you must alert users to mark the new converted dashboard as a favorite.

-   **Usage**

    A list of all the homepages that have not been viewed in the last 30 days.


![Animated gif of homepage deprecation dashboard that scrolls through all four tabs](../image/hp-dep-db-overview.gif "Homepage deprecation dashboard")

## Overview tab

The **Overview** tab includes links for getting started and several reports that enable you to choose homepages that need attention.

In the **How to start** section, admins have links to disable creation of new homepages and to populate the homepage migration status table.

|Report|Type|Description|
|------|----|-----------|
|Homepages not deprecated|![](../../reporting/image/icon-single-score-report-p.png) Single score|Number of homepages that you have not converted or retired. Select this report to see the associated homepages on the [Homepage migration status table](../concept/homepage-migration-status-table.md).|
|Converted homepages|![](../../reporting/image/icon-single-score-report-p.png) Single score|Number of homepages that you’ve converted to responsive dashboards. Select this report to see the associated homepages on the [Homepage migration status table](../concept/homepage-migration-status-table.md).|
|Retired homepages|![](../../reporting/image/icon-single-score-report-p.png) Single score|Number of homepages that you’ve retired. Select this report to see the associated homepages on the [Homepage migration status table](../concept/homepage-migration-status-table.md).|
|Restored homepages|![](../../reporting/image/icon-single-score-report-p.png) Single score|Number of retired dashboards that you’ve restored as responsive dashboards. Select this report to see the associated homepages on the [Homepage migration status table](../concept/homepage-migration-status-table.md).|
|Assigned to users|![](../../reporting/image/icon-bar-report-p.png) Bar report|Homepages that are assigned to users. The bar labeled **empty** accounts for homepages that don’t have any assigned users. Select any bar in this report to see the associated homepages on the [Homepage migration status table](../concept/homepage-migration-status-table.md).|
|Assigned to groups|![](../../reporting/image/icon-bar-report-p.png) Bar report|Homepages that are assigned to groups. The bar labeled **empty** accounts for homepages that don’t have any assigned groups. Select any bar in this report to see the associated homepages on the [Homepage migration status table](../concept/homepage-migration-status-table.md).|
|All converted homepages from app and other actions|![](../../reporting/image/icon-list-report-p.png) List report|All dashboards that have been converted from homepages, whether in the help tool, or by other means.|

## Personal homepages

This tab shows a list of the homepages whose owners are inactive or otherwise locked out. These homepages may be good candidates for retirement. Select the link to open a filtered list containing only the personal homepages to retire or convert them.

## Menus and Favorites

The Menus and Favorites tab has three lists.

-   **Homepages connected to menus**

    Shows the homepages that are connected to menus in the filter navigator. When you convert or retire these homepages, you must point the menu item to the converted dashboard or remove the menu item.

-   **Homepages connected to favorites**

    Shows homepages that users identify as a favorite. When you convert or retire these homepages, tell them that they should mark the converted dashboard as a favorite.

-   **Menus and Modules connected to Homepages**

    Shows homepages that appear in the filter navigator as either menu items or modules. Edit the menu and module items to open the converted dashboard. Remove menu or module items that open retired homepages.


## Usage

The Usage tab shows a list of all homepages not viewed in the last 30 days. These homepages may be good candidates for retirement.

