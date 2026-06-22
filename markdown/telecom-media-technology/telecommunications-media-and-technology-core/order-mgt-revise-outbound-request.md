---
title: Revise an outbound request for the service order
description: As a provider, revise the outbound request that was previously created for a service order by using the Order Management for Telecommunications, Media, and Technology application. This way, you can share any inflight order changes with the external systems during the order fulfillment process.OM revamp project - unable to validate this task against the UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/order-mgt-revise-outbound-request.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Revise an outbound request for the service order

As a provider, revise the outbound request that was previously created for a service order by using the Order Management for Telecommunications, Media, and Technology application. This way, you can share any inflight order changes with the external systems during the order fulfillment process.

## Before you begin

Ensure that you have first created an outbound request for a service order.

Role required: sn\_ind\_tmt\_orm.order\_fulfilment\_agent, sn\_ind\_tmt\_orm.order\_fulfillment\_manager, sn\_ind\_tmt\_orm.service\_order\_agent, sn\_ind\_tmt\_orm.service\_order\_manager

## About this task

If you make any changes in the order properties, such as updating the domain order characteristics through the user updates or inflight changes while the order fulfillment is in progress, you might need to share the updated order details with the external systems. To learn more about managing the inflight order changes, see [Managing inflight order changes and cancellation requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/inflight-order-change-mgt-overview.md) and [Cancel orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/order-mgt-review-cust-order-detail.md).

A new Updates available order attribute tracks for any updates in the service order. If you update an order characteristic or revise the domain order \(Updated or Canceled\) as a part of the inflight revision, the value of the Updates available field is set to true. Also, the Revise Outbound Request UI action appears on the domain order form to trigger the revision of the outbound request.

## Procedure

1.  Select a service order and open it.

2.  Select the **Revise Outbound Request** UI action.

    A dialog box appears with the following message: Want to revise outbound fulfillment request for the service order?

    Do one of the following actions:

    -   Don't trigger this action by selecting **Cancel**.
    -   Initiate this template by selecting **OK**.
    The revised order details are generated and sent to the external systems through the configured integration. To learn more, see [Integrating Order Management with southbound external systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/order-mgt-integrate-southbound.md).


**Related topics**  


[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/order-mgt-configuring.md)

[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/explore-order-management.md)

