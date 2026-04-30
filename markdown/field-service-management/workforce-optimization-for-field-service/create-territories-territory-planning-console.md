---
title: Create a Field Service territory
description: Create territories for optimizing agent and group scheduling. By mapping these territories to the territory model, you can maintain a record of your territory setup, ensuring efficient management.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create a Field Service territory

Create territories for optimizing agent and group scheduling. By mapping these territories to the territory model, you can maintain a record of your territory setup, ensuring efficient management.

## Before you begin

You must set up a territory geography before you start creating a territory. For more information, see [Create a GeoJSON geography in Territory Planning console](../concept/creating-a-gojson-geography.md#).

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

Set up a territory geography before creating territories. A territory is defined by its geographic area, and you can organize multiple territories in a hierarchy. The highest-level territory serves as the parent territory, covering geographic areas within it as child territories. For example, you can create a parent territory, California, and its child territories: San Francisco, Los Angeles, San Jose, and Santa Clara.

When creating a new territory, you have the option to copy an existing territory record with any modified values by selecting the **Insert and Stay** option.

## Procedure

1.  Open either Territory Planning platform or Territory Planning console.

    -   Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territories** &gt; **New**.
    -   Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console** &gt; **Create Territory**.
2.  On the form, fill in the fields.

<table id="table_nhd_jpr_stb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the territory.

</td></tr><tr><td>

Description

</td><td>

Description of the territory.

</td></tr><tr><td>

Parent

</td><td>

Name of the parent location for the territory to create a territory hierarchy.If no parent territory is specified, this territory will serve as the highest-level \(parent\) territory.

**Note:** Territory manager can only create child territories for their territories.

</td></tr><tr><td>

Rank

</td><td>

Set a ranking rule to prioritize territories for task assignment \(descending order\).

</td></tr><tr><td>

Color

</td><td>

Enter the hexadecimal code or color picker to select the color. This helps to highlight the territory on the map in the Territory Planning console. **Note:** This field becomes optional when the selected territory has been created using matching attributes geography and the selected territory is a non-assignment territory.

</td></tr><tr><td>

Model

</td><td>

Name of the territory model to which to map this territory.This field is automatically set to the default **Field\_Service\_Territories** territory model.

</td></tr><tr><td>

Assignment Territory

</td><td>

Select the check box to convert the territory into an assignment territory, allowing you to add assignment groups and field service agents to it.**Note:** An inactive assignment territory is not eligible for scheduling and does not appear in the Dispatcher Workspace.

</td></tr><tr><td>

Geography

</td><td>

Add the name of the geographic area defined for this territory. **Note:** This field is optional for a non-assignment territory.

</td></tr><tr><td>

Active

</td><td>

Indicate whether the territory is available for scheduling.**Note:** An inactive territory is not eligible for scheduling and does not appear in the Dispatcher Workspace.

</td></tr></tbody>
</table>3.  Select **Save**.

    The territory is created.


## Result

When accessing a territory record, the displayed related lists depend on whether it is categorized as assignment or non-assignment type. Non-assignment territories allow the addition of managers and child territories exclusively. However, assignment territories permits to add managers, qualification groups, dispatch groups, assignment groups, agents, child territories, capacity assignment, and crews. These assignment territories are specifically considered in the context of work order management.

## What to do next

[Configuring resources for territories](../concept/configuring-resources-for-territories.md)

