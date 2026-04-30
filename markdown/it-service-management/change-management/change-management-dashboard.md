---
title: Legacy: Change Management dashboard
description: Use this dashboard to see the trends in change request resolution over time across different change request risks, ages, and priorities. Break down change requests over time according to the assignment groups you manage.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Legacy: Change Management Platform Analytics Solutions, Using Change Management, Change Management, IT Service Management]
---

# Legacy: Change Management dashboard

Use this dashboard to see the trends in change request resolution over time across different change request risks, ages, and priorities. Break down change requests over time according to the assignment groups you manage.

**Important:**

Starting in Xanadu release, the Change dashboard is deprecated. Users can use [Change dashboard](performance-analytics/change.md) to view, and track the open changes.

![Animated tour of the tabs of the Change Management dashboard](../image/change-management.gif)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Change Manager - Needs to break down the trends in change request resolution over time to spot areas that need attention|itil|

## Change Management dashboard indicators

-   **Number of open changes**

    The number of changes open at the end of the collection date. The number of changes opened on or before the collection date and no close date or a close date after collection date.

-   **Number of new changes**

    The number of new changes with a registration date on the data collection date.

-   **Number of new emergency changes**

    The number of new changes where type=emergency

-   **Change backlog growth**

    The number of closed changes subtracted from the number of new changes.

-   **Number of closed changes**

    The number of changes with a close date on the data collection date.

-   **Average age of open changes**

    The average amount of time a change has been open.

-   **% of urgent changes**

    Percentage of urgent changes. Is a formula: Number of new changes classified as urgent / Number of new changes \* 100

-   **Average close time of changes**

    The average amount of time it has taken to close a change


The following indicators do not appear on the dashboard but are used in formulas:

-   Summed age of open changes
-   Summed duration of closed changes

## Breakdowns

-   Priority
-   Age
-   Assignment Group
-   Risk
-   Stage
-   Type

**Parent Topic:**[Legacy: Change Management Platform Analytics Solutions](change-content-pack.md)

