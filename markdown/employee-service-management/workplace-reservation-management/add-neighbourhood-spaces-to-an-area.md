---
title: Assign spaces to an area
description: Assign spaces to an area. Employees can find and reserve them when they search for an area on the Reservation portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/workplace-reservation-management/add-neighbourhood-spaces-to-an-area.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Assign spaces to an area

Assign spaces to an area. Employees can find and reserve them when they search for an area on the Reservation portal.

## Before you begin

The following plugins must be installed:

-   Workplace Central
-   Workplace Reservation Management
-   Workplace Space Management
-   Workplace Core

The area to which spaces are assigned must be configured in the application.

1.  Navigate to **Workplace Core** &gt; **Space Administration** &gt; **Areas**.
2.  Check that the area is configured.

Ensure that the spaces are assigned to the area.

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration** &gt; **Spaces** and select the space.
2.  On the form, ensure that the **Area** field has a value.

For more information, see [Providing your workplace data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-core/providing-your-workplace-data-wsd.md).

Role required: sn\_wsd\_core.workplace\_manager or sn\_wsd\_rsv.admin

## About this task

Assign desks or spaces that belong to an area. When an employee searches for an area to make a reservation, all the available spaces or desks that belong to that area are displayed. You can add spaces individually or in bulk. For example, you can add spaces individually, such as C1 and C2, or you can add one space C with a quantity of 100.

## Procedure

1.  Navigate to **Workplace Core** &gt; **Space Administration** &gt; **Spaces**.

2.  Select the space to assign to the area.

3.  Open the form in the Workplace view.

    1.  On the form, select and hold \(or right-click\) the additional actions icon.

        \[Omitted image "additional-actions.png"\] Alt text:

    2.  In the list, select **View** &gt; **Workplace**.

4.  On the Space form, in the **Organization details** tab, select the area in the **Area** field.

5.  To add a bulk quantity of this space, specify a quantity in the **Reservable quantity** field in the **Extra information** tab.

6.  Select **Update**.


## Result

The space is added to the area. On the Reservation portal, the following actions are performed:

-   When an employee searches for the area, the assigned space is displayed.
-   If you have added bulk quantity for a space, the space is displayed with a maximum capacity in the card view. When an employee makes a reservation for this space, the capacity is deducted. The space is again displayed with the available capacity for the next reservation until the maximum capacity is 0.

If the reservable module has the **Enable restricted neighborhood rules** option enabled, the space is displayed based on neighborhood restrictions. The space is not displayed in search results if you are restricted from viewing spaces in that neighborhood. It is also hidden if you are not added in the Neighbourhood User Assignment table.

## What to do next

To view the spaces assigned to an area, navigate to **Workplace Core** &gt; **Space Administration** &gt; **Areas** and select an area. The assigned spaces are displayed in the Spaces related list.

**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a reservable view]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Create a quick reservation time slot]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Microsoft Teams]()

[Connect Workplace Reservation Management with Zoom]()

[Display permanent seat assignments on floor maps]()

[Display name of the person reserving a space]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

