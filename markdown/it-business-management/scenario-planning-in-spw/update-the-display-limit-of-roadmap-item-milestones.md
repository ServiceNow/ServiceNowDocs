---
title: Update the display limit of items on Prioritization and Roadmap
description: Create a system property to update the display limit of the items shown in Prioritization and Roadmap views in Strategic Planning Workspace.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Prioritization display settings in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Update the display limit of items on Prioritization and Roadmap

Create a system property to update the display limit of the items shown in Prioritization and Roadmap views in Strategic Planning Workspace.

## Before you begin

Ensure the application scope in your instance is set to Global.

Role required: admin

## About this task

The default display limit for Prioritization and Roadmap pages are:

-   Planning items shown in the prioritization view = 250
-   Roadmap items shown in the roadmap view = 250
-   Goals shown in the hierarchy view =250
-   Item-level milestones in the roadmap view = 100
-   Items shown in all the Kanban views = 250
-   Lanes shown in all the Kanban views = 30

If the total number exceeds these default limits, the additional number of planning items, milestone indicators, and vertical lanes are not visible in the workspace. To overwrite this default setting, create a system property and set its value to a desired limit of display.

**Important:** If the value of a system property exceeds its default value, the UI performance can degrade.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    A list of all the properties in the System Properties \[sys\_properties\] table appears.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="choicetable_ygd_pdb_3rb"><thead><tr><th align="left" id="d278709e153">

Field

</th><th align="left" id="d278709e156">

Description

</th></tr></thead><tbody><tr><td id="d278709e162">

**Name**

</td><td>

-   **sn\_align\_ws.portfolio\_plan\_items\_limit**
-   **sn\_align\_ws.item\_milestone\_limit** for Roadmap planning item milestones.
-   **sn\_align\_ws.kanban\_lanes\_max\_limit** for Kanban view lanes limit \(Prioritization, portfolio roadmap and free-form roadmap\). This is applicable only for reference fields.


</td></tr><tr><td id="d278709e188">

**Type**

</td><td>

Integer

</td></tr><tr><td id="d278709e197">

**Value**

</td><td>

Desired display limit count

</td></tr></tbody>
</table>    For information on the other form fields, see the field description table in [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

4.  Select **Submit**.


**Parent Topic:**[Prioritization display settings in Strategic Planning](../concept/configuring-prioritization-and-roadmap-settings-strategic-planning.md)

