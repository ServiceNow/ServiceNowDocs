---
title: Employee Relations Executive Overview dashboard
description: The Employee Relations Executive Overview dashboard provides you with high level data on Employee Relations cases and detailed information on the types of ER cases, locations, cases by HR service and department, and trends.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Analytics and Reporting Solutions for Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Employee Relations Executive Overview dashboard

The Employee Relations Executive Overview dashboard provides you with high level data on Employee Relations cases and detailed information on the types of ER cases, locations, cases by HR service and department, and trends.

![Employee Relations Executive Overview](../../../product/human-resources/image/hr-er-pa-dashboard.png)

## Required ServiceNow AI Platform roles

**sn\_hr\_er.case\_reader**

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_ov2_tj4_2fb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Employee Relations employee or HR leadership

</td><td>

The dashboard provides:-   A high-level overview of the current ER case volume, status, and distribution.
-   An understanding of the top ER case types and issues by different employee populations.
-   Identification of hot spots early so they can be resolved quickly.
-   An analysis of trends and changes that can inform process improvements and ER strategy.

</td></tr></tbody>
</table>## Indicators

-   **ERCases.CorrectiveActions**

    Shows corrective actions taken for closed cases.

-   **ERCases.AllegationTypes**

    Shows data for each allegation type on open ER cases.

-   **ERCases.Restricted**

    The number of restricted ER cases.

-   **ERCases.NewThisWeek**

    The number of ER cases created this week.

-   **ERCases.Open**

    The total number of open ER cases.

-   **ERCases.PastSLA**

    The number or ER cases that have past the Service Level Agreement \(SLA\).


## Breakdowns

-   ERCases.AllegationTypes
-   ERCases.CorrectiveActionTypes
-   ERCases.HRService
-   ERCases.Priority
-   ERCases.State

## Reports

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open cases

</td><td>

Real-time Score

</td><td>

Employee Realtions Case \[sn\_hr\_er\_case\] table

</td><td>

The total number of open ER cases.

</td></tr><tr><td>

Open cases past SLA

</td><td>

Latest Score

</td><td>

 

</td><td>

The number of open ER cases that have passed the Service Level Agreement \(SLA\)

</td></tr><tr><td>

New cases this week

</td><td>

Real-time Score

</td><td>

 

</td><td>

The number of new ER cases for the current week.

</td></tr><tr><td>

Restricted cases

</td><td>

Real-time Score

</td><td>

 

</td><td>

The number of ER cases that are classified as restricted. For more information, see [HR Service Delivery Employee Relations case restrictions](../../../product/human-resources/concept/hr-er-case-restriction.md).

</td></tr><tr><td>

Open cases by location

</td><td>

Map

</td><td>

Employee Realtions Case \[sn\_hr\_er\_case\] table

</td><td>

Provides the number of open ER cases by geographical location. This data can help you recognize trends or you can use it for data comparisons.The location represents the location of the Opened for users at the time the case was opened.

</td></tr><tr><td>

Open cases by HR service

</td><td>

Scorecard

</td><td>

 

</td><td>

Shows the number of open ER cases by date for each HR service \(with link\) and a trending graph.

</td></tr><tr><td>

Open cases by department

</td><td>

Column \(default\)

</td><td>

 

</td><td>

Shows the number of ER cases for each department within your company.

</td></tr><tr><td>

Allegation types for open cases

</td><td>

Column \(default\)

</td><td>

 

</td><td>

The number of open ER cases for each allegation type.

</td></tr><tr><td>

Allegation types trend

</td><td>

Line Chart

</td><td>

 

</td><td>

Provides the number of ER cases by allegation type by date. It also shows a trend line that indicates if cases are going up, down, or staying neutral.

</td></tr><tr><td>

Outcomes of allegations for closed cases

</td><td>

Line Chart

</td><td>

 

</td><td>

Shows the number and corrective actions associated with a closed ER cases by allegation.

</td></tr></tbody>
</table>