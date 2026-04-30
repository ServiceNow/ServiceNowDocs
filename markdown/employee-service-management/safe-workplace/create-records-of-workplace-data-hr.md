---
title: Create records for your workplace data
description: Create individual records of your workspaces, floors, office buildings, and workplace locations within the Workplace Core application. Either insert new data or add records to the existing workplace data.
locale: en-US
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Providing your workplace data, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create records for your workplace data

Create individual records of your workspaces, floors, office buildings, and workplace locations within the Workplace Core application. Either insert new data or add records to the existing workplace data.

## Before you begin

Ensure that you have the following details:

-   Workplace data for your organization.
-   Data of workspaces that can be marked as available.

**Important:** In the Workplace Service Delivery Suite, from Workplace Core version 2.5.3, the **Space type \(space\_type\)** choice field is depreciated. After the upgrade, Space types are configured in the **Space Type Configuration**. The **Space type \(space\_type\)** field is migrated as **Space type \(location\_type\)** field in the Space table \[sn\_wsd\_core\_space\]. Customers having customization on the depreciated **Space type \(space\_type\)** field are advised to manually migrate their flow to use the new **Space type \(location\_type\)** field. A new fix script, **Populate Location Type from Space Type**, is introduced to execute the schedule job, **Populate location\_type from space\_type**, on the Space table \[sn\_wsd\_core\_space\] to migrate the depreciated **Space type \(space\_type\)** field value to the new **Space type \(location\_type\)** field.

Role required: sn\_wsd\_core.admin

## About this task

If you have a small number of workspaces, you can enter information individually for each workspace down to the Spaces level.

If you have many work sites, you might want to do the following:

1.  Create a skeleton of repeated global information.
2.  Add the individual spaces information in a spreadsheet.
3.  Import the spreadsheet into the application.

    For more information on importing, see [Configuring spreadsheets to import workplace data](../../workplace-service-delivery/concept/importing-workspace-data-wsd.md#).


If you have floor plans, you can create records of data until the Buildings level. Uploading the floor plans loads the data of floors and of the spaces associated with these floors.

## Procedure

1.  Navigate to **All** &gt; **Workplace Safety Management** &gt; **Space Administration**.

2.  Select the applicable module.

    Create the records in the following order:

    -   Regions
    -   Sites
    -   Campuses
    -   Buildings
    -   Floors
    -   Areas
    -   Spaces
    For example, if you want to locations of your offices, select **Sites**.

3.  On the form, fill in the fields.

    **Note:**

    -   The visibility of some of the following fields depends on the module that you selected.
    -   You can leave a field that does not apply to your organization empty.
    The fields on the form differ based on what module you selected. For example, the following form is for Building.

<table id="table_wgn_vnt_plb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="name"><td>

Name

</td><td>

Name of the workplace. Ensure that you enter a unique name. For example, if the **Building** field is set to **1C**, and if the **Space** field is set to **WST 1C 1601**, then an appropriate value for the **Name** field can be `1C-16` **Note:** Do not use workplace locations with the same name because it affects the reservation process.

</td></tr><tr id="region"><td>

Region

</td><td>

Region where the office is located. If your organization is located at several regions, select that region where the office that you are adding is located.

</td></tr><tr id="site"><td>

Site

</td><td>

Location of the office campus. If there are several sites in a region, select that site where the office that you are adding is located.

</td></tr><tr id="campus"><td>

Campus

</td><td>

Name of the campus where the office operates. If there are several campuses in a site, select that campus where the office that you are adding is located.

</td></tr><tr id="building"><td>

Building

</td><td>

Name of the office building for this workspace. If there are several buildings in a region, select that building where the office that you are adding is located.

</td></tr><tr id="floor"><td>

Floor

</td><td>

Name or number of the floor where this workspace is present.

</td></tr><tr id="area"><td>

Area

</td><td>

Name of the area on the office floor.

</td></tr><tr id="space-type"><td>

Space type

</td><td>

Type of the office space. To configure a new space type, see [Add a space type configuration](../../workplace-service-delivery/task/add-space-type-configuration-wsd.md).

</td></tr><tr id="active"><td>

Active

</td><td>

Option to indicate that this space is active.

</td></tr><tr id="is-reservable"><td>

Is reservable

</td><td>

Option to indicate that the spaces for this workplace entity are available for reservation.For example, if you do not mark a Building as reservable, then none the floors, areas, and spaces of this building would be available for reservation.

</td></tr><tr id="latitude"><td>

Latitude

</td><td>

Latitude of a campus or a building. The latitude is displayed in the Workplace Service Portal Location directory map.

</td></tr><tr id="longitude"><td>

Longitude

</td><td>

Longitude of a campus or a building. The longitude is displayed in the Workplace Service Portal Location directory map.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

-   If you have floor plans for your workplace, you can upload them to create and display floor and workspace data. For more information, see [Upload a workplace floor plan](upload-workplace-floor-map.md).
-   If you are using a spreadsheet to enter and import bulk data for workspaces, see [Configuring spreadsheets to import workplace data](../concept/importing-workspace-data.md#).
-   If you have added all of your workplace data, you can define employee shifts. For more information, see [Define shifts for your workplace](create-shifts.md).

**Parent Topic:**[Providing your workplace data](../concept/providing-your-workplace-data.md)

