---
title: Field mapping in solution configuration
description: Field mapping defines how field values pass from a parent blueprint to a child blueprint when a solution configuration session is running.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/field-mapping-in-solution-configuration.html
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Solution configurations, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Field mapping in solution configuration

Field mapping defines how field values pass from a parent blueprint to a child blueprint when a solution configuration session is running.

When you configure a configurable product action, you can define field mappings that specify which parent fields send their values to which child fields. Field mapping runs when a child configuration is created and again whenever a mapped source field changes.

Field mapping is directional: values flow only from parent to child, one level at a time. To continue mapping across multiple levels, define the mappings on each blueprint in the chain.

## Supported field types

You can map fields of the same type only. The following field types are supported:

-   Number
-   Text
-   Boolean
-   Picklist

## Restrictions

-   Target fields are read-only in the child configuration during a session. The child buyer cannot change a value that was mapped from the parent.
-   System fields can act as source fields, but cannot be set as target fields.
-   Fields inside a Set can be mapped to a field on the child blueprint.
-   Mapping of an entire Set or an entire Product Picker is not supported.
-   Product Picker subfields cannot be mapped to a field on the child blueprint.

**Related topics**  


[Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/define-field-mappings-sol-config.md)

[Field mapping supported field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md)

