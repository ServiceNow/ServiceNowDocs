---
title: Add a floor using Workplace Space Management
description: Create a record for every floor of a building. Specify the measurement details of the floor such as the total size and the usable size.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-22"
reading_time_minutes: 5
---

# Add a floor using Workplace Space Management

Create a record for every floor of a building. Specify the measurement details of the floor such as the total size and the usable size.

## Before you begin

Ensure that the building of the floor record is active.

Role required: sn\_wsd\_core.admin

## About this task

You can assign a an allocation to all the entities of the floor by using the push down functionality. Specify the gross and usable size of the floor to plan maintenance activities, infrastructure, workspace allocation, and more.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select **Floors**.

3.  Click **New**.

4.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

        The form view changes.

5.  On the form, fill in the fields.

<table id="table_lyg_hbt_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the floor. Ensure that you enter a unique name. For example, use the location name `<location-name>-16` rather than just `16`.

**Note:** Do not use duplicate names as it may affect the reservation process. If you change the name of a building after updating it, a message is displayed to show that the **Name** will be overwritten in the next synchronization process. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr><tr><td>

Region

</td><td>

Region where the office is located. If your organization is located at several regions, select that region where the office that you are adding is located.

</td></tr><tr><td>

Site

</td><td>

Location of the office campus. If there are several sites in a region, select that site where the office that you are adding is located.

</td></tr><tr><td>

Campus

</td><td>

Name of the campus where the office operates. If there are several campuses in a site, select that campus where the office that you are adding is located.

</td></tr><tr><td>

Building

</td><td>

Building where the floor is located.

</td></tr><tr id="active"><td>

Active

</td><td>

Option to activate the location. This field depends on the **Status** field. If the **Status** is set as **Future** or **Retired**, then the **Active** field is turned off.

</td></tr><tr><td>

Is reservable

</td><td>

Option to indicate whether the areas, rooms, and spaces that are located on this floor are available for reservation.

</td></tr><tr><td>

Order

</td><td>

When a sort Order is configured, the floor names are sorted accordingly. If the sorting Order value is not specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The floor names are alphabetically sorted based on the label name.

</td></tr><tr id="status"><td>

Status

</td><td>

Status of the location.-   If the status of the location is active, select **Active**. If you set the status to **Active**, the **Active** field is enabled.
-   if the location will be available only in the future, select **Future**. If you set the status to **Future**, the **Active** field is turned off.
-   If the location is no longer functional for usage select **Retired**. If you set the status as **Retired**, the **Active** field is turned off.
-   To make the location available only for a temporary duration, select **Temporary**. This space is available when assigned to a user or for any workplace-related activities. The **Active** field is always enabled.


</td></tr><tr id="pln-stdate"><td>

Planned start date

</td><td>

Date for when you are planning to activate or reactivate the location. If the status is set to **Temporary**, then this date is when the location is reactivated.

</td></tr><tr id="pln-enddate"><td>

Planned end date

</td><td>

Date by when you are planning to end the **Future** or **Retired** status of the location.

</td></tr><tr id="act-stdate"><td>

Actual start date

</td><td>

The date starting when the location should be active.

</td></tr><tr id="act-enddate"><td>

Actual end date

</td><td>

The date by when the location must be retired.

</td></tr><tr><td>

Push down

</td><td>

Definition of the push down functionality if the floor is associated to any allocation. The allocation is assigned to the child locations of the floor, such as rooms, areas, and spaces, based on the selected push down action. The following choices are available:-   **No, keep floor and space/area info separate**: The cost center or department is not assigned to the areas, rooms, and spaces of the floor.
-   **Yes, and replace existing allocations**: The cost center or department is assigned to all the areas, rooms, and spaces of the floor. If an area, room, or space already has an allocation, then it is replaced.
-   **Yes, but keep existing allocations**: The cost center or department is assigned to all the areas, rooms, and spaces of the floor. If an area, room, or space already has an allocation, then it is not replaced.
**Note:** The push down functionality also depends on if the **Push down** functionality is enabled on the child locations.

</td></tr><tr id="push-down-state"><td>

Push down state

</td><td>

State of the push down functionality. The statuses are as follows:-   **In progress**: The push down process is still running.
-   **Completed**: The push down process is complete.


</td></tr><tr id="managed-by-group"><td>

Managed by group

</td><td>

Group that manages the workplace-related operations.

</td></tr><tr id="managed-by"><td>

Managed by

</td><td>

Workplace manager who manages all the workplace-related operations.

</td></tr><tr><td class="sub-head" colspan="2">

**Measurement Details**

</td></tr><tr><td>

Total size

</td><td>

Total size of the floor that is calculated based on the **Size** specified for each space or room on the floor. Depending on the selected unit, the **Total size** field name changes. For example, if you select **Square feet** as the unit, then the fields is displayed as **Total square feet**.

 The size is calculated regardless of the usability that is specified in the Space type configuration for child rooms and spaces.

 This field is automatically set based on the size specified in its child locations.

</td></tr><tr><td>

Usable size

</td><td>

Usable size on the floor.Depending on the selected unit, the **Usable size** field name changes. For example, if you select **Square feet** as the unit, then the field is displayed as **Usable square feet**.

 This is the amount of space that is available for planning maintenance activities, infrastructure, and so on. The usable size is calculated based on the Space type configuration for child rooms and spaces. If the **Space type** of a space is configured as **Usable**, then the size of the space is included in the calculation.

</td></tr></tbody>
</table>6.  The **Time zone** of a location is required to synchronize Indoor Mapping and Workplace Service Delivery.

    Workplace reservation is created in a location's timezone.

    For more information, see Indoor Mapping place types with Workplace Service Delivery space types, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

7.  Select **Unlink Floor** to unlink a floor from Indoor Mapping map provider.

    For more information about how to link and synchronize Indoor Mapping map data objects with Workplace Indoor Mapping see, [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

8.  Select **Block location** to define a time period to block these locations for reservation.

9.  To add an indoor map, select the Additional Actions icon \(![Additional Actions to switch to the Workplace view.](../images/additionalactions-icon.png)\) to select **View** &gt; **Workplace Indoor Mapping Floor**.

    1.  In the **Indoor map floor** field, search for a floor and add it.

10. Click **Submit**.


## Result

The floor is added to the building.

