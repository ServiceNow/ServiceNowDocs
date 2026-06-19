---
title: Legacy: Request Management - Requested Item dashboard
description: Track the progress of purchase orders, transfer orders, and software assignments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/service-management-for-the-enterprise/service-management-legacy/requested-item-mgmt-dashboard.html
release: zurich
product: Service Management \(Legacy\)
classification: service-management-legacy
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request Management Platform Analytics Solutions, Request Management in a Service Management application, Service Management]
---

# Legacy: Request Management - Requested Item dashboard

Track the progress of purchase orders, transfer orders, and software assignments.

**Important:**

Starting in Xanadu release, the Request Management Platform Analytics Solutions dashboards are deprecated. Users can use the  to view the actionable data visualizations that help in improving the business processes and practices.

\[Omitted image "requested-item-mgmt-dashboard.gif"\] Alt text: Animated tour through the tabs of the Requested Item Management dashboard

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Request manager who needs to track the rate of progress of item requests

</td><td>

sn\_request\_read, sn\_request\_writeTo see the 'Basic requested items indicators' widget, the pa\_viewer role is necessary

</td></tr></tbody>
</table>## Indicators

Indicators are displayed in Performance Analytics widgets.

-   **Number of open requested items**

    Records on the Requested Item \[sc\_req\_item\] table opened on or before today and not closed.

-   **Number of new requested items**

    Records on the Requested Item \[sc\_req\_item\] table opened today and not closed.

-   **Number of closed requested items**

    Records on the Requested Item \[sc\_req\_item\] table closed today.

-   **Average age of open requested item**

    The result in days of the formula `[[Summed age of open requested item]] / [[Number of open requested items]] / 24`

-   **Average close time of requested items**

    The result in days of the formula `[[Summed duration of closed requested items]] / [[Number of closed requested items]] / 24`

-   **Requested items backlog growth**

    The result of the formula `[[Number of new requested items]] - [[Number of closed requested items]]`


Indicators not appearing in dashboard widgets but used in formulas:

-   **Summed age of open requested item**

    The aggregate sum of the RequestedItem.Age.Hours script. This script calculates the difference between the latest and the first time stamp for an open item request record.

-   **Summed duration of closed requested items**

    The aggregate sum of the RequestedItem.CloseTime.Hours script. This script calculates the difference between the time stamp when an item request is opened and the time stamp of when it is closed.


## Breakdowns

-   Age
-   Assignment Group
-   Priority
-   Stage
-   State

**Parent Topic:**[Request Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-management-for-the-enterprise/service-management-legacy/request-content-pack.md)

