---
title: Legacy: Open Problem Age Monitor dashboard
description: Use this dashboard to track the progress of open problems across different age buckets. You can break down the problems by priority or assignment group.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy: Problem Management Platform Analytics Solutions, Problem Management, IT Service Management]
---

# Legacy: Open Problem Age Monitor dashboard

Use this dashboard to track the progress of open problems across different age buckets. You can break down the problems by priority or assignment group.

**Important:**

Starting in Xanadu release, the Problem age dashboard is deprecated. Users can use [Problem dashboard](performance-analytics/problem.md) to view, and track the open problems.

![Open Problem Age Monitor workbench](../image/problem-open-age-monitor.png)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Problem manager - Track how their groups are managing long-standing problems|itil to read records, otherwise none|
|Problem agent - Track long-standing problems that they own|itil to read records, otherwise none|

## Indicators

-   **Number of open problems**

    Problems on the Problem \[problem\] table created on or before today and with no Closed date. This indicator is used in several other indicators on the dashboard.

-   **Average age of open problems**

    The score for this indicator is calculated according to the formula \[\[Summed age of open problems\]\] / \[\[Number of open problems\]\] / 24

-   **Average re-assignment of open problems**

    The average number of times an open problem gets reassigned. The score for this indicator is calculated according to the formula \[\[Summed re-assignment of open problems\]\] / \[\[Number of open problems\]\].

-   **Average age of updated since of open problems**

    The average time in days since the last update of an open problem. The score for this indicator is calculated according to the formula \[\[Summed age of updated since of open problems\]\] / \[\[Number of open problems\]\] / 24.


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open problems
-   Summed re-assignment of open problems
-   Summed age of updated since of open problems

## Breakdowns

-   Priority
-   State
-   Assignment Group

