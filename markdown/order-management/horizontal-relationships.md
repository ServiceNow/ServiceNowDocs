---
title: Horizontal relationships between products
description: By using a compatibility rule, you can define the horizontal relationships between your product, service, and resource specifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/horizontal-relationships.html
release: australia
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 2
breadcrumb: [Order fulfillment, Order Management, Use, Sales Customer Relationship Management]
---

# Horizontal relationships between products

By using a compatibility rule, you can define the horizontal relationships between your product, service, and resource specifications.

When you create a product catalog, you can create a vertical relationship, which is the relationship between your parent and child entities. As a product catalog manager, you can also enable a horizontal relationship, which is a relationship between a product to product, product to service, or product to resource, by defining compatibility rules in the product catalog.

## Using a horizontal relationship

The compatibility rules include the horizontal relationships between your product, service, and resource specifications. Your customers can place orders for enterprise products where a product can depend on another product in the same or different product offering, like a sibling or a peer.

A compatibility rule pairs a source specification with a target specification and defines the relationship between them. You can define one of two relationship types:

-   **Requires**

    The source specification needs the target specification.

-   **Excludes**

    The source specification cannot be ordered with the target specification.


You can establish the relationship by selecting the specifications or by defining their characteristics. You can also set the minimum and maximum quantity of specifications to support order fulfillment.

Let's look at an example of a horizontal relationship, such as the relationship between the Voice over Internet Protocol \(VoIP\) and an internet service. VoIP requires an active internet connection but VoIP and an internet service are defined in a different product hierarchy. With a horizontal relationship, you can define a Requires relationship between VoIP and an internet service in the product catalog to support the order creation process for VoIP and to fulfill the order.

**Note:** To configure a compatibility rule for a horizontal relationship, see [Configuring compatibility rules for horizontal relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-compatibility-management.md).

**Parent Topic:**[Order fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/reviewing-orchestration-plans-order-fulfillment.md)

**Related topics**  


[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-configuring.md)

[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md)

