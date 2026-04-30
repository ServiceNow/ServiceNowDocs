---
title: Create product offering relationship groups
description: Use relationship groups to organize child offer options or relationships into logical groups and set up cardinality rules at the group level in Sales Customer Relationship Management. Groups of product offerings then appear on the product configurator.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create product offerings, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create product offering relationship groups

Use relationship groups to organize child offer options or relationships into logical groups and set up cardinality rules at the group level in Sales Customer Relationship Management. Groups of product offerings then appear on the product configurator.

## Before you begin

Role required: sn\_prd\_pm\_product\_catalog\_admin and sn\_prd\_pm\_product\_catalog\_manager

## About this task

Create product offering relationship groups to organize product bundles into groups in the product configurator.

For example, an internet and OTT Bundle Product Offering is configured to have three product offering relationship groups: modem group, internet group, and the plan streaming channel group.

Bundled product offerings can be other bundles or individual product offerings.

Assign child product offerings in a bundle to the product offering relationship group, which presents the options in logical groups on the product configurator to the agent. The following example shows how product offering groups appear in the product configurator.

![The image shows the product configurator in the Sales Customer Relationship Management application that lets agents select options when building product orders.](../image/l2c-rel-groups-product-configurator.png)

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

2.  Navigate to **Offerings** &gt; **Product Offerings** and select the product offering you’re working with.

3.  Select the **Product Offering Relationship Groups** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the relationship group.|
    |Description|A description of the relationship group.|
    |Product offering|Reference to the current product offering in context.|
    |Order|Order in which the relationship group is displayed in the product configurator.|
    |Max options|Maximum number of options that can be selected in the relationship group during configuration.|
    |Min options|Minimum number of options that must be selected in the relationship group.|

6.  Select **Save**.

    The relationship group is created as part of the product offering.


## What to do next

-   [Create product characteristics and characteristic options](som-product-config-add-characteristics.md)
-   [Add product visuals](som-product-config-add-visuals.md)
-   [Add product catalog categories](som-product-config-offering-categories.md)
-   [Create product offering relationships](som-product-config-offering-relationships.md)
-   [Add related contracts to product offerings](som-product-config-related-contracts.md)
-   [Add a unit of measure to a product offering](som-product-config-add-unit-of-measure.md)
-   [Create a product offering version](som-product-config-create-new-version.md)

