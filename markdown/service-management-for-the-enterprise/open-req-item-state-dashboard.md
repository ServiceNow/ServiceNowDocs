---
title: Open Requested Item State Monitor dashboard
description: Use this dashboard when you wish to dive into open requests for items divided by State: Pending, Work in Progress, or all Open requests.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Request Management Platform Analytics Solutions, Request Management in a Service Management application, Service Management]
---

# Open Requested Item State Monitor dashboard

Use this dashboard when you wish to dive into open requests for items divided by State: Pending, Work in Progress, or all Open requests.

![Open Requested Item State Monitor reflecting requests in the Pending state](../image/open-req-item-state-monitor.png "Open Requested Item State Monitor focused on Pending requests")

## Indicators

-   **Number of open requested items**

    Records on the Requested Item \[sc\_req\_item\] table opened on or before today and not closed.

-   **Number of open requested item not updated in last 30 days**

    As Number of open requested items, but the Updated value is either empty or from more than 30 days ago.

-   **Number of open requested item not updated in last 5 days**

    As Number of open requested items, but the Updated value is either empty or from more than five days ago.

-   **% of open requested items not updated in last 30 days**

    Result of the formula `( [[Number of open requested items not updated in last 30 days]] / [[Number of open requested items]] ) * 100`

-   **% of open requested items not updated in last 5 days**

    Result of the formula `( [[Number of open requested items not updated in last 5 days]] / [[Number of open requested items]] ) * 100`

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

