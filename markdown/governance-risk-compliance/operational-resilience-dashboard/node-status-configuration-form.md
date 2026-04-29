---
title: Node status configuration form
description: Use the Node status configuration form to configure the Node status conditions and parameters for the selected node configuration table.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Node status configurations, Configure the Node configurations, Configure the Main node configurations, Configuring Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Node status configuration form

Use the Node status configuration form to configure the Node status conditions and parameters for the selected node configuration table.

## Node status configuration new record form

|Field|Description|
|-----|-----------|
|Node configuration|Node configuration record for which the Node status configuration is being configured.|
|Table|Table associated with the node configuration for which the conditions and parameters are updated. For example, Entity \[sn\_grc\_profile\].|
|Conditions|Entity and related list conditions. Once the conditions are satisfied, the node status is updated and reflected in the Nexus map.|
|Color|Color to be displayed for the node status once the conditions are satisfied, for example, Critical or Magenta.|
|Icon|Icon to be used for the node in the main node UI, for example, exclamation-outline.|
|Order|Order assigned to the Node status configuration. This field is auto-assigned. The system selects the configuration to use when a node satisfies the condition and has the least order.|
|Context menu options|
|Configuration for set as main node|Nexus map configuration required to enable the "Make this primary" functionality at the node level. This configuration reflects the hierarchy flow for the node that is designated as primary.|
|Configuration for 360° view|360° view type that is selected for the Nexus map configuration.|
|Context record|Context record for the table selected. This field is auto-filled. for example, for the Entity \[sn\_grc\_profile\] table, the "Applies to record" value is auto-filled for this field.|

