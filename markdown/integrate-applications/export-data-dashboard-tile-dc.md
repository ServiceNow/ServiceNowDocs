---
title: Export data from a dashboard tile
description: Download the data or an image of a single card or chart from the Adoption overview or Collector health tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/export-data-dashboard-tile-dc.html
release: brazil
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Data Catalog Analytics, Data Catalog, Workflow Data Fabric]
---

# Export data from a dashboard tile

Download the data or an image of a single card or chart from the Adoption overview or Collector health tab.

## Before you begin

You can open the tab that contains the tile. See [Data Catalog Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-analytics-overview-dc.md).

Role required: admin, maint, df\_data\_steward, or connection\_admin.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  In the left sidebar, select the **Data Catalog Analytics** icon.

3.  Select a tab: **Adoption overview** or **Collector health**.

4.  Set the filters so the tile shows the data to export.

5.  On the tile, select the **three-dot menu**.

6.  Under **Export as**, select a format.

    -   On a chart, select **CSV**, **JPEG**, **PNG**, or **Excel \(.xls\)**.
    -   On a card, select **CSV** or **Excel \(.xls\)**.

## Result

The browser downloads a file in the format you select.

The same menu has a **Refresh** option that reloads the tile's data.

Export is available on cards and charts only. The collector freshness, collector run history, and top active users tables don't have an export option.

**Parent Topic:**[Data Catalog Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-analytics-overview-dc.md)

