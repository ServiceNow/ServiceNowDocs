---
title: Product and capability usage records
description: The product and capability usage records are automatically created and updated when changes occur in sold product configurations, capability mappings, or in the data context engine.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a product capability, Customer success, Configure, Customer Success Management]
---

# Product and capability usage records

The product and capability usage records are automatically created and updated when changes occur in sold product configurations, capability mappings, or in the data context engine.

Product and capability usage records are created or updated when:

-   A record is added or modified in the Applicable Sold Products table. If product capability records for the sold product exist, corresponding capability usage records are created.
-   The Adoption score for a sold product is calculated. A Product Usage record is created for the sold product and the Adoption score field is updated.
-   A new active record is added to the Product Capability table. A capability usage record is created and the Total Capabilities in Use field is updated in the corresponding Product Usage record.

## Product Usage table

Product usage data provides insights into how customers interact with a product. This table contains the following fields:

<table id="table_lwb_52n_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company

</td><td>

The name of the account associated with the sold product.

</td></tr><tr><td>

Customer priority

</td><td>

The customer priority for this product.-   Critical
-   High
-   Moderate
-   Nice to have
-   Not required

</td></tr><tr><td>

Business criticality

</td><td>

The business criticality for this product.-   Critical
-   High
-   Moderate
-   Nice to have
-   Not required

</td></tr><tr><td>

Asset

</td><td>

Asset related to this product.

</td></tr><tr><td>

Sold product

</td><td>

The sold product for which the product usage data is being calculated.

</td></tr><tr><td>

Install base item

</td><td>

The install base item for which the product usage data is being calculated.

</td></tr><tr><td>

Activation status

</td><td>

Indicates if the product is in use.

</td></tr><tr><td>

Usage plan

</td><td>

Usage plan for this product.-   No plan
-   Planned
-   Activated
-   Deactivated

</td></tr><tr><td>

Total child products

</td><td>

The number of child products available.

</td></tr><tr><td>

Child products in use

</td><td>

Child products that are already being used.

</td></tr><tr><td>

Total capabilities

</td><td>

Total number of capabilities available.

</td></tr><tr><td>

Capabilities in use

</td><td>

The number of capabilities

</td></tr><tr><td>

Adoption score

</td><td>

Calculated adoption score for this product.

</td></tr><tr><td>

Perceived adoption score

</td><td>

Perceived adoption score for this product.

</td></tr><tr><td>

Breadth product score

</td><td>

Child products in use divided by the Total no of child products.

</td></tr><tr><td>

Monthly active users

</td><td>

Number of monthly active users.

</td></tr><tr><td>

Licenses used

</td><td>

Number licenses in use.

</td></tr><tr><td>

Transactions

</td><td>

Number of transactions for this product.

</td></tr></tbody>
</table>## Product Capability Usage table

Product capabilities usage data provides insights into how a specific capability is being used. This table contains the following fields:

<table id="table_vl4_wfn_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company

</td><td>

The name of the account associated with the sold product.

</td></tr><tr><td>

Capability

</td><td>

The capability for the product.

</td></tr><tr><td>

Asset

</td><td>

Asset related to this record.

</td></tr><tr><td>

Sold product

</td><td>

The sold product for which the capability usage data is being calculated.

</td></tr><tr><td>

Install base item

</td><td>

The Install base item for which the product capability usage data is being calculated.

</td></tr><tr><td>

Activation status

</td><td>

Indicates if the capability is in use.

</td></tr><tr><td>

Usage plan

</td><td>

Usage plan for this capability.-   No plan
-   Planned
-   Activated
-   Deactivated

</td></tr><tr><td>

Customer priority

</td><td>

The customer priority for this capability.-   Critical
-   High
-   Moderate
-   Nice to have
-   Not required

</td></tr><tr><td>

Business criticality

</td><td>

The business criticality for this capability.-   Critical
-   High
-   Moderate
-   Nice to have
-   Not required

</td></tr><tr><td>

Adoption score

</td><td>

Calculated adoption score for this capability.

</td></tr></tbody>
</table>To configure how this usage data is displayed in the workspace, see [Configure DCE Visualizations](../task/account-lifecycle-configure-dce-visual.md).

**Parent Topic:**[Create a product capability](../task/account-lifecycle-create-prod-cap.md)

