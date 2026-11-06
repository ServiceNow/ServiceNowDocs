---
title: Allocation - types, setting, and impact
description: You can categorize the locations in your organization based on cost center, department, or workplace entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/workplace-space-management/setting-an-allocation-and-its-impact.html
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 10
keywords: [allocation, allocation type, allocation profile, allocation percentage, time-bound allocation, workplace entity]
breadcrumb: [Reference, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Allocation - types, setting, and impact

You can categorize the locations in your organization based on cost center, department, or workplace entity.

Allocate a workplace location to an allocation type. The application uses this classification for workplace-related activities, such as searching for spaces to reserve and planning scenarios.

## Allocation types

You can allocate your workplace location under the following system provided allocation types:

-   Cost center
-   Department
-   Workplace entity

**Important:** Starting from Workplace Core version 2.16.1, the allocation type **Department and cost center** is no longer available. A new allocation type **Workplace entity** is introduced that provides more advantages.

## System property

The application provides the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property. Use it to specify the allocation type. The allocation type determines which spaces are retrieved and displayed when users search for spaces to reserve, during scenario planning, and space recommendation.

Space search results depend on the allocation type, the user's workplace profile, and the **Require allocation check**and **Enable allocation duration check** settings in the reservable module. The duration check follows only the start and end dates of the allocation, which are set in the system time zone.

If you don't specify any allocation in the system property, then the **Require Allocation check** field is not available in the reservable module form.

## Setting an allocation type

On the workplace location's record, you can create or activate an existing allocation in the Allocations related list. For more information, refer to [Allocate a cost center, department, or workplace entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/add-cost-center-department-floor.md).

If you're an existing customer and are using Workplace Core version 2.16.1, a fix script is automatically applied to map your existing allocations to the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] property. For example, if your allocations are based on Department, then the property is set as Department. Similarly, if your allocations are based on Cost center, then the property is set as Cost center. If your allocations include both Cost center and Department, then the property is set as empty and warnings are displayed to specify an allocation type.

## Allocation profile and allocation percentage

When a space is co-owned or shared, you can record how each allocation relates to the space and what share of the space it covers. On an allocation record, you can specify the following fields:

-   **Allocation profile**: Indicates whether the cost center, department, or workplace entity owns the space or occupies it as a tenant.
-   **Allocation percentage**: The share of the space that the allocation covers, as a whole number. You can't enter a negative number, a decimal, or a fraction.

The application validates the allocation percentage as follows:

-   If you enter a value greater than 100, the record isn't saved. The application displays the message "Allocation percentage value for a record can't exceed 100%".
-   If the allocation percentages for an allocation profile don't add up to 100, the application displays the message "The total allocation percentage value doesn't add up to 100%". This check applies to spaces, areas, and floors, and is based on the allocation profile, not the allocation type.

You can set the allocation profile and allocation percentage in the Allocations related list of a space, area, or floor. In map-based space administration, you can also set them for one or more spaces by using the **Allocation** action.

## Time-bound allocations

You can limit the period during which an allocation applies by specifying a start date and an end date on the allocation record.

-   The **Start date** and **End date** fields are optional and contain a date with no time. They are available for all allocation types, regardless of the value of the **sn\_wsd\_core.ALLOCATION\_TYPE** system property.
-   You can set the dates on a floor, an area, or a space.
-   To restrict reservation search results by the allocation dates, select **Enable allocation duration check** in the reservable module. This option is available only when **Require allocation check** is selected. If you clear **Require allocation check**, the application clears and hides **Enable allocation duration check**. By default, it is cleared.

When an allocation reaches its end date, the following actions are performed:

-   A scheduled job deactivates active allocations that have an end date in the past.
-   A scheduled job that runs daily sends a notification titled "Upcoming Expiry of Space Allocation in 30 Days" for allocations that expire in 30 days. The notification includes a link to the list of expiring allocations.

The notification recipients depend on the allocation type:

-   Cost center: the manager of the cost center.
-   Department: the primary contact of the department.
-   Workplace entity: the **Managed by** user and the **Managed by group** of the workplace entity.

The **Managed by** user and the **Managed by group** of the building that contains the allocated location also receive the notification. For workplace entities, specify the **Managed by group** and **Managed by** fields on each entity record. Child entities don't inherit these fields. For more information, refer to [Configure Workplace entity and entity types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/workplace-entity.md).

When the allocation of a space has expired or hasn't started, the workplace profile location assignments that reference the space are flagged as an allocation anomaly. The application still creates the assignment regardless of the allocation dates.

## Impact of allocation

Depending on a workplace location's allocation, the following actions are performed:

-   When an employee searches for a location to reserve, the **Require allocation check** and **Enable allocation duration check** options on the reservable module control which locations appear. The locations displayed depend on the allocations the employee can access. The duration check follows only the start and end dates of the allocation, which are set in the system time zone.
-   You can make allocations based on the cost center, department, and the workplace entity to which a location or employee belongs.
-   You can make allocations based on the business hierarchy of your organization. You can assign a location or an employee to a workplace entity and create a hierarchy. The application enables you to configure entity types based on your businesses and assign workplace entities to them. You can also create a parent-child hierarchy between workplace entities. For more information, refer to [Configure Workplace entity and entity types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/workplace-entity.md).
-   During scenario creation, you can specify based on what type of allocation you want to group the spaces. The grouping options are displayed to you based on the allocation that is specified in the system property **sn\_wsd\_core.ALLOCATION\_TYPE**.

    **Important:** You cannot create a scenario based on workplace entities. You can only view and make map space administration for workplace entities.

-   During scenario planning, you can also change the **View by** option of a scenario to view based on different allocations. However, you cannot edit the scenario if the **View by** that you selected is different than the **Group by** setting of the scenario.
-   Scenarios created with a **Group by** option that differs from the current allocation type in the **sn\_wsd\_core.ALLOCATION\_TYPE** system property are read-only.
-   For a space, you can create multiple allocations of different types.
-   When an employee raises a space assistance request, the space allocation type is set by the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property.
-   When a space assistance request is deployed for an allocation type, the application doesn't override the following allocations:
    -   Allocations of other allocation types
    -   Allocations of the same or another type that have an active or future timeframe
    -   Parent workplace entity allocations that have an encompassing timeframe
-   The application takes the start and end dates of allocations into account when it calculates space utilization and capacity.

## Push down functionality in Workplace Space Management

The Workplace Space Management application enables you to push down the cost center or department of a parent workplace location to its child locations.

You can assign the cost center or department to child locations such as areas, rooms, and spaces. Select the **Push down** option on the Floor or Area form to apply the values of the **Cost center** or **Department** fields. The cost center or department is applied based on the **Push down** option selected in child workplace locations.

When you push down allocations from a floor or an area, the application copies the entire allocation record to the child locations. The copied record includes the start date, end date, allocation profile, and allocation percentage. You can choose whether to keep or replace the allocations that already exist on the child locations.

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
</table>If a space is assigned to multiple restricted neighborhoods, a user can access the space when the user belongs to at least one of those neighborhoods.

For users who don't have a department, cost center, or workplace entity assigned, access to spaces depends on the **sn\_wsd\_rsv.UNASSIGNED\_USER\_ACCESS\_MODE** system property.

## Space access for users without an allocation

Use the **sn\_wsd\_rsv.UNASSIGNED\_USER\_ACCESS\_MODE** system property to control which spaces a user can reserve when the user doesn't have a department, cost center, or workplace entity assigned. The property is available only when Workplace Space Management is installed.

The property has the following values:

-   **unrestricted** \(default\): The user can access all spaces regardless of their allocations.
-   **restricted**: The user can access only the spaces whose allocation matches the allocation type that is set in the **sn\_wsd\_core.ALLOCATION\_TYPE** system property.

The setting applies to all types of space reservations. If **Enable allocation duration check** is selected in the reservable module, the application also considers the allocation dates. A space that has no allocation during a period is available to restricted users in that period.

**Parent Topic:**[Workplace Space Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/workplace-space-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Space Management]()

[Properties installed with Workplace Space Management]()

[View by Configuration form]()

[KPI Configuration form]()

[]()

