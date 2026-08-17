---
title: Advanced product filtering for quotes
description: Advanced product filtering dynamically controls which products appear in the quote catalog based on admin-defined business rules and transaction context in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-advanced-product-filtering.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Advanced product filtering for quotes

Advanced product filtering dynamically controls which products appear in the quote catalog based on admin-defined business rules and transaction context in CPQ.

Advanced product filtering enables administrators to dynamically filter the product catalog using business rules. Filtering logic runs during the Add Lines operation in ServiceNow Quote Experience. The feature supports real-time data synchronization from managed tables and maintains sub-second search performance even with catalogs of more than a million products.

## Use cases

Advanced product filtering is useful when catalog visibility must be controlled based on factors such as:

-   Country, region, or compliance constraints
-   Product availability or configuration status
-   Transaction-specific input fields, such as customer segment or deal type

## Key features

|Feature|Description|
|-------|-----------|
|Advanced filter rule search|Contextual product filtering with sub-second results.|
|Real-time data sync|Managed table and rule changes take effect immediately without redeployment.|
|Rule-based filtering engine|Include and exclude products using dynamic logic.|
|No-code admin experience|UI-based rule builder with column mapping and conditions.|
|Catalog scale|Performance maintained with more than one million products.|

## Prerequisites

The following must be enabled before using advanced product filtering.

-   The tenant setting `enableCatalogFilter` must be set to ON. Submit a request to DevOps to enable this setting.
-   The ServiceNow Quote Experience module must be enabled to ensure the Add Lines operation uses the defined product filter rules.

## Managed table data synchronization

Product filter rules that reference managed tables do not need to be redeployed when only the managed table data changes. This behavior is enabled when the `filterrules.scheduler.enable = true` setting is active. The system syncs updated managed table data every 15 minutes, making the latest information available during product filtering.

**Note:** Any change made to a product filter rule itself — not just the referenced table data — must be redeployed for it to take effect.

