---
title: Edge status configuration form
description: Use the Edge configuration form to configure the Edge status settings for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2025-11-07"
reading_time_minutes: 1
breadcrumb: [Configure the Edge status configurations, Configure the Edge configurations, Configure the Node configurations, Configure the Node relationship configurations, Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Edge status configuration form

Use the Edge configuration form to configure the Edge status settings for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.

|Field|Description|
|-----|-----------|
|Edge configuration|Edge configuration to be defined between two specific entities.|
|Relationship table|Relationship table for the source and target tables. For example, Entity hierarchy \[sn\_grc\_m2m\_profile\_profile\]|
|Conditions|Entity and related list conditions. Once the conditions are satisfied, the edge status is updated and reflected in the Nexus map.|
|Color|Color to be displayed for the edge status once the conditions are satisfied, for example, Critical or Magenta.|
|Edge type|Edge type to be defined for the node, for example, Solid.|
|Label|Label to be defined for the node, for example, Primary.|
|Order|Order assigned to the Edge status configuration. This field is auto-assigned. The system selects the configuration to use when an edge satisfies the condition and has the least order.|

