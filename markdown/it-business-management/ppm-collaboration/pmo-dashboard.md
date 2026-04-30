---
title: PMO dashboard
description: The PMO dashboard provides comprehensive reports to the portfolio and program managers. The dashboard uses Platform Analytics to provide a trend of historical data as well as regular reports. It gives an overview of your investments, provides a pipeline view of upcoming intake and a calendar view of upcoming dates.
locale: en-US
release: zurich
product: PPM Collaboration
classification: ppm-collaboration
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 9
breadcrumb: [Analytics and reporting, Project Portfolio Management, Strategic Portfolio Management]
---

# PMO dashboard

The PMO dashboard provides comprehensive reports to the portfolio and program managers. The dashboard uses Platform Analytics to provide a trend of historical data as well as regular reports. It gives an overview of your investments, provides a pipeline view of upcoming intake and a calendar view of upcoming dates.

**Note:** The PMO dashboard is available in the next experience UI framework which can be accessed through **Analytics Portfolio**. In the next experience, these features are not supported:

-   **Pipeline details** pane in the **Pipeline** tab.
-   **Highlight based on** list and **View all records** link in the **Calender** tab.

## PMO dashboard in Next experience UI

This animation shows all of the data visualizations in the PMO dashboard tab by tab. They are described in the Data Visualizations section of this topic.

![Animated tour of the PMO Dashboard in Next experience UI](../image/pmo-dashboard.gif)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Portfolio manager: Needs visibility into programs, projects, and demands in their portfolio and actions that should be taken.|it\_portfolio\_manager|
|Program manager: Needs visibility into projects and demands in their programs and actions that should be taken.|it\_program\_manager|
|Project manager: Has access to the dashboards.|it\_project\_manager|

## Indicators

The Summary, Pipeline, and Project Health tabs in the dashboard contain widgets with the following indicators. The data for projects is collected from the \[pm\_project\] table, the data for demands is collected from the \[dmn\_demand\] table, and the data for ideas is collected from the \[idea\] table.

-   **PPM – Number of Active Projects**

    Count of active projects. Projects are considered active where actual end date is &lt;after today&gt; or &lt;empty&gt;.

    **Note:** If the Actual End Date for a project is in the future but the project is in Closed state, the reports still pick up the project as active.

-   **PPM – Allocated Hours less than Planned Hours**

    Count of active projects that have resource plans where the allocated hours is less than the planned hours.

-   **PPM – Active Projects in Open, Pending, Work in Progress state**

    Count of active projects in Open, Pending, or Work in Progress state.

-   **PPM – Number of Active Red Projects**

    Count of active projects that have an overall red status.

-   **PPM – Total age of Open Project**

    Total age of all active projects in days. It is the difference between the planned start date of the active project and the date when the indicator score is collected. The indicator is used to calculate the average age of open projects.

-   **PPM – Planned Cost**

    Total planned cost for all the active projects.

-   **PPM – Actual Cost**

    Total actual cost for all the active projects.

-   **PPM – Number of Active Projects with negative ROI**

    Count of active projects with a negative Return on Investment.

-   **PPM – Estimate at Completion**

    Total estimated cost at completion for all active projects.

-   **PPM – Number of Projects with High Risks**

    Count of active projects that have a Risk in Pending state and Probability as Absolute or High.

-   **PPM – Number of Projects with Critical Issues**

    Count of active projects that have an Issue with state Open or Work in Progress and priority as Critical.

-   **PPM – Number of Projects with Missed Milestones**

    Count of active projects that have a milestone with planned end date due before today.

-   **PPM – Number of Active Overdue Projects**

    Count of active projects that have **Planned end date** before today.

-   **PPM – Unallocated Resources**

    Count of projects in state Work in Progress that have resource plans in Planning, Requested, or Confirmed state.

-   **PPM – Allocated Hours less than Actual Hours**

    Count of active projects that have resource plans where the actual hours is greater than the allocated hours. 

-   **PPM – Planned Benefits**

    Total planned benefit for all active projects.

-   **PPM – Actual Benefits**

    Total actual benefit for all active projects.

-   **PPM – Number of Projects with critical Change Requests**

    Count of active projects that have a Project Change Request with state as Open and priority as Critical.

-   **PPM – Number of Total Demands this Month**

    Count of demands in the given month with state other than Draft.

-   **PPM – Number of Demands with Projects this Month**

    Count of demands that are converted to projects in the given month.

-   **PPM – Open Demands Submitted, Screening, Qualified or Approved**

    Count of demands in Submitted, Screening, Qualified, or Approved state.

-   **PPM – Total Age of Open Demand in Submitted, Screening, Qualified, Approved state**

    Total age \(in days\) of active demands in Submitted, Screening, Qualified, or Approved state. It is the difference between the creation date of the demand and the date when the indicator score is collected. The indicator is used to calculate the average age of open demands.

-   **PPM – Total Age of Demand to Project this Month**

    Total age \(in days\) of all demands that are converted to projects in the given month. It is sum of the difference between the creation date of demands and the creation date of corresponding projects. The indicator is used to calculate the average age of Demand to Project.

-   **PPM – Number of Open Ideas**

    Count of ideas in Submitted state and no Demand associated.

-   **PPM – Total Age of Open Idea**

    Total number of days an idea is in state Submitted before conversion to demand.

-   **PPM – Number of Total Ideas this Month**

    Count of ideas other than Draft state and created in the given month.

-   **PPM – Number of Ideas with Demands this Month**

    Count of ideas converted to demands in the given month.


The dashboard also uses the following formula indicators. The formula indicators are based on few of the preceding indicators.

-   **PPM – Average age open project**

    Average number of days a project is in state Pending, Open, or Work in Progress. The indicator is calculated using the **PPM – Total Age of Open Project** and **PPM – Number of Active Projects** indicators.

-   **PPM – Percentage of Ideas to Demands last 12 months**

    Percentage of ideas converted to demands in last 12 months.

-   **PPM – Average age Demand to Project last 12 months**

    Average number of days before a demand has been converted to a project.

-   **PPM – Percentage of Demand to Project last 12 months**

    Percentage of demands converted to projects in last 12 months.

-   **PPM – Average age open demand**

    Average number of days a demand is in state Submitted, Screen, Qualified, or Approved and has not been converted to project.

-   **PPM – Average age open idea**

    Average number of days an idea is in state Submitted before conversion to demand.

-   **PPM – Portfolio Health**

    Percentage of portfolio health based on active projects in overall red status, active projects that are overdue, and active projects with critical issues.


## Breakdowns

-   Business Unit
-   Demand Category
-   Demand Manager
-   Demand State
-   Demand Type
-   Department
-   Impact
-   Portfolio
-   Portfolio Manager
-   Priority
-   Program
-   Program Manager
-   T-Shirt Size
-   Execution Type
-   Investment Class
-   Investment Type
-   Project Manager
-   Project Phase
-   Project State
-   Project Status
-   Overall Health

## Data visualizations

The dashboard includes the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Benefit Plans by Category|Pie chart ![Pie chart](../../performance-analytics/image/donut-icon.png)|Breakdown of the number of benefit plans in each category for active projects.|
|Projects Planned Benefits by Category \(Monetary\)|Horizontal bar chart ![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)|Total planned financial benefits in each category for active projects.|
|Projects by Business Unit|Pie chart ![Pie chart](../../performance-analytics/image/donut-icon.png)|Breakdown of the number of active projects in each business unit.|
|Projects by Investment Type|Pie chart ![Pie chart](../../performance-analytics/image/donut-icon.png)|Breakdown of the number of active projects grouped by investment type.|
|Projects by Investment Class|Pie chart ![Pie chart](../../performance-analytics/image/donut-icon.png)|Breakdown of the number of active projects grouped by investment class.|
|Projects by Priority|Horizontal bar chart ![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)|Breakdown of the number of active projects grouped by priority.|
|Hours by Project Time Category|Line chart![Line chart](../../performance-analytics/image/line-icon.png)|Trend of total hours reported in time cards for each Project Time Category. The trend is displayed from the beginning of last quarter until the end of next quarter.|
|Active Demands|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of demands in Submitted, Screened, Qualified, and Approved state with no project associated.|
|Demands – No Manager|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no associated demand manager.|
|Demands – No Business Case|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no business case.|
|Demands – No Planned Cost|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with zero total planned cost.|
|Demands – No Start Date|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no start date.|
|Demands – No Investment Class|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no associated investment class.|
|Demands – No Budget Cost|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with zero capital and zero operating budget.|
|Demands – No Due Date|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no due date.|
|Demands – No Investment Type|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no associated investment type.|
|Demands – No Financial Benefits|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no or zero financial benefit.|
|Demands – No Portfolio|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no associated portfolio.|
|Demands – No Program|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no associated program.|
|Demands – No ROI|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active demands with no Return on Investment.|
|Active Projects|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of projects with actual end date &lt;after today&gt; or &lt;empty&gt;.|
|Projects – No Manager|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no associated project manager.|
|Projects – No Business Case|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no business case.|
|Projects – No Planned Cost|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with zero total planned cost.|
|Projects – No Task|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no associated project tasks.|
|Projects – No Investment Class|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no associated investment class.|
|Projects – No Budget Cost|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with zero budget cost.|
|Projects – No Description|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects that have no description.|
|Projects – No Investment Type|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no associated investment type.|
|Projects – No Planned Benefit|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with zero planned benefit.|
|Projects – No Portfolio|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no associated portfolio.|
|Projects – No Program|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no associated program.|
|Projects – No ROI|Single score ![Single-score](../../performance-analytics/image/single-score.png)|Number of active projects with no planned Return on Investment.|
|Planned vs Budget vs Actual Cost|Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)|Comparison of total planned, budget, and actual costs for active projects grouped by fiscal period.|
|Allocated vs Actual Hours|Step line chart![Step Line chart](../../performance-analytics/image/SteplineReportIcon.png)|Monthly trends of total allocated and actual hours for resource plans associated with active projects.|
|Monetary Planned vs Actual Benefits|Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)|Comparison of total planned and actual financial benefits for active projects grouped by fiscal period.|
|Non-monetary Planned vs Actual Benefits|Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)|Comparison of total planned and actual non-financial benefits for active projects grouped by fiscal period.|
|Monetary Planned vs Actual Benefits by Category|Bar chart ![Bar chart](../../performance-analytics/image/column-icon.png)|Comparison of total planned and actual financial benefits in each benefit plan category for active projects.|
|Project Completion Calendar|Calendar![Calender](../../performance-analytics/image/CalenderReportIcon.png)|Calender view of planned end dates of projects, project tasks, and milestones.|

**Parent Topic:**[Project Portfolio Management Platform Analytics Solutions](project-portfolio-content-pack.md)

