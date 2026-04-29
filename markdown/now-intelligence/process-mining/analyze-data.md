---
title: Refining a process map
description: View your visualized workflow project for insights and improvement opportunities in your business process.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# Refining a process map

View your visualized workflow project for insights and improvement opportunities in your business process.

The visualized process map helps you see data that is specific to a problem. Within the map, you can drill down to understand the root causes. Also display routes according to the KPIs you want to view or measure.

**Note:** You can reproduce most of the functionality of a process map in a dashboard on a configurable workspace. For more information, see [Configure a Process Mining map on a dashboard](../../../use/par-for-workspace/task/configure-po-map.md).

-   Use the activity and connection sliders to focus on the process steps which occurred most frequently. You can also include steps which occurred at lesser frequencies.
-   Move an activity to a different position on the map workspace.
-   Slide a metric number along a connection to improve the visual display.
-   Select an activity or connection to view [metric](../task/apply-metrics.md) details.

<table id="table_pb4_hyc_jvb"><thead><tr><th>

Example

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

![regular node transition](../image/regular-node-transition.png)

</td><td>

Regular node transition line presenting minimum one and maximum two performance metrics. The following performance metrics can be shown: -   Total occurrences
-   Unique occurrences
-   Minimum duration
-   Maximum duration
-   Avg duration
-   Total duration
-   Standard deviation
-   Median duration

</td></tr><tr><td>

![inter-model transition](../image/inter-model-transition.png)

</td><td>

The inter-model transition slider shows the number of transitions hidden in the graph. Users can select on the inter-model transition line to change the % of transitions within the graph show. One line per parent-child relation is shown.

</td></tr><tr><td>

![artificial lines](../image/artifical-lines.png)

</td><td>

Artificial lines help the user to understand from which nodes the process ends. Multiple artificial lines from different nodes to process end per entity can occur.

</td></tr><tr><td>

![dashed line](../image/dashed-line.png)

</td><td>

The dashed line shows that the entity is collapsed. The line will disappear when the user expands the entity by selecting the + icon.

</td></tr><tr><td>

![directional arcs](../image/directional-arcs.png)

</td><td>

The direction of the arcs show the sequence of the activity occurrence. For example, for 2.2k records, state New occurs on average 10 months before they moved into the state Assigned.

</td></tr></tbody>
</table>**Parent Topic:**[Analyzing and getting process insights](analyze-get-process-insights.md)

