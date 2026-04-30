---
title: Exporting and importing pricing entities
description: As a pricing admin, you can both export and import pricing entities between ServiceNow instances. For example, you can promote pricing entities such as price lists from a non-production instance to a production instance. Each process involves a separate set of steps.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Exporting and importing pricing entities

As a pricing admin, you can both export and import pricing entities between ServiceNow instances. For example, you can promote pricing entities such as price lists from a non-production instance to a production instance. Each process involves a separate set of steps.

You choose the pricing entities, such as price lists, to be exported. Before you export your pricing entities to a target instance, be sure that your product catalog admin has first imported the product catalog base entities, product offering catalog, and product offerings to your target instance. Your pricing entities are associated with product offerings and catalogs, so the offering and catalog information must exist before you import pricing entities. For more information on the product entities that must be imported to your target instance, see [Exporting and importing product catalog entities](export-import-product-catalog-entities.md).

## Export and import process for pricing entities

Follow these steps to export and import pricing entities.

|Step|Description|
|----|-----------|
|[Export pricing entities](../task/export-pricing-entities.md)|Export pricing entities from one instance to another. The entities are exported as JSON and are downloaded to your local download directory.|
|[View export job status](../task/view-export-job-status.md)|Check the state of the export job.|
|[Import pricing entities](../task/import-pricing-entities.md)|Import pricing entities exported as JSON files to another instance.|
|[View import job status](../task/view-import-job-status.md)|Check the state of the import job.|

