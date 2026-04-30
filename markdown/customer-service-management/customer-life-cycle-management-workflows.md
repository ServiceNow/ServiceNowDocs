---
title: Customer Life Cycle Management Workflows
description: Manage the life cycle of your sold products by activating the Customer Life Cycle Management Workflows \(com.snc.customer\_lifecycle\_mgmt\_workflows\) application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Customer Life Cycle Management Workflows

Manage the life cycle of your sold products by activating the Customer Life Cycle Management Workflows \(com.snc.customer\_lifecycle\_mgmt\_workflows\) application.

## Overview

The Customer Life Cycle Management Workflows \(com.snc.customer\_lifecycle\_mgmt\_workflows\) application enables you to update the existing configurations, and to modify, suspend, resume, or disconnect the sold products and their complete hierarchy. The workflows are built and composed by using the lead-to-cash transactional operations like Effect, Create Instance, Delta, and Commit Instance. To learn more about the transactional operations of the Lead to Cash Core \(com.snc.l2c\_core\) plugin, see [Sales and Order Management workflows](lead-to-cash-workflows.md).

## Plugins for the Customer Life Cycle Management Workflows

The following table lists the required plugins for the Life Cycle Management Workflows plugin.

<table id="table_l4p_23q_b1c"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service Install Base Management \(com.snc.install\_base\)

</td><td>

Enables customers to capture the current state of a customer's install base and establish the relationship to any downstream entities that might impact their functioning.To learn more about install base management, see [Configure install base](../task/configure-install-base.md).

</td></tr><tr><td>

Product Catalog Management Core\(com.sn\_prd\_pm\)

</td><td>

Enables companies to define the products and services they market, sell, and deliver to customers.To learn more about product catalogs, see [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).

</td></tr><tr><td>

Lead to Cash Core\(com.snc.l2c\_core\)

</td><td>

Enables customers to compose and build the workflows for various entities. To learn more about the Lead to Cash Core plugin, see [Sales and Order Management workflows](lead-to-cash-workflows.md).

</td></tr></tbody>
</table>## Life Cycle workflows and configurations

Perform the **Modify**, **Suspend**, **Resume**, and **Disconnect** declarative actions on the complete hierarchy of the sold products.These actions will transform and maintain their state and characteristics. You can perform these actions on the sold product entities to update the existing products or services. The declarative actions are available on the sold product related list on the account detail page on Configurable Workspace.

**Note:** The declarative actions with the sold product to order flow are available only if the Order Management \(com.sn\_ind\_tmt\_orm\) plugin is installed.

The Sold Product related list on the Accounts page displays all the sold products regardless of the product offer having a product specification. You can also select a sold product with a product specification associated to the product offering and perform any of the MACD flows. Ensure to upgrade to Xanadu to perform the modify, suspend, resume, and disconnect actions on product offerings that have a specification associated with it.

**Note:** The **Modify**, **Suspend**, **Resume**, and **Disconnect** actions are disabled if Product Inventory records are selected.

Workflows

Multiple sub-flows are based on the modify, suspend, resume, and disconnect actions that help to update the sold products and their configurations. The flows are based on a set of entity configurations that are shipped when you activate the Customer Life Cycle Management Workflow plugin.

The following table lists the flows for the declarative actions.

<table id="table_swj_wyc_d1c"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sold product to Suspend order

</td><td>

This flow is responsible for creating a suspend order when the **Suspend** action is triggered on a sold product.

</td></tr><tr><td>

Sold product to Resume order

</td><td>

This flow is responsible for creating a resume order when the **Resume** action is triggered on a sold product.

</td></tr><tr><td>

Sold product to Disconnect order

</td><td>

This flow is responsible for creating a disconnect order when the **Disconnect** action is triggered on a sold product.

</td></tr><tr><td>

Add order to sold product

</td><td>

This flow is responsible for creating a sold product order when order is moved to completed.**Note:** The sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management property is set to **False** by default with the Order Management \(com.sn\_ind\_tmt\_orm\) plugin. However, if the Order Management for Telecom, Media and Tech \(com.sn\_om\_tmt\) plugin is installed, the property value is set to **True**.

If the property value is false, a record is created in the sold product \(sn\_install\_base\_sold\_product\) table. If the property value is true, a record is created in the Product inventory \(sn\_prd\_invt\_product\_inventory\) table.

</td></tr><tr><td>

Modify order to sold product

</td><td>

The sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management property is set to **False** by default with the Order Management \(com.sn\_ind\_tmt\_orm\) plugin. However, if the Order Management for Telecom, Media and Tech \(com.sn\_om\_tmt\) plugin is installed, the property value is set to **True**.If the property value is false, a record is created or updated in the sold product \(sn\_install\_base\_sold\_product\) table. If the property value is true, a record is created or updated in the Product inventory \(sn\_prd\_invt\_product\_inventory\) table.

</td></tr><tr><td>

Suspend order to sold product

</td><td>

This flow is responsible for suspending a sold product on completion of an order.

</td></tr><tr><td>

Resume order to sold product

</td><td>

This flow is responsible for resuming a sold product on completion of an order.

</td></tr><tr><td>

Disconnect order to sold product

</td><td>

This flow is responsible for disconnecting a sold product on completion of an order.

</td></tr></tbody>
</table>**Note:** The last five flows in the above table are disabled if the 'sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management' property is set to true.

**Note:** The back and forth flow of the data \(from a sold product to an order, an order to a sold product\) happens with the help of a set of entity configurations.

Configurations

Configurations are a set of end-to-end flows that enable the data to flow from one entity to the other. The subflows that are triggered with each declarative action are based on the configurations that are listed in the following table.

|Configuration|Configuration ID|Source Entity|Target Entity|
|-------------|----------------|-------------|-------------|
|Sold product to Order|sn\_l2c-cust\_flows\_sp\_to\_order|Sold product|Order|
|Order to Sold Product|sn\_l2c\_cust\_flows\_order\_to\_sp|Order|Sold product|

To learn more about the configurations, see [Entity configuration and mapping](../reference/entity-configuration-and-mapping.md).

**Related topics**  


[Modify a sold product and hierarchy](../task/modify-a-sold-product.md)

[Modify a sold product to create a quote](../task/modify_a_sold_product_to_create_a_quote.md)

[Resume a single sold product](resuming_sold_products.md#)

[Resume multiple sold products](resuming_sold_products.md#)

[Disconnect a single sold product](disconnecting_sold_products.md#)

[Disconnect multiple sold products](disconnecting_sold_products.md#)

[Suspend a single sold product](supending_sold_products.md#)

[Suspend multiple sold products](supending_sold_products.md#)

