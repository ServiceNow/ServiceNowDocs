---
title: Order decomposition examples
description: Examples using demo data illustrating how customer and service orders can be decomposed under diverse conditions help you to understand the decomposition process. The conditions include optional characteristics, quantity-based decomposition, staggered fulfillment, and exclusion rules that support complex order management and fulfillment workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 7
breadcrumb: [Order decomposition, Order Management, Use, Sales Customer Relationship Management]
---

# Order decomposition examples

Examples using demo data illustrating how customer and service orders can be decomposed under diverse conditions help you to understand the decomposition process. The conditions include optional characteristics, quantity-based decomposition, staggered fulfillment, and exclusion rules that support complex order management and fulfillment workflows.

## Specification relationship and decomposition rule example

The Managed Firewall service demo data is an example of a customer facing service specification that has a Requires relationship with the following three resource-facing service specifications:

-   Firewall administrator
-   Firewall and DMZ
-   Threat and Intrusion Prevention service

The decomposition process creates an RFS service order only when the corresponding characteristic is available in the order line item for the Managed Firewall service specification.

After receiving a service order for adding a Managed Firewall service, a service manager reviews and approves it. This process triggers decomposition, which creates the RFS service orders and resource orders. The service order has one order line item for the Managed Firewall service, which includes all of its characteristics. The service order decomposition process creates the following:

-   A CFS service order for Managed Firewall service.
-   Three RFS service orders for all three RFS specifications.
-   Three resource orders for resource specifications.

Next, the ServiceNow AI Platform triggers a fulfillment workflow for the decomposed service and resource orders. This workflow generates the required order tasks for fulfilling the domain orders and uses decision tables to identify the workflow for a decomposed order. The selected workflow is based on various attributes in the original service order. These attributes include the specification category, and an order line item action \(Add, Change, or Delete\), among others.

To learn more about decision tables, see [Decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/decision-tables/decision-table.md):

## Example of an order decomposition that is based on specification relationships

Specification relationships define the relationships between a product, service, and resource. When you define specification relationships, you can optionally create decomposition rules to specify how a customer order is decomposed, fulfilled, and delivered to your customer.

The best way to view a decomposition rule is as an exclusion rule. You use decomposition rules to specify to exclude domain orders from being created when you receive a customer order that doesn't contain a characteristic or characteristic option. For example, in the SD-WAN Service Package demo data, the following occurs:

-   A specification relationship is defined between the SD-WAN Controller product specification and its service specifications.
-   The service specification details the services that are required for the product. When an order is received for the SD-WAN Controller product, a product order and a service order are generated for the SD-WAN Controller Service.

Decomposition runs on the specification that is associated with the customer order line item and its hierarchy of specifications. It works as follows:

-   If the relationships between the source and target specifications are Bundles, Realized as, or Requires types, a product, service, or resource order is created for the target specification when the customer order is decomposed.
-   Decomposition establishes the hierarchical relationship between the source and targets while generating the product, service, and resource orders.
-   If the specification relationship is of a Composed of type, decomposition doesn't happen.

The SD-WAN Service Package demo data is an example of a composite product specification that bundles three other product specifications within it:

-   SD-WAN Controller
-   SD-WAN Edge Device
-   SD-WAN Security

The SD-WAN Service Package defines the following relationships:

-   SD-WAN Service Package has a Bundles relationship with an SD-WAN Controller
-   SD-WAN Service Package has a Bundles relationship with an SD-WAN Edge Device
-   SD-WAN Service Package has a Bundles relationship with SD-WAN Security

When a customer order is received for the SD-WAN Service Package, and that order is approved, decomposition is triggered. The customer order line item for the SD-WAN Service Package has a single product order for the SD-WAN Service Package. That SD-WAN Service Package Product order has three child product orders:

-   SD-WAN Controller
-   SD-WAN Edge Device
-   SD-WAN Security \(if the option security product was ordered\)

## Example of order decomposition that is based on defined decomposition rules

When you define specification relationships, you can optionally create decomposition rules. With a decomposition rule, you can specify to exclude domain orders from being created when you receive a customer order that doesn't contain a specific characteristic or characteristic option. The following example shows that the SD-WAN Controller Tenancy product characteristic was designated as optional.

![Product Specification page displaying the decomposition rules tab view of SD-WAN controller along with field description. For more information, refer to the description that follows.](../image/specification-relationship1.png "SD-WAN Controller Tenancy product characteristic")

In the example, you see that a decomposition rule was defined for the SD-WAN Controller product specification relationship to the SD-WAN Controller Service. This rule excludes the specification when a customer does not select the **Tenancy** option.

![Decomposition rule field details of SD-WAN controller service. To learn more about fields, refer to the following description.](../image/decomp-rule2.png "SD-WAN Controller Service decomposition rule")

When a customer places an order and doesn't select the **Tenancy** option, the related service order doesn't generate for it.

## Example of order decomposition that include references to characteristics and options

You can define the decomposition rules for a specification relationship and include references to a characteristic and characteristic option. The following elements comprise the specification relationship:

-   The source specification is the specification that defines the specification relationship.
-   The target specification is the specification that the relationship is being defined to.
-   Both values are automatically defined when you create the decomposition rule from the specification relationship.

If the characteristic and value are present on the order line, the ServiceNow AI Platform applies the decomposition rules to Add and Change type orders. They are not applied to customer order line items with a Disconnect \(Delete\) order action.

In this example, the SD-WAN Edge Device is a product specification and SD-WAN Security is a service specification.

-   The SD-WAN Edge Device has a characteristic called WAN Optimization and has a Realized as relationship with SD-WAN Security.
-   There is a decomposition rule for this relationship with WAN Optimization as the characteristic.

If you receive an order for the SD-WAN Service Package that doesn’t include the WAN Optimization characteristic, the decomposition rule prevents the generation of an SD-WAN Controller Service service order. The rule designates that the decomposition of that service order only happens if that characteristic is ordered.

## Order decomposition for order line-item quantity and order quantity characteristics changes

When order decomposition process uses the order quantity information from the order capture process to create multiple product orders that match the line item quantity for a customer order. An agent then fulfills each instance of the product separately, which create the inventory records for each of the fulfillment instances.

When a customer submits an order for three instances of the SD-WAN Service Package product and you approve the order, the decomposition process creates three product orders for the SD-WAN Service Package including one product order for each order line item. Each product order in the SD-WAN Service Package creates three child orders for the products and services for the order fulfillment process.

## Example of staggered decomposition

The following example describes the staggered decomposition process for a product offering called SD-WAN Bronze Plan.

![Product Offering page displaying the decomposition process of SD-WAN bronze plan. For more information, refer to the description that follows.](../image/SD-WAN-Bronze-Plan.png "SD-WAN Bronze Plan product offering")

The SD-WAN Bronze Plan product offering uses a product specification, called an SD-WAN Service Package \(as shown in the following example\), that has three target specifications:

-   SD-WAN Edge Device
-   SD-WAN Security
-   SD-WAN Controller

![Product Specification page displaying the specification relationships tab view of SD-WAN service package along with field details. For more information, refer to the description that follows.](../image/SD-WAN-Service-Package.png "SD-WAN Service Package product specifications")

The SD-WAN Edge Device product specification has specification relationships with SD WAN Optimization Service and SD-WAN Routing, and the underlying decomposition rules don't have any values for WAN Optimization and Routing characteristics.

![View of the specification relationships tab view of SD-WAN edge device and its field details. For the image description, refer to the text that follows.](../image/SD-WAN-Bronze-Plan-Specification-Relationships.png "SD-WAN Bronze Plan specification relationships")

The following example shows the decomposition rules for the product offering for the SD-WAN Bronze Plan.

![View of the decomposition rules tab view of SD-WAN edge device and its field details. For the image description, refer to the text that follows.](../image/SD-WAN-Bronze-Plan-Decomposition-Rules.png "SD-WAN Bronze Plan decomposition rules")

When your customer places an order for the SD-WAN Bronze Plan product offering and you approve this customer order, decomposition begins with the creation of the domain orders as per the defined specification relationships and decomposition rules. Because this customer order doesn't have the values for these characteristics for Routing and WAN Optimization, the decomposition rule doesn't create the service orders.

However, as a part of the order fulfillment process, the information for Routing and WAN Optimization must be available. When your fulfillment agent provides the values for these characteristics, the decomposition rule creates the necessary service orders and the order decomposition completes.

