---
title: Configure a reservable module to group spaces in an area
description: Create a reservable module to group spaces in an area. Enable employees to reserve a space in an area.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure a reservable module, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a reservable module to group spaces in an area

Create a reservable module to group spaces in an area. Enable employees to reserve a space in an area.

## Before you begin

-   Ensure that you have the following details.
    -   Workplace data for your organization
    -   Data of workspaces that can be marked as available
-   Create the records in the following order.
    1.  Regions
    2.  Sites
    3.  Campuses
    4.  Buildings
    5.  Floors
    6.  Areas
    7.  Spaces

Role required: sn\_wsd\_rsv.admin

## About this task

An employee can view all the spaces of an area in a single module.

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module**.

2.  Click **New**.

3.  On the Reservable Module form, fill in the fields.

<table id="table_z5t_jbm_tyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the Reservable module. For example, as the module is to display all the spaces of an area, the name should be categorical like 'Desks within an area'.

</td></tr><tr><td>

Title

</td><td>

Title for the Reservable module.

</td></tr><tr><td>

Active

</td><td>

Option to make the module available for reservation.

</td></tr><tr><td>

Active from

</td><td>

Date from when the reservable module must be active and available for reservation.

</td></tr><tr><td colspan="2">

**Reservable Table Configuration**

</td></tr><tr><td>

Selection type

</td><td>

Selection type dictates what would be displayed on the search result. From the drop-list select **Container**.

**Note:** Specific unit indicates that the search result will show individual reservable unit to be reserved.

</td></tr><tr><td>

Reservable type

</td><td>

Type of the reservable item. Select **Location**.

</td></tr><tr><td>

Reservable table

</td><td>

Table that contains the reservable workplace items.Select the Space \[sn\_wsd\_core\_space\] table.

**Note:** If you selected Location for the Reservable type field, then use only the Space \[sn\_wsd\_core\_space\] table and its extended tables.

</td></tr><tr><td>

Reservable quantity field

</td><td>

Select Reservable quantity.

</td></tr><tr><td>

Reservable filter

</td><td>

Filter conditions on the reservable items in the Reservable table. The application displays the reservable items based on the given conditions.-   To add a condition, select **Add Filter Condition**.
-   To add an OR condition, select **Add OR Clause**.
**Note:** If you are adding a filter on a location, ensure that the **Active** and **Is reservable** fields are set to **True**. If these conditions are not set, the application displays even the inactive items that are not reservable as available for Rservation.

</td></tr><tr><td colspan="2">

Container selection, reservable quantity settings

</td></tr><tr><td>

Reservable container field

</td><td>

Level of the container. This field is automatically set to **Area**.

</td></tr><tr><td colspan="2">

Reservable Module Configuration

</td></tr><tr><td>

Short description

</td><td>

Short description about the module.

</td></tr><tr><td>

Description

</td><td>

Detailed description about the module and the reservable items.

</td></tr><tr><td>

Override check-in policy

</td><td>

Option to specify how to implement the reservation check-in policy.-   **No override**: The check-in policy is implemented as set in the **Requires check-in** field of a workplace space or room.
-   **Always require check-in**: The check-in policy is required irrespective of what is set in the **Requires check-in** field of a workplace space or room.
-   **Never require check-in**: The check-in policy is removed irrespective of what is set in the **Requires check-in** field of a workplace space or room.


</td></tr><tr><td>

Requires Approval

</td><td>

Option to make approval required before making a reservation.

</td></tr><tr><td>

Requires subject

</td><td>

Option to make a reservation subject required before making a reservation.

</td></tr><tr><td>

Require cancel notes

</td><td>

Option to make a cancellation note required before making a cancellation.

</td></tr><tr><td>

Apply to shift

</td><td>

Option to enable shift-based reservation on the module.

</td></tr><tr><td>

Max days in future

</td><td>

The maximum number of the days in the future up to when an employee can make a reservation. For example, if you set the number of days to 10, employees can make future reservation on this module only up to 10 days in advance.

</td></tr><tr><td>

Min duration

</td><td>

Minimum reservation duration of the reservable module.

</td></tr><tr><td>

Max duration

</td><td>

Maximum reservation duration of the reservable module.

</td></tr><tr><td>

Allow whole day reservation

</td><td>

Option to enable employees to reserve a workplace item of the module for an entire day.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The reservable module is added to the application. On the Reservation portal, employees can view the spaces of an area in this module.

**Parent Topic:**[Configure a reservable module](config-reservable-module.md)

