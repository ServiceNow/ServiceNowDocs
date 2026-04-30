---
title: Exporting and importing product catalog entities
description: As a product catalog admin, you can both export and import product catalog entities between ServiceNow instances. For example, you can promote catalog entities from a non-production instance to a production instance. Each process involves a separate set of steps.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Exporting and importing product catalog entities

As a product catalog admin, you can both export and import product catalog entities between ServiceNow instances. For example, you can promote catalog entities from a non-production instance to a production instance. Each process involves a separate set of steps.

## Managing product catalog entities

The first step before exporting product catalog entities is adding the **Code** field values to product catalog entities. The **Code** field value is used by the system to determine whether an entity is to be inserted or updated in the target instance.

You then choose the product catalog entities to be exported and run the export process.

After you export your product catalog entities, certain base entities must be imported first to your target instance, such as characteristics, characteristic options, template, and Unit of Measure \(UOM\), since they're referenced by product offerings, product specifications, and service specifications. For this reason, import certain product catalog entities to your target instance in the following order:

1.  Import the exported base entities.
2.  Import the product offering catalog if you're exporting product offerings.
3.  Import product offerings and product specifications.

## Export and import process

Follow these steps to export and import product catalog entities.

|Step|Description|
|----|-----------|
|[Add Code field values to catalog entities](../task/run-fix-script-sched-job-export.md)|Add the **Code** field values for the main product catalog entities on your source and target instances.|
|[Export product catalog entities](../task/export-product-catalog-entities.md)|Export product catalog entities from one instance to another. The entities are exported as JSON and are downloaded to your local download directory.|
|[View export job status](../task/view-export-job-status.md)|Check the state of the export job.|
|[Import product catalog entities](../task/import-product-catalog-entities.md)|Import product entities exported as JSON files to another instance.|
|[View import job status](../task/view-import-job-status.md)|Check the state of the import job.|

