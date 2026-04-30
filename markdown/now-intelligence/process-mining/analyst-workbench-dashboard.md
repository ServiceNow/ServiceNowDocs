---
title: Analyst Workbench
description: View the visualized process map with tools for managing visualizations and perform analysis tasks from a project's page.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Process details page, Process Mining workspace, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Analyst Workbench

View the visualized process map with tools for managing visualizations and perform analysis tasks from a project's page.

## Access the Analyst Workbench

From the Analyst Workbench, you can access visualized process workflow data and tools for analyzing the data.

To access the Analyst Workbench:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Open a project, and navigate to Analyst Workbench.

    When you open a project, by default the Analyst Workbench opens.


![Analyst workbench view](../image/explore-analyst-workbench2.png)

## Breakdown filters

<table id="table_txt_ckt_21c"><tbody><tr><td>

Use the **Breakdown Filters** tab to create and delete filter sets, and set advanced filter conditions.

 View breakdowns for different elements using the **Selected table** drop-down, or selecting elements within the process map.

 **Note:** You can apply breakdown filters only on parent tables. However, the breakdown statistics are available on both child and parent tables.

</td><td>

![Breakdown filter tab within the Analyst workbench](../image/breakdown-filter.png)

</td></tr><tr><td>

Use the **Filter Breakdown** icon \(![Filter breakdown](../../../use/performance-analytics/image/funnel-icon.png)\) to filter your breakdowns based on criteria you select in the

</td><td>

![Breakdown filter tab within the Analyst workbench](../image/breakdown-filter-modal.png)

</td></tr><tr><td>

Use the **Transitions** button to define advanced filters on your transitions. For details on this process, see [Apply a transition filter on an activity](../task/node-to-node-conditions.md).

</td><td>

![Add activity conditions using the Transitions filter](../image/transition-location-1.png)

</td></tr></tbody>
</table>## Variation analysis

<table id="table_ebf_glt_21c"><tbody><tr><td>

Use the **Variation Analysis** tab to view the routes taken by your records, the number of cases, average duration, and number of steps involved in each route. Select a route to highlight the route in the process map.

 View analysis for different elements using the **Selected table**, or selecting elements within the process map.

</td><td>

![Breakdown filter tab within the Analyst workbench](../image/variation-analysis.png)

</td></tr></tbody>
</table>## Process map

<table id="table_hnq_llt_21c"><tbody><tr><td>

Use the **Process map** to view a visualized map of your project. Within the map, you can drill down into your business process to better understand and optimize them. The process map also displays routes according to the KPIs you want to view or measure.

</td><td>

![Breakdown filter tab within the Analyst workbench](../image/process-map-example.png)

</td></tr><tr><td>

Select a node or transition line within the map to view additional details about the selected item in a modal window.

 These windows contain bar chart histograms displaying additional information.

-   Select a node to view distribution or repetition information.
-   Select a transition line to view duration or repetition information.

 Select a bar, and select **Apply as filter** to filter by these results.

 For more information on using this tool, [Refining a process map](analyze-data.md).

 When you select a node, the modal window displays the outgoing and incoming distribution of records via the selected node.

 This information is displayed in the **Records from** and **Records to** collapsible sections.

 From the **Investigate** drop-down, you can also view the relevant records, run cluster analysis, root cause analysis, or apply a transition. These tasks are run using scheduled tasks that run in the background.

</td><td>

![Details of a node or transition line](../image/node-details-analystwb.png)

 ![Records from, to, and Investigate options in Analyst workbench](../image/process-map-example-2.png)

</td></tr><tr><td>

When you select a transition line, the modal window displays the occurrences, repetitions, and duration for the transition.

 From the **Investigate** drop-down, you can also view the relevant records, work notes analysis, run cluster analysis, root cause analysis, or apply a transition. These tasks are run using scheduled tasks that run in the background.

 For information on each analysis, see the following topics:

-   [Cluster analysis](cluster-analysis.md)
-   [Work notes analysis](worknotes-analysis.md)
-   [Automated root cause analysis](auto-rca.md)

</td><td>

![Transition line details](../image/aw-tran-details.png)

</td></tr><tr><td>

If a node name is long and is being truncated, you can view its full name. From the Modal Options window, **Auto fit node names** option.

</td><td>

![Auto-fit nodes](../image/auto-fit-nodes.gif)

</td></tr><tr><td>

You can chose to hide only incoming arcs, only outgoing arcs, or both.

 From **Modal Options**, select **Hide incoming connections**, **Hide outgoing connections**, or both to view the connections as per your need.

 **Note:** This option is available only for multi-table projects.

</td><td>

![Hide incoming and outgoing arcs](../image/hide-incoming-outgoing.gif)

</td></tr></tbody>
</table>**Note:** You can reproduce most of the functionality of a process map in a dashboard on a configurable workspace. For more information, see [Configure a Process Mining map on a dashboard](../../../use/par-for-workspace/task/configure-po-map.md).

**Parent Topic:**[Process details page](project-view-screen.md)

