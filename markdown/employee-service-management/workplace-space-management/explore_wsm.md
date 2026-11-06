---
title: Exploring Workplace Space Management
description: Space Management helps users find and book desks, meeting rooms, and parking spaces. You can optimize the inventory of available workplace spaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/workplace-space-management/explore\_wsm.html
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Exploring Workplace Space Management

Space Management helps users find and book desks, meeting rooms, and parking spaces. You can optimize the inventory of available workplace spaces.

## Enhanced space administration

The Workplace Space Management application is an enhanced version of the existing Space administration module that is available in the ServiceNow® Workplace Core application. While you have complete access to the Workplace Core application, the Workplace Space Management application also enables you to perform workplace-related forms in the Space Management view.

\[Omitted image "spaces-flow-space-mgmt-to-workplace-central.svg"\] Alt text: Diagram showing how spaces flow from Space Management to Workplace Central.

## Monitor workplace locations

As a Workplace manager, you can administer any workplace location, such as employee workspaces, conference rooms, office buildings, and campuses. You can work with workplace locations from a single place. You can manage regions, sites, campuses, buildings, floors, areas, rooms, and spaces using the application.

If you use Indoor Mapping, you can also administer spaces on interactive floor plans in Workplace Central. Map-based space administration lets you edit space attributes and allocation data individually or in bulk, and export the data. Changes update production data immediately.

## Perform exclusive space-related actions

Apart from the features provided by Workplace Core, the Workplace Space Management application enables you to do the following exclusive space-related actions:

-   Use all space administration-related actions available in the Workplace Core application.
-   Specify the measurement details of a location such as the measuring unit and size of a space.
-   Assign a cost center or department to a space.
-   Configure a workspace or desk as flexible or permanent.
-   Configure a space type as usable.
-   Update or recalculate a workplace location's total and usable size whenever there are changes.
-   View the reason for anomalies caused in a workplace profile.

For more information about each feature, refer to [Managing workplace locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/Creating-workplace-location-records-using-spce-mgmt.md).

## Optimize spaces by planning scenarios

Install the Workplace Central application to use the Space optimization feature that helps you plan scenarios to allocate spaces, change user assignments, and make other space-related changes. Perform scenario planning using stack plans and a floor map view. For more information about Workplace Central - Space optimization, refer to [Space Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/space-optimization.md).

## Allocate spaces in Workplace Central

Spaces that you create in the Workplace Space Management application are the same location records that Workplace Central uses. Space planners view these spaces in Workplace Central, and then allocate and assign them. The workplace location tables extend the global location table, so each record keeps its sys\_id and relationships. The **Class** value of a location record determines which workplace location table displays it. If you use Indoor Mapping, keep its parallel set of location tables in sync with the workplace location tables.

Space planners use the following structures to allocate spaces.

-   Neighborhoods are groups of spaces assigned to a set of employees, such as a department or business unit. A neighborhood can span multiple campuses, buildings, and floors.
-   Workplace entities are custom organizational hierarchy levels, such as business units or divisions, that you associate with spaces and neighborhoods. They extend allocation by department or cost center.
-   Space ownership and tenancy are usage allocations on individual space records for entities, departments, or cost centers. They represent shared or co-owned spaces.

Allocation determines which entity, department, cost center, or neighborhood owns or uses a space. User assignments determine which employees occupy it. In Workplace Central, planners can view allocations by department, cost center, neighborhood, space type, assignment type, or space status.

Floor plan-based scenario planning requires Indoor Mapping floor plans. In Map Studio, configure the **Space Planning** view for each campus. Without configured maps, planners can view stack plans at the building level only.

## Use Workplace Core features

The application enables you to perform the following actions as you would in the Workplace Core application, but with extra features:

-   [Create records for your workplace data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/create-records-of-workplace-data-wsd.md).
-   [Configuring spreadsheets to import workplace data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/importing-workspace-data-wsd.md).
-   [Add a space type configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/add-space-type-configuration-wsd.md).
-   [Block a workplace location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/block-workplace-location.md).

-   **[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/space-mgmt-overview.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/space-mgmt-overview.md)**  

-   **[Space Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/space-optimization.md)**  
As a space planner, you can use the Workplace Central to monitor all your scenarios and workplace-related information from a single page called Space Optimization.
-   **[Scenario Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/scenario-planning.md)**  
Manage space allocations in your workplace in the most efficient way using the Space optimization scenario planning feature. Adjust your existing space allocations, floor arrangements, and employee seating plan by creating a scenario and deploying it.
-   **[Schedule Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/schedule-planning.md)**  
Manage space assignments to help employees head back to the office.

**Parent Topic:**[Workplace Space Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/workplace-space-mgmt-ovw.md)

