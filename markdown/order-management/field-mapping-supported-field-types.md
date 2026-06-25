---
title: Field mapping supported field types
description: Field types that are supported as source and target fields in solution configuration field mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/field-mapping-supported-field-types.html
release: australia
topic_type: reference
last_updated: "2026-03-26"
reading_time_minutes: 1
keywords: [field mapping, supported field types, source field, target field]
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Field mapping supported field types

Field types that are supported as source and target fields in solution configuration field mappings.

**Note:** Source and target fields must be the same type. For example, a Picklist field cannot be mapped to a Text field.

|Field type|Supported|Notes|
|----------|---------|-----|
|Number|Yes|Can be used as a source or target field. Maps to a Number field on the child blueprint.|
|Text|Yes|Can be used as a source or target field. Maps to a Text field on the child blueprint.|
|Boolean|Yes|Can be used as a source or target field. Maps to a Boolean field on the child blueprint.|
|Picklist|Yes|Can be used as a source or target field. Maps to a Picklist field on the child blueprint.|
|Set \(entire\)|No|Mapping of an entire Set is not supported. Individual fields inside a Set can be used as source fields.|
|Fields inside a Set|Yes \(source only\)|Can be used as a source field. Maps to a compatible field on the child blueprint.|
|Product Picker \(entire\)|No|Mapping of an entire Product Picker is not supported.|
|Product Picker subfields|No|Product Picker subfields cannot be used as source or target fields in any mapping.|
|System fields — as source|Yes|System fields can be used as source fields.|
|System fields — as target|No|System fields cannot be set as target fields.|

**Parent Topic:**[CPQ reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

**Related topics**  


[Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/define-field-mappings-sol-config.md)

[Solution configuration limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

