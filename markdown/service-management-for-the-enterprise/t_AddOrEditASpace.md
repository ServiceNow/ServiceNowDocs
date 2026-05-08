---
title: Add or edit a space
description: Spaces are assigned to floors or levels, and can be cubicles, conference rooms, restrooms, gymnasiums, elevators, parking spaces, and so on. Spaces are assigned users and assets, and have the most data defined.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer-created maps, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Add or edit a space

Spaces are assigned to floors or levels, and can be cubicles, conference rooms, restrooms, gymnasiums, elevators, parking spaces, and so on. Spaces are assigned users and assets, and have the most data defined.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Space Management** &gt; **Space**.

2.  Continue with one of the following options.

<table id="choicetable_b35_kc4_ht"><thead><tr><th align="left" id="d28222e101">

Option

</th><th align="left" id="d28222e104">

Action

</th></tr></thead><tbody><tr><td id="d28222e110">

**To add a space**

</td><td>

-   Click **New**. The Facility Space interceptor page displays. Select the type of space you are creating.![Facility Space interceptor page displays list of space types.](../image/SpaceInterceptor.png)


</td></tr><tr><td id="d28222e133">

**To edit the details of a space**

</td><td>

-   Click the name of the floor or level you want to edit.


</td></tr></tbody>
</table>3.  Fill in the fields on the form, as appropriate.

<table id="table_wdh_p14_r4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

An auto-generated label based on the **Name**, **Building**, and **Floor** entries.

 For example, if the **Name** is 1002, the **Building** is Santa Clara Building 1, and the **Floor** is Floor 1, the **Display name** is Santa Clara Building 1 - Floor 1 – 1002.

</td></tr><tr><td>

Name

</td><td>

Enter a descriptive name for the space.

</td></tr><tr><td>

Building

</td><td>

Select the building for which you are defining the space.

</td></tr><tr><td>

Floor

</td><td>

Select the floor for which you are defining the space.

</td></tr><tr><td>

Area

</td><td>

Enter the value associated with the space size and the **Area unit** field: square feet or square meters.

</td></tr><tr><td>

Area unit

</td><td>

Select the unit used for defining the space size: square feet or square meters.

 **Note:** The **Area unit** assigned to all spaces must be consistent for the rollup calculations to work properly. See [Space roll up calculations](../concept/c_SpaceRollupCalculations.md).

</td></tr><tr><td>

Cost center

</td><td>

Select the cost center for the space. Cost centers are defined in IT Cost Management and require activation of cost management. For more information, see [Activate Cost Management](https://www.servicenow.com/docs/access?context=t_ActivatingCostManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US). This field is a reference to \[cmn\_cost\_center\] table for charge backs reasons.

</td></tr><tr><td>

Department

</td><td>

Select the department for the space. Departments are defined in User Administration. This field is a reference to the \[cmn\_department\] table.

</td></tr><tr><td>

Status

</td><td>

Select the status of the space \(active, planned, maintenance, retired\).

</td></tr><tr><td>

Availability

</td><td>

Select the availability of the space \(vacant, partially occupied, at capacity, over capacity or reserved\).

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Current occupancy

</td><td>

Displays the number of users currently associated with the space. Calculation is generated using business rules on the Associated User \[m2m\_fm\_user\_to\_space\] table.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Max occupancy

</td><td>

Enter the maximum capacity of users for this space.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Percent occupied

</td><td>

Displays the percentage of total space occupied.

 **Note:** This field depends on the **Occupiable** option being selected.

</td></tr><tr><td>

Occupiable

</td><td>

Select this check box if the space can be occupied. See [Space roll up calculations](../concept/c_SpaceRollupCalculations.md).

</td></tr></tbody>
</table>4.  Use the **Associated Users** and **Assets** related lists to view or add users and assets to the space.

5.  Use the **Associated Departments** related list to view or add which departments are associated with this space.

6.  Continue with one of the following options.

<table id="choicetable_zlc_rp4_ht"><thead><tr><th align="left" id="d28222e433">

Option

</th><th align="left" id="d28222e436">

Action

</th></tr></thead><tbody><tr><td id="d28222e442">

**To add the space**

</td><td>

-   Click **Submit**.


</td></tr><tr><td id="d28222e460">

**To update the space details**

</td><td>

-   Click **Update**.


</td></tr></tbody>
</table>
**Parent Topic:**[Customer-created maps](../reference/r_Manually-builtMaps.md)

