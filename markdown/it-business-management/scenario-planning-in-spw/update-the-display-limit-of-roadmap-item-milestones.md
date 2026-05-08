---
title: Update the display limit of items on Prioritization and Roadmap
description: Create a system property to update the display limit of the items shown in Prioritization and Roadmap views in Strategic Planning Workspace.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Prioritization display settings in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Update the display limit of items on Prioritization and Roadmap

Create a system property to update the display limit of the items shown in Prioritization and Roadmap views in Strategic Planning Workspace.

## Before you begin

Ensure the application scope in your instance is set to Global.

Role required: admin

## About this task

The default display limit for Prioritization and Roadmap pages are:

-   Planning items shown in the Prioritization tab = 250
-   Roadmap items shown in the Roadmap tab = 250
-   Goals shown in the Hierarchy tab =250
-   Item-level milestones in the Roadmap view = 100
-   Items shown in the Kanban tab = 250
-   Lanes shown in the Kanban tab = 30

If the total number exceeds these default limits, the additional number of planning items, milestone indicators, and vertical lanes are not visible in the workspace. To overwrite this default setting, create a system property and set its value to a desired limit of display.

**Important:** If the value of a system property exceeds its default value, the UI performance can degrade.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    A list of all the properties in the System Properties \[sys\_properties\] table appears.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="choicetable_ygd_pdb_3rb"><thead><tr><th align="left" id="d293023e159">

Field

</th><th align="left" id="d293023e162">

Description

</th></tr></thead><tbody><tr><td id="d293023e168">

**Name**

</td><td>

-   **sn\_align\_ws.portfolio\_plan\_items\_limit**
-   **sn\_align\_ws.item\_milestone\_limit** for Roadmap planning item milestones.
-   **sn\_align\_ws.kanban\_lanes\_max\_limit** for Kanban view lanes limit \(Prioritization, portfolio roadmap and free-form roadmap\). This is applicable only for reference fields.


</td></tr><tr><td id="d293023e194">

**Type**

</td><td>

Integer

</td></tr><tr><td id="d293023e203">

**Value**

</td><td>

Desired display limit count

</td></tr></tbody>
</table>    For information on the other form fields, see the field description table in Add a system property.

4.  Select **Submit**.


**Parent Topic:**[Prioritization display settings in Strategic Planning](../concept/configuring-prioritization-and-roadmap-settings-strategic-planning.md)

