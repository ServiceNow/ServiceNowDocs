---
title: Managing Entity Based Access
description: You can manage access to the objects or record types in a system by using the Entity Based Access application. You can restrict access by using an entity, entity class, or entity type configuration.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Managing Entity Based Access

You can manage access to the objects or record types in a system by using the Entity Based Access application. You can restrict access by using an entity, entity class, or entity type configuration.

You can apply entity-based access restriction in a two-step process.

1.  Configure an entity-based access restriction for the following types:
    -   Entity access to provide access to users or user groups.
    -   Entity class to define an entity class, such as Business Process, Business Service, or Database, and to manage the object access for the entity that is linked to that particular entity class.
    -   Entity type to specify an entity type, such as Company or Vendors, and control object access for the entity that is linked to that entity type.
2.  Configure a bulk access update to configure the restrictions across all the records that are related to an entity.

**Important:** Make sure to complete both these steps to enable an entity-based access restriction.

-   **[Configure access to an entity's related records](../task/create-an-entity-access-configuration.md)**  
Configure access to an entity for your users or user groups so that they can access the entity's related records.
-   **[Configure an entity class for a linked object](../task/create-an-entity-class-configuration-for-entity-based-access.md)**  
Configure an entity class for a linked object by using the Entity Based Access application. You can define an entity class, such as Business Process, Business Service, or Database, and manage the object access for the entity that is linked to that entity class.
-   **[Configure an entity type for a linked object](../task/create-an-entity-type-configuration-for-entity-based-access.md)**  
Configure an entity type by using the Entity Based Access application. You can specify an entity type, such as Company or Vendors, and manage the object access for the entity that is linked to that entity type.
-   **[Set access restrictions using an entity based record access update utility](../task/create-a-bulk-access-update-configuration.md)**  
Set access restrictions for the existing records in bulk by using the Entity based record access update utility guided-experience. Use the workflow to enable or disable access to record types.
-   **[Configure entity-based record access rules](../task/configure-continuous-eba-monitoring-on-record-types.md)**  
Configure entity-based record access rules on record types to apply access restrictions to new records automatically.
-   **[Deactivate entity-based access configuration](../task/deactivate-entity-based-access-configuration.md)**  
Deactivate an entity-based access \(EBA\) configuration to disable access restrictions from associated records, confirming only active and relevant configurations control data access.

**Parent Topic:**[Entity Based Access](entity-based-access.md)

