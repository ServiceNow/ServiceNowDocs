---
title: Entity configuration and mapping
description: Use the Entity Configuration tables and forms to configure and map an entity that defines a structure and transfers the data from the source entity to the target entity.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Sales and Order Management workflows, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Entity configuration and mapping

Use the Entity Configuration tables and forms to configure and map an entity that defines a structure and transfers the data from the source entity to the target entity.

## Overview

Create the configurations and mappings for the entities by using the Entity Configuration tables.

## Entity Configuration tables

The entity configuration tables provide you with the information for the fields on the entity configuration form.

<table id="table_m4r_cp1_b1c"><thead><tr><th>

Table

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lead to Cash Entity

</td><td>

sn\_l2c\_core\_entity

</td><td>

Defines and manages the lead-to-cash entities.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

sn\_l2c\_core\_entity\_definition

</td><td>

Defines and manages the definitions that are associated with the lead-to-cash entities.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

sn\_l2c\_core\_entity\_attribute

</td><td>

Defines and manages the attributes that are associated with the lead-to-cash entities.The lead-to-cash attributes are based on the definitions that are set for the entities.

</td></tr></tbody>
</table>Each field on the entity configuration form gathers the information from one entity configuration table. The following table has the information about the fields, their descriptions, and the entity tables that the data is populated from.

**Note:** The Lead to Cash Entity Definition and Lead to Cash Entity Attributes are related lists on the Entity Configuration form.

<table id="table_ckf_5p1_b1c"><thead><tr><th>

Table

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lead to Cash Entity

</td><td>

Name

</td><td>

Name of the lead-to-cash entity.

</td></tr><tr><td>

Lead to Cash Entity

</td><td>

Config ID

</td><td>

Unique configuration ID for the entity.

</td></tr><tr><td>

Lead to Cash Entity

</td><td>

Active

</td><td>

Status of the entity, whether active or inactive for the configuration.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Entity

</td><td>

Reference to the lead-to-cash entity definition.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Type

</td><td>

Type of the entity definition.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Table

</td><td>

Table that is associated with a lead to cash entity.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Label

</td><td>

Label for the entity definition.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Parent definition

</td><td>

Parent of the current entity definition.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Relationship field

</td><td>

Query field that is associated with the parent entity definition record.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Parent field

</td><td>

Query field that is associated with the current entity definition record.

</td></tr><tr><td>

Lead to cash Entity Definition

</td><td>

Inherit parent definition

</td><td>

Parent definition that is also used by the current entity definition.**Note:** To make the current entity definition record follow the same definition that is associated to the parent record, select **Inherit parent definition**.

</td></tr><tr><td>

Lead to Cash Entity Definition

</td><td>

Order

</td><td>

Numerical order to process and visualize the hierarchy of configurations.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

Field

</td><td>

Name of the field.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

Entity

</td><td>

Reference to the lead-to-cash entity attribute.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

Table

</td><td>

Table that is associated with the lead-to-cash attribute.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

Key

</td><td>

Unique key for the entity attribute.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

Advanced

</td><td>

Option for advanced configurations.**Note:** To modify the script according to your requirements, select **Advanced**.

</td></tr><tr><td>

Lead to Cash Entity Attribute

</td><td>

Script

</td><td>

Script for the advanced attributes.

</td></tr></tbody>
</table>## Entity mappings

With entity mappings, you can map the source and target tables to transfer the data between the entities that depend on the available entity configurations. The entity mapping tables provide the information for the fields on the entity mapping forms.

|Table|Name|Description|
|-----|----|-----------|
|Lead to Cash Entity Mapping|sn\_l2c\_core\_entity\_mapping|Defines and maps the lead-to-cash entity mappings.|
|Lead to Cash Entity Table Mapping|sn\_l2c\_core\_entity\_table\_mapping|Defines and manages the mappings for the different tables that are associated with the lead-to-cash entities.|
|Lead to Cash Entity Attribute Mapping|sn\_l2c\_core\_entity\_attribute\_mapping|Defines and manages the attributes and their mappings with the corresponding lead-to-cash entity.|

The entity mapping form enables you to map the entities with their corresponding tables and attributes.

**Note:** The Lead to Cash Entity Table Mapping and Lead to Cash Entity Attribute Mapping are related lists on the Entity Mapping form.

<table id="table_lll_4t1_b1c"><thead><tr><th>

Table

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lead to Cash Entity Mapping

</td><td>

Mapping name

</td><td>

Name of the mapping.

</td></tr><tr><td>

Lead to Cash Entity Mapping

</td><td>

Mapping config ID

</td><td>

Unique ID for the mapping.

</td></tr><tr><td>

Lead to Cash Entity Mapping

</td><td>

Source entity

</td><td>

Source entity in the mapping process.

</td></tr><tr><td>

Lead to Cash Entity Mapping

</td><td>

Target entity

</td><td>

Target entity in the mapping process.

</td></tr><tr><td>

Lead to Cash Entity Mapping

</td><td>

Active

</td><td>

State of the target entity, whether active for mapping or not.

</td></tr><tr><td>

Lead to Cash Entity Table Mapping

</td><td>

Source entity table

</td><td>

Table that is associated with the source entity.

</td></tr><tr><td>

Lead to Cash Entity Table Mapping

</td><td>

Target entity table

</td><td>

Table that is associated with the target entity.

</td></tr><tr><td>

Lead to Cash Entity Table Mapping

</td><td>

Use condition

</td><td>

Conditions required for mapping.**Note:** To set specific mapping conditions, select **Use condition**.

</td></tr><tr><td>

Lead to Cash Entity Table Mapping

</td><td>

Condition

</td><td>

Conditions for mapping tables from the source entity to the target entity.

</td></tr><tr><td>

Lead to Cash Entity Table Mapping

</td><td>

Active

</td><td>

State of the source entity, whether active for mapping or not.

</td></tr><tr><td>

Lead to Cash Entity Table Mapping

</td><td>

Order

</td><td>

Numerical priority for mapping.

</td></tr><tr><td>

Lead to Cash Entity Attribute Mapping

</td><td>

Entity table mapping

</td><td>

Reference to the Lead-to-Cash entity table mapping.

</td></tr><tr><td>

Lead to Cash Entity Attribute Mapping

</td><td>

Source attribute

</td><td>

Attribute that is associated with the source entity.

</td></tr><tr><td>

Lead to Cash Entity Attribute Mapping

</td><td>

Target attribute

</td><td>

Attribute that is associated with the target entity.

</td></tr><tr><td>

Lead to Cash Entity Attribute Mapping

</td><td>

Advanced

</td><td>

Option for advanced mapping.**Note:** To modify the script according to your requirements, select **Advanced**.

</td></tr><tr><td>

Lead to Cash Entity Attribute Mapping

</td><td>

Script

</td><td>

Script to customize the mappings.

</td></tr></tbody>
</table>