---
title: Filter shopfloor insights data
description: Use filters on the Insights Overview tab to refine shopfloor insights data by functional location, equipment, and time period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/igt-filter-shopfloor-insights.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [shopfloor insights, filter, Industrial Guided Tasks]
breadcrumb: [Industrial Guided Tasks, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Filter shopfloor insights data

Use filters on the Insights Overview tab to refine shopfloor insights data by functional location, equipment, and time period.

## Before you begin

Roles required: sn\_icw\_igt.user and sn\_icw.report\_user

## About this task

The Insights Overview dashboard provides filter options to customize the data displayed. By default, the dashboard displays data from the last 7 days. Use filters to perform the following:

-   Compare execution results across different functional locations, equipment, and time periods.
-   View data which is automatically filtered based on the published standard.

## Procedure

1.  On the Insights Overview tab, locate the filter options at the top of the dashboard.

2.  To filter by functional location:

    1.  Select the **Functional location** filter.

    2.  Choose a functional location from the list.

        Select all functional locations manually through a filter which provides multiple options.

        **Note:**

        Data of the child functional locations is not displayed.

3.  To filter by equipment:

    1.  Select the **Equipment** filter.

    2.  Choose an equipment from the list.

        The equipments that are not part of selected filters are still visible but they are not available for selection \(greyed out\).

4.  To filter by date range:

    1.  Select the **Date filter**.

    2.  Choose a time period from the available options:

        -   Last day: Data from the previous day. Aggregated by shift.
        -   Today: Data from the current day. Aggregated by shift.
        -   Last week \(default\): Data from the previous week. Aggregated by shift.
        -   Last 7 days: Data from the past 7 days. Aggregated by shift when a standard has a shift configuration.
        -   Last month: Data from the past month. Aggregated by production week.
        -   This month: Data from the current month. Aggregated by production week.
        -   Last 6 months: Data from the past 6 months. Aggregated by production week.
    The dashboard updates to show execution data for the selected time period. Data aggregation is adjusted for a standard according to its shift configuration. If a standard does not have a shift configuration, data aggregation is adjusted based on a standard calendar.

5.  Review the filtered data in the dashboard visualizations.

    All indicators and charts are updated to reflect the applied filters. Use this filtered view to:

    -   Compare execution across different shifts or time periods.
    -   Analyze performance for specific equipment or locations.

**Parent Topic:**[Using Industrial Guided Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/using-industrial-guided-tasks.md)

