---
title: Creating contracts and entitlements using workflows
description: After a product offer is selected by the customer and the product is sold to the customer, this workflow creates contracts and entitlements based on the services associated with that sold product and the extra services that the customer has purchased.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Contracts and Entitlement Workflows, Configure Customer Contracts and Entitlements, Product data, Set up your environment, Configure, Customer Service Management]
---

# Creating contracts and entitlements using workflows

After a product offer is selected by the customer and the product is sold to the customer, this workflow creates contracts and entitlements based on the services associated with that sold product and the extra services that the customer has purchased.

There are the product offering scenarios and their configurations.

|Offering types|Description|
|--------------|-----------|
|Offers for entitlements|The workflow creates entitlement records for such offerings. These entitlements can be associated with existing sold products, install base items, product inventory records, or the customer.|
|Offers for services \(contract lines\)|The workflow enables automatic creation of a customer contract, customer contract lines, and the entitlements for those contract lines.|
|Implicit offerings|Implicit entitlements and customer contract lines are not shown on order lines. These offers can be marked as implicit when they do not need to be configured while capturing the order and are available as part of a package. These entitlements and customer contract lines are automatically created as a part of this workflow.|

## Creating a contract from an order

For every order with multiple product offerings, a single contract with multiple contract lines is created. As part of the order processing, a sold product is generated for every order line.

## Creating contracts from product inventory records

If the system property sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management is set to true, order fulfillment workflows create product inventories based on customer orders, product offerings and specifications. On creation of a product inventory, contract lines and entitlements will be created. When a product inventory undergoes a state change, the associated contract lines and entitlements are synced. For more information, see [Product inventory configurations](../../customer-service-management/concept/product_inventory_configurations.md). Product inventory records trigger updates to contracts and entitlements under the following conditions:

-   Process Telecom Order Line flow: The ADD flow creates contract and entitlement records from the product inventory. The MODIFY flow updates the states of the contract line items and entitlements.
-   Post Process Telecom Top Domain Order flow: The MODIFY flow updates the states, fields, and characteristics for contract line items and entitlements.
-   Product Inventory Operations record: Depending on the scheduled date and time, the DISCONNECT, RESUME, and SUSPEND flows cancels, activates, or suspends the contract line items and entitlements.

## Configuring Customer Life Cycle Workflows Policy decision table

Customer Life Cycle Workflows Policy decision table decides the target entity while renewing and modifying customer contracts, customer contract lines, and entitlements. Based on this decision table, you can create a quote, an order, an opportunity, or an opportunity and a quote together while renewing or modifying a customer contract. For a target entity, you can also select when you want to initiate the renewal of the customer contract.

![Customer Life Cycle Workflows Policy decision table](../images/customer-lc-decision-table-input.png "Inputs in Customer Life Cycle Workflows Policy decision table")

![Customer Life Cycle Workflows Policy decision table](../images/customer-lc-decision-table-conditions.png "Conditions in Customer Life Cycle Workflows Policy decision table")

You can configure rules based on the six available input parameters to a required target entity while renewing and modifying contracts. Select the following values in the Target Entity Name column to create the corresponding target entities.Using Customer Life Cycle Workflows Policy Decision Table 

<table id="table_khy_45b_v2c"><thead><tr><th>

Value

</th><th>

Target Entity

</th></tr></thead><tbody><tr><td>

`sn_ind_tmt_orm_order_line_item`

</td><td>

Order

</td></tr><tr><td>

`sn_quote_mgmt_core_quote_line_item`

</td><td>

Quote

</td></tr><tr><td>

`sn_opty_mgmt_core_opportunity_line_item`

</td><td>

Opportunity**Note:** You cannot create opportunities for modifying process.

</td></tr><tr><td>

`sn_quote_mgmt_core_quote_line_item,sn_opty_mgmt_core_opportunity_line_item`

</td><td>

Opportunity and quote together**Note:** You cannot create opportunities and quotes for modifying process.

</td></tr></tbody>
</table>**Note:** To create an opportunity or opportunity and quote together during renewal, the admin needs to set up the following records:

-   Sales Cycle Type: In the Code field, enter **RENEW** and set the Active option to **True**. For more info, see Create a sales cycle for an opportunity.
-   Opportunity Stage: In the Name field, enter **Develop** and set the Active option to **True**. For more info, see Create opportunity stages.

If the user selects an opportunity and a quote as target entities, a renewal opportunity and a quote is created. The opportunity and the quote are associated to each other.

For any target entity, select one of the following options in the Auto Renewal Initiation column to indicate when you want to automatically renew the contract: 90, 60, 30 days before contract end date or on the contract creation date. For target entity as opportunity and quote together, you can also select the following options to create the renewed opportunity and quote on separate dates:

-   With contract, 12 months before end date respectively: Opportunity is auto renewed on the contract creation date and the quote is renewed 12 months before the contract expiry date.
-   90, 90 days before end date respectively: Opportunity and quote both are renewed 90 days before the contract expiry date.

