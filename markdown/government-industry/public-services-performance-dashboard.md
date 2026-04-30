---
title: Public Services Performance Overview dashboard
description: Use the Public Services Performance Overview dashboard to assess key performance indicators and data visualizations on public services offered to and requested by constituents, businesses, and agencies.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Public Services Performance Overview dashboard, Public Services Performance metrics, Assess Public Services Performance]
breadcrumb: [Analytics and Reporting, Public Sector Digital Services \(PSDS\)]
---

# Public Services Performance Overview dashboard

Use the Public Services Performance Overview dashboard to assess key performance indicators and data visualizations on public services offered to and requested by constituents, businesses, and agencies.

![Use leading metrics and KPIs to analyze and report performance. This information is displayed as percentage values, line graphs, and bar charts.](../image/public-serv-perf-overview-dashboard-new.png "Public Services Performance Overview - Overview tab")

![Benchmarking tab displaying various graphical representation of services requested and provided by service type. For the text description, refer to the Reports section.](../image/public-service-perf-dashboard-benchmarking-new.png "Public Services Performance Overview - Benchmarking tab")

## Required ServiceNow AI Platform roles

-   sn\_gsm.service\_offered\_viewer, required to view the dashboard widgets and data.
-   sn\_gsm.service\_offered\_admin, required to edit the dashboard.

## Access the Public Services Performance Overview dashboard

To open the dashboard, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards** &gt; **Public Services Performance Overview**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_ykx_kdd_htb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

Reviews benchmarking information to track the public services offered to and requested by constituents, businesses, and agencies.

</td></tr><tr><td>

Government service manager, service viewer,and owner

</td><td>

Monitors the public services offered to and requested by constituents, businesses, and agencies. Does the following:

-   Observes short and long-term trends and patterns in service delivery.
-   Identifies opportunities to improve case resolution, agent performance, and the service experience.

</td></tr></tbody>
</table>## Indicators

-   **GSM-Government Case Count for Services requested**

    Daily number of government services requested by constituents, businesses, and agencies.

-   **GSM-Average of Government Case for Services requested**

    Daily average of government cases for services requested by constituents, businesses, and agencies. The average is calculated by using this formula: \[\[GSM-Government Case Count for Services requested\]\]/30.

-   **GSM-Average resolution duration of Government Cases**

    Average number of days to resolve government cases.

-   **GSM-Average number of services provided each week by service type**

    Average count of government services requested each work, by type of service. The count is calculated by using this formula: \[\[GSM-Average days to provide services by service type\]\]/7.

-   **GSM-Average resolution duration of Government Cases in last 365 days**

    Average number of days to resolve government cases in the last 12 months.

-   **GSM-Avg number of services requested each week by service type**

    Average count of government services requested weekly by service type. The count is calculated by using this formula: \[\[GSM-Count of services requested each week by service type\]\]/7.

-   **GSM-Count of services requested each week by service type**

    Average number of government services requested each week, by service type. Measured daily.

-   **GSM-Average days to provide services by service type**

    Count of government services provided each week by type of service. Measured daily.

-   **GSM-Government Services with fastest/slowest time to resolve**

    Government services that have the quickest and slowest resolution times.


## Breakdowns

-   GSM-AssignmentGroup
-   GSM-Government.ServiceOffered.Type
-   GSM-Product
-   GSM-State

## Data visualizations

<table id="table_dlx_kdd_htb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Top 10 services requested in the last 30 days

</td><td>

![Bar graph.](../../../reuse/reporting/image/trend.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Top 10 requested services over a 30-day \(monthly\) period.

</td></tr><tr><td>

Top 10 services with most open cases in last 7 days

</td><td>

![Bar graph.](../../../reuse/reporting/image/trend.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Top 10 requested services over a seven-day \(weekly\) period.

</td></tr><tr><td>

Top 10 services requested in the last 6 months

</td><td>

![Bar graph.](../../../reuse/reporting/image/trend.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Top 10 requested services over a 6-month period.

</td></tr><tr><td>

Services requested by service type

</td><td>

![](../../../use/reporting/image/inline-data-vis-96px-pie.png)Pie chart

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Distribution \(percentage\) of government services requested by constituents, businesses, and agencies.

</td></tr><tr><td>

Public Services

</td><td>

![Single score value enclosed in a circle.](../../../reuse/reporting/image/single-score.svg)

</td><td>

Service Definition \[sn\_case\_type\_selection\]

</td><td>

Total number of all government services available in the system.

</td></tr><tr><td>

Public Services by application

</td><td>

![](../../../use/reporting/image/inline-data-vis-96px-pie.png)Pie chart

</td><td>

Service Definition \[sn\_case\_type\_selection\]

</td><td>

Distribution \(percentage\) of government services available in the system.

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting Solutions for Public Sector Digital Services](../../../use/application-content-packs/concept/psds-content-pack.md)

