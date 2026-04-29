---
title: Exporting and importing pricing entities
description: As a pricing admin, you can both export and import pricing entities between ServiceNow instances. For example, you can promote pricing entities such as price lists from a non-production instance to a target production instance. Each process involves a separate set of steps.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Exporting and importing pricing entities

As a pricing admin, you can both export and import pricing entities between ServiceNow instances. For example, you can promote pricing entities such as price lists from a non-production instance to a target production instance. Each process involves a separate set of steps.

## Before exporting and importing pricing entities

Before you export your pricing entities to a target instance, note the following prerequisites:

-   **Import product-related entities to your target instance**

    Verify that your product catalog admin has first imported the product catalog base entities, product offering catalog, and product offerings to your target instance. Your pricing entities are associated with product offerings and catalogs, so the offering and catalog information must exist before you import pricing entities. For more information on the product entities that must be imported to your target instance, see [Exporting and importing product catalog entities](export-import-product-catalog-entities.md).

-   **Export the update set for decision table changes to your target instance before exporting the associated pricing matrix**

    If you have a new version of a pricing matrix that has decision table changes, such as a reference to a new product offering, ask your admin to export the system-generated update set that includes the decision table changes to your target instance. Next, you export the new pricing matrix, then import the pricing matrix to your target instance. For more information, see [Export pricing entities](../task/export-pricing-entities.md) and [Import pricing entities](../task/import-pricing-entities.md).


## Export and import process for pricing entities

Follow these steps to export and import pricing entities.

|Step|Description|
|----|-----------|
|[Export pricing entities](../task/export-pricing-entities.md)|Export pricing entities from one instance to another. The entities are exported as JSON and are downloaded to your local download directory.|
|[View export job status](../task/view-export-job-status.md)|Check the state of the export job.|
|[Import pricing entities](../task/import-pricing-entities.md)|Import pricing entities exported as JSON files to another instance.|
|[View import job status](../task/view-import-job-status.md)|Check the state of the import job.|

