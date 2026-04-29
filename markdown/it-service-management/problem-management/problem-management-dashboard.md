---
title: Legacy: Problem Management dashboard
description: Use this dashboard to gain a high-level view across the problem management process, from opening to closing.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy: Problem Management Platform Analytics Solutions, Problem Management, IT Service Management]
---

# Legacy: Problem Management dashboard

Use this dashboard to gain a high-level view across the problem management process, from opening to closing.

**Important:**

Starting in Xanadu release, the Problem management dashboard is deprecated. Users can use [Problem dashboard](performance-analytics/problem.md) to view, and track the open problems.

![Problem Overview tab of the Problem Management dashboard](../image/problem-mgmt-overview.png "Problem Overview tab")

![Tab with information about open problems on the Problem Management dashboard](../image/problem-mgmt-open.png "Problem Open tab")

![Tab with information about new problems on the Problem Management dashboard](../image/problem-mgmt-new.png "Problem New tab")

![Tab with information about closed problems on the Problem Management dashboard](../image/problem-mgmt-closed.png "Problem Closed tab")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Problem manager|pa\_viewer needed to view the Basic Indicators list|

## Indicators

-   **Number of open problems**

    Problems on the Problem \[problem\] table created on or before today and with no Closed date. This indicator is used in several other indicators on the dashboard.

-   **Number of new problems**

    Problems on the Problem \[problem\] table created today. This indicator is used in several other indicators on the dashboard.

-   **Number of closed problems**

    Problems on the Problem \[problem\] table closed today. This indicator is used in several other indicators on the dashboard.

-   **Problem backlog growth**

    The score for this indicator is calculated according to the formula \[\[Number of new problems\]\] - \[\[Number of closed problems\]\].

-   **Average age of open problems**

    The score for this indicator is calculated according to the formula \[\[Summed age of open problems\]\] / \[\[Number of open problems\]\] / 24

-   **% of new critical problems**

    The score for this indicator is calculated according to the formula \( \[\[Number of new problems &gt; Priority = 1 - Critical\]\] / \[\[Number of new problems\]\] \) \* 100

-   **Average close time of problems**

    The score for this indicator is calculated according to the formula \[\[Summed duration of closed problems\]\] / \[\[Number of closed problems\]\] / 24


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   Summed age of open problems
-   Summed duration of closed problems

## Breakdowns

Priority.

