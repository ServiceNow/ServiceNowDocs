---
title: Entities in GRC
description: In Governance, Risk, and Compliance, an entity can be a person, process, department, application, or object, whose exposure must be managed. These entities have controls that are defined to view the status.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring the entities, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Entities in GRC

In Governance, Risk, and Compliance, an entity can be a person, process, department, application, or object, whose exposure must be managed. These entities have controls that are defined to view the status.

To understand entities, consider the following example. Assume that you’re a new GRC user and you want to implement a change management process to all your critical financial systems. All the systems can be considered as individual entities. Map all the systems to an entity class called Financial. Have an entity type filter for critical financial systems to determine the systems that are identified as critical.

The primary benefit of creating entities is that you can maintain accountability because each entity has an owner. To understand this benefit, assume that you want to configure all the servers in a new way. After you finish the configuration, you perform an audit and then discover that only one server failed to comply with the new configuration. If you had not defined all the entities, then the entire audit result would have been deemed as failed. But because you have the entities defined, then only the non-compliant server entity and its identified owner are held accountable instead of all the servers.

Having defined entities ensures that the entity owners can be identified and that appropriate controls can be applied to those entities. It also helps in tracking the entities that are non-compliant. Any entity that has child entities can be said to have downstream entities. Any entity that has parent entities can be said to have upstream entities.

When a source record linked to an entity filter is created, an entity is automatically generated in GRC. If the source record name or owner changes after the entity is created, the entity name and owner can update to match the source record.

You can control this synchronization at the entity level using the Sync entity name and entity owner with source record check box. When selected, the Name and Owner fields become read only and stay in synchronization with the source record. Clearing the check box enables you to manually override the entity name and owner.

The actual synchronization work is performed by a scheduled job called Sync entity name and entity owner with source record. When an entity is first created, the synchronization happens automatically. For continuous synchronization of future changes to source records, this scheduled job must be active. The job syncs entity names and owners based on GRC properties that control its behavior:

-   Frequency of syncing the entity name and entity owner with the source record: Determines how often the job runs \(options: daily, weekly, monthly\). Based on the selected frequency, the synchronization occurs at regular intervals.
-   Maximum batch size while syncing the entity name and entity owner with the source record: Controls the number of records processed in each batch.

After creating entities, you can tag the similar entities by defining the entity class for them individually or you can link them to an existing entity class.

## Entity classes

Entity classes are used to add a conceptual information about the entity or tag the entity. To understand the concept of entity class, consider the following example. A company has office branches in three cities. The office space is considered as an entity and the entity class for these entities would be the location. You can create an entity class by associating it with an entity tier as shown in the following example.

![Sample configuration for an entity class.](../image/entity-class-associated-with-entity-tier.png "Sample configuration for an entity class")

## Entity class rules

Entity class rules help to assign classes to the entities at the table level. Any new entity created on the table gets that entity class automatically. Entity classes are used to tag your entities.

When you create an entity over a specific table, the class associated with that table automatically gets assigned to the entity. You can set a new entity class rule for a table.

## Entity types

An entity type is a grouping of entities that is based on filtering. Entity types enable you to find and create entities that match a set of filter conditions. Hierarchy can be created within the entity classes.

Entity types also enable you to create risks and controls for each entity without spending much time. For example, an organization can have multiple departments, such as finance, HR, or IT. All these departments can be considered as entities and can be grouped under the entity type called Departments.

You can create an entity type by associating it with the core business pillar such as Technologies or Facilities as shown in the following example.

![Sample configuration for an entity type.](../image/entity-type-new-record.png "Sample configuration for an entity type")

## Entity tiers

When you create entity tiers, you apply a level or hierarchy to the entity classes. This level applies to all the entities in those entity classes. Entity tiers enable you to select and view the status of the most critical items in the business as shown in the following example.

![List view for an entity tier.](../image/entity-tier-list-view.png "List view for an entity tier")

**Parent Topic:**[Exploring the entities](manage-entities.md)

**Parent Topic:**[Exploring the entities](exploring-the-entities.md)

