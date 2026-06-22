---
title: Service order decomposition
description: Learn how a service order is decomposed into its domain orders for fulfillment.OM content revamp - This topic has been removed from the SOM bundle. Common content that applies to both customer and service order has been moved to the order-,gt-order-decomposition.dita and order-decomposition-examples.dita topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/service-order-mgt-order-decomposition.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service order for fulfillment, Approve and fulfill service orders, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Service order decomposition

Learn how a service order is decomposed into its domain orders for fulfillment.

## Decomposition that is based on specification relationships

Specification relationships define the relationships between product, service, and resource specifications. Specification relationships and decomposition rules specify how a service order is decomposed, fulfilled, and delivered to your customer.

Decomposition runs on the specification that is associated with the captured service order line item and its hierarchy of specifications. It works as follows:

-   If the relationships between the source and target specifications are Bundles, Realized as, or Requires types, the product, service, or resource orders are created for the target specification. This action takes place when the captured service order is decomposed.
-   Decomposition establishes the hierarchical relationship between the source and targets while generating the service and resource orders.
-   Decomposition doesn't happen if the specification relationship is of a Composed of type.

    **Note:** To learn more about specification relationship types, see [Create specification relationships, quantity mapping, and decomposition rules for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/order-mgt-specification-rels.md).


## Decomposition that is based on defined decomposition rules

Specification relationships define the relationships between product, service, and resource specifications. When you define specification relationships, you can optionally create decomposition rules. Specification relationships and decomposition rules dictate how a service order is decomposed, fulfilled, and delivered to the customer.

The best way to view a decomposition rule is as an exclusion rule. You use decomposition rules to exclude the creation of domain orders when you receive a service order that doesn’t contain a specific characteristic or characteristic option.

For example, in the Managed firewall service demo data, the Managed Firewall service is defined as a customer-facing service specification. It has a relationship with the following three resource-facing service specifications:

-   Firewall administrator
-   Firewall and DMZ
-   Threat and Intrusion Prevention service

Each of these resource-facing service specifications has relationships with the corresponding resource specifications that are required to deliver the Managed Firewall service.

-   If the relationships between the source and target specifications are Bundles, Realized as, or Requires types, decomposition creates the following types of orders for the target specification:
    -   A corresponding customer-facing service order \(CFS\), which is a service order that is generated for performance of customer-faced services.
    -   A resource-facing service order \(RFS\), which is a service order that is generated for internal use of resources required to perform the actual services for the customer.
    -   Resource order.
-   Decomposition establishes the relationship between the source and targets while generating domain service orders and resource orders. The following elements comprise the specification relationship:
    -   The source specification is the specification that is defining the specification relationship.
    -   The target specification is the specification that the relationship is being defined to.
    -   Both values are automatically defined when the decomposition rule was created for the specification relationship.

Optional decomposition rules are defined for a specification relationship between a source specification and a target specification. The rules use the characteristic and characteristic value \(optional\) of a source specification, for mapping to a target specification. These rules enable targeted order decomposition of a source specification that is based on the characteristic and characteristic value available in the source specification.

**Note:** To learn more about specification relationships and decomposition rules, see [Create specification relationships, quantity mapping, and decomposition rules for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/order-mgt-specification-rels.md).

