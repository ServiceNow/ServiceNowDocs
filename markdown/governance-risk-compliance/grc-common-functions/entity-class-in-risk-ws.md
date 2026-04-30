---
title: Entity classes
description: Entity classes are used to add a conceptual information about the entity or to tag the entity. They are used to classify the entities and they represent a collection of entities that have the same attributes.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity classes

Entity classes are used to add a conceptual information about the entity or to tag the entity. They are used to classify the entities and they represent a collection of entities that have the same attributes.

To understand the concept of entity class, consider an example. A company has office branches in three cities. The office space is considered as an entity and the entity class for these entities would be the location. For example, Risk as an entity could be a process or it could be the department in an organization. The entity class defines whether it belongs as a process or as a class in this example.

Entity classes are listed under Lists in the workspace view. Click an entity class in the List view to display its details.

The **Details** tab in the Entity classes form displays the following fields:

-   Name
-   Tier
-   Parent class
-   Description
-   Is root check box condition

The Entity classes page displays the following related lists:

<table id="table_b22_ynv_lqb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entities

</td><td>

Information on the entities:-   Name
-   Owned by
-   Compliance Score \(%\)

</td></tr><tr><td>

Child classes

</td><td>

Information on the child classes:-   Name
-   Tier
-   Is root check box

</td></tr></tbody>
</table>To save the newly created entity class configuration, click **Save**.

-   **[Create an entity class](../task/create-new-entity-class-ws.md)**  
Create an entity class that is associated with an entity. Entity classes are used to add a conceptual information about the entity and classify the entities. They represent a collection of entities that have the same attributes such as Department, Business Unit, or Business Service. You can gather data about the entities based on the entity class.
-   **[Update entity classes for multiple entities](../task/bulk-update-entity-class.md)**  
Provide an entity class for multiple entities where the class field is empty. Entity classes are used to add a conceptual information about the entity and classify the entities. As an administrator, you can update the entity classes for multiple entities with a single click.
-   **[Scheduled jobs for Governance, Risk, and Compliance](../../grc-common/concept/scheduled-jobs.md)**  
Scheduled jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule. GRC administrators run the scheduled jobs on demand to automate the tasks such as setting an entity class on the entities depending on the entity class rule.

**Parent Topic:**[Exploring the entities](../../grc-common/concept/exploring-the-entities.md)

