---
title: Add or edit a building
description: Buildings are assigned to campuses with a unique name, and contain floors or levels, a location, and utilization thresholds.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customer-created maps, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Add or edit a building

Buildings are assigned to campuses with a unique name, and contain floors or levels, a location, and utilization thresholds.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Space Management** &gt; **Building**.

2.  Continue with one of the following options.

<table id="choicetable_b35_kc4_ht"><thead><tr><th align="left" id="d27465e102">

Option

</th><th align="left" id="d27465e105">

Action

</th></tr></thead><tbody><tr><td id="d27465e111">

**To add a building**

</td><td>

-   Click **New**.


</td></tr><tr><td id="d27465e129">

**To edit the details of the building**

</td><td>

-   Click the name of the building you want to edit.


</td></tr></tbody>
</table>3.  Fill in the fields on the form, as appropriate.

<table id="table_BuildingForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Provide a descriptive name for this building.

</td></tr><tr><td>

Campus

</td><td>

Select the campus where this building is located.

</td></tr><tr><td>

Floors

</td><td>

Enter the number of floors the building has.

</td></tr><tr><td>

Location

</td><td>

Select the location for this building. Define the locations in Organization Management. A good practice is to select a location that is defined at the address, not at the floor level. Floors are defined separately in Facilities Service Management.

</td></tr><tr><td>

Assignable area

</td><td>

Displays only the area of the building that is assignable to users.

</td></tr><tr><td>

Usable area

</td><td>

Enter only the area of the building that is available for the creation of spaces.

</td></tr><tr><td>

Gross area

</td><td>

Enter the total area of the building, including non-usable and non-assignable spaces.

</td></tr><tr><td>

Area unit

</td><td>

Select the unit used for defining the space size: square feet or square meters.

 **Note:** The **Area unit** assigned to all spaces must be consistent for the roll-up calculations to work properly. See [Space roll up calculations](../concept/c_SpaceRollupCalculations.md).

</td></tr><tr><td>

Current occupancy

</td><td>

Displays the number of users currently associated with the space. Calculation is generated using business rules on the Associated User \[m2m\_fm\_user\_to\_space\] table.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Max occupancy

</td><td>

Displays max occupancy of the building based on rollup calculations from the spaces below it.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Percent occupied

</td><td>

Displays the percentage of total space occupied based on rollup calculations from the spaces below it.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Utilization Min

</td><td>

Enter a number to define the minimum level of utilization for the building.

</td></tr><tr><td>

Utilization Max

</td><td>

Enter a number to define the maximum level of utilization for the building.

</td></tr></tbody>
</table>4.  Click **Save** and the **Related Links** section displays.

    -   Show Floor Plan: Click to display a floor plan of the selected floor.
    -   View Facilities Schedule: Click to create a facilities schedule blackout and prevent work from being performed in a defined area for a scheduled time period.
5.  Three tabs appear:

    -   Levels: List of levels for the building. Click **New** to create a level or on an existing level to edit.
    -   Assets: List of assets associated with the building. Click **New** to create an asset or on an existing asset to edit.
    -   Expense Lines: List of expense lines for the building. Click **New** to create an expense line or on an existing expense line to edit.
6.  Continue with one of the following options.

<table id="choicetable_pbs_zp4_ht"><thead><tr><th align="left" id="d27465e400">

Option

</th><th align="left" id="d27465e403">

Action

</th></tr></thead><tbody><tr><td id="d27465e409">

**To add the building**

</td><td>

-   Click **Submit**.


</td></tr><tr><td id="d27465e427">

**To update the building details**

</td><td>

-   Click **Update**.


</td></tr></tbody>
</table>
**Parent Topic:**[Customer-created maps](../reference/r_Manually-builtMaps.md)

