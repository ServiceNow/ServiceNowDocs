---
title: View Space Optimization metrics
description: Use the Space Optimization dashboard Workplace Analytics to analyze space capacity and utilization trends to achieve optimal use of workspaces.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Working with Workplace Analytics, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# View Space Optimization metrics

Use the Space Optimization dashboard Workplace Analytics to analyze space capacity and utilization trends to achieve optimal use of workspaces.

## Prerequisites for accessing the Space Optimization dashboard

-   Ensure that the Workplace Central application is installed. For more information, see [Install Workplace Central](install-workplace-central.md)
-   Ensure that the Workplace Space Management \(sn\_wsd\_spcmgmt\) application is installed. For more information, see [Install Workplace Space Management](../../workplace-space-management/task/install-workplace-space-mgmt.md).
-   Ensure that the Workplace Central and Workplace Space Management applications and all of their associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Run the scheduled job **Workplace Analytics Space Management report data generation** before viewing the Space Optimization dashboard for the first time. For more information, see [Run the scheduled job for the Space Optimization dashboard](run-job-space-opt-dashboard.md).

## Accessing the dashboard

To access the Space Optimization dashboard, you must have any of the following roles: sn\_wsd\_spcmgmt.space\_planner, sn\_wsd\_spcmgmt.manager, sn\_wsd\_rsv.manager, or sn\_wsd\_core.workplace\_manager.

Access the dashboard using one of the following navigation paths:

-   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
-   **Workspaces** &gt; **Workplace Central**

## Reports

The following default reports show data for the past year only. You can adjust the data range by using the available filters for Date, Region, Site, Campus, Allocation, Workplace entity.

Allocation type \[sn\_wsd\_core.ALLOCATION\_TYPE\] enables you to specify an allocation type based on space utilization.Only allocations that are active in the selected time frame are considered for the reports. For more information, see [Allocate a cost center, department, or workplace entity](../../workplace-space-management/task/add-cost-center-department-floor.md).

![Filter data by Allocation type on the Space Optimization dashboard.](../images/wsd-space-optimize-dashboard-workplace-entity.png)

For more information, see [Allocation - types, setting, and impact](../../workplace-space-management/reference/setting-an-allocation-and-its-impact.md).

The Space Optimization dashboard also enables you to visualize data based on the Entity type. Manage space allocations based on the workplace entity to ensure proper space utilization.

![Space optimization dashboard showing headcount trends.](../images/wsd-space-optimization-dashboard.png)

For more information, see [Map designated workspaces to user profiles](../../workplace-service-delivery/task/map-employees-to-existing-workplace-locations-wsd.md).

Capacity is calculated based on the following criteria:

-   Total capacity is the total number of hours an active space is available for reservation.
-   Capacity is calculated using the reservation properties **Start time of the working day** and **End time of the working day**.

Utilization is calculated using the following criteria:

-   For employees with permanent seat allocation, space utilization is calculated using the reservation properties Start time of the working day \[sn\_wsd\_rsv.day\_start\] and End time of the working day \[sn\_wsd\_rsv.day\_end\].
-   For employees that don’t have a permanent seat allocation, space utilization is calculated from the total reservation time in day's work shift hours. The work shift or office hours is calculated from the Start time of the working day \[sn\_wsd\_rsv.day\_start\] and End time of the working day \[sn\_wsd\_rsv.day\_end\].
-   For example, if the office work hours are 9 hours and a meeting room is reserved for 11 hours, the total utilization in this case is 9 hours. The Start time of the working day \[sn\_wsd\_rsv.day\_start\] and End time of the working day \[sn\_wsd\_rsv.day\_end\] properties are used while calculating office hours. The unallocated hours in a day for a reserved space aren’t considered while calculating the total reservation time duration for a day or a multi-day reservation. The reservation property for office hours is set in **\(** &gt; **All** &gt; **Workplace Reservation Management** &gt; **Properties**.

-   **Capacity vs utilization**

    This report facet displays the available space resources versus its occupancy.

    Benefits:

    -   Select the more options icon \(![More options icon to refresh the report.](../images/dashboard-report-refresh-icon.png)\) to refresh the report.
    -   Insight into the space availability versus the occupancy trend.
    -   Enables you to reconfigure your space assignments and space optimization to achieve optimal resource utilization.
    -   A desk can be shared by multiple workplace entities.

        For example, a seat or desk is shared by user A and user B. If user A reserves the seat, the application checks the workplace entity of User A and calculates the space utilization and capacity ratio.

    -   Select a report facet or card and double-click to see the details.

-   **Peak utilization days**

    This report displays the average utilization for days of the week.

    Benefits:

    -   Select the more options icon \(![More options icon to refresh the report.](../images/dashboard-report-refresh-icon.png)\) to refresh the report.
    -   Insight into the space utilization for the days of the week.
    -   Enables you to prioritize resources according to the demand.
    -   Select a report facet and double-click to see the details.
    Calculation:

    `Average utilization = [Total utilization in hours for a weekday/Number of spaces available for the week day]`


-   **Space utilization by workplace entity**

    This report facet displays the average capacity and average utilization based on the workplace entity.

    ![Space utilization by workplace entity metrics.](../images/wsd-space-ulitization-by-workplace-entity.png)

    Benefits:

    -   Select the more options icon \(![More options icon to refresh the report.](../images/dashboard-report-refresh-icon.png)\) to refresh the report.
    -   Select the **Allocation** tab in the Filter by options and allocate by different workplace entity.
    -   Select **Entity type** in the Filter by options and select a workplace entity to view the space utilization metrics for a selected entity.
    -   Compare the set of data for average capacity and average utilization for a workplace entity.
    -   Select a report facet and double-click to see the details.
    Calculation:

    `Average capacity by workplace entity = [Total capacity in hours for a workplace entity/Number of spaces available for a workplace entity]`


-   **Space type utilization**

    This report facet displays the average capacity and average utilization for a space type.

    Benefits:

    -   Select the more options icon \(![More options icon to refresh the report.](../images/dashboard-report-refresh-icon.png)\) to refresh the report.
    -   Compare data for average capacity and average utilization for a space type.
    -   Add or remove space types to achieve the optimal space optimization.
    Calculation:

    `Average capacity by space type = [Total capacity in hours for a space type based on the office hours/Number of spaces available for a workplace entity]`


## Customizing widgets

You can customize the widgets to display relevant metrics by using the UI Builder. For more information, see [UI Builder tutorial](https://www.servicenow.com/docs/access?context=uib-tutorial&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   **[Run the scheduled job for the Space Optimization dashboard](run-job-space-opt-dashboard.md)**  
As an admin, run the scheduled job **Workplace Analytics Space Management report data generation** to calculate capacity and utilization for all spaces.

**Parent Topic:**[Working with Workplace Analytics](../concept/working-with-workplace-analytics.md)

**Related topics**  


[View Occupancy Dashboard](../../workplace-connectors/task/view-badging-tables.md)

[View Lease Administration metrics](view-lease-admin-analytics.md)

[View Maintenance Management metrics](view-maintenence-mgmt-analytics.md)

[Manage Workplace Dashboards](workplace-dashboards-wsd-central.md)

