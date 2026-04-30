---
title: Create a request from Universal Request
description: As a routing agent, create a request from a universal request and then assign it to the appropriate assignment group. The request manager handles the requested items and takes further actions to fulfill the request.
locale: en-US
release: zurich
product: Request Management
classification: request-management
topic_type: task
last_updated: "2025-07-31"
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


## Result

A request is created and is automatically assigned to the appropriate assignment group. If required, you can also add more details on the Requested item form.

On the Requested item form, the universal request number that was used for creating the request is displayed. The request item number \(RITM\#\) appears in the **Primary ticket** field on the Universal Request form and also under the Associated Requests related list.

**Parent Topic:**[Request Management integration with Universal Request](../concept/request-mgmt-integration-ur.md)

