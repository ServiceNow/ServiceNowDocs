---
title: Open Requested Item Age Monitor dashboard
description: Use this dashboard when you wish to dive into open requests for items divided by Age.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request Management Platform Analytics Solutions, Request Management in a Service Management application, Service Management]
---

# Open Requested Item Age Monitor dashboard

Use this dashboard when you wish to dive into open requests for items divided by Age.

![Open Requested Item Age Monitor dashboard](../image/open-incidents-age-monitor.png)

## Indicators

-   **Number of open requested items**

    Records on the Requested Item \[sc\_req\_item\] table opened on or before today and not closed.

-   **Average age of updated since of open requested items**

    Result of the formula `[[Summed age of updated since of open requested item]] / [[Number of open requested items]] / 24`

-   **Average age of open requested item**

    The result in days of the formula `[[Summed age of open requested item]] / [[Number of open requested items]] / 24`

-   **Average re-assignment of open requested items**

    Result of the formula `[[Summed re-assignment of open requested item]] / [[Number of open requested items]] / 24`


Indicators not appearing in dashboard widgets but used in formulas:

-   **Summed age of open requested item**

    The aggregate sum of the RequestedItem.Age.Hours script. This script calculates the difference between the latest and the first time stamp for an open item request record.

-   **Summed re-assignment of open requested item**

    The aggregate sum of reassignment counts for open requested items

-   **Summed age of updated since of open requested item**

    The aggregate sum of the results of the script RequestedItem.UpdatedSince.Hours. This script calculates the difference between the latest time stamp of an open request and the last time stamp of an update to that request.


## Breakdowns

-   Age
-   Assignment Group
-   Stage
-   State

**Parent Topic:**[Request Management Platform Analytics Solutions](request-content-pack.md)

