---
title: Create an entity class
description: Create an entity class that is associated with an entity. Entity classes are used to add a conceptual information about the entity and classify the entities. They represent a collection of entities that have the same attributes such as Department, Business Unit, or Business Service. You can gather data about the entities based on the entity class.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Entity classes, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Create an entity class

Create an entity class that is associated with an entity. Entity classes are used to add a conceptual information about the entity and classify the entities. They represent a collection of entities that have the same attributes such as Department, Business Unit, or Business Service. You can gather data about the entities based on the entity class.

## Before you begin

Roles required: sn\_grc.manager, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

## About this task

Entity classes are used to classify and tag your entities. After tagging the entities, you can gather data about the entities based on the entity classes.

## Procedure

1.  Navigate to the desired workspace, go to the List view, and select **Entity classes**.

2.  To create a entity class, select **New**.

3.  In the **Details** tab, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Structure

</td><td>

Structure of the entity class. The options are as follows:-   **Single**: Option to configure a single dimension entity class.
-   **Composite**: Option to configure a multidimensional entity class.
**Note:** The Composite Entity Management application must be installed to configure a composite entity class.

</td></tr><tr><td>

Number of dimensions

</td><td>

Option to select the required number of entity class dimensions. This field appears only when **Composite** is selected from **Structure**.**Note:** You can select up to 5 dimensions.

</td></tr><tr><td>

Applicable entity classes

</td><td>

Option to select the required entity classes. The order in which you select them doesn’t affect the risk roll-up, but the same order will be used to choose entities from each class. This field appears only when **Composite** is selected from **Structure**.

</td></tr><tr><td>

Name

</td><td>

Name of the entity class.**Note:** If you select **Composite** in the **Structure** field, the name is automatically generated based on the selected entity classes, with a separator between them.

</td></tr><tr><td>

Description

</td><td>

Additional information about the entity class.

</td></tr><tr><td>

Parent class

</td><td>

Parent class associated with the new entity class such as Company or Department. This field appears only when **Single** is selected from **Structure**.

</td></tr><tr><td>

Is root

</td><td>

Condition to check if the new entity class is a root. Options are **True** or **False**. This field appears only when **Single** is selected from **Structure**.

</td></tr><tr><td>

Primary risk assessment methodology

</td><td>

Risk assessment methodology that must be used as the primary methodology for the entity class.

</td></tr><tr><td>

Tier

</td><td>

Tier for the new entity class such as Application or Business. This field appears only when **Single** is selected from **Structure**.

</td></tr><tr><td>

Attachments

</td><td>

Attachments associated with the entity class that is displayed in the side panel.

</td></tr></tbody>
</table>4.  Select **Save**.

    After saving, the new entity class is displayed in the Entity classes list in the List view. When you select the new entity class, the following additional related lists are displayed:

    -   Entities
    -   Child classes
5.  Navigate to the Entities related list and fill in the fields under the Entity class section.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the entity.|
    |Owned by|Owner of the entity.|
    |Compliance Score percentage|Compliance score percentage for the entity.|

6.  Navigate to the Child classes related list and fill in the fields under the Entity class section.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the entity class.|
    |Tier|Tier for the new entity class.|
    |Is root|Condition to check if the new entity class is root. Options are True or False.|

7.  To save the entity class, select **Save**.


**Parent Topic:**[Entity classes](../concept/entity-class-in-risk-ws.md)

