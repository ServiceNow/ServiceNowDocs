---
title: Creating orders for services, service changes, or disconnects
description: With Order Capture, your service agents can directly enter multi-site service orders with one or more services on behalf of your customers. They can also manually create service change requests and disconnect orders in the ServiceNow AI Platform. Order Capture is supported in the San Diego release and later releases.OM revamp project - This topic is redundant and obsolete. The content is covered in the newly created topics. This topic has been removed from the SOM bundle on OCt 6, 2025.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/order-capture-overview-service-orders.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Creating orders for services, service changes, or disconnects

With Order Capture, your service agents can directly enter multi-site service orders with one or more services on behalf of your customers. They can also manually create service change requests and disconnect orders in the ServiceNow AI Platform. Order Capture is supported in the San Diego release and later releases.

**Note:** To learn more about creating customer \(product\) orders in Order Capture, see .

## When to use Order Capture for a direct service order entry

Most service orders that you process in the ServiceNow AI Platform are automatically captured from third-party order management systems through the Service Order Open \(TMF641\) API.

Your agents can use Order Capture to create manual service orders with additional services that have been identified as customer needs during order fulfillment. They can also create orders to change or disconnect services. When you create a manual service order, the following actions occur:

1.  You select and configure the service specifications and then perform reviews before submission.
2.  When you submit the service order, the ServiceNow AI Platform creates a service order record to manage the order fulfillment. A service order has one or more associated order line items that describe the services being performed.
3.  To review or modify a service order after you have submitted it, use the same procedures that you use for all other orders, regardless of their origin. To learn more, see [Reviewing service orders for fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-review-approve-service-orders.md).

4.  After the service managers complete their order review, they can approve \(or reject\) the order for fulfillment by service agents. To learn more about reviewing and fulfilling service orders, regardless of their source of origin, see [Approving and fulfilling service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-fulfillment-processing.md).


