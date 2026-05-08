---
title: Visualizations in the Service reliability dashboard
description: List of visualizations and options on the Service reliability dashboard in Service Reliability Management \(SRM\).
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Visualizations in the Service reliability dashboard

List of visualizations and options on the Service reliability dashboard in Service Reliability Management \(SRM\).

## Service state charts

Top-level charts show the number of services in critical, at-risk, and stable states. Their states are based on the error budget remaining on their service level objectives \(SLOs\). You can select the charts to view service names, adjust the time range, and access additional chart options.

**Note:** An error budget is the amount of failure a service can experience before breaching its SLO.

Each visualization also includes a trend line showing changes in service count over the past 12 months. Smaller figures indicate how the count has changed compared to a week ago, for example, ↓25 \(22%\) since Jun 11.

|Chart|What it is|How to use it|
|-----|----------|-------------|
|Critical|Displays the number of services in a critical state. Critical services have 0% error budget remaining on their SLOs.|View how many services have consumed their error budgets and identify the services needing immediate attention.|
|At risk|Displays the number of services at risk. At-risk services have &lt;= 25% error budget remaining on their SLOs.|Monitor how many services are approaching critical thresholds and find issues early.|
|Stable|Displays the number of stable services. Stable services have more than 25% error budget remaining on their SLOs.|Get insights into overall service health and identify if services are staying reliable over time.|

## Risk trends over time

Line charts track the number of SLOs with high burn rates and low error budget remaining over the past 12 months. You can use them to find recurring patterns and potential reliability risks.

<table id="table_zzq_cmz_tfc"><thead><tr><th>

Chart

</th><th>

What it is

</th><th>

How to use it

</th></tr></thead><tbody><tr><td>

High burn rate \(&gt;=1\)

</td><td>

Shows the number of SLOs with a burn rate &gt;= 1 over time. A high burn rate indicates that the service linked to the SLO is likely to breach its error budget before the compliance period ends.For example, if a service has 30 days to meet its SLO but is using up its error budget in 15 days, the burn rate is 2.

</td><td>

-   Find risks early by seeing when services begin consuming error budgets too quickly.
-   Identify emerging or recurring reliability issues by tracking burn rates over time.
-   Point to the chart to see the number and percentage of SLOs with a high burn rate at that time.
-   Select the chart to view SLO details, adjust the time range, and access additional chart options.

</td></tr><tr><td>

Low budget remaining \(&lt;=25%\)

</td><td>

Shows the number of SLOs with low or no error budget remaining over time.

</td><td>

-   Monitor how many services are nearing or have breached their SLOs.
-   Track rising trends, which might indicate declining reliability or recurring issues that need investigation.
-   Point to the chart to see the number and percentage of SLOs with little or no error budget remaining at that time.
-   Select the chart to view SLO details, adjust the time range, and access additional chart options.

</td></tr></tbody>
</table>## Service level objectives \(SLOs\) table

The SLOs table lists the SLOs defined in Service Reliability Management \(SRM\), and it’s sorted by SLO name by default. Use the table to monitor overall reliability, identify services at risk, and find the assigned teams.

The SLO table includes the following columns by default. To customize the columns shown, select the gear icon.

-   Name - Name of the SLO. You can select the arrow to sort the table by SLO name, and you can select the name to view the SLO record.
-   Reliability - Current state of the SLO. For example, stable, at risk, or critical.
-   Measured reliability - Percentage showing the actual performance of the service. For example, if your SLO is 99.9% success, and the actual performance for the month is 99.7%, the measured reliability is 99.7%.
-   Objective \(percentage\) - Target SLO value.
-   Burn rate - Numeric value showing how quickly the service is consuming its error budget.
-   % Error budget remaining - Percentage of the error budget still available in the current compliance period.
-   Service - Name of the service associated with the SLO. You can select the service name to view the service record.
-   Assigned - Team responsible for the service.

## Dashboard filters and actions

The Service reliability dashboard is built with Platform Analytics and includes standard dashboard features. For details on customizing, duplicating, or sharing dashboards, see the Dashboards in Platform Analytics documentation.

**Note:** Changes to the Service reliability dashboard affect all SRM users on your instance. To create a personalized version, either build a new dashboard or duplicate the existing dashboard and edit it. Learn more in Create a dashboard with the in-line editor and Duplicate a Platform Analytics dashboard.

**Parent Topic:**[SLO Management reference](../../slo-management/reference/service-level-objective-management-reference.md)

