---
title: Legacy- Tracking view in portfolio workbench
description: Once the financial planning is complete, the Track Portfolio option in portfolio workbench is enabled. You can track the progress of demands and projects, and monitor the status of cost, resource, schedule, and scope for the selected fiscal period for the portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/track-view-portfolio-workbench.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Legacy- Track the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Tracking view in portfolio workbench

Once the financial planning is complete, the **Track Portfolio** option in portfolio workbench is enabled. You can track the progress of demands and projects, and monitor the status of cost, resource, schedule, and scope for the selected fiscal period for the portfolio.

**Note:** The content in this topic is applicable for customers upgrading from a previous release to Brazil. If you are a new customer, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

The portfolio workbench comprises the following components in tracking view:

**Timeline View**: The tab displays a list of the selected demands and projects that are part of the portfolio, and a Gantt chart over time.

On the Timeline View tab, you can:

-   configure the colors of the portfolio items in the Gantt chart with [Dashboard Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_AccessThePortfolioWorkbench.md) settings.
-   select the zoom level in the Gantt chart calender to **Auto Fit**. The Gantt view fits in one page to view entire timeline without using the scrollbar.
-   [review the external dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/review-external-dependencies-between-projects.md) between projects in a portfolio.

**Note:** The admin can [customize](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/custom-columns-planning-console.md) which columns appear in the column filter list \(\[Omitted image "filter\_icon.png"\] Alt text: screenshot for filter icon\) in the timeline view.

**Project KPI**: The tab displays the most recent status of project KPIs such as overall health, schedule, cost, resources, and scope of all the selected projects in the portfolio. This information is populated from the most recent [status report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/t_CreateAProjectStatusReport.md) created for the projects.

You can:

-   click the name of a project on the tab to open the latest status report created for the project.
-   point to a status indicator for a project KPI to view the comments entered for the KPI for that project.

**Cost \(Planned vs. Actual\)**: The chart displays the actual costs from all selected projects in the portfolio compared to the planned cost. The actual cost for projects is derived from the [expense lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/t_CreateAExpenseLine.md).

**Note:** An expense line can be created manually for a project when a specific expense is incurred. For example, if hardware is procured for a project, an expense line can be created for the amount spent on procuring the hardware. If you receive an item using ServiceNow Procurement, an expense line is created automatically. For resource hours, the expense lines are created automatically when the time cards for the project are approved.

The display settings for the chart can be modified by selecting any of the following from the choice list:

-   **Capex**: Displays the cost chart for capital expense only.
-   **Opex**: Displays the cost chart for operating expense only.
-   **All**: Displays the cost chart for both capital and operating expenses.

**Resource \(Allocated vs. Actual\)**: The chart displays the actual resource time spent on all project tasks versus the resource hours allocated to execute the selected projects and demands in the portfolio. The actual time spent is taken from processed time cards for the projects.

**Risks**, **Issues**, and **Changes**: The tabs provide the following information:

-   **Risks**: Displays risks concerning all the selected demands and projects in portfolio and their probability. This information is populated from the risks that are part of demands and projects associated with the portfolio.
-   **Issues**: Displays all issues across all selected projects in the portfolio and their priority. This information is populated from the issues that are reported for the projects in a portfolio.
-   **Changes**: Displays all [project change requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/create-project-change-request.md) across all selected projects in the portfolio and their priority. This information is populated from the change requests created for the projects in a portfolio.

\[Omitted image "PortfolioTrackingExample1.png"\] Alt text: The timeline tracking view in portfolio workbench

\[Omitted image "PortfolioTrackingExample2.png"\] Alt text: The project KPI tracking view in portfolio workbench

**Parent Topic:**[Legacy- Track the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_ReviewFinancialPlanning.md)

