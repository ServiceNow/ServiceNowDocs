---
title: Collector health tab
description: The Collector health tab shows how often collectors run, how many runs fail, and which collectors have stopped running.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/collector-health-tab-dc.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 4
breadcrumb: [Data Catalog Analytics, Data Catalog, Workflow Data Fabric]
---

# Collector health tab

The Collector health tab shows how often collectors run, how many runs fail, and which collectors have stopped running.

Use this tab to find collectors that fail or have stopped running so you can fix them before catalog metadata becomes outdated. The tab has two filters. **Time range** offers **last 7 days**, **last 30 days**, **last 90 days**, **last 1 year**, and **all time**. **Configuration** offers all configurations or a single collector. The default is the last 30 days across all configurations. Both filters apply to every card, chart, and table except the freshness table, which ignores the ti me range.

\[Omitted image "dc-analytics-collector-health.png"\] Alt text: Collector health tab showing run summary cards, date charts, and freshness table

## Cards, charts, and tables

|Card|Definition|
|----|----------|
|Total collector runs|Collector runs that finished in the selected time range, whether they succeeded or failed. The change compares with the previous range of the same length.|
|Collector success rate|The percentage of runs that finished in the selected time range and succeeded. The card is blank when no runs finished. The change compares with the previous range of the same length, in percentage points.|
|Failed collector runs|Collector runs that finished with an error in the selected time range. The change compares with the previous range of the same length.|
|Active collectors|The number of configurations with at least one finished run in the selected time range. When you select a single configuration, the card shows 1 if it ran and 0 if it did not. The change compares with the previous range of the same length.|
|Failed collector runs by date|A stacked column chart of runs that finished with an error on each day of the time range, with one segment for each configuration. Deactivated configurations do not appear.|
|Successful collector runs by date|A stacked column chart of runs that succeeded on each day of the time range, with one segment for each configuration. Deactivated configurations do not appear. A configuration keeps the same color in both date charts.|
|Runs by collector|A stacked bar chart of succeeded and failed runs for each configuration, for runs that finished in the time range. A configuration with no runs shows an empty row. Deactivated configurations do not appear, so the bars can add up to less than the Total collector runs card.|
|Collector status|One row for each active collector that shows its current state. The time range does not apply. The status comes from the collector's last finished run: **Error** if it failed, **Needs attention** if it never ran or last succeeded more than 7 days ago, and **OK** otherwise.|
|Collector run history|Collector runs that finished from the first day of the selected time range through now, plus any run still in progress. Test \(dry\) runs do not appear.|

## Collector freshness

This table lists each active collector with six columns: status, collector, last run status, last run, last successful run, and the time of the last successful run. The last run status is **Success**, **Error**, or **Running**. You can search for a collector by name. The status is one of the following:

-   **Error**: the collector's last finished run failed.
-   **Needs attention**: the collector has never run, or its last successful run was more than seven days ago.
-   **OK**: the collector meets neither condition.

## Collector run history

This table lists collector runs, newest first, 10 at a time with page controls and a setting for records per page. It has the following columns: collector, status, start, end, duration, assets, reason, message, and recommended action. The status is **Running**, **Success**, or **Error**. For a failed run, the reason, message, and recommended action explain what went wrong and what to do. Filter by status or reason, search messages, and sort on any column. Sorting on computed columns and filtering by failure reason apply to the newest 5,000 runs, and the table tells you when the time range contains more.

## How current the data is

Cards and charts show data through the previous day in UTC. The freshness and run history tables show data through the current time. The information icons next to **Time range** and on each table show which dates apply.

To change the filters, see [View catalog adoption and collector health data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/view-catalog-adoption-collector-health-dc.md). To download tile data, see [Export data from a dashboard tile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/export-data-dashboard-tile-dc.md).

**Parent Topic:**[Data Catalog Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-analytics-overview-dc.md)

