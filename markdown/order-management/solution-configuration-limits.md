---
title: Solution configuration limits
description: Structural limits that apply to solution configurations, including hierarchy depth, total configuration count, and field mapping constraints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/solution-configuration-limits.html
release: australia
topic_type: reference
last_updated: "2026-03-26"
reading_time_minutes: 1
keywords: [solution configuration limits, hierarchy depth, maximum configurations, field mapping constraints]
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Solution configuration limits

Structural limits that apply to solution configurations, including hierarchy depth, total configuration count, and field mapping constraints.

|Limit|Value and notes|
|-----|---------------|
|Maximum hierarchy depth|4 levels, including the solution root. The BOM hierarchy can have an arbitrary depth.|
|Maximum configurations per session|20 total — the solution root plus up to 19 active child configurations across all depths.|
|Circular references|Not permitted. A blueprint cannot appear more than once in any path from a child configuration back to the solution root.|
|Configurable products per action|One configurable product per configurable product action. To add multiple child configurations from a single rule, add multiple configurable product actions to that rule.|
|Field mapping direction|Parent to child only, one level at a time. To continue a mapping across multiple levels, define the mapping on each blueprint in the chain.|
|Field types supported for mapping|Number, Text, Boolean, and Picklist only. For the full list, see [Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/define-field-mappings-sol-config.md) .|
|Sets and Product Pickers in mapping|Mapping of an entire Set or an entire Product Picker is not supported. Fields inside a Set can be mapped. Product Picker subfields cannot be mapped.|
|Reverting a configurable product action|Once a product action is marked as configurable, it cannot be changed back to a standard product action.|

**Parent Topic:**[CPQ reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

**Related topics**  


[Solution configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/solution-configurations.md)

[Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md)

[Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/define-field-mappings-sol-config.md)

