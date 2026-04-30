---
title: Exporting and importing product catalog entities
description: As a product catalog admin, you can both export and import product catalog entities between ServiceNow instances. For example, you can promote catalog entities from a non-production instance to a production instance. Each process involves a separate set of steps.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Exporting and importing product catalog entities

As a product catalog admin, you can both export and import product catalog entities between ServiceNow instances. For example, you can promote catalog entities from a non-production instance to a production instance. Each process involves a separate set of steps.

## Overview

You choose the product catalog entities to be exported. However, after you export your product catalog entities, certain base entities must be imported first to your target instance, such as characteristics, characteristic options, template, and Unit of Measure \(UOM\), since they're referenced by product offerings, product specifications, and service specifications. For this reason, import certain product catalog entities to your target instance in the following order:

1.  Import the exported base entities.
2.  Import the product offering catalog if you're exporting product offerings.
3.  Import product offerings and product specifications.

## Export and import process

Follow these steps to export and import product catalog entities.

|Step|Description|
|----|-----------|
|[Export product catalog entities](../task/export-product-catalog-entities.md)|Export product catalog entities from one instance to another. The entities are exported as JSON and are downloaded to your local download directory.|
|[View export job status](../task/view-export-job-status.md)|Check the state of the export job.|
|[Import product catalog entities](../task/import-product-catalog-entities.md)|Import product entities exported as JSON files to another instance.|
|[View import job status](../task/view-import-job-status.md)|Check the state of the import job.|

**Note:** Your system administrator must [add the Code field values to your main product catalog entities](../task/run-fix-script-sched-job-export.md) on your source and target instances if they weren't added after upgrading to the Washington DC release.

