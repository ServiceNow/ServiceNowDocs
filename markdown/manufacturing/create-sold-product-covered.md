---
title: Create sold product
description: Create a sold product or an install base item for a contract. The customer contracts and entitlements application use the Sold Product Covered form to add sold products \(install base items\) that are covered.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Related list for an install base item, Create an install base item, Set up MCO, Configure, Manufacturing Commercial Operations]
---

# Create sold product

Create a sold product or an install base item for a contract. The customer contracts and entitlements application use the Sold Product Covered form to add sold products \(install base items\) that are covered.

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

-   The sold products list is filtered by the account linked to the contract or entitlement.

-   The **Sold Product** field is automatically removed, when an install base item is added,
-   You can add a sold product, if it isn't listed. Select **New** in the Install Base Item window. For more information, see [Create a sold product](https://www.servicenow.com/docs/access?context=create-sold-item&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).


</td></tr><tr><td>

Install Base Item

</td><td>

The related install base item.**Note:**

-   The list of sold products is filtered based on the account related to the contract or entitlement.
-   The **Install Base Item** field is automatically removed, when an install base item is added,
-   You can add an install base item if it isn't listed. Select **New** in the Install Base Item window. For more information, see [Create an install base item](mco-create-install-base-item.md).


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


