---
title: Adoption overview tab
description: The Adoption overview tab shows how many users can use Data Catalog, how many are active, and how that activity trends over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/adoption-overview-tab-dc.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 4
breadcrumb: [Data Catalog Analytics, Data Catalog, Workflow Data Fabric]
---

# Adoption overview tab

The Adoption overview tab shows how many users can use Data Catalog, how many are active, and how that activity trends over time.

Use this tab to see whether people are using the catalog after setup. The tab has a **Time range** filter and a **Role** filter. **Time range** offers **last 7 days**, **last 30 days**, **last 90 days**, **last year**, and **all time**. The default is the last 30 days across all roles. The time range sets the period for the trend charts and the top active users tile, and for the change shown on each tile. It does not change user counts such as provisioned, activated, and monthly active users. The role filter limits every tile on the tab to users with the selected role. For example, when you select **Connection Admin**, the **Users by role** chart shows only that role.

\[Omitted image "dc-analytics-adoption-overview.png"\] Alt text: Adoption overview tab showing user activity tiles and trend charts

## What counts as an active user

Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing the Data Catalog Analytics dashboard does not count. Every activity-based tile on this tab uses this definition.

## Tiles and charts

|Tile|Definition|
|----|----------|
|Total provisioned users|Users who currently hold at least one Data Catalog role: data steward, connection admin, or consumer. The time range does not change the count. The change compares with the value on the first day of the range.|
|Activated users|Users who have been active in Data Catalog on at least one day. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count. The time range does not change the count. The change compares with the value on the first day of the range.|
|Monthly active users|Distinct users active in Data Catalog in the last 30 days, whatever time range is selected. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count. The change compares with the same 30-day count on the first day of the range.|
|WAU / MAU ratio|Weekly active users \(last 7 days\) as a percentage of monthly active users \(last 30 days\), as of the latest data. A higher value means people come back more often. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count. The time range does not change the ratio. The change compares with the value on the first day of the range.|
|Daily active users|A line chart of distinct users active in Data Catalog on each day of the time range. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count.|
|Weekly active users|A line chart that shows, for each day of the time range, the distinct users active in Data Catalog in the 7 days up to that day. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count.|
|Monthly active users|A line chart that shows, for each day of the time range, the distinct users active in Data Catalog in the 30 days up to that day. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count.|
|WAU / MAU|For each day of the time range, weekly active users as a percentage of monthly active users. A higher value means people come back more often. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count.|
|Users by role|A donut chart of users who currently hold each Data Catalog role. The time range does not change the chart. A user with more than one role counts once in each.|
|Top active users|Users ranked by how many days they were active in Data Catalog during the selected time range. Active days appear as days active out of the days in the range. Users are active on a day when they run a search, open a search result, or open a Data Catalog page. Viewing this dashboard does not count. Real usernames appear only to admin and maint users.|

The top active users table has three columns: rank, user, and active days. Active days appear as days active out of the days in the time range, such as 14/30 for a 30-day range.

Each tile has an information icon that describes what it counts and how the time range applies.

## How current the data is

The information icon next to **Time range** shows the date that all tiles on the tab report through. This is the oldest latest score across the six indicators on the tab.

To change the filters, see [View catalog adoption and collector health data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/view-catalog-adoption-collector-health-dc.md). To download tile data, see [Export data from a dashboard tile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/export-data-dashboard-tile-dc.md).

**Parent Topic:**[Data Catalog Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-analytics-overview-dc.md)

