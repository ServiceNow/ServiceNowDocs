---
title: Connector status configuration form
description: Use the Connector status configuration form to configure the Connector status settings for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/edge-status-configuration-form.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure the Connector status configurations, Configure the Connector configurations, Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Connector status configuration form

Use the Connector status configuration form to configure the Connector status settings for the selected Nexus map configuration. You can customize the display of connectors that meet specific conditions by assigning them distinct colors and connector types.

|Field|Description|
|-----|-----------|
|Connector configuration|Connector configuration to be defined between two specific entities.|
|Relationship table|Relationship table for the source and target tables. For example, Entity hierarchy \[sn\_grc\_m2m\_profile\_profile\]|
|Conditions|Entity and related list conditions. Once the conditions are satisfied, the connector status is updated and reflected in the Nexus map.|
|Color|Color to be displayed for the connector status once the conditions are satisfied, for example, Critical or Magenta.|
|Connector type|Connector type to be defined for the node, for example, Solid.|
|Label|Label to be defined for the node, for example, Primary.|
|Order|Order assigned to the Connector status configuration. This field is auto-assigned. The system selects the configuration to use when a connector satisfies the condition and has the least order.|

