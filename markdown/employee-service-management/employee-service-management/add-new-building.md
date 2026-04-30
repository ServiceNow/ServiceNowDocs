---
title: Add a building using Workplace Space Management
description: Create a record for every building that is part of your organization. Specify to which region, site, and time zone does the building belong to.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Add a building using Workplace Space Management

Create a record for every building that is part of your organization. Specify to which region, site, and time zone does the building belong to.

## Before you begin

Ensure that the region, site, and the campus of the building are active.

Role required: sn\_wsd\_core.admin and sn\_wsd\_spcmgmt.manager

## About this task

Add details of your building. If your organization has several offices located all over the world, then add the details such as, in which region, site of the region, and campus in the site, the building that you are adding is located.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select **Buildings**.

3.  Click **New**.

4.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

        The form view changes.

5.  On the form, fill in the fields.

<table id="table_odt_q5s_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the building. Ensure that you enter a unique name. For example, use the location name `<location-name>-16` rather than just `16`.

**Note:** Do not use duplicate names as it may affect the reservation process. If you change the name of a building after updating it, a message is displayed to show that the **Name** will be overwritten in the next synchronization process. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr><tr><td>

Region

</td><td>

Select the region where the building is located.

</td></tr><tr><td>

Site

</td><td>

Select the site in the region where the building is located.

</td></tr><tr><td>

Campus

</td><td>

Select the campus of the site where the building is located.

</td></tr><tr><td>

Managed by group

</td><td>

Group that manages the entire workplace-related operations.

</td></tr><tr><td>

Managed by

</td><td>

Workplace manager who manages all the workplace-related operations.

</td></tr><tr><td>

Active

</td><td>

Option to activate the location. This field depends on the **Status** field. If the **Status** is set as **Future** or **Retired**, then the **Active** field is turned off.

</td></tr><tr><td>

Is reservable

</td><td>

Option to indicate that the spaces for this building are available for reservation.For example, if you do not mark a Building as reservable, then none the floors, areas, and spaces of this building would be available for reservation.

</td></tr><tr><td>

Order

</td><td>

When a sort**Order** is configured, the building names are sorted accordingly. If the sorting order is not specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The building names are alphabetically sorted based on the label name.

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

Time zone

</td><td>

Time zone of the building.

</td></tr><tr><td>

Latitude

</td><td>

Latitude of a campus or a building. The latitude is displayed in the Workplace Service Portal Location directory map.

</td></tr><tr><td>

Longitude

</td><td>

Longitude of a campus or a building. The longitude is displayed in the Workplace Service Portal Location directory map.

</td></tr><tr><td colspan="2">

**Measurement Details**

</td></tr><tr id="measuring-unit-field"><td>

Unit

</td><td>

Measuring unit of the size. Depending on the selected unit, the **Total size** and **Usable size** field name changes. For example, if you select **Square feet** as the unit, then the fields are displayed as **Total square feet** and **Usable square feet**. For more information, see [Compute CAD file properties to extract space or room surface area](../../wsd-indoor-mapping/task/compute-cad-properties.md).

</td></tr><tr id="gross-size"><td>

Total size

</td><td>

Total size of the building that is calculated based on the **Size** specified for each room or space on the floor. Depending on the selected unit, the **Total size** field name changes. For example, if you select **Square feet** as the unit, then the fields is displayed as **Total square feet**.

 The size is calculated regardless of the usability that is specified in the Space type configuration for child rooms and spaces.

 This field is automatically set based on the size specified in its child locations.

</td></tr><tr id="usable-size"><td>

Usable size

</td><td>

Usable size in the building. Depending on the selected unit, the **Usable size** field name changes. For example, if you select **Square feet** as the unit, then the field is displayed as **Usable square feet**.

 This is the amount of space that is available for planning maintenance activities, infrastructure, and so on. The usable size is calculated based on the Space type configuration for child rooms and spaces. If the **Space type** of a space is configured as **Usable**, then the size of the space is included in the calculation.

 This field is automatically set based on the size specified in its child locations.

</td></tr><tr><td>

Enable employee location privacy and preference

</td><td>

Option to set location privacy preference for the building. Note the following:-   Set this option only if you want to have a different location privacy setup for the building.
-   By default, the location privacy preference that is set in the Workplace Reservation Management system property **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY** is considered.
-   The field is set to **None** by default.
-   You can specify if you want to set privacy on workplace profiles, or reservations, or on both.
-   You can also select **No privacy** if you don't want any privacy for the building.
-   If the field is set as **None**, then, the privacy preferences set in the Workplace Reservation Management system property **sn\_wsd\_core.ENABLE\_LOCATION\_PRIVACY** is considered.
 For more information about each field, refer to [Location privacy settings and impact](../../wsd-reservation-management/reference/location-privacy-settings-and-impact.md)

</td></tr><tr><td>

Allow employees to override location privacy on reservations

</td><td>

Enables you to let employees override the location privacy while reserving spaces that belong to this building. The field is set to **None** by default. For more information, refer to [Location privacy settings and impact](../../wsd-reservation-management/reference/location-privacy-settings-and-impact.md).

</td></tr></tbody>
</table>6.  Select **Unlink Building** to unlink a building from Indoor Mapping map provider.

    For more information about how to link and synchronize Indoor Mapping map data objects with Workplace Indoor Mapping see, [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

7.  Select **Block location** to define a time period to block these locations for reservation.

8.  To add an indoor map building, select the Additional Actions icon \(![Additional Actions to switch to the Workplace view.](../images/additionalactions-icon.png)\) to select **View** &gt; **Workplace Indoor Mapping Building**.

    1.  In the **Indoor map Building** field, search for a building and add it.

9.  Click **Submit**.


## Result

The building is added to the selected region, site, and campus.

