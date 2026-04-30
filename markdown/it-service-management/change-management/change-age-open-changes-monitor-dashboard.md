---
title: Legacy: Age of Open Changes Monitor dashboard
description: This workbench dashboard enables you to view and assess all open changes separated into age brackets: less than one day, from 1-5 days, from 6-30 days, from 31-90 days, and over 90 days.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2023-02-02"
reading_time_minutes: 1
breadcrumb: [Legacy: Change Management Platform Analytics Solutions, Using Change Management, Change Management, IT Service Management]
---

# Legacy: Age of Open Changes Monitor dashboard

This workbench dashboard enables you to view and assess all open changes separated into age brackets: less than one day, from 1-5 days, from 6-30 days, from 31-90 days, and over 90 days.

**Important:**

Starting in Xanadu release, the Change dashboard is deprecated. Users can use [Change dashboard](performance-analytics/change.md) to view, and track the open changes.

![Age of Open Changes Monitor dashboard](../image/change-open-changes-monitor.png "Age of Open Changes Monitor tab")

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


## Breakdowns

-   Priority
-   Risk
-   Assignment Group
-   State

**Parent Topic:**[Legacy: Change Management Platform Analytics Solutions](change-content-pack.md)

