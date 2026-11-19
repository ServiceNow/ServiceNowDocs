---
title: Create product offerings
description: Create and publish a product offering in Sales Customer Relationship Management. Product offerings represent entities that are orderable from the provider of the catalog and includes pricing information. Once published, product offerings are available to agents as they create leads, opportunities, quotes, and orders and to customers placing orders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/som-create-product-offering.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create product offerings

Create and publish a product offering in Sales Customer Relationship Management. Product offerings represent entities that are orderable from the provider of the catalog and includes pricing information. Once published, product offerings are available to agents as they create leads, opportunities, quotes, and orders and to customers placing orders.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin or sn\_prd\_pm.product\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Offerings** &gt; **Product Offering** and select **New**.

    **Note:** You can also create a product offering from the product specification.

4.  In the Details tab, fill in the fields.

<table id="table_customer_order_workspace"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-assigned number for the product offering.

</td></tr><tr><td>

Name

</td><td>

Alternative name for the product offering to differentiate it from similar product names.

</td></tr><tr><td>

Display name

</td><td>

Name of the product offering to be added.

</td></tr><tr><td>

Code

</td><td>

System-generated code based on the product name. Although system generated, you can edit the code to represent a SKU or any other industry-specific product codes. The code can include any character except an asterisk \(\*\) or a percent sign \(%\). When you save, letters are converted to uppercase and any \* or % characters are removed. For example, `bl-ui.test/1` is saved as `BL-UI.TEST/1`, and `BL*UI` is saved as `BLUI`. The code must be unique for the offering version. If the saved code matches an existing code, the record isn't saved; enter a different code.

</td></tr><tr><td>

Product family

</td><td>

The product offering family to which this product belongs. Select the product offering family, which is a collection of products that share similar or common features. A product offering can belong to a single family only.

</td></tr><tr><td>

Sellable

</td><td>

Option, if selected, indicates that the product offering can be sold as a standalone item. If not selected, the product offering can be sold as part of bundle but not as a standalone item.

</td></tr><tr><td>

Configuration Status

</td><td>

Indicates the status of the product offering: -   None: The product offering is not configured. This is the default value.
-   Creating: Creation of the product offering in ServiceNow CPQ Administration is in progress.
-   Created: The product offering is created in ServiceNow CPQ Administration and is available as a blueprint.
-   Error: An error occurred while creating blueprint for the product offering in ServiceNow CPQ Administration.


</td></tr><tr><td>

Configurable

</td><td>

Option that indicates the product is customizable and can be configured by agents and customers using the CPQ Configurator, if implemented in your organization. For more information, see [Using the ServiceNow CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-servicenowcpq.md).

</td></tr><tr><td>

Allow multiple configurations

</td><td>

Option that enables agents or customers to create and manage multiple configurations of a child product offering so each configuration can be handled as a separate line item in a configurable product. **Note:** If the product has an associated product specification, this option is enabled automatically and can't be deselected.

For more information on how multiple configurations work in configurable products, see [Multiple configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/multiple-child-offering-configurations.md).

</td></tr><tr><td>

Transient

</td><td>

Option indicating that the product is for one-time use. **Note:** When the order for a transient product is completed, the sold product or product inventory record for the product is set to an Inactive state, to differentiate the product from persistent products.

-   Move, Add, Change, Disconnect \(MACD\) actions can't be performed on the sold product or product inventory records of transient product offerings.
-   The **Create contract** option is not applicable to transient product offerings.
For more information on transient products, see [Defining transient products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configuring-transient-products.md).

</td></tr><tr><td>

Description

</td><td>

Short description of the product offering. The description helps the agent identify the product when creating a lead, opportunity, quote, or order.

</td></tr><tr><td>

State

</td><td>

State of the product offering. States include In Draft, Published, Retired, and Archived. You can update product offerings In Draft state.

</td></tr><tr><td>

Start date

</td><td>

Date and time that the product offering is available for Sales Customer Relationship Management applications. Select the Calendar icon \[Omitted image "field-calendar.png"\] Alt text: to choose the start date and time, then select **OK**.

</td></tr><tr><td>

End date

</td><td>

Date and time that the product offering is deleted from Sales Customer Relationship Management applications. Select the Calendar icon \[Omitted image "field-calendar.png"\] Alt text: to choose the end date and time, then select **OK**.

</td></tr><tr><td>

Offering type

</td><td>

Type of product offer. Select one of the following:-   Product: A product entity that an agent or customer can add to a Sales CRM transaction. For example, agents can add products to a lead, opportunity, quote, or order from the CRM Workspace. Customers can add products to an order from the Business Portal.
-   Entitlement: An entity such as a warranty or subscription that can be added to a lead, opportunity, quote, or order by an agent.
An entitlement offering can have only entitlement offerings as child offerings. A product offering can have both product and entitlement child offerings. For example, a router product offering can include a warranty entitlement offering as a child, but a warranty entitlement offering can't include the router.

If you add a product offering as a child of an entitlement offering, the relationship isn't saved and you see this error: `Source Product Offering of type "Entitlement" cannot have Target Product Offering of type "Product".` To fix it, select an entitlement offering as the target offering, or change the parent offering type to Product.

</td></tr><tr><td>

Offering sub-type

</td><td>

Category of the offering. This field is optional, has no default value, and is available for both the Product and Entitlement offering types. For example, select Subscription for a product offering that is billed as a software subscription, or Warranty for a warranty entitlement offering. Select one of the following:-   Warranty
-   Extended warranty
-   License
-   Subscription


</td></tr><tr><td>

Distribution channel

</td><td>

Option to set and lock in a distribution channel. For example, you can specify web as a channel. You can specify multiple channels.If you're using the Service Exchange Order Management for Providers application, enter Service Exchange.

</td></tr><tr><td>

Owner

</td><td>

Person responsible for the product offering.

</td></tr><tr><td>

Product specification

</td><td>

Functional view of a product offering that drives order fulfillment. Select the product specification associated with the product offering. **Note:** Only published specifications appear.

</td></tr><tr><td>

Product model

</td><td>

Name of the product model.**Important:** If you select a product model and save the offering, all relationship groups of this product offering are deleted. Its child offering relationships are no longer assigned to a relationship group. To keep relationship groups, don't select a product model for the offering.

</td></tr><tr><td>

Copy child specification characteristics

</td><td>

Option that when selected copies all child specification characteristics in a specification hierarchy. For example, if the product offer has an associated product specification, this option indicates that the characteristics are inherited from the child specifications in addition to the parent specification.This field displays when a product specification for a composite product is entered and the product offering is saved.

</td></tr><tr><td>

Pricing method

</td><td>

Pricing method for the product. This field is optional. In a bundle, child offerings can use a different pricing method from the parent offering. For example, a bundle can include a router with a one-time fee and an internet service with a recurring fee. Select one of the following:-   One-time: A single fee for the product.
-   Recurring: A fee that occurs at scheduled intervals. You can set the **Periodicity** for a recurring fee.
**Note:** If you're creating a configurable product offering that can have ramps, select Recurring as the **Pricing method** so that the **Enable ramps** option can be selected.

</td></tr><tr><td>

Periodicity

</td><td>

Recurring pricing: Monthly or annually.

</td></tr><tr><td>

Monthly recurring charges

</td><td>

Charges that are applied monthly.

</td></tr><tr><td>

Non recurring charges

</td><td>

Charges that are applied once. Supported for backward compatibility. Use price lists to define prices.

</td></tr><tr><td>

Enable ramps

</td><td>

Option that enables the ramp feature, where sales agents can create ramps for transaction lines, such as quotes, to schedule price and quantity increases over certain time periods. To learn more, see [Price and quantity ramps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/defining-products-with-ramps.md).

</td></tr><tr><td>

Create contract

</td><td>

Option indicating to agents that entitlement contracts can be added to the product order. If selected, service contracts are created after order fulfillment. Used when entitlements are managed as contracts.**Note:** For transient product offerings, this option isn’t available.

</td></tr><tr><td>

Contract term

</td><td>

Length of the contract:-   12 months
-   24 months
-   36 months
-   48 months
-   60 months


</td></tr><tr><td>

Version

</td><td>

Version number that is assigned to this product offering version.

</td></tr><tr><td>

Initial version

</td><td>

Name of the initial version of the product offering.

</td></tr><tr><td>

Previous version

</td><td>

Several versions of a product offering can exist. This field lets you view previous versions.

</td></tr></tbody>
</table>5.  Select **Save** and then select **Publish**.


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

