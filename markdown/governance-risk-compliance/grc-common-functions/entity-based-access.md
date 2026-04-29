---
title: Entity Based Access
description: The Entity Based Access \(EBA\) application enables you to segregate data on the records that are based on entities. Entity-based access administrators can use this tool to set up secure, controlled access to various objects.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Entity Based Access

The Entity Based Access \(EBA\) application enables you to segregate data on the records that are based on entities. Entity-based access administrators can use this tool to set up secure, controlled access to various objects.

## Entity Based Access overview

Before the Yokohama release, user restrictions were based only on their roles within the system without consideration for their geographical locations or specific functions. Access to objects like risks, controls, and issues was broadly managed. For example, a risk manager in North America had access to risk records across all regions, not just their own.

From the Yokohama release onwards, Entity Based Access facilitates object access via entities. You can map entities to specific users or user groups, enabling you with a granular level of access control.

With Entity Based Access, you can segregate data and manage access to help ensure that users can only access permitted data through entity-based access. Your administrators can grant access to an entity’s related records. They can add users or user groups for access. Access can also be granted through entity user fields or entity user group fields, minimizing the risk of unnecessary data exposure.

To use the Entity Based Access configuration, navigate to **Entity Based Access Configurations** in an instance.

## Key features of Entity Based Access

Key features of the Entity Based Access configuration include:

-   Detailed control over access to various objects via entities within the system.
-   Versatile configuration options. For example, you can configure Entity Based Access within an entity hierarchy to restrict access to the entity and its downstream related records or across a group of entities by using an entity class or entity type. With bulk access update configurations, you can apply access restrictions selectively to scoped records. You can implement access restrictions gradually to help ensure smooth adoption without operational disruptions.
-   Access that is provided by including specific user field or user group fields in the entity-based access configuration. Users who are part of the configuration get dynamic access to the records.

## Key points to note about Entity Based Access

Entity Based Access restricts access to records to users based on the configuration as shown in the following diagram:

![Entity-based access security flow that is described in the text that follows.](../image/eba-security-flow.png "Entity-based access security flow")

The details about the entity-based access security flow are:

-   If User Hierarchy Access or User Group Access is enabled, you can't use Entity Based Access.
-   Confidential users can continue to access the confidential records whether they’re or not part of the entity-based access configuration.

**Important:**

-   For information about the performance limitations, see [KB2069935](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069935).
-   For information on how to use Entity Based Access on custom tables, see the steps in [KB1646304](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1646304).
-   For information about the limitations of Entity Based Access, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2054513](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2054513).

-   **[Sample use case scenarios](sample-usecases.md)**  
Use case scenarios offer a clear and comprehensive explanation of why you would use the Entity Based Access application.
-   **[User roles for Entity Based Access](../reference/user-roles-for-entity-based-access.md)**  
Users with specific user roles have access to read or update the Entity Based Access configuration or the bulk access update configuration.
-   **[Entity based record access update utility](entity-based-access-playbook.md)**  
The entity based record access update utility is a guided assistance, designed to simplify the application of enabling or disabling access restrictions across large volumes of records.
-   **[Entity-based record access rules](continuous-monitoring-of-entity-based-access.md)**  
The entity-based record access rules let admins apply restrictions automatically to new and changed records. This configuration ensures that access settings stay enforced. No manual updates are needed when records are created, modified, or when users are added to user fields or user group fields.
-   **[Deactivating entity-based access configuration](deactivating-entity-based-access.md)**  
Deactivating entity-based access \(EBA\) not only disables the configuration but also streamlines admin workflows by automating record-level access evaluation.
-   **[Configuring Entity Based Access](setting-up-entity-based-access.md)**  
Configure the Entity Based Access application by installing it from the ServiceNow Store and by setting up Entity Based Access properties in the instance.
-   **[Managing Entity Based Access](using-entity-based-access.md)**  
You can manage access to the objects or record types in a system by using the Entity Based Access application. You can restrict access by using an entity, entity class, or entity type configuration.
-   **[Entity Based Access reference](../reference/entity-based-access-reference.md)**  
Entity-based access restriction can be applied on some GRC tables.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

