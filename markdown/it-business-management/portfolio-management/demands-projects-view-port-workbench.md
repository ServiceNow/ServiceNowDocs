---
title: Legacy- Planning view in portfolio workbench
description: View all the demands and projects scheduled for the selected fiscal year with their planned cost, resource requirements, and priorities to finalize them for execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/demands-projects-view-port-workbench.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Planning view in portfolio workbench

View all the demands and projects scheduled for the selected fiscal year with their planned cost, resource requirements, and priorities to finalize them for execution.

These sections are presented in the planning view in the portfolio workbench:

## Demands and projects

The demands and projects are presented on two different tabs:

-   **Bubble Chart** tab: Shows all qualified or approved demands planned for the selected fiscal year. The demands are scored based on attributes such as planned cost, ROI%, and risk, and are presented in [bubble chart format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/demand-management/c_DemandWorkbenchBubbleChart.md).

    The demands that are selected for execution are highlighted with a blue border \(\[Omitted image "SelectedDemandBorder.png"\] Alt text: selected demand icon\).

    The number of selected demands versus the total number of demands are displayed as a counter in the top-right corner of the chart \(\[Omitted image "DemandNumbers.png"\] Alt text: Selected versus total demands\).

    **Note:** The demands may have converted to projects and the projects are in the **Work in Progress** state. These demands aren't shown in the bubble chart. View these demands as projects in the timeline view.

-   **Timeline View** tab: Shows a list of all the demands and projects that are part of the portfolio. It also shows a Gantt chart of all the projects, demands, and programs in the portfolio over time.

    All demands selected for execution in the bubble chart are shown as selected in the timeline view.

    As a portfolio manager, you can perform the following actions:

    -   Configure the colors of the portfolio items in the Gantt chart with [Dashboard Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_AccessThePortfolioWorkbench.md) settings.
    -   Select the zoom level in the Gantt chart calender to **Auto Fit**. The Gantt view fits on one page to view the entire timeline without using the scrollbar.
    -   Select or clear a demand or a project for execution by selecting the check box next to each demand or project. The number of selected demands, the total number of demands, the number of selected projects, and the total number of projects are displayed as respective counters: \(\[Omitted image "DemandNumbers.png"\] Alt text: Selected versus total demands\) and \(\[Omitted image "ProjectNumbers.png"\] Alt text: Selected versus total projects\).
    -   Review or revise the Capex and Opex budget for individual projects and demands directly by using the **Capex Budget** and **Opex Budget** columns, if required.
    -   [Review the external dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/review-external-dependencies-between-projects.md) between projects in a portfolio.
    -   Rank demands and projects based on score, currency, numeric attributes, or manual adjustment. Ranks help in prioritizing demands and projects for their approval and execution within a portfolio.

        By default, the **Rank By Score** list ranks demands and projects based on system-generated scores. The list provides the following options:

        -   **Rank By Visual Sort**: To rank projects and demands based on any currency or number attribute, such as ROI%, priority, and planned cost, first sort by the required attribute. Then perform this action to rank by that attribute.
        -   **Adjust Rank**: Gaps in ranks can occur when projects are moved to the next fiscal year or are canceled. Perform this action to rearrange the projects. For example, if the ranks are 1, 2, 5, 8, this action adjusts the ranks as 1, 2, 3, and 4.
        As a portfolio manager, you can also change a rank by editing the **Rank** field. When the rank of a project or demand is changed, the other ranks are automatically adjusted. For example, if a number 2 ranked project is ranked as 4, the number 3 ranked project automatically assumes rank 2, and the number 4 ranked project automatically assumes rank 3.

        **Note:** Rank of an entity is specific to a fiscal year. A project can be ranked as number 3 in FY17, but can be ranked as number 6 in FY18.

    **Note:**

    -   Key milestones appear as overlays on top of the project timeline.
    -   An administrator can [customize](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/custom-columns-planning-console.md) which columns appear in the column filter list \(\[Omitted image "filter\_icon.png"\] Alt text: filter icon\) in the timeline view.

## Charts

The charts presented represent different aspects of a portfolio to help you plan the portfolio:

-   **Cost \(Planned vs. Target\)**: Displays the planned costs versus the targets that you entered in the **Set Target** step. Use this chart when you [select projects and demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_SelectProjectsAndDemands.md) for portfolio planning.

    As you select a demand or a project, the cost bar starts filling up, representing the total planned cost for all selected demands and projects. The exception icon \(\[Omitted image "ExceptionIcon.png"\] Alt text: icon for exceptions\) appears with the total planned cost when it exceeds the target budget.

    In this widget, you can:

    -   Select a fiscal period in the list.
    -   View the planned cost only for Capex, or, Opex, or All.
-   **Resource Overview and % Utilization**: Use these charts when you select projects and demands for portfolio planning:
    -   **Resource Overview** tab: Shows the following items in the stacked bar chart. Point to any of the sections on the bar chart to view its details.

        -   **Capacity**: The total capacity of all groups or resources requested by selected demands and projects in the portfolio.
        -   **Requested hours**: The total number of hours requested by all selected demands and projects of the portfolio. It does not include requested hours by demands or projects of other portfolios.
        -   **Confirmed hours**: The number of hours confirmed across all portfolios for the groups requested by selected demands and projects.
        -   **Allocated hours**: The number of hours allocated across all portfolios for the groups requested by selected demands and projects.
        You can modify the settings of the chart by selecting any of the following options:

        -   **Hours**: Displays the chart in relation to hours and fiscal periods.
        -   **FTE**: Displays the chart in terms of FTE and fiscal periods.
        -   **Person Days**: Displays the chart in relation to person days and fiscal periods.
        Ideally, the total resource hours \(for all quarters\) must be less than or equal to the total capacity of resources. If total hours exceed the capacity, you can defer a few demands or projects. Alternatively, you can add more resources to increase the capacity.

        Clicking a section of the bar chart that shows allocated, or confirmed, or requested opens the associated resource plans.

    -   **% Utilization** tab: Shows the heat map for the percentage of utilization for all the resources requested by the selected demands and projects in the portfolio. The percentage of utilization for each resource group or role for a group is calculated as follows:

        `(Total requested hours by selected demands and projects of current portfolio + Total confirmed and allocated hours for the group by selected demands and projects across all portfolios)/Group capacity`

        If the percentage of utilization of a group is more than 100%, the portfolio manager can drill down to see requests for demands or projects. You can then exclude low priority demands or projects to balance the utilization.

        You can modify the display settings of the heat map by selecting either of the following options:

        -   **Group**: Displays the heat map for the resource groups requested for the portfolio.
        -   **Role**: Displays the heat map for the resource roles requested for the portfolio.
        Clicking any cell in the heat map drills down to the associated resource plans and shows where the specific group is being requested. For example:

        \[Omitted image "PortWbResDrillDown.png"\] Alt text: The resource plan drill-down from heat map


## UI actions

The following options are available at the top of the planning view in the portfolio workbench:

-   **Refresh** icon \(\[Omitted image "RefereshIcon.png"\] Alt text: icon for refreshing\): Manually refreshes the cost and resource charts after a demand or a project is selected or deselected for execution.
-   **Auto Refresh** switch: Clicking the configuration icon \(\[Omitted image "PersonalizeIcon.png"\] Alt text: configuration icon\) displays the **Auto Refresh** switch. The switch enables the automatic refresh of cost and resource charts when a demand or a project is selected or deselected for execution.

\[Omitted image "PortPlanningView.png"\] Alt text: The bubble chart planning view in portfolio workbench

\[Omitted image "PortPlanningView2.png"\] Alt text: The timeline planning view in portfolio workbench

**Parent Topic:**[Legacy- Plan the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md)

