---
title: View metrics for CIs in a Dependency Views map
description: Operational Intelligence processes metrics data for CIs, calculates statistics and aggregations, and detects metrics anomalies. A Dependency Views map lets you switch to metrics mode to directly access the Insights Explorer that displays metrics data for CIs on the map.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View metrics for CIs in a Dependency Views map

Operational Intelligence processes metrics data for CIs, calculates statistics and aggregations, and detects metrics anomalies. A Dependency Views map lets you switch to metrics mode to directly access the Insights Explorer that displays metrics data for CIs on the map.

## Before you begin

The Operational Intelligence \(com.snc.sa.metric\) plugin must be activated to enable this functionality, and metrics data needs to be processed for the CIs on the Dependency Views map.

Role required: admin

## About this task

Open a Dependency Views map in metric mode which integrates a Dependency Views map with the Insights Explorer functionality that is tailored to the map. In this mode, you can access Insights Explorer functions directly from the map, to explore metrics data for the CIs on the map. All map CIs are accessible in the right hand side pane, from where you can drill into metrics data.

## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **View Map** to open a map.

2.  Right-click on a CI on the map and select **View Metrics** to open the Dependency View map in metrics mode.

    In the panel on the right side, the CI that you selected on the Dependency View map is selected by default, and the list of all the metrics available for that CI are displayed.

3.  Click the '**&lt;**' sign on the left of the CI to display all the CIs that you can explore metrics for.

    The Insights Explorer is scoped for exploring only the CIs that currently display on the Dependency Views map, and you cannot add or remove CIs from the list. If you use map settings or filters to filter out CIs from the map, the same filtering will apply to the list of CIs that you can explore metrics for.

4.  Click on a CI in the CIs list or right-click on a CI on the Dependency Views map, to drill down to the CI's metrics.

5.  Click the **Dependencies Map** tab or the **Metrics** tab to switch modes:

    1.  In **Metrics** mode: The full functionality of the Insights Explorer is available, you can create metric charts by dragging metrics into the canvas.

        You can modify chart settings, select different time ranges for the charts, and perform other actions as described in [View metric values in the Insights Explorer](https://www.servicenow.com/docs/access?context=view-metrics-explorer&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

    2.  In **Dependencies Map** mode: Select a CI on the map to drill down to its metrics data, drop-down the **Layout** list to choose a different layout, or modify map settings.


**Parent Topic:**[Use Dependency Views](../topic/p_UseNGBSM.md)

**Related topics**  


[View a Dependency Views map](t_AccessNGBSM.md)

[Save or load a Dependency Views map](t_SaveLoadMapView.md)

[Delete a saved Dependency Views map view](t_DeleteSavedMapView.md)

[Change the layout of Dependency Views map](t_ChangeLayoutNGBSMMap.md)

[Filter the view of a Dependency Views map](t_FilterViewNGBSMMap.md)

[Perform actions on nodes in a Dependency Views map](t_PerformActionsOnNGBSMMap.md)

[Export a Dependency Views map](t_ExportAnNGBSMMap.md)

[View collapsed nodes in a Dependency Views map](t_ViewCollapsedNodesInNGBSM.md)

