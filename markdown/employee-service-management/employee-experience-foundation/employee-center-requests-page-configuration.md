---
title: Employee requests page
description: The requests page is where employees can view all their requests on a single page in the Employee Center. You can configure the requests page by applying filters to show a user's service catalog requests, IT incidents, HR cases, and more.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Employee requests page

The requests page is where employees can view all their requests on a single page in the Employee Center. You can configure the requests page by applying filters to show a user's service catalog requests, IT incidents, HR cases, and more.

## Overview of the requests page

The requests page displays all of an employee's requests. The following GIF shows an example of an employee viewing and opening requests on the requests page.

**Note:** Leverage the Enhanced Requests Experience to get more flexibility of configuration and requests management on Employee Center. For more information, see [Enhanced Requests Experience](my-requests-update-intro.md).

![Using request page](../images/request-gif.gif)

## Configuring the requests page

You control the type of requests that appear by configuring the request filters. The filters define the table and conditions that a request must meet for it to appear on the requests page for an employee. For example, you can configure a Service Catalog Request filter by associating it with the Request \[sc\_request\] table with the conditions that the request is active and that the request was opened by or for the employee.

**Note:** If you are using Employee Center as part of HR Service Delivery, HR cases appear on the requests page for the user that the case was opened for. If an HR case has one or more child cases, the child cases are automatically rolled up with the parent case up to three generations \(children, grand-children, and great-grand-children\). Furthermore:

-   HR child cases that are rolled up with the parent do not appear as separate requests on the requests page.
-   Non-HR child cases \(such as IT or service catalog requests\) appear both as a separate request and as part of the roll-up on the parent case.

To learn more, including how to configure the view for the subject person of an HR case, see [HR Case Management](../../human-resources/concept/c_HRCaseManagement.md).

## Preconfigured filters

The following filters are included with the Employee Center application. You can use them or configure your own.

<table id="table_cxm_vzg_wfb"><thead><tr><th>

Application

</th><th>

Filters

</th></tr></thead><tbody><tr><td>

Employee Center

</td><td>

-   Incident Portal
-   Service Catalog Request
-   Service Catalog Request Portal
-   Service Order Portal

</td></tr><tr><td>

With HR Service Delivery

</td><td>

-   HR-My Requests
-   HR Cases Closed
-   HR Cases Open
-   HR Service Request Closed
-   HR Service Request Open

</td></tr></tbody>
</table>