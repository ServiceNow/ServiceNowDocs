---
title: Software Asset Management Foundation dashboard
description: View compliance and true-up cost trend charts on the Software Asset Management Foundation dashboard.
locale: en-US
release: xanadu
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Management Foundation plugin classic, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Software Asset Management Foundation dashboard

View compliance and true-up cost trend charts on the Software Asset Management Foundation dashboard.

**Note:** The Software Asset Management Foundation dashboard is no longer available for new Xanadu users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Xanadu without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Xanadu. If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Xanadu but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard. If you activated the workspace plugin \(before or after upgrading to Xanadu, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

The Software Asset Management Foundation dashboard is accessed by navigating to **Software Asset** &gt; **Overview**. Click an element within a report to see more information, or add and move widgets as needed.

Results are updated daily, or whenever a new reconciliation result is available, and can be refreshed by clicking the **Refresh** icon for each result. You can also save charts in PNG or JPG formats.

The source for overview data is the Product Result \[samp\_product\_result\] table.

![Overview data on the Product Result table](../image/SAMOverviewSAMF.png)

|Report|Description|
|------|-----------|
|Publishers out of Compliance|Number of publishers that have at least one software model out of compliance.|
|Products out of Compliance|Number of products that have at least one software model out of compliance.|
|Total True-up Cost|Cost to be compliant based on the average prices in entitlements for the rights.|
|Top 10 Products by True-up Cost|Top 10 products graphed in order of true-up cost.|

**Parent Topic:**[Using Software Asset Management Foundation plugin classic](using-samf-classic.md)

