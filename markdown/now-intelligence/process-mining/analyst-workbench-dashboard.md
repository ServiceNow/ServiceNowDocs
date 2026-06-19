---
title: Analyst workbench page
description: View the visualized process map with tools for managing visualizations and performing analysis tasks from a project's page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/analyst-workbench-dashboard.html
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Details page, Workspace, Explore, Process Mining, Platform Analytics]
---

# Analyst workbench page

View the visualized process map with tools for managing visualizations and performing analysis tasks from a project's page.

## Access the Analyst workbench

From Analyst workbench, you can access visualized process workflow data and tools for analyzing the data.

To access Analyst workbench:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Open a project, and navigate to Analyst workbench.

\[Omitted image "explore-analyst-workbench2.png"\] Alt text: Analyst workbench view

## Breakdowns

<table id="table_txt_ckt_21c"><tbody><tr><td>

Use the **Breakdowns** tab to create and delete filter sets, and set advanced filter conditions.

 **Note:** You can apply breakdown filters on parent and child tables.

</td><td>

\[Omitted image "breakdown-filter.png"\] Alt text: Breakdown filter tab within the Analyst workbench

</td></tr><tr><td>

Use the Filter breakdowns icon \(\[Omitted image "filter.png"\] Alt text: Filter breakdown\) to filter your breakdowns based on criteria you select in the filters.

</td><td>

\[Omitted image "breakdown-filter-modal.png"\] Alt text: Filter breakdowns modal within the Analyst workbench

</td></tr><tr><td>

Use the **Process steps** button to define advanced filters on your transitions. For details on this process, see [Create a process step filter manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-transition-manually.md).You can filter the parent and the child tables in the multidimensional projects.

</td><td>

\[Omitted image "transition-location-1.png"\] Alt text: Add activity conditions using the process step filter

</td></tr><tr><td>

You can also view the number of touchpoint records from the **Breakdowns** tab by selecting the columns.

</td><td>

\[Omitted image "touchpoints-breakdown.gif"\] Alt text: Touchpoint records from Breakdowns tab

</td></tr><tr><td>

You can also view the number of idle case records from the **Breakdowns** tab by selecting the columns.

</td><td>

\[Omitted image "idletime-breakdowns.gif"\] Alt text: Idle case records from Breakdowns tab

</td></tr></tbody>
</table>## Variation analysis

<table id="table_ebf_glt_21c"><tbody><tr><td>

Use the **Variants** tab to view the routes taken by your records, the number of cases, average duration, and number of steps involved in each route. Select a route to highlight the route in the process map.

</td><td>

\[Omitted image "variation-analysis.png"\] Alt text: Variations tab within the Analyst workbench

</td></tr><tr><td>

View the number of touchpoints from the **Variants** tab by selecting the columns.

</td><td>

\[Omitted image "touchpoint-variation.gif"\] Alt text: Touchpoints from the Variations tab

</td></tr><tr><td>

View the number of idle case records from the **Variants** tab by selecting the columns.

</td><td>

\[Omitted image "idletime-variation.gif"\] Alt text: Idle time from the Variants tab

</td></tr></tbody>
</table>## Process map

<table id="table_hnq_llt_21c"><tbody><tr><td>

Use the **Process map** to view a visualized map of your project. Within the map, you can drill down into your business process to better understand and optimize them. The process map also displays routes according to the KPIs you want to view or measure.

</td><td>

\[Omitted image "process-map-example.png"\] Alt text: Process map within the Analyst workbench

</td></tr><tr><td>

Select a node or transition line within the map to view additional details about the selected item in a modal window.

 These windows contain bar chart histograms displaying additional information.

-   Select a node to view distribution or repetition information.
-   Select a transition line to view duration or repetition information.

 Select a bar, and select **Apply as filter** to filter by these results.

 For more information on using this tool, [Refining a process map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/analyze-data.md).

 When you select a node, the modal window displays the outgoing and incoming distribution of records via the selected node.

 This information is displayed in the **Transitions** section.

</td><td>

\[Omitted image "node-details-analystwb.png"\] Alt text: Details of a node or transition line

</td></tr><tr><td>

When you select a transition line, the modal window displays the occurrences, repetitions, and duration for the transition.

 From the **Investigate** drop-down, you can also view the relevant records, work notes analysis, run cluster analysis, root cause analysis, or apply a transition. These tasks are run using scheduled tasks that run in the background.

 For information on each analysis, see the following topics:

-   [Cluster analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/cluster-analysis.md)
-   [Work notes analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/worknotes-analysis.md)
-   [Automated root cause analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/auto-rca.md)

</td><td>

\[Omitted image "aw-tran-details.png"\] Alt text: Transition line details

</td></tr><tr><td>

Select a node or transition, and from the dialog box, select **Filter on Process step** in the **Investigate** section.You can edit the process step and apply it. This task runs using the scheduled tasks that run in the background. After the task completes, you can view the result.

</td><td>

\[Omitted image "filter-process-step.png"\] Alt text: Filter on process step

</td></tr><tr><td>

Select a node, and from the dialog box, select **Outgoing** or **Incoming** from the **Transitions** section.Now, go to the Investigate section, and select **Filter on process steps**.

The filter is created with the preference you chose in the **Transitions** section. Select **Apply**.

This task runs using the scheduled tasks that run in the background. After the task completes, you can view the result.

</td><td>

\[Omitted image "filter-on-node.gif"\] Alt text: Set filter on node

</td></tr><tr><td>

If a node name is long and is being truncated, you can view its full name. From the Modal Options window, **Auto fit node names** option.

</td><td>

\[Omitted image "auto-fit-nodes.gif"\] Alt text: Auto-fit nodes

</td></tr><tr><td>

You can apply multiple activity definitions in one view. Select multiple activity definitions from the Views area, and select **Apply view**.

</td><td>

\[Omitted image "multiple-ads.png"\] Alt text: Applying multiple activity definitions in one view

</td></tr><tr><td>

You can chose to hide only incoming arcs, only outgoing arcs, or both.

 From **Modal Options**, select **Hide incoming connections**, **Hide outgoing connections**, or both to view the connections as per your need.

 **Note:** This option is available only for multi-table projects.

</td><td>

\[Omitted image "hide-incoming-outgoing.gif"\] Alt text: Hide incoming and outgoing arcs

</td></tr><tr><td>

You can view the number of touchpoints for the project from the process map.Select a transition and view the details to know how many touchpoints took place between the selected steps.

Select a node and view the details to know how many touchpoints took place until the record moves to any next step. You can view the histogram distribution of touchpoints on the node.

You can also set a touchpoint from the histogram as a filter. Select a node. On the details window, select **Touchpoints** from the **Metrics** list of the **Records distribution** section. Now, select a touchpoint from the histogram, and select **Set as filter**.

This task runs in the background using scheduled tasks. Yo can view the data on this filter after the task is complete.

</td><td>

\[Omitted image "touchpoint.gif"\] Alt text: Touchpoints from the process map

</td></tr><tr><td>

You can view the number of idle time cases for the project from the process map.From the model options, filter the view by a team \(for example, Assignment group\). Select a node, and view the details to know the total idle time cases. You can view the histogram distribution of idle time on the node.

</td><td>

\[Omitted image "idletime.gif"\] Alt text: Idle time cases from the process map

</td></tr><tr><td>

Create a Task Mining project.Select a node, then select the **Create project** button in the Task Mining section.

For information on creating a Task Mining project, see [Create Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-task-mining-project.md).

You can access the associated Task Mining projects from the right panel using the icon \(\[Omitted image "icon-asso-proj.png"\] Alt text: Task Mining icon\).

</td><td>

\[Omitted image "wrkbench-tm.png"\] Alt text: Create a Task Mining project

</td></tr></tbody>
</table>**Note:** You can reproduce most of the functionality of a process map in a dashboard on a configurable workspace. For more information, see [Configure a Process Mining map on a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-po-map.md).

**Parent Topic:**[Process details page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/project-view-screen.md)

