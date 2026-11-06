---
title: IT Agent dashboard for Service Operations Workspace
description: The dashboard displays the closed incidents that belong to you and your assignment groups through personalized metric visualizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/it-agent-dashboard-sow.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Platform Analytics ITSM Dashboards, IT Service Management]
---

# IT Agent dashboard for Service Operations Workspace

The dashboard displays the closed incidents that belong to you and your assignment groups through personalized metric visualizations.

Navigate to **Workspaces** &gt; **Service Operations Workspace**.

Select the Dashboard icon \[Omitted image "dashboard-icon-sow.png"\] Alt text: Dashboard icon to view the dashboard.

Procure the ITSM Pro package subscription to get additional performance analytics features.

For more information on performance analytics subscription, see [Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/c_PremiumPerformanceAnalytics.md).

You can monitor data by any of the following time aggregations.

-   **Weekly**: View the data aggregated weekly. For counts, this data is the weekly sum of the daily values. For percentages, this data is the weekly average of the daily percentages.
-   **Monthly**: View the data aggregated monthly. For counts, this data is the monthly sum of the daily values. For percentages, this data is the monthly average of the daily percentages.
-   **Quarterly**: View the data aggregated quarterly. For counts, this data is the quarterly sum of the daily values. For percentages, this data is the quarterly average of the daily percentages.
-   **Yearly**: View the data aggregated yearly. For counts, this data is the yearly sum of the daily values. For percentages, this data is the yearly average of the daily percentages.

After you set the time aggregation, all scorecards show the data for that period.

You can also view the summary for **Today**, **Yesterday**, **Last 6 months**, and **Custom range** time periods.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|itil|View only the incidents in the base system. A user with the itil role can also view the metrics related to change, problem, and request if the administrator configures them in the Service Operations Workspace.|

## Data visualizations

|Title|Description|
|-----|-----------|
|Average resolution time|Average resolution time of resolved incidents|
|Closed incidents|Number of closed incidents is measured daily|
|Incidents that missed SLA|Number of incidents that missed the SLA is measured daily|
|Percent of incidents resolved without reassignment|Percentage of incidents resolved by first assigned group|
|Average age of open incidents|Average age of open incidents|
|Percent of incidents resolved on same day opened|Percentage of incidents resolved on the same day opened|

