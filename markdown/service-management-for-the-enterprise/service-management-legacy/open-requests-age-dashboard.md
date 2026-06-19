---
title: Open Requests Age Monitor dashboard
description: Use this dashboard when you wish to dive into open requests divided by Age.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/service-management-for-the-enterprise/service-management-legacy/open-requests-age-dashboard.html
release: zurich
product: Service Management \(Legacy\)
classification: service-management-legacy
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request Management Platform Analytics Solutions, Request Management in a Service Management application, Service Management]
---

# Open Requests Age Monitor dashboard

Use this dashboard when you wish to dive into open requests divided by Age.

\[Omitted image "open-req-age-monitor.png"\] Alt text: Open request age monitor showing the 0-1 day bucket

## Indicators

-   **Number of open requests**

    Records on the Request \[sc\_req\_item\] table opened on or before today and not closed.

-   **Average age of updated since of open requests**

    Result of the formula `[[Summed age of updated since of open request]] / [[Number of open requests]] / 24`

-   **Average age of open request**

    The result in days of the formula `[[Summed age of open request]] / [[Number of open requests]] / 24`

-   **Average re-assignment of open requests**

    Result of the formula `[[Summed re-assignment of open request]] / [[Number of open requests]] / 24`


Indicators not appearing in dashboard widgets but used in formulas:

-   **Summed age of open request**

    The aggregate sum of the Requests.Age.Hours script. This script calculates the difference between the latest and the first time stamp for an open item request record.

-   **Summed re-assignment of open request**

    The aggregate sum of reassignment counts for open requests

-   **Summed age of updated since of open request**

    The aggregate sum of the results of the script Requests.UpdatedSince.Hours. This script calculates the difference between the last update of an open request \(sys\_updated\_on\) and the last second of yesterday \(score\_end\) and returns negative value if sys\_updated\_on is after score\_end.


## Breakdowns

-   Age
-   Assignment Group
-   Priority
-   State

**Parent Topic:**[Request Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-management-for-the-enterprise/service-management-legacy/request-content-pack.md)

