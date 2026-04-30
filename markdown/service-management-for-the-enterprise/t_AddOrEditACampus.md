---
title: Add or edit a campus
description: A campus represents the top level in the organization space, and contains buildings and map sets. Details include its location, manager, gross area, and usable area. Occupancy and utilization metrics are calculated using these details.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customer-created maps, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Add or edit a campus

A campus represents the top level in the organization space, and contains buildings and map sets. Details include its location, manager, gross area, and usable area. Occupancy and utilization metrics are calculated using these details.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Space Management** &gt; **Campus**.

2.  Continue with one of the following options.

<table id="choicetable_b35_kc4_ht"><thead><tr><th align="left" id="d20304e102">

Option

</th><th align="left" id="d20304e105">

Action

</th></tr></thead><tbody><tr><td id="d20304e111">

**To add a campus manually**

</td><td>

-   Click **New**.


</td></tr><tr><td id="d20304e129">

**To add a campus using a map set**

</td><td>

-   [Process GeoJSON map files](t_ProcessMapFiles.md)


</td></tr><tr><td id="d20304e149">

**To edit the details of the campus**

</td><td>

-   Click the name of the campus you want to edit.


</td></tr></tbody>
</table>3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name for the campus.|
    |Managed by|Select the employee who manages the campus.|
    |Location|Select from the location hierarchy.|
    |Gross area|The total floor space of a campus. Includes unusable space or excluded areas.|
    |Usable area|The total useable area of a campus. Excludes unusable space or excluded areas.|
    |Assignable area|Indicates a space roll-up calculation. See [Space roll up calculations](../concept/c_SpaceRollupCalculations.md).|
    |Area unit|Select the unit used for defining the space size: square feet or square meters.|
    |Current occupancy|Displays the number of users currently associated with the space. The calculation is generated using business rules on the Associated User \[m2m\_fm\_user\_to\_space\] table.|
    |Max occupancy|Enter the maximum capacity of users for this space. This value is intended for reporting purposes.|
    |Percent occupied|The percentage of the total floor space that is occupied.|
    |Default campus|Check to indicate that this campus is the primary location for the company.|
    |Notes|Notes or comments about this campus.|

4.  Continue with one of the following options.

<table id="choicetable_zlc_rp4_ht"><thead><tr><th align="left" id="d20304e333">

Option

</th><th align="left" id="d20304e336">

Action

</th></tr></thead><tbody><tr><td id="d20304e342">

**To add the campus**

</td><td>

-   Click **Submit**.


</td></tr><tr><td id="d20304e360">

**To update the campus details**

</td><td>

-   Click **Update**.


</td></tr></tbody>
</table>
**Parent Topic:**[Customer-created maps](../reference/r_Manually-builtMaps.md)

**Related topics**  


[Space roll up calculations](../concept/c_SpaceRollupCalculations.md)

