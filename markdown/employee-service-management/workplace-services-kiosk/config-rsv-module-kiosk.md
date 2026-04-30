---
title: Configure Reservable Module for kiosk reservation
description: Configure the Reservable Module for Workplace Services Kiosk to enable employees and guests to make reservations. Employees and guests can find available spaces on the kiosk map and make reservations.
locale: en-US
release: zurich
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 8
breadcrumb: [Configure, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Configure Reservable Module for kiosk reservation

Configure the Reservable Module for Workplace Services Kiosk to enable employees and guests to make reservations. Employees and guests can find available spaces on the kiosk map and make reservations.

## Before you begin

Install and configure the following:

-   Workplace Reservation Management
-   Workplace Services Kiosk
-   Workplace Central
-   Workplace Indoor Mapping
-   Workplace CoreWorkplace Space Management

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Reservable Module**.

    For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md). On the Reservable Module Configuration page, select the Kiosk module and configure it. This configuration enables employees and guests to select a kiosk on their physical device and make reservations.

2.  Complete the following information for creating a kiosk reservation Reservable Module:

    -   Name: Name of the Kiosk module.
    -   Title: Title of the Kiosk that you want to create.
    -   Inline Title: Inline title for the kiosk.
    -   Active: Check box option to indicate that Kiosk is active.
    -   Image: Add an image for the kiosk.
3.  Select the Reservable Table Configuration tab.

    On the form, fill in the information.

    ![Reseravable Table Configuration form.](../../wsd-reservation-management/image/Reservable-module-table.png)

<table id="table_zkf_5wr_wfc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Selection type

</td><td>

Type of selection to display in the search results when employees search. Select one of the following options:-   **Specific unit**: The search result displays every workplace item.
-   **Container**: The search result displays the parent or container of the workplace items. If you select **Container**, the search results are displayed in groups with a defined quantity available for reservation. Employees can select a container to reserve and any available space from the container is assigned for reservation.


</td></tr><tr><td>

Reservable type

</td><td>

Type of the reservable item. For example, Locations.

</td></tr><tr><td>

Reservable table

</td><td>

Table for the reservable workplace items.**Note:** If you have selected **Location** in **Reservable type**, use only the Space \[sn\_wsd\_core\_space\] table and its extended tables.

</td></tr><tr><td>

Reservable filter

</td><td>

Filter conditions on the reservable items in the Reservable table. The reservable items are displayed on the application based on the given conditions. Filter conditions on the reservable items in the Reservable table. The reservable items are displayed on the application based on the given conditions.

To add a condition, select **Add Filter Condition**. To add an **OR**condition, select **Add "OR"** Clause.

-   To add a condition, select **Add Filter Condition**.
-   To add an OR condition, select **Add "OR" Clause**.
**Note:** When applying filter criteria on a location, verify that the **Active** and**Is reservable** check boxes are active and selected for rooms and spaces that are added to a location. Not performing this step adds and displays the inactive or non-reservable spaces and rooms while making a reservation. [Add a room using Workplace Space Management](../../workplace-space-management/task/add-a-room.md) and [Add a room form](../../wsd-reservation-management/reference/add-room-form.md).

</td></tr><tr><td>

**Area \(Container\) selection** section

</td><td>

Specify the field details.

</td></tr><tr><td>

Reservable container field

</td><td>

Specify the grouping criteria. The field appears only if you selected **Container** as the **Selection type**. The field is automatically set to **Area**. For example, when the field is set to **Area**, the reservation search results appear as groups based on areas.

</td></tr><tr><td>

Reservable quantity field

</td><td>

Reservable quantity for workplace spaces. The **Reservable Quantity** field determines the number of times a container can be booked within a specific reservation time period. This setting provides with flexibility in setting up space reservations without out the need to create individual space records for reservation. For example, if you select **Reservable Quantity**, the container can be reserved as many times as the combined reservable quantity values of all spaces within that container. The reservable quantity depends on the number of spaces provided in the Capacity column of the Workplace Core Space table.

</td></tr></tbody>
</table>4.  Select the **Reservable Module Configuration** tab.

    ![Reservable Configuration Tab form. Select the Kiosk Module to allow employees to make reservation.](../images/kiosk-rsv-config-module-settings-.png)

    **Note:** Kiosk Module configuration enables employees to select a kiosk on their device and make workplace reservations. For more information, see [Make workplace reservations on the kiosk](rsv-space-kiosk-map.md).

    Fill in the field information.

<table id="table_qk1_x3s_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Available in

</td><td>

Select **Kiosk reservation**.**Note:** You can’t select any other Reservable Module options along with the Kiosk Module. If you select a different Reservable module along with Kiosk Module, application shows an error message "

```
A reservable module assigned to Kiosk can’t be shared with other experiences. Please update the Available-in accordingly
```

". Remove all options in **Available in** before adding the Kiosk Module. For example, remove **Advanced Reservation**, **Quick Reservation**, **Outlook Add-in**, and so on.

</td></tr><tr><td>

All day

</td><td>

All day options can be set to: -   Disabled: The All day option is disabled and isn’t displayed on the Reservation portal.
-   Default: The All day option is available and the current office time is selected by default. For example, if you’re making reservation at 11.30 am, based on your building time zone, the start time of the reservation is selected as 11.30 am. Employees change the timings, if necessary.
-   Enabled: The All day option is available and employees can reserve a space for a day.

This configuration is dependent on the \(sn\_wsd\_rsv.day\_start\) and \(sn\_wsd\_rsv.day\_end\) reservation property. For more information, see [Properties installed with Workplace Reservation Management](../../wsd-reservation-management/reference/properties-installed-with-wsd-reservation-mgmt.md).

-   Required: The All day option is displayed as selected and can’t be changed. The All day field is set as required. Based on the building time zone, regular office hours as set by your administrator is shown. For example, 9 am to 5 pm. For more information, see [Properties installed with Workplace Reservation Management](../../wsd-reservation-management/reference/properties-installed-with-wsd-reservation-mgmt.md).


</td></tr><tr><td>

All day meaning

</td><td>

Set the **All day meaning** to **Full day** \(00 to 23.59\) or **Office hours** \(9 am to 5 pm\). Timings are shown based on the building time zone. Full day setting ensures that employees or workplace users must book a space with a Reservable Module for an entire day or full day. The "All day" option is enabled by default on the reservation portal and the time can no longer be edited by employees or workplace users.

</td></tr><tr><td>

Max days in Future

</td><td>

Option to specify the maximum number of the days in the future up to which the reservable module can be reserved. For example, if you set the max number of days in future to 90, employees can make future reservations on this module only up to 90 days in advance.If this option is enabled, users can’t select a date beyond the specified value in Max days in future while making a reservation. For more information, see [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).

</td></tr><tr><td>

Min duration

</td><td>

Option to specify the minimum reservation duration of the reservable module. When you try to make a reservation beyond the Min duration value, an error message is on the shown on the Kiosk map.

</td></tr><tr><td>

Max duration

</td><td>

Option to specify the maximum reservation duration of the reservable module.When you try to make a reservation beyond the Min duration value, an error message is on the shown on the Kiosk map.

</td></tr><tr><td>

Show as

</td><td>

Option to specify the status of the reservation shown on the employee's calendar when a reservation is synchronized. This field appears only if Workplace Calendar synchronization is installed. -   **Busy**: The reservation is displayed in the Employee's calendar with a Busy status. The employee's calendar is blocked during the reservation duration.
-   **Free**: The reservation is displayed in the Employee's calendar with a Free status. The employee's calendar won’t be blocked during the reservation duration.


</td></tr></tbody>
</table>5.  Select the **Reservation Widget Configuration** and select the **Require Subject** check box.

    If the **Require Subject** check box is selected, you’re required to provide the **Reservation subject** in the Reservation Summary page.

6.  After configuring the Kiosk Reservable Module, navigate to **Workspaces** &gt; **Workplace Central**.

7.  Select the Kiosk Indoor Mapping icon \(![Kiosk Indoor Mapping icon.](../../workplace-central/images/kiosk-indoor-mapping-icon.png)\) and configure the default map configuration for the Kiosk Reservable Module that you created \(see Step 4\).

    Kiosk default map configuration enables employees to select the Kiosk Reservable Module and assign spaces configured in the reservable module to it. Employees and guests can search for spaces and make reservations on the **Kiosk Map**. For more information, see [Configure map features for kiosk](../../workplace-central/task/config-map-features.md).

8.  After configuring the kiosk map, kiosk operators can bind or assign the kiosk to a device for employees and guests to make workplace reservations.

    For more information, see [Setup a kiosk on a physical device for reservations](kiosk-setup-rsv-space.md).

    For more information, see [Make workplace reservations on the kiosk](rsv-space-kiosk-map.md).


**Parent Topic:**[Configure Workplace Services Kiosk](../concept/configure-workplace-services-kiosk.md)

