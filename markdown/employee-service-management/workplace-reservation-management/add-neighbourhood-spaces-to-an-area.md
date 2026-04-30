---
title: Assign spaces to an area
description: Add spaces to an area to make them available for reservation. On the Reservation portal, when an employee searches for an area, all the available spaces that are assigned to that area are displayed.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Assign spaces to an area

Add spaces to an area to make them available for reservation. On the Reservation portal, when an employee searches for an area, all the available spaces that are assigned to that area are displayed.

## Before you begin

Ensure that the area to which you are assigning spaces is configured in the application.

1.  Navigate to **Workplace Core** &gt; **Space Administration** &gt; **Areas**.
2.  Check that the area is configured.

Ensure that the spaces are assigned to the area.

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration** &gt; **Spaces** and select the space.
2.  On the form, ensure that the **Area** field has a value.

For more information, see [Providing your workplace data](../../workplace-service-delivery/concept/providing-your-workplace-data-wsd.md).

Role required: sn\_wsd\_core.workplace\_manager or sn\_wsd\_rsv.admin

## About this task

Assign desks or spaces that belong to an area. When an employee searches for an area to make a reservation, all the available spaces or desks that belong to that area are displayed. You can add spaces individually or in bulk. For example, you can add spaces individually like C1 and C2, or you can add one space C with a quantity of 100.

## Procedure

1.  Navigate to **Workplace Core** &gt; **Space Administration** &gt; **Spaces**.

2.  Select the space that you want to assign to the area.

3.  Open the form in the Workplace view.

    1.  On the top-left corner of the form, right-click the additional actions icon.

        ![Additional actions icon.](../image/additional-actions.png)

    2.  In the list, select **View** &gt; **Workplace**.

4.  On the Space form, in the **Organization details** tab, select the area in the **Area** field.

5.  To add a bulk quantity of this space, specify a quantity in **Reservable quantity** field in the **Extra information** tab.

6.  Click **Update**.


## Result

The space is added to the area. On the Reservation portal, the following actions are performed:

-   When an employee searches for the area, the assigned space is displayed.
-   If you have added bulk quantity for a space, the space is displayed with a maximum capacity in the card view. When an employee makes a reservation for this space, the capacity is deducted. The space is again displayed with the available capacity for the next reservation until the maximum capacity is 0.

If the reservable module to which the space is assigned has the **Enable restricted neighborhood rules** option enabled, then the space is displayed to the user based on the restrictions. That is, if the user is restricted to view the spaces of this neighbourhood, then the space is not displayed to him in the search results. If the user is restricted to view the spaces of a neighbourhood to which they don't belong or, if the user is not added in the Neighbourhood User Assignment table.

## What to do next

To view the spaces assigned to an area, navigate to **Workplace Core** &gt; **Space Administration** &gt; **Areas** and select an area. The assigned spaces are displayed in the Spaces related list.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

