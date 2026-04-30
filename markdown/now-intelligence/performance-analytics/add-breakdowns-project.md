---
title: Group data by breakdown definitions
description: Each project can have a set of breakdown definitions that you can use to group the data in KPIs. These breakdown definitions provide the specifications for Performance Analytics breakdowns that you eventually create.Provide the functional description of how to build an actual Performance Analytics breakdown in a breakdown definition. Once an appropriate Performance Analytics breakdown exists, you can link to it in the breakdown definition.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [KPI Composer projects, Design your Performance Analytics solution with KPI Composer, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Group data by breakdown definitions

Each project can have a set of breakdown definitions that you can use to group the data in KPIs. These breakdown definitions provide the specifications for Performance Analytics breakdowns that you eventually create.

Prerequisites
:   [Create a KPI Composer project](create-kpi-composer-project.md)

## Before you begin

Role required: sn\_kpi\_composer.user \(own project\), sn\_kpi\_composer.admin \(any project\), admin. No role required for responsible user or user with edit access from project sharing.

## Procedure

1.  Navigate to **All** &gt; **KPI Composer** and create or open a project.

2.  In the Analysis tab, click the 'Group by' icon \(![](../image/kpi-comp-bkdown-icon.png)\) at the top right of the screen.

3.  In the 'Group by' dialog, use the sliders to select which breakdown definitions to include in your project.

    !['Group by' dialog for projects, with sliders and Add Item link](../image/kpi-comp-project-bkdowns.png)

    The selected breakdown definitions appear in the header of the KPI tree canvas. From here, you can drag them onto artifacts.

4.  To add a new breakdown definition to your project, click **Add Item** and enter the term.

    ![Add Item field filled in with new breakdown name](../image/kpi-comp-new-breakdown.png)

    The new item appears in the 'Group by' list, and a matching breakdown definition record is created.


## Selecting breakdown definitions for a KPI Composer project

In the following short animation, you see how to select the breakdown definitions Assignment Group, Impact, and Priority to a project. Then you see how to group the values of a KPI tree artifact by Assignment Group and Priority.![Short animation showing 'Group by' terms being added](../image/kpi-comp-add-breakdowns.gif)

## What to do next

Drag breakdown definitions \('Group by' items\) onto existing artifacts on the canvas. You can group the data associated with an artifact by any number of breakdown definitions. The colored dots on an artifact show which breakdown definitions the artifact is grouped by. To see the names of these breakdown definitions, point to any of the colored dots on the artifact.

By holding down the Ctrl/Command or Alt/Option key while dropping a breakdown definition onto an artifact, you activate the following advanced functions:

-   **Hold Ctrl while dropping**

    Add the breakdown definition to the artifact on which it is dropped and to all child artifacts of that artifact.

-   **Hold Alt while dropping**

    Remove the breakdown definition from the artifact on which it is dropped.

-   **Hold Ctrl and Alt while dropping**

    Remove the breakdown definition from the artifact on which is dropped and from all child artifacts of that artifact.


**Parent Topic:**[KPI Composer projects](../concept/kpi-composer-projects.md)

**Previous topic:**[Add personas to a project](add-personas-project.md)

**Next topic:**[Write journal entries for a project](write-journal-entries-kpi-composer.md)

## Define a breakdown

Provide the functional description of how to build an actual Performance Analytics breakdown in a breakdown definition. Once an appropriate Performance Analytics breakdown exists, you can link to it in the breakdown definition.

### Before you begin

Role required: sn\_kpi\_composer.user, sn\_kpi\_composer.admin \(to link to Performance Analytics breakdown\), admin. No roles required for responsible user or user with edit access, except to link to link to Performance Analytics breakdown.

### About this task

The breakdown definitions that you add to KPI Composer projects are not actual Performance Analytics breakdowns. They are only placeholders that describe what the Performance Analytics breakdown should be. In KPI Composer breakdown definitions, you provide either or both of the following pieces of information:

-   The details that a Performance Analytics expert needs to create the actual breakdown.
-   A reference to an existing Performance Analytics breakdown that meets your requirements.

### Procedure

1.  In the Analysis tab, click the 'Group by' icon \(![](../image/kpi-comp-bkdown-icon.png)\).

2.  Click the name of the breakdown you want to define.

3.  Fill in the following information:

<table id="table_dql_qnv_njb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

PA Breakdown\(Restricted to sn\_kpi\_composer.admin and admin roles\)

</td><td>

A Performance Analytics breakdown that exists on this instance.

</td><td>

If a breakdown definition does not have a reference to a Performance Analytics breakdown, consider creating that breakdown.

</td></tr><tr><td>

Facts Table

</td><td>

The table that the breakdown source for the Performance Analytics breakdown has to reference.

</td><td>

Key information for creating a breakdown.

</td></tr><tr><td>

Conditions

</td><td>

The filter conditions to apply to the facts table either in the breakdown source or in the breakdown itself.

</td><td>

 

</td></tr></tbody>
</table>
