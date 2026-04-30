---
title: Entity types in GRC
description: Entity types enable you to find and create entities that match a set of filter conditions. Entity types also enable you to create risks and controls for each entity without spending much time.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring the entities, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Entity types in GRC

Entity types enable you to find and create entities that match a set of filter conditions. Entity types also enable you to create risks and controls for each entity without spending much time.

An organization can have multiple entities. Each of those entities can have several risks and controls associated with them. The conventional method for mapping each risk with each entity was by using multiple spreadsheets. This method is not the most accurate or reliable method because the risks and controls exist in silos and a standard risk taxonomy is not created. A risk taxonomy is a comprehensive, common, and stable set of risk categories that are used within an organization. When you create entity types and associate risk statements to them, the risks are automatically created for all the entities. The association is done via your risk taxonomy. The benefit of creating entity types is that it eliminates the need for maintaining multiple spreadsheets with the associated risks and controls for each entity. By applying entity types, you can quickly create entities by using the entity filters that are present within the entity types. Entity types can contain entities associated with different classes.

For example, an organization can have multiple departments, such as finance, HR, or IT. All these departments can be considered as entities and can be grouped under the entity type called Departments.

Grouping entities also helps in rolling up and aggregating the risk scores after risk assessments are performed. To understand how grouping entities contribute to rolling up the risk scores, consider the following example. Assume that there's a banking organization called Acer Finance. Acer Finance has two business lines: Banking and Retail. The Banking division has further subdivisions such as Commercial Banking and Private Banking. The risk assessments are generally performed at the bottom-most level. In this example, the assessment is performed at the Commercial Banking and Private Banking levels. The reporting, however, is done at the top-most level. This means that the risk assessment scores of Commercial Banking and Private Banking will roll up and aggregate at the Banking level. Similarly, the scores of the Banking and Investment will roll up to the Acer Finance organization level.

![Graphical representation of the given example](../image/entity-types-in-grc.png "Graphical representation of the example")

**Parent Topic:**[Exploring the entities](manage-entities.md)

**Related topics**  


[Entity classes in GRC](entity-class.md)

