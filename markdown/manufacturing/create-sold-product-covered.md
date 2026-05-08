---
title: Create sold product or install base item for contract
description: The customer contracts and entitlements application uses the Sold Product Covered form to add sold products or install base items that are covered to the Customer Contracts and Entitlements entities.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Related list for an install base item, Create an install base item, Set up Manufacturing Commercial Operations, Configure, Manufacturing Commercial Operations]
---

# Create sold product or install base item for contract

The customer contracts and entitlements application uses the Sold Product Covered form to add sold products or install base items that are covered to the Customer Contracts and Entitlements entities.

## Before you begin

Role required: admin

## About this task

Sold products are products and components that have been sold to an account or a consumer and can have multiple contracts. An install base item is an instance of sold product that has been provisioned for an account or consumer.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **MCO Setup** &gt; **Install base** &gt; **Contracts**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_swx_w1h_4fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract

</td><td>

Reference number of the associated service contract.

</td></tr><tr><td>

Sold Product

</td><td>

Products that were sold to a customer.**Note:**

-   The list of sold products is filtered based on the account related to the contract or entitlement.
-   If a product is added, the **Install Base Items** field is automatically removed.
-   If a product isn't listed, you can add it. Select **New** in the Sold Products window. For more information, see Create a sold product.


</td></tr><tr><td>

Install Base Item

</td><td>

The related install base item.**Note:**

-   The list of sold products is filtered based on the account related to the contract or entitlement.
-   If an install base item is added, the **Sold Product** field is automatically removed.
-   If an install base item isn't listed, you can add it. Select **New** in the Install Base Item window. For more information, see [Create an install base item](mco-create-install-base-item.md).


</td></tr><tr><td>

Date added

</td><td>

Date when the product is added to the entity.

</td></tr><tr><td>

Date removed

</td><td>

Date until which the product is active on the entity.

</td></tr></tbody>
</table>4.  Select **Save**.


