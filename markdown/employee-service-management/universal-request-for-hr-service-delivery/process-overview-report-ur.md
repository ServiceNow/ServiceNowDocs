---
title: Universal Request Process Overview dashboard
description: Analyze the behavior of universal requests in your organization and track transfers. As a process owner, use this dashboard to measure efficiency and to determine necessary improvements in the overall implementation of Universal Request.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reporting solutions for Universal Request, Universal Request, Employee Service Management]
---

# Universal Request Process Overview dashboard

Analyze the behavior of universal requests in your organization and track transfers. As a process owner, use this dashboard to measure efficiency and to determine necessary improvements in the overall implementation of Universal Request.

To view the Universal Request Process Overview dashboard, navigate to **Universal Request** &gt; **Process Overview**. The reports are based on closed universal requests. You can select the time period for the reports using the date filter. Click and open each indicator for more details.

You can view the dashboard in the Next Experience UI Framework. Select any indicator widget to view it's details in a list view.

Use the **Edit** button to modify the dashboard and the widgets with the in-line editor. For more information, see [Edit Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

![Universal Request Reporting Process overview tab.](../image/ur-process-overview.png "Process Overview tab")

The **SLA Trends** tab displays dynamic Performance Analytics reports for Universal Request. To view this tab, activate the Performance Analytics and Reporting for Universal Request plugin \(com.snc.universal\_request.pa\). The **SLA trends** tab displays reports based on closed universal requests. By default, the monthly data is displayed. To collect daily data for this tab, run the **\[PA Universal Request\] Daily Data Collection** job. To collect data for the past three months, run the **\[PA Universal Request\] Historical Data Collection** job.

![SLA Trends tab in the Universal Request Process overview.](../image/ur-process-ovrv-sla-trends.png "Process Overview SLA Trends tab")

## Required ServiceNow AI Platform roles

The following roles can view the Universal Request Process overview dashboard:

-   Admin
-   UR Admin \[sn\_uni\_req.ur\_admin\]
-   Service owner \[sn\_uni\_req.ur\_service\_owner\]

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|admin, sn\_uni\_req.ur\_admin|View and edit the dashboard. Manage users, groups, and roles of the dashboard.|
|sn\_uni\_req.ur\_service\_owner|View and analyze the UR behaviors and track transfers to make informed decisions about your service.|

## Indicators

All the following indicators are measured on a monthly basis.

-   **Universal Request Response SLA Breaches**

    The number of breaches in Universal Request Response SLA.

-   **Universal Request Response SLA Average**

    The average value for Business elapsed time \(in minutes\) of response SLAs for Universal Request.

-   **Universal Request Resolution SLA Average**

    The average value for Business elapsed time \(in minutes\) of resolution SLAs for Universal Request.

-   **Universal Request Resolution OLA Breaches**

    The number of breaches in Universal Request Resolution OLA.

-   **Universal Request with Primary Ticket Resolution SLA Average**

    The average value for Business elapsed time \(in minutes\) of resolution SLAs for Universal Requests with a primary ticket.

-   **Universal Request Primary Ticket Transfer Without Resolution**

    The number of Universal Request primary tickets that are transferred without resolution.

-   **Universal Request Primary Ticket SLA Breaches**

    The number of SLA breaches in primary tickets which have an associated universal request.

-   **% of breached Resolution SLAs of Universal Request with primary ticket**

    The result of the formula `([[Universal Request with primary ticket Resolution SLA Breaches]] / [[Universal Request with primary ticket Resolution SLA]]) * 100`.


The following indicators are used only to calculate formulas and are not shown directly on the dashboard:

-   Universal Request with primary ticket Resolution SLA Breaches
-   Universal Request with primary ticket Resolution SLA

## Breakdowns

The breakdowns in the Universal Request Process Overview dashboard are as follows:

-   UR Service Configurations
-   UR Assignment groups
-   Universal Request \(Inactive\)

## Data visualizations

The visualizations in the **SLA trends** tab are based on closed universal requests per month.

<table id="table_n5c_d4t_mpb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment Group Changes by Group

</td><td>

Bar

</td><td>

universal\_request\_instrumentation

</td><td>

The number of times the UR is moved between the UR assignment group.

</td></tr><tr><td>

Resolution Time Consumed by Group

</td><td>

Bar

</td><td>

sla\_breakdown\_by\_primary\_ticket\_and\_group

</td><td>

The total resolution time consumed by universal requests spread across different assignment groups, such as IT, UR, or HR routing group. Resolution time is the total time consumed by the UR from the creation to closure.

</td></tr><tr><td>

Sources

</td><td>

Donut

</td><td>

universal\_request\_instrumentation

</td><td>

The percentage of universal requests created from various sources, such as interaction, UR record producers, virtual agent, or email interactions.

</td></tr><tr><td>

Resolution Time Consumed by Service

</td><td>

Bar

</td><td>

sn\_uni\_req\_sla\_breakdown\_primary\_task\_service

</td><td>

The total resolution time consumed by each department on the primary ticket. Resolution time is the total time consumed by the primary ticket from its creation to closure.

</td></tr><tr><td>

Triage Time Consumed by Group

</td><td>

Bar

</td><td>

sla\_breakdown\_by\_primary\_ticket\_and\_group

</td><td>

The total triage time consumed by different assignment groups on the UR. Triage time is the time consumed by the ticket in the UR assignment group queue before the department ticket is created. The triage time pauses when the department ticket is created.

</td></tr><tr><td>

Transfer Disposition

</td><td>

Donut

</td><td>

universal\_request\_instrumentation

</td><td>

The disposition selected by the routing agents while transferring the tickets back to the UR. The statuses captured are the percentages of tickets that are either of the following:-   Transferred with resolution
-   Transferred without resolution

</td></tr><tr><td>

Sensitive Universal Requests

</td><td>

Pie

</td><td>

universal\_request\_instrumentation

</td><td>

The number of tickets restricted by the employees and agents.

</td></tr><tr><td>

Transfers with Sensitive Comments/Attachments

</td><td>

Donut

</td><td>

universal\_request\_instrumentation

</td><td>

The percentage of universal requests that were transferred with sensitive information.

</td></tr></tbody>
</table>## Filter

The date filter is available for the **Overview** tab.

|Name|Type|Description|
|----|----|-----------|
|Date|Choice|The time period for the data that will be filtered.|

**Parent Topic:**[Reporting solutions for Universal Request](../../../product/universal-request/concept/reporting-soln-for-ur.md)

