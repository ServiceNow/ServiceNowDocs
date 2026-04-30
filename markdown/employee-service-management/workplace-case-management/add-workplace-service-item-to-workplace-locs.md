---
title: Make a workplace service item available to a workplace location
description: Make a workplace service item available to specific workplace locations. Select any workplace location such as a region, site, campus, building, floor, area, or a space.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Add a workplace service item to a workplace service, Configure Workplace Case Management, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Make a workplace service item available to a workplace location

Make a workplace service item available to specific workplace locations. Select any workplace location such as a region, site, campus, building, floor, area, or a space.

## Before you begin

Role required: sn\_wsd\_case.manager

## About this task

Select workplace locations where the workplace item must be available. Employees can order the item while making a workplace service request. Select a parent location such as a region, site, or a campus. You can also select child locations such as a building or its spaces.

-   You can specify different costs for different workplace locations by creating multiple Workplace Service Item Location records.
-   The cost of the workplace service item is also applied to all the child workplace locations of that selected workplace location. If the workplace item has a different cost specified for any child workplace location, then the same cost is applied instead of the parent location. For example, assume you specified the cost of the workplace item as $100 for the region ABC. You also specified a separate cost for the workplace item in its site XYZ as $75. Then, the cost of the child workplace location \($75\) is applied.
-   If the workplace service item isn't assigned to any location, then the availability of the item depends on the availability of the workplace service to the specified workplace locations. You can view the details of the workplace locations where the workplace service is available in the Workplace locations related list.
-   The availability of a workplace service item depends on the locations specified in the workplace service location and the workplace service item location.
    -   If there are no workplace service location and no service item location specified for a Workplace service, then the workplace service items are available to all the locations.
    -   If there is a workplace service location specified and there is no service item location specified for a Workplace service, then the workplace service items are available to that location and child locations specified in a Workplace service location.
    -   If you specified locationA for the workplace service and specified locationB \(not in the hierarchy of locationA\) in the workplace service item location \(in Workplace Service Item Locations related list of the workplace service item\), then the following actions are performed when an employee raises a workplace service request:

        -   If the employee raises the request for locationA or any locations in the hierarchy of locationA, then all the workplace service items that are available to locationA, except items available to locationB are displayed.
        -   If the employee raises the request for locationB or any locations in the hierarchy of locationB, then no workplace service items are displayed as it isn't in any hierarchy of locationA.
        The same logic is applied while displaying workplace service items associated with workplace spaces in general.

        Configuring **Lead time for ordering** restricts in adding any extra service items to a reservation, if it is within the lead time for ordering.

        **Restrict cancellation of requested services** restricts employees to cancel the requested services.


## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select the workplace service in which the workplace service item is added.

3.  On the form, scroll down to the Workplace Service items related list.

4.  Select the workplace service item that you want to assign to a workplace location.

5.  On the form, scroll down to the Workplace Service Item Locations related list.

6.  Click **Edit...**.

7.  To select and move the service, do the following:

    1.  On the Edit Members form, select the service.

    2.  From the **Collection** column on the left, select the workplace location.

    3.  To move the workplace location to the **Workplace location List** column on the right, use the add-remove icon.

        Select the add-remove icon \(![Add-remove icon.](../../wsd-reservation-management/image/add-remove-icon.png)\).

8.  Click **Save**.

9.  To change the cost of the item for a particular workplace location, do the following:

    1.  On the form, scroll down to the Workplace Service Item Locations related list.

    2.  To change the cost, select the preview icon next to the workplace location.

        Select the preview icon \(**Open record**![Preview icon.](../image/preview-icon.png)\).

    3.  In the preview dialog box, click.

    4.  On the form, edit the **Cost** field.

    5.  Click **Update**.


## Result

The workplace service item will now be available to order at the specified locations. The cost of the workplace item at a location depends on the cost specified on its nearest workplace location in the workplace location hierarchy. For example, if a cost is specified for a campus and also for its building, then the cost that is specified on the building is applied.

**Parent Topic:**[Add a workplace service item to a workplace service](add-workplace-service-items.md)

