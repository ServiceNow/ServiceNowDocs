---
title: Configure access to an entity's related records
description: Configure access to an entity for your users or user groups so that they can access the entity's related records.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Configure access to an entity's related records

Configure access to an entity for your users or user groups so that they can access the entity's related records.

## Before you begin

Role required: sn\_grc\_ent\_access.admin

## About this task

You can provide granular access control on objects that are linked to entities. You can also restrict the access to records that are associated with specific entities, permitting only designated users and user groups to access them.

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity Configurations**.

2.  Select **New**.

    The Entity Based Access form is displayed.

    To apply the configuration to the selected entity, you can select the **Selected entity only** option in the **Applicability** field. To apply the configuration to the selected entity and its downstream entities, select the **Selected entity and downstream entities** option.

3.  On the [form](../reference/entity-configurations-form.md), fill in the fields.

    For a description of the field values, see [Entity configurations form](../reference/entity-configurations-form.md).

    The Entity Based Access Configuration record is displayed.

    When a configuration is applied to the selected entity only, the selected user can access all objects that are associated with that entity.

    When a configuration is applied to the selected entity and its downstream entities, the selected user can access all objects that are associated with that entity and its downstream entities.

4.  Activate the configuration by selecting **Activate**.

    The access setup for the chosen entity is outlined and displayed in the instance. Access to the records is granted to the designated users and user groups according to the conditions that are set in the entity configuration.


-   **[Entity configurations form](../reference/entity-configurations-form.md)**  
Use the Entity configurations form to configure access to the objects through an entity.

**Parent Topic:**[Managing Entity Based Access](../concept/using-entity-based-access.md)

