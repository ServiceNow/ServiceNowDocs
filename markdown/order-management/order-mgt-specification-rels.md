---
title: Create specification relationships, quantity mapping, and decomposition rules for Order Management
description: Create the specification relationships and optional decomposition rules that define the associations between the product, service, and resource specifications for a product that you offer. These relationships impact how an order is fulfilled for a customer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/order-mgt-specification-rels.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Specifications and product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create specification relationships, quantity mapping, and decomposition rules for Order Management

Create the specification relationships and optional decomposition rules that define the associations between the product, service, and resource specifications for a product that you offer. These relationships impact how an order is fulfilled for a customer.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_manager

## About this task

Specification relationships define the relationships and associations between the product, service, and resource specifications. They designate how an order that contains the source specification is decomposed, fulfilled, and delivered to the customer. For example, if you have a product that you deliver through a service specification, you can designate that it is composed of three unique service specifications \(product, service, or resource\).

**Note:** The target product, service, or resource specification you select in the **Target Specification** field can be in any state, including a Draft state. The selected specification does not have to be published before selecting it in this field.

You can also select the characteristic options of the quantity characteristic for the specification relationship to provide the quantity of the target specifications. The order decomposition process refers to the mapped quantity to decompose the order for the source specification and creates the required number of domain orders for the target specification.

If the quantity characteristic has a number as a characteristic option, the decomposition process refers to the characteristic option and creates the number of domain orders for the target specification.

Optionally, you can create decomposition rules for the selected source and target specification relationships. The specification relationships can have product, service, or resource specifications as the source specifications.

**Note:** To learn more, see the following:

-   [Order quantity support in Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-quantity-support.md)
-   [Order decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-mgt-order-decomposition.md)

## Procedure

1.  Open CRM Workspace.

2.  Navigate to **List** &gt; **Specifications** and select a specification type.

    -   Product Specifications
    -   Service Specifications
    -   Resource Specifications
    A list of specification records is displayed.

3.  Select a record you want to modify.

4.  Navigate to the **Specification Relationships** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

<table id="table_ytw_wcr_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name for the specification relationship.

</td></tr><tr><td>

Source specification

</td><td>

Product, service, or resource specification that you create the relationship from. For example, the source specification could be a product specification for an SD-WAN.

</td></tr><tr><td>

Target type

</td><td>

Type of specification:-   Product Specification
-   Service Specification
-   Resource Specification


</td></tr><tr><td>

Target specification

</td><td>

Specification that you create the relationship to. For example, the target specification could be a service specification for an SD-WAN.**Note:** The target product, service, or resource specification you select can be in any state, including a Draft state. The selected specification does not have to be published before selecting it in this field.

</td></tr><tr><td>

Mandatory

</td><td>

Option that designates if the relationship between the selected source and target specifications is mandatory and should always exist when a customer orders the product.-   If selected, the target specification is always included with the source specification. During the ordering process,you must select the characteristics and characteristic values for the target specification.

For example, if you are defining an SD-WAN Service Package, you designate that the SD-WAN Edge Device and SD-WAN Controller target specifications are mandatory.

-   If cleared, it is an optional target specification and is only included with the product if the customer selected it during the ordering process.

For example, if you designate that the SD-WAN Security specification is optional, it's included in an ordered SD-WAN Service Package only if the customer selected it during the ordering process.

</td></tr><tr><td>

Relationship type

</td><td>

Type of relationship that designates how an order that contains the source specification decomposes for fulfillment after you receive and approve it. -   **Composed of**

Source specification that is composed of the selected target specification.

An order that contains the source specification and characteristics decompose into a single service order.

-   **Realized as**

Source specification that is realized as the selected target specification.

-   **Bundles**

Source specification bundles as the selected target specification.

An order that contains the source specification and characteristics decompose into unique order line items for each of the target specifications bundled from that parent product specification.

-   **Requires**

Source specification that requires the selected target specification.

To enable the delivery of the promised services in the specification, an order that contains the source specification and characteristics also requires the target resource specification.

</td></tr><tr><td>

Order

</td><td>

Enter a numeric value that represents the order in which this relationship is applied, if there is more than one relationship.

</td></tr><tr><td>

Minimum quantity

</td><td>

Required minimum number of specifications for an order.

</td></tr><tr><td>

Default quantity

</td><td>

Default quantity if there is no selected amount.

</td></tr><tr><td>

Maximum quantity

</td><td>

Maximum quantity of specifications.

</td></tr><tr><td>

Quantity characteristic

</td><td>

Source specification characteristic that is used for quantity mapping. The quantity characteristic is supported only for a specification relationship in a product specification.

</td></tr><tr><td>

Rule

</td><td>

Configuration rule that defines the condition-based logic for decomposing the source specification into the target specification. This field is available only when the condition-builder decomposition feature is enabled, and is populated automatically when you create a decomposition rule.

</td></tr></tbody>
</table>7.  Select **Save**.


## What to do next

Optionally, create decomposition rules for selected specification relationships that have a product, service, or resource specification as the source specification. For more information, see: .

**Parent Topic:**[Setting up specifications and product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-mgt-product-catalog.md)

**Related topics**  


[Using product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)

[Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-managment.md)

