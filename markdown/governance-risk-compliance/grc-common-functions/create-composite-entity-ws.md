---
title: Create a composite entity
description: Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. In Governance, Risk, and Compliance, entities can be people, processes, departments, applications, or objects.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Composite entity, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Create a composite entity

Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. In Governance, Risk, and Compliance, entities can be people, processes, departments, applications, or objects.

## Before you begin

Roles required: sn\_grc.manager, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

The Composite Entity Management application and Risk Workspace must be installed to create a composite entity.

## About this task

When you create a composite entity by combining two or more individual entities, the composite entity automatically becomes a downstream entity for each of the individual entities involved. For example, if you create a composite entity named "Document handover \| Mexico" using the entities "Document handover" and "Mexico," the composite entity appears as a downstream entity for both "Document handover" and "Mexico." This structure helps in organizing related data and simplifies tracking dependencies across entities.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

2.  Navigate to the list view and select **Entities**.

3.  Select **New**.

4.  On the form, fill in the fields.

    For a description of the field values on the Create New Entity form, see [Create new composite entity form](../Reference/create-new-composite-entity-form-ws.md).

5.  Select **Save**.

    **Note:** When you create an entity, only the **Details** tab is displayed. After the entity is created, the **Overview** tab, **Details** tab, and other related lists are displayed.

    After saving the entity, an entity form is displayed with the Details tab, Hierarchy tab, and the following related lists.

    For information on the fields in these related lists, see [An entity in the workspace view](../concept/entities-in-risk-ws.md).


-   **[Create new composite entity form](../Reference/create-new-composite-entity-form-ws.md)**  
Use the Create New Entity form to create a composite entity by combining two or more entities from different entity classes using the Composite Entity Management application.

**Parent Topic:**[Composite entity in Governance, Risk, and Compliance](../concept/composite-entity-in-grc.md)

**Related topics**  


[Create an entity class](create-new-entity-class-ws.md)

