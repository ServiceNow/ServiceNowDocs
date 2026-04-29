---
title: Add a space using Workplace Space Management
description: Create a space record for every workspace located on a floor. Specify the space type and the size of the space.
locale: en-US
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Add a space using Workplace Space Management

Create a space record for every workspace located on a floor. Specify the space type and the size of the space.

## Before you begin

Ensure that the room, area, and floor of the space are active.

Role required: sn\_wsd\_core.admin and sn\_wsd\_spcmgmt.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select **Spaces**.

3.  Click **New**.

4.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

        The form view changes.

5.  On the form, fill in the fields.

<table id="table_agj_xld_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the space.Ensure that you enter a unique name. For example, use the location name `<location-name>-16` rather than just `16`.

**Note:** Do not use duplicate names as it may affect the reservation process. If you change the name of a building after updating it, a message is displayed to show that the **Name** will be overwritten in the next synchronization process. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr><tr><td>

Title

</td><td>

Title of the space.

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

Name of the office building for this workspace. If there are several buildings in a region, select that building where the office that you are adding is located.

</td></tr><tr><td>

Floor

</td><td>

Name or number of the floor where this workspace is present.

</td></tr><tr><td>

Area

</td><td>

Name of the area on the office floor.

</td></tr><tr><td>

Active

</td><td>

Option to activate the location. This field depends on the **Status** field. If the **Status** is set as **Future** or **Retired**, then the **Active** field is turned off.

</td></tr><tr><td>

Is reservable

</td><td>

Option to indicate whether the space is available for reservation.

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

Space type

</td><td>

Type of the office space. To configure a new space type, see [Add a space type configuration](../../workplace-service-delivery/task/add-space-type-configuration-wsd.md).

</td></tr><tr><td>

Space function

</td><td>

The field value is derived from the space type configuration of the space.

</td></tr><tr><td>

BOMA type

</td><td>

BOMA type that you want to associate this space with. If the Space type that you selected is already mapped with a BOMA type, the field is auto-filled with the mapped BOMA type.For more information about BOMA types and to configure a BOMA type, refer to [Configure a BOMA type](configure-a-boma-type.md).

</td></tr><tr><td>

BOMA type overridden

</td><td>

Option to specify the override behaviour when the space type and BOMA type mapping is changed.

</td></tr><tr><td>

Assignment type

</td><td>

Assignment type of the space. Specify if the space is a flexible or a permanent workspace. This field appears only when you select the **Space type** as **Workspace/Desk**.

</td></tr><tr id="managed-by-group"><td>

Managed by group

</td><td>

Group that manages the workplace-related operations.

</td></tr><tr id="managed-by"><td>

Managed by

</td><td>

Workplace manager who manages all the workplace-related operations.

</td></tr><tr><td>

Capacity

</td><td>

Capacity of the location. By default, the value is set to 1.

</td></tr><tr><td>

Capacity ratio

</td><td>

Capacity ratio of the location. By default, the value is set to 1. The field signifies the number people the location can accommodate, for example, 1.5,2 etc.

</td></tr><tr><td>

Total capacity

</td><td>

The field is automatically filled and is read-only. The total capacity is calculated as: Total capacity = Capacity \* Capacity ratio.

</td></tr><tr><td>

Occupancy status

</td><td>

The occupancy status of the space.

</td></tr><tr><td>

**Measurement Details**

</td><td>

 

</td></tr><tr id="measuring-unit-field"><td>

Unit

</td><td>

Measuring unit of the size.

</td></tr><tr><td>

Size

</td><td>

Size of the space.

</td></tr><tr><td>

Size Square Feet

</td><td>

Surface area computed in square feet or square meters.Ability to compute surface area automatically in square meters or square feet from the CAD polylines if polylines are defined as closed shapes or if a unit is set. For more information, see [Compute CAD file properties to extract space or room surface area](../../wsd-indoor-mapping/task/compute-cad-properties.md).

</td></tr></tbody>
</table>6.  Select **Create QR code** to generate and print QR codes for this space.

7.  Select **Unlink Space** to unlink a space from Indoor Mapping map provider.

    For more information about how to link and synchronize Indoor Mapping map data objects with Workplace Indoor Mapping see, [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

8.  Select **Block location** to define a time period to block these locations for reservation.

9.  To add an image to a space, select the Additional Actions icon \(![Additional Actions to switch to the Workplace view.](../images/additionalactions-icon.png)\) to select **View** &gt; **Workplace**.

    1.  Select the **Extra Information** tab.

    2.  Select an **Image** that you want to add to a space and upload it.

        The image that you have added is shown on the reservation summary page for a selected space.

10. Click **Submit**.


## Result

The space is added to the area. The size of the area and the floor are calculated based on the specified space size.

## What to do next

Add an allocation, that is, associate the space to a cost center, department and workplace entity. For more information on how to add an allocation, see [Allocate a cost center, department, or workplace entity](add-cost-center-department-floor.md). In the procedure, select the Spaces module instead of the Floors module.

-   **[Configure a space type as usable with Workplace Space Management](assign-a-space-as-usable.md)**  
Specify if a space type is usable or not by using the Space type configuration functionality. Specify if the space can or cannot be used for reservations.

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building-1.md)

[Add a floor using Workplace Space Management](add-a-floor-1.md)

[Add an area using Workplace Space Management](add-an-area.md)

[Add a room using Workplace Space Management](add-a-room.md)

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

