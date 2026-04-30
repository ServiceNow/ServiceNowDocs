---
title: Open Requests State Monitor dashboard
description: Use this dashboard when you wish to dive into open requests divided by State: Pending Approval or Approved.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Request Management Platform Analytics Solutions, Request Management in a Service Management application, Service Management]
---

# Open Requests State Monitor dashboard

Use this dashboard when you wish to dive into open requests divided by State: Pending Approval or Approved.

![Open Requests State Monitor dashboard](../image/open-req-state-monitor.png)

## Indicators

-   **Number of open requests**

    Records on the Request \[sc\_req\_item\] table opened on or before today and not closed.

-   **Number of open request not updated in last 30 days**

    As Number of open requests, but the Updated value is either empty or from more than 30 days ago.

-   **Number of open request not updated in last 5 days**

    As Number of open requests, but the Updated value is either empty or from more than five days ago.

-   **% of open requests not updated in last 30 days**

    Result of the formula `( [[Number of open requests not updated in last 30 days]] / [[Number of open requests]] ) * 100`

-   **% of open requests not updated in last 5 days**

    Result of the formula `( [[Number of open requests not updated in last 5 days]] / [[Number of open requests]] ) * 100`

-   **Average age of updated since of open requests**

    Result of the formula `[[Summed age of updated since of open request]] / [[Number of open requests]] / 24`

-   **Average age of open requests**

    The result in days of the formula `[[Summed age of open request]] / [[Number of open requests]] / 24`

-   **Average re-assignment of open requests**

    Result of the formula `[[Summed re-assignment of open request]] / [[Number of open requests]] / 24`


Indicators not appearing in dashboard widgets but used in formulas:

-   **Summed age of open requests**

    The aggregate sum of the Requests.Age.Hours script. This script calculates the difference between the latest and the first time stamp for an open item request record.

-   **Summed re-assignment of open requests**

    The aggregate sum of reassignment counts for open requests

-   **Summed age of updated since of open requests**

    The aggregate sum of the results of the script Requests.UpdatedSince.Hours. This script calculates the difference between the latest time stamp of an open request and the last time stamp of an update to that request.


## Breakdowns

-   Age
-   Assignment Group
-   Priority
-   State

**Parent Topic:**[Request Management Platform Analytics Solutions](request-content-pack.md)

