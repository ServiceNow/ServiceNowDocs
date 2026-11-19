---
title: Configure Workplace entities and entity types
description: Workplace entity types and workplace entities model your organization’s business hierarchy. Use them to associate workplace locations with the businesses that use them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/workplace-entity.html
release: brazil
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2026-11-15"
reading_time_minutes: 7
keywords: [workplace entity, workplace entity type, entity type, entity hierarchy, business hierarchy, allocation type, space allocation, push down]
breadcrumb: [Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure Workplace entities and entity types

Workplace entity types and workplace entities model your organization’s business hierarchy. Use them to associate workplace locations with the businesses that use them.

The Workplace Core applications enable you to classify your workplace locations based on their cost center, department, and workplace entity. The workplace entity-based allocation helps you create an organized business structure where you can configure parent-child-based hierarchies and manage various workplace-related activities. You can create a structure exactly as your organization's business by configuring workplace entity types and workplace entities. You can associate locations with the business that uses them.

To allocate locations by workplace entity, set the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property to **Workplace entity**. The property determines the allocation type that the application uses for space searches, scenario planning, and space recommendations.

As a workplace manager, you can manage space allocations based on their entity levels that are set and verify proper space utilization according to business. You can visualize data on the stack plan and floor map based on the workplace entities that you’ve configured. You can view the space allocations of a building based on workplace entities. At any time, you can select a space and know its hierarchy level, that is, the details of its parent and child if present. This business-based hierarchy model, that is, workplace entity-based allocation, enables you to control the space consumption of each business in your organization. The Space Optimization dashboard also enables you to visualize data based on the different workplace entities configured. For more information about how workplace entities and other allocations work, refer to [Allocation - types, setting, and impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-space-management/setting-an-allocation-and-its-impact.md).

**Important:** You can view and perform map-based space administration for workplace entities on a Scenario.

You can filter your workplace locations and perform actions directly on these entities. You can assign an order to each entity type to set the hierarchy. For a parent-child hierarchy, you can also perform direct actions on a parent if you want to implement the same throughout its child entities.

With the hierarchy-based configuration, you can perform the following actions:

-   You can create various entity types and set their level using the entity-mapping options. When you create workplace entities, you can assign them to these entity types.
-   You can set the order of an entity type based on its level in the hierarchy. The lower the order, the higher the entity type is set in the hierarchical structure. The entity type with the lowest order value is at the top of the hierarchy. For example, if you set ABC with order 1000 and XYZ with order 600, XYZ is placed above ABC in the hierarchy.
-   You can use the **Push down** option if you want to push down the workplace entity to child locations at any time.
-   When you select the **Push down** option on a floor or an area, you choose how the workplace entity associations apply to its child locations:
    -   No, keep the floor, area, and space allocation information separate. The entities that you add stay at that level, and the associations on child locations don’t change.
    -   Yes, and replace existing allocations. The entities are pushed down to the child locations, and the existing allocations on those locations are deactivated.
    -   Yes, but keep existing allocations. The entities are pushed down only to the spaces, areas, and rooms that don’t already have an allocation.
-   You can activate or deactivate a workplace entity. Deactivating a workplace entity also deactivates the child workplace entity.

    **Important:** If the parent is inactive, you can’t activate a workplace entity.


When you add or update workplace entity records, the following rules apply:

-   You can add an entity without a parent, so the hierarchy can have more than one root entity.
-   The entity type of a parent entity must be at a higher level than the entity type of its child entities. The application doesn’t allow an entity to reference itself or one of its own child entities as a parent.
-   You can’t change the entity type of an existing entity. To use a different entity type, add a new entity and deactivate the existing one.
-   You can rename an entity or an entity type. The new name is applied wherever the entity is used, including existing allocations. Entity type names must be unique, but entity names can be duplicated.
-   You can’t delete an entity. To retire it, deactivate it from its form. If the entity is the parent of active entities, a warning is displayed. Deactivating a parent entity also deactivates its child entities and makes their location associations inactive.

On each workplace entity record, specify the **Managed by** and **Managed by group** fields. These users are notified when the space allocations of the entity are about to expire. Child entities don’t inherit these fields. For more information about expiry notifications, refer to [Allocation - types, setting, and impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-space-management/setting-an-allocation-and-its-impact.md).

-   **[Add a workplace entity type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/add-a-workplace-entity-type.md)**  
Create an entity type according to your organizational requirement. You can group your workplace entities under this entity type and perform various actions on all entities that belong to this type at a time.
-   **[Add workplace entities to an entity type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/add-workplace-entities-to-an-entity-type.md)**  
Create workplace entities based on your organization's business structure. Specify the entity type to which they belong. You can also specify a parent to the entity based on its hierarchy.

**Parent Topic:**[Manage Workplace Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet]()

[]()

[Configure a workplace card]()

[Block a workplace location]()

[Managing Neighborhoods]()

[Enable favorites option for Workplace Service Portal]()

[Create a workplace performer criteria]()

[Mapping employees to their designated workspaces]()

[Assign the workplace user role to employees]()

[Configuring shifts for your workplace]()

[Managing workplace shifts that you own]()

[Managing workplace reservations for employees]()

[Setting and tracking arrivals at the workplace]()

[Approve employee workplace reservation requests]()

[Managing workplace tasks]()

[Workplace knowledge management]()

[QR code management]()

[Location migration]()

[View workplace service usage analytics with Usage Insights]()

