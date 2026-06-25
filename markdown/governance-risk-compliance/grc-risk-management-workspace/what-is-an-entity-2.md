---
title: Entities in GRC
description: An entity is a person, process, department, application, or other object whose compliance exposure is tracked in GRC. Each entity has an owner, so non-compliant items and their owners can be identified individually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/what-is-an-entity-2.html
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring the entities, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Entities in GRC

An entity is a person, process, department, application, or other object whose compliance exposure is tracked in GRC. Each entity has an owner, so non-compliant items and their owners can be identified individually.

Before you can work with entities, you need three supporting constructs:

-   An entity class groups entities by category, such as Financial or Location, and associates that category with a tier.
-   An entity type uses filter conditions to identify which source records are set to entities. For example, all records where Category = Financial and Criticality = High.
-   An entity tier assigns a criticality level to entity classes. For example, Tier 1 for critical items and Tier 2 for standard items.

    Once these constructs are in place, GRC generates entities automatically when a matching source record is created.


To understand how these constructs work together, consider the following example. Your organization wants to track compliance across its critical financial systems. First, create an entity tier called Tier 1 to represent high-criticality items. Then create an entity class called Financial and associate it with Tier 1. Next, create an entity type called Critical Financial Systems with a filter that matches records where Category = Financial and Criticality = High. When a source record matching that filter is created, GRC automatically generates an entity, assigns it the Financial class, and surfaces it in the Tier 1 view. If one system fails an audit, only that system's entity and its owner are held accountable. The other systems are unaffected.

Entities can also be related to each other. An entity with child entities has downstream entities. An entity with parent entities has upstream entities.

## Entity name and owner synchronization

When a source record linked to an entity filter is created, an entity is automatically generated in GRC. If the source record name or owner changes after the entity is created, the entity name and owner can update to match the source record.

You can control this synchronization at the entity level using the **Sync entity name and entity owner with source record** check box. When selected, the Name and Owner fields are set to read-only and stay in synchronization with the source record. Clearing the check box enables you to manually override the entity name and owner.

The synchronization is performed by the Sync entity name and entity owner with source record scheduled job. When an entity is first created, the synchronization happens automatically. For continuous synchronization of future changes to source records, this scheduled job must be active. The job syncs entity names and owners based on GRC properties that control its behavior:

-   **Frequency of syncing the entity name and entity owner with the source record**: determines how often the job runs. Options are daily, weekly, or monthly.
-   **Maximum batch size while syncing the entity name and entity owner with the source record**: controls the number of records processed in each batch.

## Entity classes

Entity classes are used to add a conceptual information about the entity or tag the entity. To understand the concept of entity class, consider the following example. A company has office branches in three cities. The office space is considered as an entity and the entity class for these entities would be the location. You can create an entity class by associating it with an entity tier as shown in the following example.

\[Omitted image "entity-class-associated-with-entity-tier.png"\] Alt text: Sample configuration for an entity class.

For more information, see [Entity classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-class-in-risk-ws.md).

## Entity class rules

Entity class rules help to assign classes to the entities at the table level. Any new entity created on the table gets that entity class automatically. Entity classes are used to tag your entities.

When you create an entity over a specific table, the class associated with that table automatically gets assigned to the entity. You can set a new entity class rule for a table.

For more information, see [Entity class rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-class-rules-in-risk-ws.md).

## Entity types

An entity type is a grouping of entities that is based on filtering. Entity types enable you to find and create entities that match a set of filter conditions. Hierarchy can be created within the entity classes.

Entity types also enable you to create risks and controls for each entity without spending much time. For example, an organization can have multiple departments, such as finance, HR, or IT. All these departments can be considered as entities and can be grouped under the entity type called Departments.

You can create an entity type by associating it with the core business pillar such as Technologies or Facilities as shown in the following example.

\[Omitted image "entity-type-new-record.png"\] Alt text: Sample configuration for an entity type.

For more information, see [Entity types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-type-in-risk-ws.md).

## Entity tiers

When you create entity tiers, you apply a level or hierarchy to the entity classes. This level applies to all the entities in those entity classes. Entity tiers enable you to select and view the status of the most critical items in the business as shown in the following example.

\[Omitted image "entity-tier-list-view.png"\] Alt text: List view for an entity tier.

For more information, see [Entity tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-tier-in-risk-ws.md).

**Parent Topic:**[Exploring the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/manage-entities.md)

**Parent Topic:**[Exploring the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/exploring-the-entities.md)

**Related topics**  


[Entity scoping in GRC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/c_Scoping.md)

