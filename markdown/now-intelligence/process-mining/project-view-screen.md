---
title: Process details page
description: The process details page for Process Mining provides access to high level insights and opportunities in addition to the interactive visualized process map.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Workspace, Explore, Process Mining, Platform Analytics]
---

# Process details page

The process details page for Process Mining provides access to high level insights and opportunities in addition to the interactive visualized process map.

From the process details page, you can do the following:

-   Select the **Summary and Insights** tab to see the speed, quality, and cost insights impacting your process.
-   Select the **Opportunity details** tab to access details about an improvement opportunity.
-   Select the **Analyst workbench** tab to access the project dashboard, where you can view the visualized process map for your project.
-   Select the **Automation opportunities** tab to find automation opportunities using machine learning and process-based analysis.
-   Select the **KPI dashboard** tab to see any KPI dashboard that you have configured in the project configuration.

**Note:** To go back to the projects landing page where you can see all the project cards, select the **Process Models** tab.

## Overview panel

When you mine and open a project, Analyst workbench opens.

![Overview panel](../image/project-view-screen-annotated2.png)

The project's overview panel displays the following overview details and brief context menu.

<table><thead><tr><th>

UI element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview details

</td><td>

Important information about a project.-   Project name
-   Table that the data reports on
-   Total records in project's scope according to the filters applied
-   Number of routes represented within the records
-   Average number of days it took the records to close
-   Standard deviation variation from route duration average value
-   Median duration value

</td></tr><tr><td>

Menu icon \(...\)

</td><td>

Access the menu for additional options:-   **Edit project**

Select this option to edit the current project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

-   **Edit Versions**

Select this option to change the name of a project version. For more information, see [Change a project version name](edit-version-name.md).

-   **Create CIM**

Select this option to create a new improvement initiative. For more information, see [Create an improvement initiative from Process Mining](../task/create-improvement-initiative.md#).


</td></tr></tbody>
</table>## Project panel

Within the project view, the project panel provides business insights, filter tools to refine the data view, and access to route details.

<table><thead><tr><th>

UI element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Summary and Insights tab

</td><td>

See business goals, summary insights for your key performance indicators, transitions, and route variation. For more information, see e[Summary and insights page](summary-insights-dashboard.md).

</td></tr><tr><td>

Analyst workbench tab

</td><td>

Select this tab to access the following:-   **Breakdowns** tab: Create and delete filter sets, and set advanced filter conditions.
-   **Variants** tab: View the routes distributed over the records in the data set.

For more information, see [Analyst workbench page](analyst-workbench-dashboard.md).

</td></tr><tr><td>

KPI Dashboard tab

</td><td>

Displays any KPI dashboard that you have configured in the project configuration.

</td></tr></tbody>
</table>## Process map

The process map shows the visualized project and routes, and provides the following tools for filtering and drilling into its view. You can access the process map through the Analyst workbench tab.

<table><thead><tr><th>

UI element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metrics

</td><td>

The primary and secondary metrics to show on the process map.

</td></tr><tr><td>

Refine

</td><td>

Tune activities and connections on the map. Select this tab to access the following:

 -   **Activities** tab: Increase or reduce the detail view of activities on the process map.
-   **Connections** tab: Increase or reduce the detail view of the connections between activities on the process map.

</td></tr><tr><td>

Show Records

</td><td>

View the records for one or more selected routes.

</td></tr><tr><td>

Model Statistics

</td><td>

Use statistics for the process model that help provide perspective when comparing to the overall model statistics. This tab shows the following statistics for the filtered records or selected variant route:-   Metric: Indicates total, project-specific, or difference in metric values between compared projects.
-   Records: Number of filtered records that follow the selected route.
-   Routes: The number of routes that the filtered records followed.
-   Avg duration: The average number of days it took the filtered records or records in a selected route to close. This value compares with the average number of days duration across all records in the model.
-   Std Deviation: The variation from the route average duration value.
-   Med Duration: The middle duration value for routes.

</td></tr><tr><td>

Bottleneck Analysis

</td><td>

View the top transitions based on the metric filters you specify.

</td></tr><tr><td>

Activity Legend

</td><td>

The defined project activities that display on the process map with symbols connoting activity categories.

</td></tr><tr><td>

Process map

</td><td>

Interactive map from which you can view metrics for a process, add activity conditions to filter by, and perform other actions.

</td></tr><tr><td>

Any analysis

</td><td>

You can do a transition analysis, work notes analysis, root cause analysis, or cluster analysis from any transition or node from the graph.

</td></tr><tr><td>

Zoom

</td><td>

Enlarge or shrink the view of the process map.

</td></tr></tbody>
</table>## Notes, initiatives, and scheduled tasks panel

The notes, initiatives, and scheduled tasks panel provides tools for creating and viewing notes, snapshots, and improvement initiatives. You can also see the status of mining tasks you've scheduled.

|UI element|Description|
|----------|-----------|
|Model options icon \(![Model options icon](../image/model-options-icon.png)\)|View and use of the bottleneck analysis.|
|Global metrics icon \(![Global metrics icon](../image/global-met-icon.png)\)|View the primary and secondary metrics.|
|Notes icon![Notes icon](../image/notes-icon.png)|View the notes list, create a note, and edit or delete a note.|
|Improvement initiatives icon \(![Initiatives icon](../image/improve-initiative-icon.png)\)|View the initiatives list, create a new initiative, link to an existing initiative, or remove an initiative.|
|Scheduled tasks icon \(![Scheduled tasks icon](../image/scheduled-tasks-icon.png)\)|View the status of scheduled mining, filtering, and requested cluster analysis tasks.|

-   **[Summary and insights page](summary-insights-dashboard.md)**  
The Summary and insights page enables you to view opportunities for optimizing your process. Access the page from a Process Mining project.
-   **[Opportunity details page](opportunity-details.md)**  
The Opportunity details page displays details about the improvement opportunities for a project. Access the page from a Process Mining project.
-   **[Analyst workbench page](analyst-workbench-dashboard.md)**  
View the visualized process map with tools for managing visualizations and performing analysis tasks from a project's page.
-   **[KPI dashboard page](kpi-dashboard.md)**  
On the **KPI dashboard** page, see any KPI dashboard that you have configured for your project.

**Parent Topic:**[Process Mining workspace](analyst-workbench-overview.md)

