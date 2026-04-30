---
title: Legacy: Change Premium dashboard
description: This dashboard uses Workbench widgets and other advanced Platform Analytics features to give you all the information about the Change process in one place.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2023-02-02"
reading_time_minutes: 3
breadcrumb: [Legacy: Change Management Platform Analytics Solutions, Use, Change Management, IT Service Management]
---

# Legacy: Change Premium dashboard

This dashboard uses Workbench widgets and other advanced Platform Analytics features to give you all the information about the Change process in one place.

**Important:**

Starting in Xanadu release, the Change premium dashboard is deprecated. Users can use [Change dashboard](performance-analytics/change.md) to view the information about the Change process in one place.

![Animated tour of the tabs of the Change Premium dashboard](../image/change-mgmt-premium.gif)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Change Manager - Needs to break down the trends in change request resolution over time to spot areas that need attention|itil|

## Indicators

-   **Number of open changes**

    The number of changes open at the end of the collection date. This calculation is the number of changes opened on or before the collection date and not closed by that date.

-   **Average age of open changes**

    \[\[Summed age of open changes\]\] / \[\[Number of open changes\]\] / 24

-   **Average re-assignment of open changes**

    \[\[Summed re-assignment of open changes\]\] / \[\[Number of open changes\]\]

-   **Average age of last update**

    The average length of time since the last update made to a change.

-   **Number of new changes**

    The number of new changes with a registration date on the data collection date.

-   **Change backlog growth**

    The number of closed changes subtracted from the number of new changes.

-   **Number of closed changes**

    The number of changes with a close date on the data collection date.

-   **% of urgent changes**

    Percentage of urgent changes. Is a formula: Number of new changes classified as urgent / Number of new changes \* 100

-   **Average close time of changes**

    The average length of time in hours between when a change request is opened and closed.

-   **Average implementation time of closed changes**

    The average length of time in hours between when a change request enters the Implementation state and when it is closed

-   **Number of reassigned open changes**

    The number of changes with a reassignment count of 1 or higher

-   **Number of unsuccessful changes**

    The number of closed changes with a Close Code of "Unsuccessful"


The following indicators are not displayed on the dashboard but are used in formulas:

-   Summed age of open changes
-   Summed age of updated since of open changes
-   Summed duration of closed changes
-   Summed implementation time closed changes
-   Summed re-assignment of open changes

## Breakdowns

-   Age
-   Category
-   Priority
-   Risk
-   State
-   Assignment Group
-   Type

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Changes Opened Today|Single Score![Single-score icon](../../performance-analytics/image/single-score.png)|Number of active changes opened on the day the dashboard is viewed.|
|Unassigned Changes|Single Score![Single-score icon](../../performance-analytics/image/single-score.png)|Number of active changes that don't have an assignee.|
|Overdue Changes|Single Score![Single-score icon](../../performance-analytics/image/single-score.png)|Number of changes that are in one of the following states: New, Assess, Authorize, or Scheduled and for which the planned start date is before the current date.|
|Changes On Hold|Single Score![Single-score icon](../../performance-analytics/image/single-score.png)|Number of changes with the status On hold.|
|Conflicting Changes|Single Score![Single-score icon](../../performance-analytics/image/single-score.png)|Number of changes with the status Conflict.|
|Rejected Changes|Single Score![Single-score icon](../../performance-analytics/image/single-score.png)|Number of changes for which the approval status is Rejected.|
|Open Changes - Grouped|Horizontal Bar![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Open changes grouped by Priority|
|Upcoming Changes \(30 days\) - Grouped|Horizontal Bar![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Active changes for which the planned start date is in the past 30 days and for which the state is Scheduled.|
|Open Changes by Risk and Priority|Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)|Active changes sorted by risk on the Y-axis and priority on the X-axis. Cells are highlighted from white for low scores to dark blue for high scores.|
|Upcoming Changes \(30 days\) by Risk and Priority|Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)| |
|Changes Opened per Month by Type|Column![Column report icon](../../performance-analytics/image/column-icon.png)|All closed reports opened in the current calendar year. Grouped by type and trended by month opened.|
|Closed Changes per Month|Line ![Line report icon](../../performance-analytics/image/line-icon.png)|Number of closed changes per month expressed on a line chart.|

**Parent Topic:**[Legacy: Change Management Platform Analytics Solutions](change-content-pack.md)

