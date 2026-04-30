---
title: Installed with Timeline Visualizations
description: Several components are installed with timeline visualizations.
locale: en-US
release: zurich
product: Timeline Visualizations
classification: timeline-visualizations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate Timeline Visualization, Timeline Visualizations, Personalize your experience, Configure user experiences]
---

# Installed with Timeline Visualizations

Several components are installed with timeline visualizations.

## Tables

Timeline visualization adds the following table.

<table id="simpletable_byr_rwm_3q"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Stores all available timeline visualizations.

</td></tr><tr><td>

Personalize Timeline \[roadmap\_user\_page\]

</td><td>

Stores timeline personalization settings for all timeline visualizations.

</td></tr></tbody>
</table>## UI Policies

Timeline visualization adds the following UI policy.

<table id="simpletable_tzh_gxm_3q"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Control Timeline Visualization configuration Page to enable/disable certain fields

</td><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Script that hides fields in the Timeline Visualization form when the form loads.

</td></tr></tbody>
</table>## Script Includes

Timeline visualization adds the following script includes.

<table id="simpletable_wmb_lxm_3q"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roadmap2DUtil

</td><td>

Timeline Visualization - 2D API to generate data for lanes and panels.

</td></tr><tr><td>

RoadmapCommonUtil

</td><td>

Timeline visualization common utility to handle generic functions.

</td></tr><tr><td>

RoadmapConfig

</td><td>

Timeline visualization utility allowing configuration through the Timeline Visualization \[roadmap\_page\] table.

</td></tr><tr><td>

RoadmapItems

</td><td>

Timeline visualization utility to get lane items.

</td></tr><tr><td>

RoadmapUtil

</td><td>

API to generate data for lanes and panels.

</td></tr></tbody>
</table>## Client Scripts

Timeline visualization adds the following client scripts.

<table id="simpletable_qjh_sxm_3q"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roadmap Color Choice

</td><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Sets color values for the color choice fields in the timeline visualization configuration page.

</td></tr><tr><td>

Roadmap Item Table

</td><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Allows changing the color fields for the item\_color\_key whenever there is a change to the panel table.

</td></tr><tr><td>

Roadmap On Load

</td><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Loads the personalized version of the roadmap/visualization.

</td></tr><tr><td>

Roadmap Panel Table Change

</td><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Allows changing the field name for item\_color\_key whenever there is a change to the panel/visualization table.

</td></tr></tbody>
</table>## Business Rules

Timeline visualization adds the following business rule.

<table id="simpletable_dtq_zxm_3q"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Check only one default

</td><td>

Timeline Visualization \[roadmap\_page\]

</td><td>

Checks if another visualization is already set as default when user sets a new visualization as the default.

</td></tr></tbody>
</table>-   **[Timeline visualizations roles](r_timeline-visualizations-roles.md#)**  
Timeline visualizations provides two roles.

**Parent Topic:**[Activate Timeline Visualization](../task/t_ActivatingTimelineVisualization.md)

