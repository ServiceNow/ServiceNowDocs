---
title: Entity class rules
description: Entity class rules help to assign classes to the entities at the table level. Any new entity created on the table gets that entity class automatically. Entity classes are used to tag your entities.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity class rules

Entity class rules help to assign classes to the entities at the table level. Any new entity created on the table gets that entity class automatically. Entity classes are used to tag your entities.

When you create an entity for a table, the class associated with that table automatically gets assigned to the entity. You can set a new rule for the entity class. Entity class rules provide the categories of the entities at the class level. The Entity class rules option is displayed under Lists in the workspace view. Click an Entity class rule to display its details.

The **Details** tab in the Entity class rules form displays the following information:

|Field|Description|
|-----|-----------|
|Table|Name of the table that the entity class is associated with after creating an entity class rule.|
|Class|Name of the entity class to be associated with the table that uses the new entity class rule.|

## Entity class rule filter

Entity class rule filter is added in the entity class rule page to provide additional filters. Earlier, records of a table can be associated to only one entity class. Using the entity class rule filter, you can associate different classes to the records of the same table.

The **Entity class rule filter** table displays the following information:

<table id="table_yfz_jhh_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter Priority

</td><td>

Filter priority is the range for the subclass. The class is populated in the entity form based on the priority given.

</td></tr><tr><td>

Subclass

</td><td>

Subclass is the child class of the parent class that is displayed in the details tab of entity class rules.

</td></tr><tr><td>

Filter Condition

</td><td>

Filter Condition is used to filter out the records of the table that defines the entity class rule.

 For example, if there are two subclasses with different condition then the parent class is populated instead of the subclasses.

**Note:** The subclasses are displayed in the entity forms only if they meet the same filter condition.

</td></tr></tbody>
</table>## Logic for assigning entity classes

Assume that there is a record in the cmdb\_ci\_linux\_server table and an entity class rule associated to this table. The entity class rule has these class rule filters:

![Entity class rule](../image/entity-class-rule.png "Entity class rule")

**Scenario 1**: If the entity's source record belongs to the cmdb\_ci\_linux\_server table and matches all the conditions of the second filter, then the entity's class is auto-populated as sub class, **Department**.

**Scenario 2**: If the entity's source record belongs to the cmdb\_ci\_linux\_server table and its name starts with lnux \(satisfies both the filters\), then the sub class **Application** is auto-populated as an entity class.

**Scenario 3**: If the entity's source record doesn't satisfy any of the class rule filters, then the class **Linux Server** is auto-populated as an entity class.

-   **[Create an entity class rule](../task/create-new-entity-class-rule-ws.md)**  
Create a rule for an entity class. Entity class rules provide the classification of the entities at the class level. You can create a new entity class rule for an entity class that is associated with a table. After creating the new entity class rule, the Entity class rules table is updated with the new record.
-   **[Create an entity class rule filter](../task/create-new-entity-class-rule-filter.md)**  
You can create an entity class rule filter to assign classes at the filter level on the same table that is defined on the class rule.

**Parent Topic:**[Exploring the entities](../../grc-common/concept/exploring-the-entities.md)

