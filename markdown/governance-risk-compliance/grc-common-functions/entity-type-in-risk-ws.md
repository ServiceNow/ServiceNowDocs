---
title: Entity types
description: Entity type is a grouping of the entities that match a set of filter conditions. You can create a hierarchy of the entity types within the entity classes. The Entity types option is displayed under the Lists view in the workspace. Click an entity type to display its details.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity types

Entity type is a grouping of the entities that match a set of filter conditions. You can create a hierarchy of the entity types within the entity classes. The Entity types option is displayed under the Lists view in the workspace. Click an entity type to display its details.

An entity type is a grouping of entities that is based on filtering. Entity types enable you to find and create entities that match a set of filter conditions. Hierarchy can be created within the entity classes. Entity types also enable you to create risks and controls for each entity without spending much time. For example, an organization can have multiple departments, such as finance, HR, or IT. All these departments can be considered as entities and can be grouped under the entity type called Departments.

Within an entity type, you can assign an owner and an entity class. You can associate a control objective and risk statements to the entity type so that risks and controls get automatically created for those entities. For every entity created using the entity type, the configuration and filter are applied so that the entity class and entity owner get automatically assigned for each entity.

When you create entity types and associate risk statements and control objectives to them, the risk and controls are automatically created for all the entities. The benefit of creating entity types is that it eliminates the need for maintaining multiple spreadsheets with the associated risks and controls for each entity. By applying entity types, you can quickly create entities by using the entity filters that are present within the entity types. Entity types can contain entities associated with different classes.

Grouping entities also helps in rolling up and aggregating the risk scores after risk assessments are performed. To understand how grouping entities contribute to rolling up the risk scores, consider the following example. Assume that there's a banking organization called Acer Finance. Acer Finance has two business lines: Banking and Retail. The Banking division has further subdivisions such as Commercial Banking and Private Banking. The risk assessments are generally performed at the bottom-most level. In this example, the assessment is performed at the Commercial Banking and Private Banking levels. The reporting, however, is done at the top-most level. This means that the risk assessment scores of Commercial Banking and Private Banking roll up and aggregate at the Banking level. Similarly, the scores of the Banking and Investment roll up to the Acer Finance organization level.

Entities in entity type are created based on the conditions set in the Entity Filter. In entity filters, the following filter conditions are defined:

-   Build your own conditions: The entity filter defines the table from which the data is pulled into each entity type for display. Options in the Entity filter related list under Entity Type are revised such that **Build your own conditions** is same as the previous condition builder.
-   Select from predefined queries: A new option is introduced as **Select from predefined queries** that uses the Configuration Management Database \(CMDB\) queries.

The Details tab in the Entity type page displays the following information:

-   Name
-   Compliance Score \(%\)
-   Check box condition to display if the entity type is active
-   Description

The Entity type page displays the following related lists:

<table id="table_b22_ynv_lqb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entities

</td><td>

Information on the entities:-   Entity
-   Description
-   Class
-   Owned by
-   Residual rating
-   Compliance Score \(%\)

</td></tr><tr><td>

Entity Filters

</td><td>

Information on the entity filters:-   Entity filter type
-   Table
-   Filter condition
-   Use owner field
-   Owner field

</td></tr><tr><td>

Risk frameworks

</td><td>

Details of the risk framework. Click **Add** to add a new risk frameworks record.

</td></tr><tr><td>

Risk Statements

</td><td>

Details of the risk statements such as Risk Statement, Framework, Category, and Description.

</td></tr><tr><td>

Policies

</td><td>

Details of the policies such as number, name, Type, Owner, State, Valid from, Valid to, and Compliance Score percentage.

</td></tr><tr><td>

Control Objectives

</td><td>

Details of the control objectives such as Control objective, Category, Type, Classification, and Compliance Score percentage.

</td></tr><tr><td>

Entity Filters

</td><td>

Details of the entity filter such as Entity Filter type, Table, Filter Condition, Query, Information objects, Use owner field, Owner field.

</td></tr><tr><td>

Policy Exceptions

</td><td>

Details of the policy exceptions.

</td></tr><tr><td>

Content References

</td><td>

Details of the content references.

</td></tr><tr><td>

Privacy assessments

</td><td>

Details of the privacy assessments for the entity type.

</td></tr><tr><td>

Attachments

</td><td>

Attachments associated with the entity type displayed in the side panel.

</td></tr></tbody>
</table>-   **[Create an entity type](../task/create-new-entity-type-ws.md)**  
Create an entity type for the entities in your system. Entity types enable you to find and create new entities that match a set of filter conditions. You can create a hierarchy of the entity types within the entity classes.
-   **[Entity filters](../../grc-common/concept/what-is-an-entity-filter.md)**  
Entity types enable you to find and create entities that match a set of filter conditions. Entity types include predefined entity filters that define the data to be displayed in the user interface. The entity filter defines the table from which data is pulled into each entity type for display.

**Parent Topic:**[Exploring the entities](../../grc-common/concept/exploring-the-entities.md)

