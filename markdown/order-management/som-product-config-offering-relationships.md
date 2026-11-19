---
title: Create product offering relationships
description: Create product relationships to bundle products and services together to make ordering more convenient. Product offering relationships drive the order capture experience by letting you group multiple product offerings into bundles. Bundles can also be added to other bundles in relationship groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/som-product-config-offering-relationships.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Create product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create product offering relationships

Create product relationships to bundle products and services together to make ordering more convenient. Product offering relationships drive the order capture experience by letting you group multiple product offerings into bundles. Bundles can also be added to other bundles in relationship groups.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin or sn\_prd\_pm.product\_catalog\_manager

## About this task

Create product offering relationships that bundle products together. A bundled product offering can be ordered as a group and can’t be changed.

**Important:** If the source product offering has a value in the **Product model** field, its relationship groups are deleted when you save the offering, and the **Product offering relationship group** field on its relationships is cleared. After you set a product model, review the relationships on the **Product Offering Relationships** tab.

## Procedure

1.  In the CRM Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  Navigate to **Offerings** &gt; **Product Offerings** and select the product offering you’re working with.

3.  Select the **Product Offering Relationships** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_urm_gvt_g1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the product relationship displayed in the interface.

</td></tr><tr><td>

Source product offering

</td><td>

System-generated reference to the source product offering.

</td></tr><tr><td>

Target product offering

</td><td>

The offering that is bundled with the source product offering. If the source is an entitlement offering, the target must also be an entitlement offering. A product offering can have both product and entitlement offerings as targets, for example a laptop offering bundled with an extended warranty entitlement. If the source is a transient offering, the target must be a transient offering that isn't a contract offering.

</td></tr><tr><td>

Relationship type

</td><td>

Option that identifies how the products are related:-   None - Indicates that the bundled products have no relationship.
-   Implicit - Indicates the products grouped in a bundle have an implicit relationship. The target must be a simple product offering, one with no product specification, no child offerings, and no characteristics for the agent to configure.


</td></tr><tr><td>

Order

</td><td>

Numerical order for the options. Options designated with the number 1 appear first in the order. The default value is 10.

</td></tr><tr><td>

Product offering relationship group

</td><td>

Reference to offer relationship groups used to logically group similar product offers.

</td></tr><tr><td>

Unit of measure

</td><td>

Unit of measure for the bundled products. Select a unit of measure, for example Box or Case.

</td></tr><tr><td>

Default

</td><td>

Option indicating that the product offering relationship is the default.

</td></tr><tr><td>

Mandatory

</td><td>

Option indicating that the product offering relationship is mandatory.

</td></tr><tr><td>

Default quantity

</td><td>

Default quantity of the target product offering in the bundle. The default value is 1.

</td></tr><tr><td>

Max quantity

</td><td>

Maximum quantity of products in the bundle. The default value is 1.

</td></tr><tr><td>

Min quantity

</td><td>

Minimum quantity of products in the bundle. The default value is 1. These quantities mean different things depending on whether each relationship is or is not part of a relationship group.

</td></tr><tr><td>

Effective from

</td><td>

Future date on which the product offering is available for quoting or ordering.

</td></tr></tbody>
</table>6.  Select **Save**.

    The relationship is created. Select the relationship on the **Product Offering Relationships** tab to make further changes.

    If the relationship doesn't save, an error message names the problem:

    -   `Source Product Offering of type "Entitlement" cannot have Target Product Offering of type "Product".`: Select an entitlement offering as the target.
    -   `The type of source product offering is entitlement and the relationship type is implicit, the target product offering needs be simple.`: Select a simple product offering as the target, or set the Relationship type to None. This message appears for any implicit relationship with a target that isn't simple, not only for entitlement offerings.

## What to do next

-   [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md)
-   [Add product visuals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-visuals.md)
-   [Add product catalog categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-offering-categories.md)
-   [Add related contracts to product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-related-contracts.md)
-   [Add a unit of measure to a product offering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-unit-of-measure.md)
-   [Create a product offering version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-create-new-version.md)
-   [Create product offering relationship groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-relationship-groups.md)

**Related topics**  


[Using product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)

[Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-managment.md)

