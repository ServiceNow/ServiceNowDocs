---
title: Legacy: Problem daily 7d - 28d dashboard
description: Track the progress made by different assignment groups in resolving problems in the daily, weekly, and monthly time frames.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy: Problem Management Platform Analytics Solutions, Problem Management, IT Service Management]
---

# Legacy: Problem daily 7d - 28d dashboard

Track the progress made by different assignment groups in resolving problems in the daily, weekly, and monthly time frames.

**Important:**

Starting in Xanadu release, the Problem daily 7d - 28d dashboard is deprecated. Users can use [Problem dashboard](performance-analytics/problem.md) to view, and track the open problems.

![The Problem daily tab of the Problem daily 7 day to 28 day dashboard](../image/problem-daily.png "Problem daily tab")

![The Problem 7 day tab on the Problem 7 day- 28 day dashboard. Same widgets as on the Problem 28 day dashboard, but different length of the time series.](../image/problem-daily-7d.png "Problem 7d tab (same widgets on Problem 28d)")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Problem manager - Track the progress of their groups in managing problems across daily, weekly, and monthly time frames|None|
|Problem agent - Track the progress of incidents they own across daily, weekly, and monthly timeframes|None|

## Indicators

In the 7 day and 28 day tabs, the widgets apply seven day and 28 day time series aggregations to the indicators.

-   **Number of open problems**

    Problems on the Problem \[problem\] table created on or before today and with no Closed date. This indicator is used in several other indicators on the dashboard.

-   **Number of closed problems**

    Problems on the Problem \[problem\] table closed today. This indicator is used in several other indicators on the dashboard.

-   **Average age of open problems**

    The score for this indicator is calculated according to the formula \[\[Summed age of open problems\]\] / \[\[Number of open problems\]\] / 24

-   **Number of open problems not updated in last 30 days**

    The number of open problems with the value of the Updated field more than 30 days ago.

-   **Number of open problems not updated in last 90 days**

    The number of open problems with the value of the Updated field more than 90 days ago.

-   **Average close time of problems**

    The score for this indicator is calculated according to the formula \[\[Summed duration of closed problems\]\] / \[\[Number of closed problems\]\] / 24


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open problems
-   Summed duration of closed problems

## Breakdowns

You can apply breakdown elements on this dashboard to all widgets simultaneously. Only Assignment Group elements are available. Select one or more assignment groups from the **Select elements** list.

![Element selection menu on the Problem daily 7 day to 28 day dashboard](../image/problem-daily-select-elements.png)

