---
title: Order decomposition
description: Order decomposition is the process of breaking down an approved customer or service order into a set of smaller, manageable domain orders for fulfillment. This process is driven by definitions in the product catalog to ensure that all necessary components are provisioned correctly. Learn about the decomposition process for customer and service order and their differences.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Order decomposition

Order decomposition is the process of breaking down an approved customer or service order into a set of smaller, manageable domain orders for fulfillment. This process is driven by definitions in the product catalog to ensure that all necessary components are provisioned correctly. Learn about the decomposition process for customer and service order and their differences.

## Overview of order decomposition

When an order is approved, the system breaks down the commercial elements of an approved order into its smaller, actionable technical components called domain orders \(product, service, and resource orders\) for fulfillment. Decomposition defines the Bill of Material for an ordered component. The decomposition is guided by specifications, specification relationships, and decomposition rules defined in the product catalog. Decomposition rules \(often exclusion rules\) determine when domain orders should or should not be created, based on characteristics or options present in the order line item. Decomposition establishes hierarchical relationships between source and target specifications, generating the necessary product, service, and resource orders.

For example, consider the SD-WAN Service Package from the demo data. For this product, specification relationships and decomposition rules determine which product, service, and resource orders are generated based on the order's characteristics.

During order decomposition, work orders are created for product or service orders that need further action. For example, installation of a device at the customer site. You must close the order tasks and work order tasks associated with the domain orders to proceed with order fulfillment. Fallout records are created if you manually close the domain orders.

## Hierarchy of domain orders

The domain order hierarchy is structured as follows:

-   **Product order \(Parent\)**

    Defines the commercial intent of what is being sold. It is based on a product specification that includes brand, pricing, terms, and other product-related materials. The product order initiates the fulfillment process by triggering associated service and resource orders.

-   **Service order \(Child of product order\)**

    Manages the fulfillment of a specific service specification. It outlines the technical realization and delivery of the service, often involving multiple service and resource orders.

-   **Resource order \(Child of service order\)**

    Handles the provisioning of physical or logical resources required to deliver the service. It is based on a resource specification and may include multiple resource orders depending on the complexity of the service.


Each product order can have multiple service orders, and each service order can have multiple resource orders, depending on the relationships defined in the product specification.

## The role of specification relationships and decomposition rules

The following core components drive the decomposition process:

-   Specifications: Define the attributes of products, services, and resources.
-   Specification relationships: Define how different specifications are related to each other.
-   Decomposition rules: Provide conditional logic for the decomposition process.

Decomposition runs on the specification associated with the order line item and its hierarchy. The type of relationship between specifications determines the outcome.

-   If the relationship is of type Bundles, Realized as, or Requires, decomposition process creates the following types of orders for the target specification:
    -   A corresponding customer-facing service order \(CFS\), which is a service order that is generated for performance of customer-faced services.
    -   A resource-facing service order \(RFS\), which is a service order that is generated for internal use of resources required to perform the actual services for the customer.
    -   Resource order.
-   If the relationship is of type Composed of, decomposition does not occur for that relationship.

Decomposition rules function as exclusion rules. They are used to prevent the creation of certain domain orders if the incoming order does not contain a specific characteristic or characteristic option. This allows for optional components within a product or service offering. For example, a rule can be set to only generate a service order for a specific feature if the customer explicitly selected that feature during the ordering process.

Specification relationships and decomposition rules can be defined to exclude domain orders when certain characteristics are not present. For example, if a customer or service order does not include a required characteristic such as Tenancy or WAN Optimization, the related domain order is not generated.

The decomposition process uses the source specification \(defining the relationship\) and the target specification \(being defined to\), with rules mapped to specific characteristics and values.

When the attribute value is increased, more number of CFS/RFS is created.

When the attribute value is decreased, it decreases the number of CFS/RFS.

## Customer order vs. Service order decomposition

While the fundamental principles of decomposition remain the same, there are key differences when decomposing a service order compared to a customer order. The most significant difference is that service order decomposition does not generate product orders. The process is focused exclusively on the fulfillment of services and their underlying resources. The decomposition of a service order generates a specific set of service and resource orders:

-   Customer-Facing Service \(CFS\) Order: A service order for the performance of a customer-facing service.
-   Resource-Facing Service \(RFS\) Order: A service order for the internal use of resources required to perform the actual service for the customer.

The scope of service order decomposition is focused on the logical breakdown of services. It does not typically involve concepts like staggered or quantity-based decomposition, which are more common in customer orders that may include physical products with variable quantities and complex, multi-stage fulfillment cycles. The key differences are listed in the following table.

<table id="table_lpt_44w_tgc"><thead><tr><th>

Aspect

</th><th>

Description

</th><th>

Customer order

</th><th>

Service order

</th></tr></thead><tbody><tr><td>

Trigger

</td><td>

Action that triggers order decomposition

</td><td>

Approval of a customer order by fulfillment manager

</td><td>

Approval of a service order by service order manager

</td></tr><tr><td>

Basis for decomposition

</td><td>

Basis on which the domain orders are generated

</td><td>

Based on specifications, specification relationships, and the decomposition rules that are defined in the product catalog between the product, service, and resource specifications.

</td><td>

Based on specifications, specification relationships, and the decomposition rules that are defined in the product catalog between the service, and resource specifications.

</td></tr><tr><td>

Domain order generated

</td><td>

Type of domain orders

</td><td>

Product, service, resource orders

</td><td>

Service and resource orders only

</td></tr><tr><td>

Staggered decomposition

</td><td>

The process that allows domain orders to be created at a later stage, based on updated information such as customer needs, service availability

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Quantity-based decomposition

</td><td>

The process that supports splitting orders based on quantity, handling changes in order quantity, and managing inventory updates or cancellations for in-flight orders

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Example

</td><td>

-

</td><td>

SD-WAN Service Package

 -   Bundles multiple product specifications.
-   Decomposition creates a parent product order and multiple child product and service orders, with rules to include or exclude based on characteristics like Tenancy or WAN Optimization.

</td><td>

Managed firewall service

 Decomposition creates a customer-facing service order \(CFS\), multiple resource-facing service orders \(RFS\), and resource orders, based on relationships and characteristics present in the order.

</td></tr></tbody>
</table>## Additional features in customer order decomposition

Customer order decomposition supports the following additional features:

-   Staggered decomposition: Customer orders may use staggered decomposition, creating domain orders at later stages based on updated information such as service availability or customer needs.
-   Quantity-based decomposition: Customer orders can be decomposed into multiple domain orders based on order quantity, supporting revisions, and fulfillment of multiple instances.
-   Support for change orders: Customer order decomposition supports updates to quantity characteristics, enabling upgrades, downgrades, and inventory management during fulfillment.

Fore more information, see [Customer order decomposition](customer-order-decomposition.md).

