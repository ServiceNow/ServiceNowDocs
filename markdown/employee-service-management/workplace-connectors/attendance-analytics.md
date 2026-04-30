---
title: Attendance Analytics
description: The Attendance analytics table computes badging data based on the employee head count at the region, site, campus, and building level. It derives occupancy data from the Employee Attendance Data table.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for badging data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Attendance Analytics

The Attendance analytics table computes badging data based on the employee head count at the region, site, campus, and building level. It derives occupancy data from the Employee Attendance Data table.

## Before you begin

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **Employee Attendance Data**.

    Verify that the Event Type column is set to **Swipe-in** and the State column is set to **Access Granted**.

2.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Workplace profiles**.

    -   Verify that the **Location** field is updated with the correct location. For more information, see [Set the primary location of a workplace profile](../../workplace-service-delivery/task/set-prim-location-of-worplace-profile.md).
    -   Verify that the **Workplace entity** column is mapped to the user workplace profile. For more information, see [Map designated workspaces to user profiles](../../workplace-service-delivery/task/map-employees-to-existing-workplace-locations-wsd.md) and [Configure Workplace entity and entity types](../../workplace-service-delivery/concept/workplace-entity.md).
3.  Navigate to **All** and in the application context menu search for **sn\_wsd\_central\_attendance\_analytics.list**.

    The Attendance Analytics page is displayed.

    **Note:** Attendance data records with N-2 timestamp are processed by the scheduled job. Here, N is the current date or day before yesterday.

    The Occupancy dashboard metrics can be viewed in Workplace Central. The following roles can access the reports:

    -   sn\_wsd\_central.workplace\_analytics\_user
    -   sn\_wsd\_wc.manager
    -   sn\_wsd\_wc.user
4.  Navigate to **All** &gt; **Workplace Central** &gt; **Occupancy Dashboard**.

    In Workplace Central, filter data by **Workplace entity** on the Occupancy dashboard data.

    -   The scheduled job **WSDHeadCount Daily Job** in Workplace Central runs daily, and retrieves data from the Employee Attendance table and loads it into the Attendance Analytics table.
    -   The WSDHeadCount Daily Job scheduled job checks for Workplace entity mapped values. It populates the employee space occupancy data based on the head count at the Region, Site, Campus, and Building level for a workplace entity.

        ![Workplace Analytics showing Occupancy Dashboard metrics.](../images/workplace-attendance-analytics-dashboard.png)

    For more information, see [View Occupancy Dashboard](view-badging-tables.md).


**Parent Topic:**[Setup Workplace Connectors for badging data](../concept/setup-workplace-connectors.md)

**Previous topic:**[Badging Data](badging-data.md)

**Next topic:**[Extension point for badging data](extension-point-for-badging-data.md)

