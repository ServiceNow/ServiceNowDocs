---
title: View catalog adoption and collector health data
description: Open Data Catalog Analytics, choose a dashboard tab, and set the filters to see adoption or collector data for the period you need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/view-catalog-adoption-collector-health-dc.html
release: brazil
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Data Catalog Analytics, Data Catalog, Workflow Data Fabric]
---

# View catalog adoption and collector health data

Open Data Catalog Analytics, choose a dashboard tab, and set the filters to see adoption or collector data for the period you need.

## Before you begin

Data Catalog is installed.

Role required: admin, maint, df\_data\_steward, or connection\_admin.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  In the left sidebar, select the **Data Catalog Analytics** icon.

3.  Select a tab: **Adoption overview** or **Collector health**.

4.  In the **Time range** list, select the period to show.

    To see how current the data is, select the information icon next to **Time range**.

5.  Choose a second filter.

    -   On **Adoption overview**, select a role in the **Role** list.
    -   On **Collector health**, select a collector in the **Configuration** list.
6.  Select the information icon on the tile to see what it counts.

7.  Select **Refresh** to reload the data on every chart and table on the tab.


## Result

The cards, charts, and tables on the tab update to match the filters. On **Adoption overview**, selecting a role limits every tile to users with that role. The tab opens on the last 30 days with all roles or all configurations until you change the filters. The collector freshness table does not change with the time range.

**Note:** Platform Analytics limits the data in the dashboard widgets to the last 180 days. If your instance has the Platform Analytics Premium entitlement, the widgets can show data older than 180 days. Without that entitlement, the widgets do not show data older than 180 days, including when you select a longer time range.

For what each tab shows, see [Adoption overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/adoption-overview-tab-dc.md) and [Collector health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/collector-health-tab-dc.md).

**Parent Topic:**[Data Catalog Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-analytics-overview-dc.md)

