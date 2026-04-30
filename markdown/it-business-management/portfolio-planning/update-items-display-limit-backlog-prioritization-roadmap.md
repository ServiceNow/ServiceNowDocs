---
title: Update the display limit of items for Prioritization and Roadmap in Portfolio Planning
description: Create a system property to update the display limit of the items shown in Prioritization page, Roadmap page, and the item milestones on the roadmap view in Portfolio Planning.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Update the display limit of items for Prioritization and Roadmap in Portfolio Planning

Create a system property to update the display limit of the items shown in Prioritization page, Roadmap page, and the item milestones on the roadmap view in Portfolio Planning.

## Before you begin

Ensure the application scope in your instance is set to Global.

Role required: admin

## About this task

The default display limit for Prioritization and Roadmap pages are:

-   Planning items shown in the prioritization view = 250
-   Roadmap items shown in the roadmap view = 250
-   Item-level milestones in the roadmap view = 100
-   Items shown in all the Kanban views = 250

If the total number exceeds these default limits, the additional number of planning items, milestone indicators, and vertical lanes are not visible in the workspace. To overwrite this default setting, create a system property and set it value to a desired limit of display.

**Important:** If the value of a system property exceeds its default value, the UI performance can degrade.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    A list of all the properties in the System Properties \[sys\_properties\] table appears.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="choicetable_ygd_pdb_3rb"><thead><tr><th align="left" id="d79049e137">

Field

</th><th align="left" id="d79049e140">

Description

</th></tr></thead><tbody><tr><td id="d79049e146">

**Name**

</td><td>

-   **sn\_align\_ws.portfolio\_plan\_items\_limit**
-   **sn\_align\_ws.item\_milestone\_limit** for Roadmap planning item milestones.
-   **sn\_align\_ws.kanban\_lanes\_max\_limit** for Kanban view lanes limit \(Prioritization, portfolio roadmap and free-form roadmap\). This is applicable only for reference fields.


</td></tr><tr><td id="d79049e172">

**Type**

</td><td>

Integer

</td></tr><tr><td id="d79049e181">

**Value**

</td><td>

Desired display limit count

</td></tr></tbody>
</table>    For information on the other form fields, see the field description table in [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

4.  Select **Submit**.


**Parent Topic:**[Configuring Prioritization and Roadmap settings in Portfolio Planning](../concept/configuring-prioritization-and-roadmap-settings-in-portfolio-planning.md)

