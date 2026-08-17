---
title: Create a request from Universal Request
description: As a routing agent, create a request from a universal request and then assign it to the appropriate assignment group. The request manager handles the requested items and takes further actions to fulfill the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/request-management/create-request-from-ur.html
release: yokohama
product: Request Management
classification: request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request Management integration with Universal Request, Configure, Request Management, IT Service Management]
---

# Create a request from Universal Request

As a routing agent, create a request from a universal request and then assign it to the appropriate assignment group. The request manager handles the requested items and takes further actions to fulfill the request.

## Before you begin

Ensure that you have the following plugins installed.

-   Universal Request plugin \(com.snc.universal\_request\)
-   Request Management plugin \(com.sn\_cs\_sm\_request\)

**Note:** A request is associated with the parent Universal Request record only when you have the following conditions set:

-   The **glide.sc.use\_cart\_layouts** system property is set to true.
-   The **Use Cart Layout**" check box for an individual catalog item is selected.

Role required: routing agent

## Procedure

1.  Navigate to **Universal Request** &gt; **All**.

2.  Open the universal request record from which you want to create a request.

3.  Select **Create Request**.

4.  In the **Create Request** dialog, fill in the required details.

<table id="table_ckl_nsg_1kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Assignment group**

</td><td>

Group assigned to fulfill the request. Auto-populated based on catalog item routing

</td></tr><tr><td>

**Short description**

</td><td>

Brief description of the request

</td></tr></tbody>
</table>    The catalog items available in the dialog depend on the service desk group assigned.

    **Note:** The request is automatically linked to the parent Universal Request record when the **glide.sc.use\_cart\_layouts** property is set to `true` and the catalog item has the **Use Cart Layout** check box selected.


## Result

A request is created and is automatically assigned to the appropriate assignment group. If required, you can also add more details on the Requested item form.

On the Requested item form, the universal request number that was used for creating the request is displayed. The request item number \(RITM\#\) appears in the **Primary ticket** field on the Universal Request form and also under the Associated Requests related list.

**Parent Topic:**[Request Management integration with Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/request-management/request-mgmt-integration-ur.md)

