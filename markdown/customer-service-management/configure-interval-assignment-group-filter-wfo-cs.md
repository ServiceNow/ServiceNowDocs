---
title: Monitor staffing and volume forecast data
description: Monitor staffing levels and volume trends to identify gaps and optimize resource allocation for your assignment groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-interval-assignment-group-filter-wfo-cs.html
release: brazil
topic_type: task
last_updated: "2026-08-10"
reading_time_minutes: 1
breadcrumb: [Forecasting, Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Monitor staffing and volume forecast data

Monitor staffing levels and volume trends to identify gaps and optimize resource allocation for your assignment groups.

## Before you begin

Role required: **sn\_agent\_forecast\_user**

## About this task

The Staffing and Volume Overview page displays two charts under a shared filter bar. The **Staffing** chart shows scheduled vs. required staff for your selected date range and groups. The **Volume forecast** chart shows historical and forecasted contact volume. Both charts update when you change the shared filters. The volume chart also has its own **Data collection definition** filter.

## Procedure

1.  Go to **Workspaces** &gt; **Manager Workspace**.

2.  Select the **Forecasting** icon \(\[Omitted image "forecasting-icon-wfo-cs.png"\] Alt text: Forecasting icon\) to open the Staffing and Volume Overview page.

3.  Set the date range for the data you want to view.

    Select the **Start date** and **End date**, or select from the following:

    -   **Last Day** — Sets both dates to today.
    -   **Current Week** — Sets the range to the current week, Sunday to Saturday.
    -   **Next 28 days** — Sets the range to the next 28-day period.
    -   **Custom** — Opens a calendar picker to select specific start and end dates.
4.  Select **Interval**.

    The default is 60 minutes.

5.  Select the required **Assignment group**.

6.  Set the **Data collection definition** for the **Volume forecast** chart to scope the volume data to specific channels.

7.  Select **Reset filters** to restore the filters to their defaults.


## Result

Both charts update to reflect the selected filters.

The **Staffing** chart displays two bar series:

-   **Scheduled staff**- The number of agents currently scheduled.
-   **Required staff**- The number of agents required to meet forecast demand.

The **Volume forecast** chart displays two series:

-   **Historical volume**- Actual case and interaction volumes from MetricBase.
-   **Forecasted volume**- Predicted contact volumes from the Agent Forecast algorithm.

**Parent Topic:**[Forecasting in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/forecasting-configurable-wfo-cs.md)

