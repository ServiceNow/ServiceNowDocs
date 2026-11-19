---
title: Data Catalog Analytics
description: Data Catalog Analytics shows how your organization uses Data Catalog and how well its metadata collectors are running, in dashboards inside Workflow Data Fabric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/data-catalog-analytics-overview-dc.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 2
breadcrumb: [Data Catalog, Workflow Data Fabric]
---

# Data Catalog Analytics

Data Catalog Analytics shows how your organization uses Data Catalog and how well its metadata collectors are running, in dashboards inside Workflow Data Fabric.

Data Catalog Analytics gives catalog administrators and data stewards a view of adoption and collector performance. Use it to see who is using the catalog and identify collectors that need attention. It appears as an icon in the sidebar of Workflow Data Fabric Home and opens a page with one tab for each dashboard.

## Dashboard tabs

Each tab focuses on a different area of catalog health.

-   [Adoption overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/adoption-overview-tab-dc.md) shows how many users have access to Data Catalog, how many are active, and how activity changes over time.
-   [Collector health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/collector-health-tab-dc.md) shows how many collector runs succeeded or failed, which collectors are active, and which collectors have not run recently.

## Dashboard access by role

Access depends on your role. Users without a listed role do not see the Data Catalog Analytics icon in the sidebar.

|Role|Adoption overview|Collector health|
|----|-----------------|----------------|
|admin|Yes|Yes|
|maint|Yes|Yes|
|df\_data\_steward|Yes|Yes|
|connection\_admin|Yes|Yes|
|wdf\_consumer|No|No|

On the Adoption overview tab, only users with the admin or maint role see real user names in the top active users tile. All other roles see anonymized names.

## Data range limit

**Note:** Platform Analytics limits the data in the dashboard widgets to the last 180 days. If your instance has the entitlement for extended data ranges, the widgets can show data older than 180 days. Check your entitlements to determine whether you have access to this capability.

-   **[Adoption overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/adoption-overview-tab-dc.md)**  
The Adoption overview tab shows how many users can use Data Catalog, how many are active, and how that activity trends over time.
-   **[Collector health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/collector-health-tab-dc.md)**  
The Collector health tab shows how often collectors run, how many runs fail, and which collectors have stopped running.
-   **[View catalog adoption and collector health data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/view-catalog-adoption-collector-health-dc.md)**  
Open Data Catalog Analytics, choose a dashboard tab, and set the filters to see adoption or collector data for the period you need.
-   **[Export data from a dashboard tile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/export-data-dashboard-tile-dc.md)**  
Download the data or an image of a single card or chart from the Adoption overview or Collector health tab.

**Parent Topic:**[Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog.md)

