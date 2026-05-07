---
title: Engineering License Overview dashboard
description: Monitor and gain insights into your engineering applications license position and usage by viewing product usage reports in the Engineering License Overview dashboard.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics Solution for Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Engineering License Overview dashboard

Monitor and gain insights into your engineering applications license position and usage by viewing product usage reports in the Engineering License Overview dashboard.

**Note:** The Engineering License Overview dashboard is no longer available for new Australia users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Australia without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Australia.

-   If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Australia but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard.
-   If you activated the Software Asset Workspace \(sn\_sam\_workspace\) store application after upgrading to Zurich, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

The Engineering License Overview dashboard displays reports on normalized products and publishers that belong to engineering applications such as AutoCAD, GIS.

Access the Engineering License Overview Dashboard by navigating to **Software Asset** &gt; **Engineering License Overview**.

To narrow your results based on products or publishers across all tabs, use the filter in the left-hand corner of the dashboard. Only products and publishers that belong to engineering applications and are listed in the Engineering Application License \[samp\_eng\_app\_license\] table appear in the filter. If no product or publisher is selected, the tabs display the cumulative data for all products and publishers that belong to engineering applications.

The **Overview**, **License Usage Summary**, and **Denial Summary** tabs are updated daily or whenever a new reconciliation result is available. You can save charts in PNG or JPG formats for viewing them locally and for sharing.

## Overview tab

This tab gives an overview of the high-level metrics of all engineering applications. You can filter the results in this tab by various date options.

**Note:** The Date filter is not applicable to **Current Spend** and **Potential Savings**.

<table id="table_bl4_ktb_2jb"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current Spend

</td><td>

Product Result

 \[samp\_product\_result\]

</td><td>

Total cost of all entitlements for all products.

</td></tr><tr><td>

Potential Savings

</td><td>

License Dashboard Inventory \[license\_dashboard\_inventory\]

</td><td>

Cost saved if licenses are not being utilized to their potential or are under-utilized. To optimize your costs, you can reallocate those licenses or return the licenses and save the cost.

</td></tr><tr><td>

Top Used Products

</td><td>

Engineering Application Usage \[samp\_eng\_app\_usage\]

</td><td>

Top products that are being currently used. The number of days and hours being used per product also appears.

</td></tr><tr><td>

Top Active Users

</td><td>

Engineering Application Usage \[samp\_eng\_app\_usage\]

</td><td>

Top users who are currently using the product. The number of days and hours being used per user also appears.

</td></tr><tr><td>

Top Idle Users

</td><td>

Engineering Application Usage \[samp\_eng\_app\_usage\]

</td><td>

Top users who have requested a license but are not using the license. The number of days and hours of inactivity per user also appears.

</td></tr><tr><td>

Top Denied Products

</td><td>

Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Top products that are denied to users as these products have reached their peak concurrent usage.

</td></tr><tr><td>

Top Denied Users

</td><td>

Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

Top users that are denied licenses to products.

</td></tr><tr><td>

Product Usage by Location

</td><td>

Engineering Application Usage \[samp\_eng\_app\_usage\]

</td><td>

Based on the count of users using products by location.

</td></tr></tbody>
</table>## License Usage Summary tab

This tab lets you view data based on a license type \(floating, network, or token\). You can filter the data in this tab by date, license type, and license management server.

<table id="table_agx_mgc_2jb"><thead><tr><th>

Report

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

License Usage overtime

</td><td>

Engineering Application License \[samp\_eng\_app\_license\]

 Engineering Application Concurrent Usage \[samp\_eng\_app\_concurrent\_usage\]

 Engineering Application Denial \[samp\_eng\_app\_denial\]

</td><td>

The total number or quantity of all available licenses; not just the active products but all the products.

-   The blue line represents the total number of licenses allocated to a product or a publisher
-   The green line indicates the concurrent usage of the licenses.
-   The red line indicates denials or if and when the concurrent usage peaks.

</td></tr><tr><td>

License Inventory

</td><td>

Engineering Application License \[samp\_eng\_app\_license\]

</td><td>

All available licenses for a product or publisher.

</td></tr><tr><td>

License Server Statistics

</td><td>

Engineering Application License Server \[samp\_end\_app\_license\_server\]

</td><td>

All the license management servers that OpenLM or Open iT connect with.

</td></tr></tbody>
</table>## Denials Summary tab

You can filter the data in this tab by date, user, or user group.

|Report|Source table|Description|
|------|------------|-----------|
|Denials Over Time|Engineering Application Denial \[samp\_eng\_app\_denial\]|Denials for a product over a period of time.|
|Denials by Product|Engineering Application Denial \[samp\_eng\_app\_denial\]|The products that have been denied to users the most.|
|Denials by License Server|Engineering Application Denial \[samp\_eng\_app\_denial\]|The license servers that have been denied licenses to products the most.|

**Parent Topic:**[Platform Analytics Solution for Software Asset Management classic](../../../use/dashboards/application-content-packs/software-asset-mgmt-content-pack.md)

