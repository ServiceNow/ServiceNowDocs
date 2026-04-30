---
title: Add a campus
description: A Workplace Service Delivery campus contains buildings, floors, areas, or spaces.
locale: en-US
release: xanadu
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2025-07-22"
reading_time_minutes: 5
breadcrumb: [Managing workplace locations, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Add a campus

A Workplace Service Delivery campus contains buildings, floors, areas, or spaces.

## Before you begin

Role required: sn\_wsd\_core.admin and sn\_wsd\_spcmgmt.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration** &gt; **Campuses**.

2.  Continue with one of the following options.

    |Option|Action|
    |------|------|
    |To add a campus manually|Click **New**.|
    |To edit or update a campus|Click open the campus that you want to edit.|

3.  Click **New** to create a new campus.

    Fill in the form field information.

<table id="table_q5r_dlb_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the campus. Ensure that you enter a unique name. **Note:** Do not use duplicate names because it may affect the reservation process. If you change the name of campus after updating it, a message is displayed to show that the **Name** will be overwritten in the next synchronization process. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr><tr><td>

Title

</td><td>

Title of campus as it appears on the map.

</td></tr><tr><td>

Region

</td><td>

Region where the campus is situated. Click![search icon](../../workplace-case-mgmt/image/search-icon.png) to search for a region.

</td></tr><tr><td>

Site

</td><td>

Campus site name. Click the search icon \(![search icon](../../workplace-case-mgmt/image/search-icon.png)\) to search for a site.

</td></tr><tr><td>

Managed by

</td><td>

User assigned to manage the campus.

</td></tr><tr><td>

Managed by group

</td><td>

Group assigned to manage the campus.**Note:** If a Workplace Service Delivery campus is synchronized with Indoor Mapping campus and if new Indoor mapping objects are added, workplace user groups are notified to synchronize the latest changes in Indoor Mapping with Workplace Service Delivery.

For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr><tr><td>

Latitude

</td><td>

Latitude coordinates of a campus location.

</td></tr><tr><td>

Longitude

</td><td>

Longitude coordinates of a campus location.

</td></tr><tr><td>

Active

</td><td>

Option to show that the campus is in active state.

</td></tr><tr><td>

Street

</td><td>

Street where the campus is located.

</td></tr><tr><td>

City

</td><td>

Address of the campus.

</td></tr><tr><td>

Zip/Postal Code

</td><td>

Zip or Postal code of the campus location.

</td></tr><tr><td>

Order

</td><td>

When a sort Order is configured for a campus, the floor names are sorted accordingly. If the sorting Order value is not specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The campus names are alphabetically sorted based on the label name.

</td></tr><tr><td>

Indoor map campus

</td><td>

Search and select the Indoor Mapping campus that you want to integrate with Workplace Core campus. The name of the Indoor Mapping campus should be same as your Workplace Core campus. Your default map provider should be Indoor Mapping.

</td></tr></tbody>
</table>4.  If you are integrating your campus with Indoor Mapping, perform the following steps:

    1.  From the Related list, select **Buildings** and set the **Is reservable** column to true for a building.

    2.  Repeat Step a for floor or floors in a building.

    3.  Repeat Step a for Space types.

5.  The place type mappings for Workplace Core space types and Indoor Mapping place types is available in the Place types mapping table \(**All** &gt; **Indoor Mapping** &gt; **Place types** &gt; **Space mapping** &gt; **Indoor Mapping administration** &gt; **Place Type mapping**\).

    If you have multiple domains in your instance, then you might have to recreate the place type mapping records in the same domain as your location records. Place types and Space types must belong to the same domain.

6.  Click **Synchronize** to synchronize floors, areas, and spaces in a campus.

    **Note:** **Time zone** of Workplace Service Delivery campus location is required to synchronize. Workplace reservation is created in a location timezone. For more information, see Indoor Mapping place types with Workplace Service Delivery space types, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

7.  To add an Indoor map campus, select the Additional Actions icon \(![Additional Actions to switch to the Workplace view.](../images/additionalactions-icon.png)\) to select **View** &gt; **Workplace Indoor Mapping Campus**.

    1.  In the **Indoor map Campus** field, search for a campus and add it.

8.  Click **Update** to edit a campus.

9.  Building, floors, areas, and spaces available in a campus are listed.


**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a building using Workplace Space Management](add-new-building-1.md)

[Add a floor using Workplace Space Management](add-a-floor-1.md)

[Add an area using Workplace Space Management](add-an-area.md)

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

