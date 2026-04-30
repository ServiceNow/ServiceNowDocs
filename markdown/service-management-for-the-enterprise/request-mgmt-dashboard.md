---
title: Legacy: Request Management - Request dashboard
description: Track the progress of new requests through the time they are worked on until they are closed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request Management Platform Analytics Solutions, Request Management in a Service Management application, Service Management]
---

# Legacy: Request Management - Request dashboard

Track the progress of new requests through the time they are worked on until they are closed.

**Important:**

Starting in Xanadu release, the Request Management Platform Analytics Solutions dashboards are deprecated. Users can use the [Request dashboard](https://www.servicenow.com/docs/access?context=request&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) to view the actionable data visualizations that help in improving the business processes and practices.

![Animated tour of the tabs of the Request Management - Requests dashboard](../image/request-mgmt-requests.gif)

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Request manager who needs to track the rate of progress of all requests

</td><td>

sn\_request\_read, sn\_request\_writeTo see the 'Basic indicators' widget, the pa\_viewer role is necessary

</td></tr></tbody>
</table>## Indicators

-   **Number of open requests**

    Records on the Request \[sc\_req\_item\] table opened on or before today and not closed.

-   **Number of new requests**

    Records on the Request \[sc\_req\_item\] table opened today and not closed.

-   **Number of closed requests**

    Records on the Request \[sc\_req\_item\] table closed today.

-   **Number of open requests not updated in last 5 days**

    As Number of open requests, but the Updated value is either empty or from more than five days ago.

-   **Number of open requests not updated in last 30 days**

    As Number of open requests, but the Updated value is either empty or from more than 30 days ago.

-   **Average age of open requests**

    The result in days of the formula `[[Summed age of open request]] / [[Number of open requests]] / 24`

-   **Average close time of requests**

    The result in days of the formula `[[Summed duration of closed requests]] / [[Number of closed requests]] / 24`

-   **Requests backlog growth**

    The result of the formula `[[Number of new requests]] - [[Number of closed requests]]`


Indicators not appearing in dashboard widgets but used in formulas:

-   **Summed age of open requests**

    The aggregate sum of the Request.Age.Hours script. This script calculates the difference between the latest and the first time stamp for an open item request record.

-   **Summed duration of closed requests**

    The aggregate sum of the Request.CloseTime.Hours script. This script calculates the difference between the time stamp when an item request is opened and the time stamp of when it is closed.


## Breakdowns

-   Age
-   Assignment Group
-   Contact Type
-   Priority
-   State

**Parent Topic:**[Request Management Platform Analytics Solutions](request-content-pack.md)

