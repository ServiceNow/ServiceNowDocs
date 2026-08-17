---
title: Solution configuration terminology
description: Terms used in solution configurations and their definitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/solution-configuration-terminology.html
release: australia
topic_type: reference
last_updated: "2026-03-26"
reading_time_minutes: 1
keywords: [solution configuration, terminology, glossary]
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Solution configuration terminology

Terms used in solution configurations and their definitions.

|Term|Definition|
|----|----------|
|Solution|The collection of blueprints and configurations linked together in a single configuration session. A configuration becomes a solution when at least one child configuration is added.|
|Solution root|The top-level configurable product in a solution. This is the product a buyer launches to start the session. All other configurations in the session are children of the solution root.|
|Solution hierarchy|The parent-child relationship between configurable products in a given solution. The solution hierarchy is independent of the BOM hierarchy.|
|Parent blueprint|A blueprint that contains a rule with a configurable product action targeting another blueprint. A parent blueprint can also be a child of another blueprint.|
|Child blueprint|A blueprint used to create a child configuration. A child blueprint must have a valid configurable product associated with it. A child blueprint can also be a parent of another blueprint.|
|Configurable product action|An extension of the product action that defines the child blueprint, the configurable product, and optional field mappings.|
|Field mapping|A definition of which fields pass data between blueprints. Data flows from the source field on the parent blueprint to the target field on the child blueprint.|
|Source field|The field on the parent blueprint whose value is passed through a field mapping.|
|Target field|The field on the child blueprint that receives the value from the source field through a field mapping. Target fields are read-only during a configuration session.|
|Solution BOM|The consolidated bill of materials that aggregates all products added across every configuration in the session, including children and grandchildren. The solution BOM is returned when a solution is saved.|

**Parent Topic:**[CPQ reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

**Related topics**  


[Solution configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/solution-configurations.md)

[Field mapping in solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/field-mapping-in-solution-configuration.md)

[Bill of Materials in solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/bill-of-materials-in-solution-configuration.md)

