---
title: Add an area using Workplace Space Management
description: Create a record for every area that is located on a floor.
locale: en-US
release: zurich
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Add an area using Workplace Space Management

Create a record for every area that is located on a floor.

## Before you begin

Ensure that the floor of the area record is active.

Role required: sn\_wsd\_core.admin and sn\_wsd\_spcmgmt.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select **Areas**.

3.  Click **New**.

4.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

        The form view changes.

5.  On the form, fill in the fields.

<table id="table_usn_2px_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the area. Ensure that you enter a unique name. For example, use the location name `<location-name>-16` rather than just `16`.

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

Name of the building where the area is located.

</td></tr><tr><td>

Floor

</td><td>

Floor name or the number of the floor where this area is located.

</td></tr><tr><td>

Order

</td><td>

When a sort **Order** is configured for an area, the area names are sorted accordingly. If the sorting **Order** value is not specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The area names are alphabetically sorted based on the label name.

</td></tr><tr><td>

Active

</td><td>

Option to activate the location. This field depends on the **Status** field. If the **Status** is set as **Future** or **Retired**, then the **Active** field is turned off.

</td></tr><tr><td>

Is reservable

</td><td>

Option to indicate whether the area, rooms, and spaces that are located in this area are available for reservation.

</td></tr><tr><td>

Status

</td><td>

Status of the location.-   If the status of the location is active, select **Active**. If you set the status to **Active**, the **Active** field is enabled.
-   if the location will be available only in the future, select **Future**. If you set the status to **Future**, the **Active** field is turned off.
-   If the location is no longer functional for usage select **Retired**. If you set the status as **Retired**, the **Active** field is turned off.
-   To make the location available only for a temporary duration, select **Temporary**. This space is available when assigned to a user or for any workplace-related activities. The **Active** field is always enabled.


</td></tr><tr><td>

Planned start date

</td><td>

Date for when you are planning to activate or reactivate the location. If the status is set to **Temporary**, then this date is when the location is reactivated.

</td></tr><tr><td>

Planned end date

</td><td>

Date by when you are planning to end the **Future** or **Retired** status of the location.

</td></tr><tr><td>

Actual start date

</td><td>

The date starting when the location should be active.

</td></tr><tr><td>

Actual end date

</td><td>

The date by when the location must be retired.

</td></tr><tr><td>

Capacity

</td><td>

Capacity of the area.

</td></tr><tr><td>

Push down

</td><td>

Option to define the push down functionality if the area is associated to any allocation. The allocation is assigned to the child locations of the area, such as rooms and spaces, based on the selected push down action. Choices are as follows:-   **No, keep floor and space/area info separate**: The cost center or department is not assigned to the areas, rooms, and spaces of the floor.
-   **Yes, and replace existing allocations**: The cost center or department is assigned to all the areas, rooms, and spaces of the floor. If an area, room, or space already has an allocation, then it is replaced.
-   **Yes, but keep existing allocations**: The cost center or department is assigned to all the areas, rooms, and spaces of the floor. If an area, room, or space already has an allocation, then it is not replaced.
**Note:** The push down functionality also depends on the **Push down** option enabled in the room and space of the area.

</td></tr><tr><td>

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

</td></tr><tr><td>

**Measurement Details**

</td><td>

 

</td></tr><tr><td>

Unit

</td><td>

Measuring unit of the size. Depending on the selected unit, the **Total size** and **Usable size** field name changes. For example, if you select **Square feet** as the unit, then the fields are displayed as **Total square feet** and **Usable square feet**. For more information, see [Compute CAD file properties to extract space or room surface area](../../wsd-indoor-mapping/task/compute-cad-properties.md).

</td></tr><tr id="gross-size"><td>

Total size

</td><td>

Total size of the area that is calculated based on the **Size** specified for each room, or space in the area.Depending on the selected unit, the **Total size** field name changes. For example, if you select **Square feet** as the unit, then the fields is displayed as **Total square feet**.

 The size is calculated regardless of the usability that is specified in the Space type configuration for child rooms and spaces.

 This field is automatically set based on the size specified in its child locations.

</td></tr><tr id="usable-size"><td>

Usable size

</td><td>

Usable size in the area. Depending on the selected unit, the **Usable size** field name changes. For example, if you select **Square feet** as the unit, then the field is displayed as **Usable square feet**.

 This is the amount of space that is available for planning maintenance activities, infrastructure, and so on. The usable size is calculated based on the Space type configuration for child rooms and spaces. If the **Space type** of a space is configured as **Usable**, then the size of the space is included in the calculation.

This field is automatically set based on the size specified in its child locations.

</td></tr><tr><td>

Size Square Feet/Meters

</td><td>

Surface area computed in square feet or square meters.Ability to compute surface area automatically in square meters or square feet from the CAD polylines if polylines are defined as closed shapes or if a unit is set. For more information, see [Compute CAD file properties to extract space or room surface area](../../wsd-indoor-mapping/task/compute-cad-properties.md).

</td></tr></tbody>
</table>6.  Select **Block location** to define a time period to block these locations for reservation.

7.  To add an image, select the Additional Actions icon \(![Additional Actions to switch to the Workplace view.](../images/additionalactions-icon.png)\) to select **View** &gt; **Workplace**.

    1.  Select an **Image** that you want to add and upload it.

8.  Click **Submit**.


## Result

The area is added to the floor.

## What to do next

You can add an allocation if there is none. For more information on how to add an allocation, see [Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md). In the procedure, select the Areas module instead of the Floors module.

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building.md)

[Add a floor using Workplace Space Management](add-a-floor.md)

[Add a room using Workplace Space Management](add-a-room.md)

[Add a space using Workplace Space Management](add-a-space.md)

[Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md)

[Configure a workspace or desk as flexible or permanent](assign-a-flex-perm-space.md)

[Update the measurement details of a workplace location](update-measurement-details-of-workplace-location.md)

[Change the status of a workplace location](change-active-status-of-workplace-location.md)

[Configure a BOMA type](configure-a-boma-type.md)

[Map a space type with BOMA type](map-a-space-type-with-boma-type.md)

[Create a Space Recommender rule](create-a-space-recommender-rule.md)

[Raise a space assistance request](raise-a-space-recommendation-request.md)

[Create a view-by configuration](create-view-by-config.md)

[Reviewing allocation changes](../concept/reviewing-allocation-changes.md)

