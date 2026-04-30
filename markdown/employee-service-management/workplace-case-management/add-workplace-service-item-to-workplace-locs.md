---
title: Make a workplace service item available to a workplace location
description: Make a workplace service item available to specific workplace locations. Select any workplace location such as a region, site, campus, building, floor, area, or a space.
locale: en-US
release: yokohama
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Add a workplace service item to a workplace service, Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Make a workplace service item available to a workplace location

Make a workplace service item available to specific workplace locations. Select any workplace location such as a region, site, campus, building, floor, area, or a space.

## Before you begin

Role required: sn\_wsd\_case.manager

## About this task

Select workplace locations where the workplace item must be available. Employees can order the item while making a workplace service request. Select a parent location such as a region, site, or a campus. You can also select child locations such as a building or its spaces.

-   You can specify different configurations like costs and durations for different workplace locations by creating multiple Workplace Service Item Location records.
-   The Workplace Service Item configurations like cost and duration for a selected workplace location are also applied to the child workplace locations.
    -   If the workplace item has different configurations specified for the parent and child workplace locations, the configuration of the child location is applied instead of the parent location. For example, if the cost of the workplace item as $100 for the region ABC and the cost for the workplace item the campus XYZ is $75, the cost of the child workplace location \($75\) is applied.
    -   If a workplace item does not have a configuration specified for a workplace location, the default configuration from the workplace service item record is applied. For example, if the cleanup duration of the Workplace Service Item is 15 minutes and the cleanup duration for a workplace location is not specified, the 15 minute cleanup duration is applied.
-   If the workplace service item isn't assigned to any location, the availability of the item depends on the availability of the workplace service. You can view the details of the workplace locations where the workplace service is available in the Workplace locations related list.
-   The availability of a workplace service item depends on the locations specified in the workplace service location and the workplace service item location.
    -   If there is no workplace service location and no service item location specified for a Workplace service, the workplace service items are available to all locations.
    -   If a workplace service location is specified for a Workplace service and no service item location is specified, the workplace service items are available to the specified location and child locations specified in the Workplace service locations related list.
    -   If you specified location A for the workplace service and specified location B \(not in the hierarchy of location A\) in the workplace service item location \(in Workplace Service Item Locations related list of the workplace service item\), then the following actions are performed when an employee raises a workplace service request:

        -   If the employee raises the request for location A or any locations in the hierarchy of location A, then all the workplace service items that are available to location A, except items available to location B are displayed.
        -   If the employee raises the request for location B or any locations in the hierarchy of location B, then no workplace service items are displayed.
        The same logic is applied while displaying workplace service items associated with workplace spaces in general.

        Configuring **Lead time for ordering** restricts in adding any extra service items to a reservation, if it is within the lead time for ordering.

        **Restrict cancellation of requested services** restricts employees to cancel the requested services.


## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select the workplace service in which the workplace service item is added.

3.  On the form, scroll down to the Workplace Service items related list.

4.  Select the workplace service item that you want to assign to a workplace location.

5.  On the form, scroll down to the Workplace Service Item Locations related list.

6.  Select **Edit...**.

7.  Select and move the service.

    1.  On the Edit Members form, select the service.

    2.  From the **Collection** column on the left, select the workplace location.

    3.  Move the workplace location to the **Workplace location List** column on the right by using the add-remove icon \(![Add-remove icon.](../../wsd-reservation-management/image/add-remove-icon.png)\).

8.  Select **Save**.

9.  Change the cost of the item for a particular workplace location.

    1.  On the form, scroll down to the Workplace Service Item Locations related list.

    2.  Select the preview icon \(![Preview icon.](../image/preview-icon.png)\) for the workplace location.

    3.  In the preview dialog box, select **Open record**.

    4.  On the form, edit the **Cost** field.

    5.  Select **Update**.


## Result

The workplace service item is available to order at the specified locations. The cost of the workplace item at a location depends on the cost specified on its nearest workplace location in the workplace location hierarchy.

