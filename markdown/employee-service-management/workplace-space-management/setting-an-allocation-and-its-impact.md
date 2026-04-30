---
title: Allocation - types, setting, and impact
description: You can categorize the locations in your organization based on cost center, department, or workplace entity.
locale: en-US
release: zurich
product: Workplace Space Management
classification: workplace-space-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Explore, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Allocation - types, setting, and impact

You can categorize the locations in your organization based on cost center, department, or workplace entity.

Allocate your workplace location to a type based on which at any time the location can be classified when performing various workplace-related activities.

## Allocation types

You can allocate your workplace location under the following system provided allocation types:

-   Cost center
-   Department
-   Workplace entity

**Important:** Starting from Workplace Core version 2.16.1, the allocation type **Department and cost center** is no longer available. A new allocation type **Workplace entity** is introduced that provides more advantages.

## System property

The application provides you with the system property, Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\], which enables you to specify an allocation type based on which you want spaces to be retrieved and displayed to users while searching for spaces to reserve, during scenario planning, space recommendation and more.

When a user searches for a space to reserve, depending on the allocation type, the workplace profile of the user, and the **Reservation Allocation check** and **Enable allocation duration check** settings in the reservable module, the spaces are displayed to the users. The duration check follows only the start and end dates of the allocation, which are set in the system time zone.

If you do not specify any allocation in the system property, then the **Require Allocation check** field is not available in the reservable module form.

## Setting an allocation type

On the workplace location's record, you can create or activate an existing allocation in the Allocations related list. For more information, refer to [Allocate a cost center, department, or workplace entity](../task/add-cost-center-department-floor.md).

If you are an existing customer and are using Workplace Core version below 2.16.1, then a fix script is automatically applied to map your existing allocations to the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] property. For example, if your allocations are based on Department, then the property is set as Department. Similarly, if your allocations are based on Cost center, then the property is set as Cost center. If your allocations include both Cost center or Department, then the property is set as empty and warnings are displayed to specify an allocation type.

## Impact of allocation

Depending on a workplace location's allocation, the following actions are performed:

-   When an employee searches for a location to reserve and if the **Require allocation check** and **Enable allocation duration check** options are enabled on the reservable module, the appearance of the resultant locations depends on the allocations that the employee can access. The duration check follows only the start and end dates of the allocation, which are set in the system time zone.
-   You can make allocations based on the cost center, department, and the workplace entity to which a location or employee belongs.
-   You can make allocations based on the business hierarchy of your organization. You can assign a location or an employee to a workplace entity and create a hierarchy. The application enables you to configure entity types based on your businesses and assign workplace entities to them. You can also create a parent-child hierarchy between workplace entities. For more information, refer to [Configure Workplace entity and entity types](../../workplace-service-delivery/concept/workplace-entity.md).
-   During scenario creation, you can specify based on what type of allocation you want to group the spaces. The grouping options are displayed to you based on the allocation that is specified in the system property **sn\_wsd\_core.ALLOCATION\_TYPE**.

    **Important:** You cannot create a scenario based on workplace entities. You can only view and make map space administration for workplace entities.

-   During scenario planning, you can also change the **View by** option of a scenario to view based on different allocations. However, you cannot edit the scenario if the **View by** that you selected is different than the **Group by** setting of the scenario.
-   In the case of scenarios that are created with a **Group by** option that is not the same as the current allocation type set in the **sn\_wsd\_core.ALLOCATION\_TYPE** system property, then such scenarios can only be viewed in a read-only mode.
-   For a space, you can create multiple allocations of different types.
-   When an employee raises a space assistance request, the allocation type of the spaces is set based in the allocation type that is specified in the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property.

## Push down functionality in Workplace Space Management

The Workplace Space Management application enables you to push down the cost center or department of a parent workplace location to its child locations.

You can assign the cost center or department to child locations such as areas, rooms, and spaces. Select the **Push down** option on the Floor or Area form to apply the values of the **Cost center** or **Department** fields. The cost center or department is applied based on the **Push down** option selected in child workplace locations.

The following table explains how the push down functionality works with respect to **Cost center** and **Department** field configuration of a workplace profile and a space:

## Access to spaces based on allocation

Users can be assigned a Cost Center, Department, or Workplace Entity. The Cost Center or Department is assigned from the Users \[sys\_user\] table and the Workplace Entity is assigned from the User Workplace Profile \[sn\_wsd\_core\_workplace\_profile\] table.

Access to a space depends on the type of allocation set in the sn\_wsd\_core.ALLOCATION\_TYPE system property and the allocation set in the space configuration.

<table id="table_m3k_y1g_wpb"><thead><tr><th>

Value of the allocation type property

</th><th>

Space configuration

</th><th>

Accessibility on the space based on the configuration match

</th></tr></thead><tbody><tr><td>

Cost center

</td><td>

**Cost center**: Null **Department**: Null or `<value>`

**Workplace Entity**: Null or `<value>`

</td><td>

The user can access.

</td></tr><tr><td>

Cost center

</td><td>

**Cost center**: `<value>`**Department**: Null or `<value>`

**Workplace Entity**: Null or `<value>`

</td><td>

The user can access if the Cost Center matches.

</td></tr><tr><td>

Department

</td><td>

**Cost center**: Null or `<value>`**Department**: Null

**Workplace Entity**: Null or `<value>`

</td><td>

The user can access.

</td></tr><tr><td>

Department

</td><td>

**Cost Center**: Null or `<value>`**Department**: `<value>`

**Workplace Entity**: Null or `<value>`

</td><td>

The user can access if the Department matches.

</td></tr><tr><td>

Workplace Entity

</td><td>

**Cost Center**: Null or `<value>`**Department**: Null or `<value>`

**Workplace Entity**: Null

</td><td>

The user can access.

</td></tr><tr><td>

Workplace Entity

</td><td>

**Cost Center**: Null or `<value>`**Department**: Null or `<value>`

**Workplace Entity**: `<value>`

</td><td>

The user can access if the Workplace Entity or its parent matches.

</td></tr><tr><td>

Null

</td><td>

**Cost Center**: Null or `<value>` **Department**: Null or `<value>`

**Workplace Entity**: Null or `<value>`

</td><td>

The user can access.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Workplace Space Management](../concept/explore_wsm.md)

**Related topics**  


[Space Optimization](../../workplace-central/concept/space-optimization.md)

[Scenario Planning](../../workplace-central/concept/scenario-planning.md)

[Schedule Planning](../../workplace-central/concept/schedule-planning.md)

