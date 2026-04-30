---
title: Entity tiers
description: When you create entity tiers, you can apply a level or hierarchy to the entity classes. This level applies to all the entities that are associated with the entity classes. Entity tiers enable you to select and view the status of the most critical items in the business.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity tiers

When you create entity tiers, you can apply a level or hierarchy to the entity classes. This level applies to all the entities that are associated with the entity classes. Entity tiers enable you to select and view the status of the most critical items in the business.

Consider the following example. Assume that the Chief Product Officer of your organization wants to see the status of only the most critical financial business applications. If you have created a hierarchy or set of tiers for the entities, then you can filter the tier 1 entities and present the required data. Each entity class can belong to only one tier.

By creating entity tiers, you can better understand how your lower tier entities affect your higher tier entities. For example, assume that you created the entity hierarchy where Business is tier 1, Application is tier 2, and IT asset is tier 3. Therefore, the risks of the entities of tier 3 affect the entities of tier 2 and that in turn affects tier 1. This roll-up or aggregation provides accurate risk scores.

The Entity tiers option is displayed under the Lists view in the workspace. Click an entity tier to display its details. The **Details** tab in the Entity tiers page displays the following information:

|Field|Description|
|-----|-----------|
|Label|Label of the entity tier that is displayed in the user interface such as Application or Business.|
|Tier level|Tier level of the entity tier such as 15 or 20.|
|Name|Name of the entity tier such as application or business.|

-   **[Create an entity tier](../task/create-new-entity-tier-ws.md)**  
Create an entity tier for the entity classes in your organization. When you create entity tiers, you can apply a level or hierarchy to the entity classes. The hierarchy level applies to all the entities associated with the entity classes.

**Parent Topic:**[Exploring the entities](../../grc-common/concept/exploring-the-entities.md)

