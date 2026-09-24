---
title: Entity filters
description: An entity filter defines the conditions used to create entities in an entity type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/what-is-an-entity-filter.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity filters

An entity filter defines the conditions used to create entities in an entity type.

You can create an entity filter by navigating to the **Entity types** tab under the **List view**.

The **Entity filter** tab under the Entity type provides the following ways to define an entity filter:

-   Build your own conditions.
-   Select from predefined queries using the Configuration Management Database \(CMDB\) Query Builder.

The **Entity filters** tab displays several fields that determine how entities are generated and assigned. See [Entity filter fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/entity-filter-fields.md) for field descriptions.

Use the Entity class field in the entity filters under the entity type to assign an entity class to an entity filter. When you use an entity filter to create an entity, an entity class gets assigned to it automatically.

You can configure an entity filter to automatically update the entity owner and entity class when source record data changes or when an entity moves between entity filters.

When **Auto-update owner** is selected, the system re-evaluates the owner and class values associated with the entity. The system then applies the appropriate values based on the applicable entity filter configuration.

To derive ownership from source data, configure the entity filter to use a source field for owner derivation. If multiple entity filters apply to the same entity, you can designate a filter as **Preferred for owner and class derivation**. This setting controls which filter is used to derive the owner and class values.

If multiple filters are marked as preferred, creation order determines precedence.

-   **[Entity filter fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/entity-filter-fields.md)**  
Descriptions of the fields displayed in the Entity filters related list under Entity type.
-   **[Create an entity filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/create-new-entity-filter-ws.md)**  
Create an entity filter under an entity type in the workspace view. Entities in entity type are created based on the conditions set in the Entity Filter. The entity filter defines the table from which data is pulled into each entity type for display.
-   **[Create an entity filter in the Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/create-entity-filter-in-classic-user-interface.md)**  
Create an entity filter under an entity type in the classic user interface. The entity filter defines the table from which data is pulled into each entity type for display. If the entities belong to an application, the users who have access to the entity class that is associated with the entity can only view those entities.
-   **[Configure automatic updates for entity owner and class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/configure-automatic-updates-for-entity-owner-and-entity-class.md)**  
Configure an entity filter to automatically update entity owner and class when source data changes or an entity moves between filters.
-   **[Entity owner and class derivation behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/entity-owner-and-class-derivation-behavior.md)**  
Entity owner and entity class derivation settings determine how the system selects owner and class values when one or more entity filters apply to an entity.

**Parent Topic:**[Exploring the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/exploring-the-entities.md)

