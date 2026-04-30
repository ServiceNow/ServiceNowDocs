---
title: Working with the Enterprise Architecture Workspace dashboard
description: The Enterprise Architecture Workspace dashboard provides a summary of the business and application portfolio of your organization. It’s arranged according to different portfolios such as the application portfolio, technology portfolio, information portfolio, and so on.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Working with the Enterprise Architecture Workspace dashboard

The Enterprise Architecture Workspace dashboard provides a summary of the business and application portfolio of your organization. It’s arranged according to different portfolios such as the application portfolio, technology portfolio, information portfolio, and so on.

As an enterprise architect, use the interactive filters to generate different graphical reports of the business applications for your portfolios. You can select a pie chart slice or graph bar to open a particular page and see the list of records under that category. To hide or show a slice in the pie chart, select its colored legend. Use the **Refresh** button to refresh the results of a pie chart.

|End user and goal|Required role|
|-----------------|-------------|
|Enterprise Architecture Analyst- Create, configure, and share dashboards|sn\_apm.apm\_analyst|
|Enterprise Architecture User- View dashboard|sn\_apm.apm\_user|

![The Enterprise Architecture Dashboard page displaying the multiple tabs and their respective widgets.](../../../product/application-portfolio-management/image/eaw-image/eaw-tabbed-dashboard-washington.gif "Enterprise Architecture Dashboard page")

## Data visualizations

The dashboards include the following visualizations.

<table id="table_m51_b3v_vzb"><thead><tr><th>

Tab name

</th><th>

Visualization title

</th><th>

Visualization type

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="9">

Application Portfolio

</td><td>

Business applications by platform

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their platform type, such as UNIX and AWS.

</td></tr><tr><td>

Business application by install type

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their installation type, such as On premise, Cloud, Third-party hosted, and so on.

</td></tr><tr><td>

Business application by application family

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their application family, such as Workday, Microsoft Office, ServiceNow HR.

</td></tr><tr><td>

Business application by user base

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the business applications by the number of users using the applications.

</td></tr><tr><td>

Business applications by technology stack

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their technology, such as Java, Net, SQL.

</td></tr><tr><td>

Business applications by application category

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications and their categories, such as Finance, Sourcing, Procurement.

</td></tr><tr><td>

Business application by lifecycle stage

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their lifecycle stage.

</td></tr><tr><td>

Business application by lifecycle stage status

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their lifecycle stage status.

</td></tr><tr><td>

Digital interfaces by business applications

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of digital interfaces categorized by their provider business application. This pie chart is displayed only when the Enterprise Architecture Digital Integration Management plugin is installed.

</td></tr><tr><td>

Business Portfolio

</td><td>

Business capabilities with low scores

</td><td>

Bar graph ![Column chart.](../../reporting/image/inline-data-vis-bar-column.png)

</td><td>

Breakdown of the number of low-scoring capabilities of the organization.

</td></tr><tr><td rowspan="4">

Technology Portfolio**Note:**

If both the Technology Portfolio Management \(sn\_apm\_tpm\) and Enterprise Architecture - TRM \(snc.apm\_trm\) plugins are inactive, the Technology Portfolio tab is not displayed.

</td><td>

TRM products by TRM phase

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of Technology Reference Model \(TRM\) products categorized by their TRM phase.

</td></tr><tr><td>

Approved software counts by TRM category

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the software products categorized by their approved TRM phase.

</td></tr><tr><td>

Top 10 business applications with highest TRM technical debt

</td><td>

Bar graph ![Column chart.](../../reporting/image/inline-data-vis-bar-column.png)

</td><td>

The top 10 business applications having the highest TRM technical debt.

</td></tr><tr><td>

Top 10 business applications with normalized TPM risk

</td><td>

Column chart ![Column chart.](../../reporting/image/inline-data-vis-bar-column.png)

</td><td>

The top 10 business applications having normalized Technology Portfolio Management \(TPM\) risk.

</td></tr><tr><td rowspan="2">

Information Portfolio

</td><td>

Business applications by data classification

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of business applications categorized by their data classification type, such as Internal, Confidential, Highly sensitive, Public.

</td></tr><tr><td>

Information objects by data domain

</td><td>

Pie chart ![Pie chart.](../../reporting/image/inline-data-vis-pie.png)

</td><td>

Breakdown of the number of information objects categorized by their data domain, such as Personally identifiable information \(PII\), Employees data, Payment card information \(PCI\).

</td></tr><tr><td rowspan="8">

Portfolio TCO**Note:**

-   All monetary values are displayed in a single currency type. The currency conversion rates are contained in the Currencies table \(fx\_currency.list\).

The currency type is determined based on the geographical location from where you’ve logged in. For example, if the system detects that you’ve logged in to the EA workspace from the USA, the default currency displayed will be USD.

-   The duration of a fiscal period displayed on the widgets is determined from the **com.glide.fiscal\_calendar.fiscal.unit** property. To set the fiscal period duration, see [Set the duration of a fiscal period property for TCO dashboards](../../../product/application-portfolio-management/task/eaw-task/eaw-set-property-tco-dashboards.md).
-   For information on TCO, see [Manage application total cost of ownership \(TCO\)](../../../product/application-portfolio-management/concept/eaw-concept/eaw-manage-application-tco.md).

</td><td>

Business application TCO for FY:Q \(Current quarter\)

</td><td>

Summary ![Summary.](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

The total cost of ownership value for all business applications, calculated for the current fiscal quarter.

</td></tr><tr><td>

Business application TCO for FY:Q \(Previous quarter\)

</td><td>

Summary ![Summary.](../../reporting/image/inline-data-vis-single-score.png)

</td><td>

The total cost of ownership value for all business applications, calculated for the previous quarter.

</td></tr><tr><td>

Business application TCO trend for year

</td><td>

Line graph ![Line graph.](../../reporting/image/inline-data-vis-line.png)

</td><td>

The value of the total cost of ownership of business applications over a year.

</td></tr><tr><td>

Business application TCO by application category

</td><td>

Column chart ![Column chart.](../../reporting/image/inline-data-vis-bar-column.png)

</td><td>

Breakdown of the total cost of ownership values of business applications grouped by their category, such as IT Service Management, IT portfolio management, Human capital management.The chart compares the total cost of ownership for the current and previous quarter, side by side.

</td></tr><tr><td>

Business application TCO by application planned disposition for FY:Q \(Current quarter\)

</td><td>

Horizontal bar graph ![Horizontal bar graph.](../../reporting/image/inline-data-vis-bar-horizontal.png)

</td><td>

Breakdown of the total cost of ownership values of business applications categorized by their planned disposition status, for the current quarter.

</td></tr><tr><td>

Business applications by TCO score

</td><td>

Column chart ![Column chart.](../../reporting/image/inline-data-vis-bar-column.png)

</td><td>

Breakdown of the number of business applications categorized by their TCO score. The chart compares the total cost of ownership for the current and previous quarter, side by side.Business application TCO scores from 0 to 1 and 9 to10 are inclusive. That is, any number from 0 \(starting point\) until 1 \(ending point\) or from 9 \(starting point\) until 10 \(ending point\) are part of the range. For example, an inclusive number range from 9 to 10 includes the numbers 9.1, 9.2, 9.3, 9.4, 9.5, 9.6, 9.7, 9.8, 9.9, 10.

Business application TCO scores from 1 to 9 are exclusive. That is it includes all numbers in the range up to but doesn’t include the ending point. For example, an exclusive number range from 1 \(starting point\) to 2 \(ending point\) includes the number 1.1, 1.2, 1.3, 1.4, 1.5, 1.6, 1.7, 1.8, 1.9.

The X-axis denotes the TCO scores while the Y-axis denotes the number of business applications.

</td></tr><tr><td>

Business application TCO by cost type and planned disposition for FY:Q \(Current quarter\)

</td><td>

Heat map![Heat map.](../../reporting/image/inline-data-vis-heatmap.png)

</td><td>

Breakdown of the total cost of ownership values associated with different application cost types in comparison to their application planned disposition state. On selecting any value on the heat map that is greater than zero, a list of business applications is displayed that are associated with that specific combination of cost type and planned disposition value. You can add your own cost types to measure application TCO. For details, see [Create a cost type for Application TCO in Enterprise Architecture Workspace](../../../product/application-portfolio-management/task/eaw-task/eaw-create-tco-cost-type.md).

</td></tr><tr><td>

Top 10 business applications with the highest cost for FY:Q \(Current quarter\)

</td><td>

List![List.](../../reporting/image/inline-data-vis-list.png)

</td><td>

A list of all business applications having the highest total cost of ownership values for the current quarter and the previous quarter. On selecting a total cost of ownership value, further details on that business application cost are displayed.

</td></tr></tbody>
</table>You can hover over or select the visualizations to see more data.

Use the following filters to narrow down the results in the dashboard page:

-   Application Category
-   Install Type
-   Application Type
-   Business Unit
-   Business Owner
-   IT Application Owner
-   Capability Owner

You can manually refresh the dashboard by using the refresh icon \(![Refresh icon.](../../../product/application-portfolio-management/image/icon-refresh.png)\).

-   **[Working with the Application Assessments dashboard](eaw-working-with-the-applications-assessment-dashboard.md)**  
The Application Assessments dashboard is a responsive dashboard that provides a complete view of applications.
-   **[Working with the Application 360 dashboard in Enterprise Architecture Workspace](eaw-working-with-application-360-dashboard-in-enterprise-architecture-workspace.md)**  
The Application 360 dashboard performs as a reporting tool and uses Performance Analytics to provide a decision-making approach by identifying which business application requires focus and attention.

**Parent Topic:**[Enterprise Architecture Workspace](../../../product/application-portfolio-management/concept/ea-workspace.md)

