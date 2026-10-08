---
title: Modify a product inventory asset
description: Modify a Product Inventory asset in the configurator to add or remove products, change attributes, and save changes during an amend flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/modify-product-inventory-asset.html
release: australia
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 3
breadcrumb: [Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Modify a product inventory asset

Modify a Product Inventory asset in the configurator to add or remove products, change attributes, and save changes during an amend flow.

## Before you begin

The Product Inventory asset you want to modify must exist and be accessible in your instance.

Each child offer in the original purchase order must have a quantity of 1. In a correctly fulfilled order, each child offer produces exactly one Product Inventory record. MACD \(Move, Add, Change, Disconnect\) is not supported when multiple Product Inventory records exist for the same child offer under the same parent offer.

**Role required:** \[Add appropriate role\]

## About this task

When a product is configured and provisioned, the system creates individual Product Inventory records — one per item — through a decomposition and enrichment process. Each item is independently addressable. You can open a single record in the configurator, make targeted changes, and save the result.

This procedure applies to the following configurable product offer types:

-   Configurable product offers with an offer hierarchy and a matching spec hierarchy, for example, Wireless Subscription 4
-   Configurable product offers with a spec hierarchy and no matching offer hierarchy, for example, SDWAN

## Procedure

1.  Navigate to the Product Inventory asset you want to modify.

2.  Open the Product Inventory record.

3.  Select to open the record in the configurator.

    The configurator loads the Product Inventory lines. Each line appears under a summary line that shows the total quantity for that product.

    **Note:** If multiple Product Inventory records exist for the same child offer — which can occur when a child offer was originally ordered with a quantity greater than 1 — the MACD does not proceed and the following message is displayed: `MACD is currently not supported when one or more child offers have quantity greater than 1.` Contact your administrator to resolve the inventory records before retrying.

4.  Make one or more of the following changes in the configurator:

    -   To add an optional product offering or specification, select it from the available options. The system sets the line type to **New** and the line action to **Add**.
    -   To remove an optional product offering or specification, deselect or disconnect it. The system sets the line type to **Cancel** and the line action to **Disconnect**.
    -   To change a configuration attribute, update the characteristic value on the relevant BOM item — for example, change a service tier or color attribute. The system sets the line type to **Amend** and the line action to **Change**.
    **Note:** The quantity for each child offer and specification is read-only during a Product Inventory MACD session. You can't change the quantity of a provisioned item in this flow.

    The **Upsell** line type doesn't apply to Product Inventory MACD flows. For example, when you move from Mobile S to Mobile M, the system sets the line type on Mobile M to **New** and the line action to **Add**.

    **Note:** The effective date is not presented during a Product Inventory MACD session and doesn't affect contract start or end dates. If the effective date field is visible in your instance, contact your administrator to remove it by updating the configurator layout.

5.  Select **Save** to save the updated configuration.

    No line splits occur when saving a Product Inventory MACD configuration, unlike MACD flows for Sold Products.

6.  Select **Submit** to complete the amend flow.

    Removed Product Inventory lines are submitted with a **Cancel** line type and **Disconnect** line action. The fulfillment process determines when the changes take effect.


## Result

Each modified Product Inventory line creates a corresponding transaction line. The following table shows the expected line type and line action for each change.

|Change|Line type|Line action|
|------|---------|-----------|
|Added a product offering or specification|New|Add|
|Removed a product offering or specification|Cancel|Disconnect|
|Changed a characteristic value|Amend|Change|

