---
title: Managing workplace locations
description: Apart from the space administration features provided by Workplace Core, the Workplace Space Management application enables you to configure exclusive space-related settings.
locale: en-US
release: yokohama
product: Workplace Space Management
classification: workplace-space-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Managing workplace locations

Apart from the space administration features provided by Workplace Core, the Workplace Space Management application enables you to configure exclusive space-related settings.

To create workplace location records for buildings, floors, areas, and spaces you can use Workplace Core or Workplace Space Management. To add a workplace records using Workplace Core, see [Create records for your workplace data](../../workplace-service-delivery/task/create-records-of-workplace-data-wsd.md).

Workplace Space Management provides more options for workplace-related functionality to the workplace location records. You can use the Workplace Space Management application to view the workplace location forms in the Space Management view.

The following features are available in the Space Management view on the workplace location form:

-   **Measurement details**

    Specify the measurement details of the workplace location such as the location size and the unit of measurement. For buildings, floors, and areas, you can also specify the total size and the usable size to plan infrastructure and other maintenance activities. For more information, see [Compute CAD file properties to extract space or room surface area](../../wsd-indoor-mapping/task/compute-cad-properties.md).

-   **Allocation**

    Allocate or assign a cost center, department, or a workplace entity to workplace locations to track locations and perform workplace-related activities.

-   **Push down the allocation to child locations**

    Automatically assign the allocation type of the parent location to the child locations. Specify how you want to implement the push down functionality in the **Push down** field. You can track the progress of the push down process in the **Push down state** field.

    The push down functionality depends on the following conditions:

    -   If the child location has an existing allocation, the child location's allocation is either replaced or not replaced based on the **Push down** option specified in the parent location.
    -   The accessibility of the spaces assigned with an allocation depends on whether the user workplace profile configuration and the Space type configuration match. For more information, see [Allocation - types, setting, and impact](../reference/setting-an-allocation-and-its-impact.md).
-   **Space usability**

    Specify whether a space type is usable. If a space type is usable, the spaces assigned to that space type are included in reservation-related activities and the usable size calculation of the parent location. If a space type isn’t set as usable, then the spaces assigned to that type aren’t included in reservation-related activities or the usable size calculation of the parent location.

-   **Flexible or permanent spaces**

    Configure a space as a flexible or a permanent space. This feature is applicable only to spaces of the space type **Workspace/desk**. If you configure a space as flexible, then the space is available for reservation on the Reservation portal. If you configure a space as permanent, then the spaces ares not available for reservation on the Reservation portal.

-   **View anomalies caused in a workplace profile**

    You can view the reason for anomalies in a workplace profile. Anomalies in workplace profiles are caused by a mismatch in the cost center, department, or assignment type between the user and the workplace location. For more information, see [Workplace location assignment anomaly types](../../workplace-service-delivery/reference/location-assignment-anomaly-types.md).


-   **[Add a campus](../task/add-a-campus.md)**  
A Workplace Service Delivery campus contains buildings, floors, areas, or spaces.
-   **[Add a building using Workplace Space Management](../task/add-new-building-1.md)**  
Create a record for every building that is part of your organization. Specify to which region, site, and time zone does the building belong to.
-   **[Add a floor using Workplace Space Management](../task/add-a-floor-1.md)**  
Create a record for every floor of a building. Specify the measurement details of the floor such as the total size and the usable size.
-   **[Add an area using Workplace Space Management](../task/add-an-area.md)**  
Create a record for every area that is located on a floor.
-   **[Add a room using Workplace Space Management](../task/add-a-room.md)**  
Create a record for every room located in an area or a floor. Specify the size of the room. Assign the room to a cost center or a department.
-   **[Add a space using Workplace Space Management](../task/add-a-space.md)**  
Create a space record for every workspace located on a floor. Specify the space type and the size of the space.
-   **[Allocate a cost center, department, or workplace entity](../task/add-cost-center-department-floor.md)**  
Assign either a cost center, department, or workplace entity to a workplace location. Manage space consumptions, expenses, workplace assignments, and reservations based on an employee cost center, department, or workplace entity.
-   **[Configure a workspace or desk as flexible or permanent](../task/assign-a-flex-perm-space.md)**  
Define if a space is flexible or permanent. On the Reservation portal, the availability of a space for a user profile depends on its assignment type.
-   **[Update the measurement details of a workplace location](../task/update-measurement-details-of-workplace-location.md)**  
Specify the size of a location. If the location is an area, floor or building, then you can update or recalculate the total and usable size.
-   **[Change the status of a workplace location](../task/change-active-status-of-workplace-location.md)**  
Change the availability of a workplace location to Active, Future, Temporary, or Retired. The availability of a workplace location for any workplace-related activities is determined based on the status that is set.
-   **[Configure a BOMA type](../task/configure-a-boma-type.md)**  
Define a BOMA type using which you can classify a space based on its BOMA standard.
-   **[Map a space type with BOMA type](../task/map-a-space-type-with-boma-type.md)**  
Using Workplace Space Management, map a space type that you created using Workplace Core with a BOMA type.
-   **[Create a Space Recommender rule](../task/create-a-space-recommender-rule.md)**  
Define a space recommender rule using which the qualifying spaces must be calculated when a user raises a space assistance request using Workplace Service Portal. You must have Workplace Central plugin.
-   **[Raise a space assistance request](../task/raise-a-space-recommendation-request.md)**  
Submit a workplace service request to get space allocation recommendations using the Workplace Service Portal. The Workplace Service Delivery space assistance provides you with the best space allocation plan options based on the space quantity and the department that you specify. You can select the most suitable allocation or none. Depending on your selection, the Space planner deploys the plan to use.
-   **[Create a view-by configuration](../task/create-view-by-config.md)**  
Create a configuration to filter the view of the scenario planner or building overview.
-   **[Reviewing allocation changes](reviewing-allocation-changes.md)**  
Review allocation changes in the Space Allocation Type Change Tracker table to plan changes for your scenarios.

**Parent Topic:**[Workplace Space Management](workplace-space-mgmt-ovw.md)

