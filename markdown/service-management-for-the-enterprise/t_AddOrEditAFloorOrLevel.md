---
title: Add or edit a floor or level
description: A floor is a level in a structure that contains spaces. It can be a floor of a building, the basement, levels in a parking lot, or outdoor areas.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer-created maps, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Add or edit a floor or level

A floor is a level in a structure that contains spaces. It can be a floor of a building, the basement, levels in a parking lot, or outdoor areas.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Space Management** &gt; **Floor**.

2.  Continue with one of the following options.

<table id="choicetable_b35_kc4_ht"><thead><tr><th align="left" id="d41270e124">

Option

</th><th align="left" id="d41270e127">

Action

</th></tr></thead><tbody><tr><td id="d41270e133">

**To add a floor or level**

</td><td>

-   Click **New**.


</td></tr><tr><td id="d41270e151">

**To edit the details of a floor or level**

</td><td>

-   Click the name of the floor or level you want to edit.


</td></tr></tbody>
</table>3.  Fill in the fields on the form, as appropriate.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Provide a descriptive name for this floor or level.

</td></tr><tr><td>

Building

</td><td>

Select the building that the floor is in.

</td></tr><tr><td>

Main level

</td><td>

Select this check box if this floor is the main level of the building.

</td></tr><tr><td>

Abbreviation

</td><td>

Enter an alphanumeric string to identify the level the floor is on. For example, enter `G` for garage or `3` for the third floor.

</td></tr><tr><td>

Assignable area

</td><td>

Displays only the area of the floor that is assignable to users.

</td></tr><tr><td>

Usable area

</td><td>

Enter only the area of the floor that is available for the creation of spaces.

</td></tr><tr><td>

Gross area

</td><td>

Enter the total area of the floor, including non-usable and non-assignable spaces.

</td></tr><tr><td>

Area unit

</td><td>

Select the unit used for defining the space size: square feet or square meters.

 **Note:** The **Area unit** assigned to all spaces must be consistent for the rollup calculations to work properly. See [Space roll up calculations](../concept/c_SpaceRollupCalculations.md).

</td></tr><tr><td>

Current occupancy

</td><td>

Displays the number of users currently associated with the space. Calculation is generated using business rules on the Associated User \[m2m\_fm\_user\_to\_space\] table.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Max occupancy

</td><td>

Displays max occupancy of the floor based on rollup calculations from the spaces below it.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Percent occupied

</td><td>

Displays the percentage of total space occupied on this floor based on rollup calculations from the spaces below it.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Utilization min

</td><td>

Enter a number to define the minimum level of utilization for the floor or level.

</td></tr><tr><td>

Utilization max

</td><td>

Enter a number to define the maximum level of utilization for the floor or level.

</td></tr></tbody>
</table>4.  Click **Save** and the **Related Links** section displays.

    -   Show Floor Plan: Click to display a floor plan of the selected floor.
    -   View Facilities Schedule: Click to create a facilities schedule blackout and prevent work from being performed in a defined area for a scheduled time period.
5.  The **Facility Spaces** section displays with a list of spaces that are part of the floor or level. Click **New** to add a facility space or click a facility space to edit.

6.  Continue with one of the following options.

<table id="choicetable_pbs_zp4_ht"><thead><tr><th align="left" id="d41270e410">

Option

</th><th align="left" id="d41270e413">

Action

</th></tr></thead><tbody><tr><td id="d41270e419">

**To add the floor**

</td><td>

-   Click **Submit**.


</td></tr><tr><td id="d41270e437">

**To update the floor details**

</td><td>

-   Click **Update**.


</td></tr></tbody>
</table>
