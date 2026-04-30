---
title: Process details page
description: The process details page for Process Mining provides access to high level insights and opportunities in addition to the interactive visualized process map.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Process Mining workspace, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Process details page

The process details page for Process Mining provides access to high level insights and opportunities in addition to the interactive visualized process map.

From the process details page, you can do the following:

-   Select the **Summary and Insights** tab to see the speed, quality, and cost insights impacting your process.
-   Select the **Analyst Workbench** tab to access the project dashboard, where you can view the visualized process map for your project.
-   Select the **Automation Opportunities** tab to find automation opportunities using machine learning and process-based analysis.

**Note:** To go back to the projects landing page where you can see all the project cards, select the **Process Projects** tab.

## Overview panel

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
-   Average number of days it took records to close
-   Standard deviation variation from route duration average value.
-   Median duration value
-   Number of records included in the project's data

</td></tr><tr><td>

Menu icon \(![](../image/po-ellipsis-purple.png)\)

</td><td>

Access the menu for additional options:-   **Edit project**

Select this option to edit the current project. For more detail see [Create a project or template using Project Builder](../task/define-workflow-model.md).

-   **Edit Versions**

Select this option to change the name of a project version. For more detail see [Change a project version name](edit-version-name.md).


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

See business goals, summary insights for your key performance indicators, transitions, and route variation.

</td></tr><tr><td>

Analyst Workbench tab

</td><td>

Select this tab to access the following:-   **Breakdown Filters** tab: Create and delete filter sets, and set advanced filter conditions.
-   **Variation Analysis** tab: View the routes distributed over the records in the data set.

</td></tr><tr><td>

Automation Opportunities tab

</td><td>

Helps to identify automation opportunities for your workflows. Only available for ITSM.

</td></tr></tbody>
</table>## Process map

The process map shows the visualized project and routes, and provides the following tools for filtering and drilling into its view. You can access the process map through the Analyst Workbench tab.

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

Zoom

</td><td>

Enlarge or shrink the view of the process map.

</td></tr></tbody>
</table>## Notes, initiatives, and scheduled tasks panel

The notes, initiatives, and scheduled tasks panel provides tools for creating and viewing notes, snapshots, and improvement initiatives. You can also see the status of mining tasks you've scheduled.

|UI element|Description|
|----------|-----------|
|Notes icon![](../image/notes-icon.png)|View the notes list, create a note, and edit or delete a note.|
|Initiatives icon \(![](../image/improve-initiative-icon.png)\)|View the initiatives list, create a new initiative, link to an existing initiative, or remove an initiative.|
|Scheduled tasks icon \(![](../image/scheduled-tasks-icon.png)\)|View the status of scheduled mining, filtering, and requested cluster analysis tasks.|

-   **[Summary and Insights page](summary-insights-dashboard.md)**  
The Summary and Insights page enables you to view opportunities for optimizing your process. Access the dashboard from a Process Mining project.
-   **[Analyst Workbench](analyst-workbench-dashboard.md)**  
View the visualized process map with tools for managing visualizations and perform analysis tasks from a project's page.
-   **[Automation opportunities page](automation-opportunities.md)**  
Use the automation opportunities page to find automation opportunities using machine learning and process-based analysis.

**Parent Topic:**[Process Mining workspace](analyst-workbench-overview.md)

