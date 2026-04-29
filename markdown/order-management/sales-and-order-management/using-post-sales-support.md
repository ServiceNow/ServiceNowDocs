---
title: Using Customer Contracts and Entitlements
description: Learn how consumers, managers, agents, and administrators use the Customer Contracts and Entitlements application to generate customer contracts and contract lines.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, price, quote apps, Use, Sales and Order Management]
---

# Using Customer Contracts and Entitlements

Learn how consumers, managers, agents, and administrators use the Customer Contracts and Entitlements application to generate customer contracts and contract lines.

Customer contracts, customer contract lines, and entitlements can be created in the following ways:

-   Via workflows: You can create customer contracts, customer contract lines, and entitlements by using the contracts and entitlements workflow. For more information, see [Creating contracts and entitlements using workflows](create-cont-ent-workflows-csm.md).

    **Note:** When a customer contract line or entitlement is created via the Sales and Order Management workflow, the account/consumer/household details are copied from the sold product and it inherits the state of the sold product. Further, when the state of the contract line changes, the same state is synced back to the parent sold product.

-   Via API integrations:
    -   [Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)
    -   [Entitlement API](https://www.servicenow.com/docs/access?context=entitlement-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

You can perform the following features using Customer Contracts and Entitlements Workflows:

-   Standard renewals: A standard renewal occurs when a contract is renewed on schedule. The system creates a new contract with the existing contract lines, entitlements, and child records, with the new term starting immediately after the original contract ends. There is no pricing adjustments that are needed beyond the agreed renewal terms.
-   Non-standard renewals: A non-standard renewal occurs when a contract is renewed outside of the renewal cycle. This covers three scenarios: an early renewal, a late renewal, and a short-term renewal. For more info, see [Renew a customer contract line](../task/cce-renew-service-contract-line.md).
-   Consolidation of Contracts: You can merge multiple contracts for the same account into a single contract. Use contract consolidation during renewal to align contract terms and combine subscriptions into one contract. For more info, see [Renew a customer contract line](../task/cce-renew-service-contract-line.md).
-   Upsell or Downsell: You can add or reduce the quantity to an existing contract during its term.

-   **[Add a sold product or install base item to a customer contract](../task/add-products-service-contract.md)**  
Add the sold products or the install base items covered to customer contracts, contract lines, or entitlements.
-   **[Record the usage on the entitlement](../task/record-usage-entitlement.md)**  
Record the consumption or usages made out of the total characteristic quantities allotted for an entitlement.

**Parent Topic:**[Using configure, price, quote applications](../../tmt-order-mgt/concept/using-cpq.md)

