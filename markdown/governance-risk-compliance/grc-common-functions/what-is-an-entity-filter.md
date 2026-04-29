---
title: Entity filters
description: Entity types enable you to find and create entities that match a set of filter conditions. Entity types include predefined entity filters that define the data to be displayed in the user interface. The entity filter defines the table from which data is pulled into each entity type for display.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Entity types, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity filters

Entity types enable you to find and create entities that match a set of filter conditions. Entity types include predefined entity filters that define the data to be displayed in the user interface. The entity filter defines the table from which data is pulled into each entity type for display.

Entities in entity type are created based on the conditions set in the entity filter. You can create a new entity filter by navigating to the Entity types tab under the List view.

The options in the **Entity filter** tab under the Entity type are revised so that **Build your own conditions** condition builder uses the same option that was used in the previous condition builder. In addition, the new **Select from predefined queries** option leverages the Configuration Management Database \(CMDB\) queries. The following options are now available in the Entity filters related list under Entity type:

-   Build your own conditions.
-   Select from predefined queries using the Configuration Management Database \(CMDB\) Query Builder.

The **Entity filters** tab displays the following information:

-   Entity filter type: Entity filter type such as Build your own conditions or Select from predefined queries.
-   Table: Table that contains the records to be queried such as sn\_audit\_advanced\_auditable\_unit.
-   Filter condition: Filter conditions for the source table to generate entities.
-   Use owner field: Use the default owner to assign risks to a single user when the owner field is empty.
-   Owner field: Person who owns any new entities generated from the entity type. Identify the user reference field on the source table to automatically identify risk and control owners.

Use the new Entity class field in the entity filters under the entity type to assign an entity class to an entity filter. When you use an entity filter to create an entity, an entity class gets assigned to it automatically.

-   **[Create an entity filter](../../grc-common-workspace/task/create-new-entity-filter-ws.md)**  
Create an entity filter under an entity type in the workspace view. Entities in entity type are created based on the conditions set in the Entity Filter. The entity filter defines the table from which data is pulled into each entity type for display.
-   **[Create an entity filter in the Core UI](../task/create-entity-filter-in-classic-user-interface.md)**  
Create an entity filter under an entity type in the classic user interface. The entity filter defines the table from which data is pulled into each entity type for display. If the entities belong to an application, the users who have access to the entity class that is associated with the entity can only view those entities.

**Parent Topic:**[Entity types](../../grc-common-workspace/concept/entity-type-in-risk-ws.md)

