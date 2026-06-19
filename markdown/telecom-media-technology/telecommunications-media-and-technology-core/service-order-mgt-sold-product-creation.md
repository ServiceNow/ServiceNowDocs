---
title: Sold product creation for service orders
description: Learn how to create and maintain the customer service inventory. By using the Order Management application, you can maintain an accurate information of your customer services.OM revamp project - This topic is obsolete and has been removed from the SOM bundle on Oct 14, 2025.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-sold-product-creation.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service order for fulfillment, Approve and fulfill service orders, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Sold product creation for service orders

Learn how to create and maintain the customer service inventory. By using the Order Management application, you can maintain an accurate information of your customer services.

## Sold product creation overview

The sold product configuration stores the service specifications and services, both customer-facing and resource-facing, that are associated with a service order. All characteristics of the service and resource specifications are updated in the Product Characteristics \[sn\_ind\_tmt\_orm\_product\_characteristics\] table.

## New order workflow

The new order workflow is as follows:

1.  After the service order manager approves the service order, the Sold Product \[sn\_install\_base\_sold\_product\] record is created. This record has placeholders for all the specifications that are generated after decomposition. The associated models have an Installation Pending state.
2.  During the fulfillment process, when the service and resource orders are closed, the state of the associated specification updates to Active in the record.
3.  When you close the service order, all the characteristics that are associated with the specifications on the service order update the record.

## Change order workflow

The change order workflow is as follows:

1.  After the service order manager approves the service order, the state of the changed or removed specifications are updated to Change Pending. The models that are associated with the changed specifications are also updated to reflect the latest model that is generated due to the change.
2.  During the fulfillment process, when the service and resource orders are closed, the state of the associated specification updates to Active in the Sold Product \[sn\_install\_base\_sold\_product\] record.
3.  When you close the service order, all the characteristics that are associated with the specifications on the service order update the record.
4.  If the change order included a product that is discontinued, the state of the associated sold product is moved to Closed.

