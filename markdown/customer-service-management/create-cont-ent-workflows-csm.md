---
title: Creating contracts and entitlements using workflows
description: After a product offer is selected by the customer and the product is sold to the customer, this workflow creates contracts and entitlements based on the services associated with that sold product and the extra services that the customer has purchased.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Contracts and Entitlement Workflows, Configure Customer Contracts and Entitlements, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Creating contracts and entitlements using workflows

After a product offer is selected by the customer and the product is sold to the customer, this workflow creates contracts and entitlements based on the services associated with that sold product and the extra services that the customer has purchased.

There are the product offering scenarios and their configurations:

-   Products with entitlements: From the Offering type list, select **Entitlement**. Make sure the **Create contract** check box is cleared.
-   Service contract lines for service plan: From the Offering type list, select **Entitlement** and select the **Create contract** check box.
-   Service contract lines for subscription plans: From the Offering type list, select **Product** and select the **Create contract** check box.
-   Bundled offerings combining more than one product offering: Select the offering types as needed.

|Offering types|Description|
|--------------|-----------|
|Offers for entitlements|The workflow creates entitlement records for such offerings. These entitlements can be associated with existing sold products, install base items, product inventory records, or the customer.|
|Offers for services \(contract lines\)|The workflow enables automatic creation of a service contract, service contract lines, and the entitlements for those contract lines.|
|Implicit offerings|Implicit entitlements and service contract lines are not shown on order lines. These offers can be marked as implicit when they do not need to be configured while capturing the order and are available as part of a package. These entitlements and service contract lines are automatically created as a part of this workflow.|

## Creating a contract from an order

For every order with multiple product offerings, a single contract with multiple contract lines is created. You can add multiple product offerings from an order to an existing contract. To add a product offering to an existing contract, add the contract reference in the **Existing Contract** field of the order line item.

## Creating contracts from product inventory records

If the system property sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management is set to true, order fulfillment workflows create product inventories based on customer orders, product offerings and specifications. On creation of a product inventory, contract lines and entitlements will be created. When a product inventory undergoes a state change, the associated contract lines and entitlements are synced. For more information, see [Product inventory configurations](../../customer-service-management/concept/product_inventory_configurations.md). Product inventory records trigger updates to contracts and entitlements under the following conditions:

-   Process Telecom Order Line flow: The ADD flow creates contract and entitlement records from the product inventory. The MODIFY flow updates the states of the contract line items and entitlements.
-   Post Process Telecom Top Domain Order flow: The MODIFY flow updates the states, fields, and characteristics for contract line items and entitlements.
-   Product Inventory Operations record: Depending on the scheduled date and time, the DISCONNECT, RESUME, and SUSPEND flows cancels, activates, or suspends the contract line items and entitlements.

## Configuring Customer Life Cycle Workflows Policy decision table

Customer Life Cycle Workflows Policy decision table decides the target entity while renewing and modifying service contracts, service contract lines, and entitlements. Based on this decision table, users can create a quote or an order while renewing or modifying a service contract, service contract line, or an entitlement.

![Customer Life Cycle Workflows Policy decision table.](../images/cust-lifecycle-wf-decisiontable.png "Customer Life Cycle Workflows Policy decision table")

You can configure rules based on the five available input parameters to create quotes while renewing and modifying contracts. Select the value of Target Entity Name as `sn_ind_tmt_orm_order_line_item` to create an order. Select the value of Target Entity Name as `sn_quote_mgmt_core_quote_line_item` to create a quote. If the user selects a quote, the quote is approved and the status changes to **Complete** to create an order. Ensure that you have installed Order Management \(com.sn\_ind\_tmt\_orm\) and Quote Management \(sn\_quote\_mgmt\) plugins to enable selecting the target entity for renewal and modify workflows. Both these plugins will enable users to create a quote or an order while renewing or modifying a service contract, service contract line, or an entitlement.

