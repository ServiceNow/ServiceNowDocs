---
title: Constituent Service dashboard
description: Use this dashboard to monitor the health of citizen services, gain insights on how efficiently government cases are handled, and assess the overall performance of services offered.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Analytics and Reporting, Public Sector Digital Services \(PSDS\)]
---

# Constituent Service dashboard

Use this dashboard to monitor the health of citizen services, gain insights on how efficiently government cases are handled, and assess the overall performance of services offered.

![Constituent Services Overview tab that displays indicators and reports for constituent cases represented by various graphs and tiles.](../../../product/public-sector/image/constituent-service-overview-dboard-new.png "Constituent Service Dashboard Overview tab")

![Constituent Services Performance tab that displays KPIs and reports on open and closed cases represented by line and bar graphs.](../../../product/public-sector/image/constituent-service-dboard-performance-new.png "Constituent Service Dashboard Performance tab")

## Required ServiceNow AI Platform roles

-   sn\_gsm.constituent\_agent, required to view the dashboard widgets and data.
-   sn\_gsm.constituent\_admin, required to edit the dashboard.

## Access the Constituent Service dashboard

To open the dashboard, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_twv_3vr_gtb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Admin or agent

</td><td>

Creates and monitors cases from constituents to accelerate case resolution and increase customer satisfaction. Does the following:

-   Tracks cases that have been open for a period of time.
-   Monitors the number of cases for a certain type of service type.
-   Reviews the average closing time of cases for each service type.
-   Drills down into details of cases for specific service types.

</td></tr><tr><td>

Government service manager

</td><td>

Monitors the health of government services. Tracks case resolution to drive improvements in service delivery processes and agent performance.

</td></tr></tbody>
</table>## Indicators

-   **Average response time for cases**

    Average hours for agents to respond to a new government case. This score is calculated by using this formula: \[\[GSM-Summed duration of FirstResponseTime\]\] / \[\[GSM-Number of Responded Cases\]\]

-   **GSM-Number of Open Cases**

    Number of open cases created daily.

-   **GSM-CSAT**

    Customer satisfaction score based on survey results. The score is calculated by using this formula: \[\[GSM\_Number of satisfied customers \(CSAT\)\]\]/\[\[GSM\_Number of CSAT survey respondents\]\]\*100.

-   **GSM-Average close time of cases**

    Average number of days to close cases. This score is calculated by using this formula: \[\[GSM-Summed duration of closed cases\]\] / \[\[GSM-Number of closed cases\]\] / 24.

-   **GSM-Average age of open cases**

    Average number of days that cases remain open. The score is calculated by using this formula: \[\[GSM-Summed age of open cases\]\] / \[\[GSM-Number of Open Cases\]\] / 24.

-   **Average resolution time of cases**

    Average number of days to resolve cases. The score is calculated using this formula: \[\[GSM\_Summed duration of resolved cases\]\] / \[\[GSM\_Number of resolved cases\]\] / 24

-   **GSM-Case Average Response Time**

    Average length of time for an agent to respond to a case. The score is calculated using this formula: \[\[GSM-Summed duration of FirstResponseTime\]\]/\[\[GSM-Number of Responded Cases\]\].

-   **GSM\_Number of resolved cases**

    Daily count of government cases resolved. The goal for this indicator is to maximize the count.

-   **GSM-Number of closed cases**

    Daily count of closed cases.

-   **GSM-Number of Responded Cases**

    Daily count of cases to which agents responded.


The following indicators are not shown directly on the dashboard but are used in calculating formulas:

-   GSM-Summed duration of closed cases \(hours\)
-   GSM-Summed duration of FirstResponseTime \(hours\)
-   GSM-Summed age of open cases
-   GSM-Summed duration of resolved cases \(hours\)

## Breakdowns

-   GSM-Account
-   GSM-Age
-   GSM-AssignedTo
-   GSM-AssignmentGroup
-   GSM-Category
-   GSM-Channel
-   GSM-Contact
-   GSM-Priority
-   GSM-Product
-   GSM-State

## Data visualizations

<table id="table_ywv_3vr_gtb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open cases older than 30 days by stage and state

</td><td>

Pivot![](../../../product/public-sector/image/pivot.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Detailed summary of open cases older than one month, arranged by stage and state.

</td></tr><tr><td>

Open cases

</td><td>

Score![](../../../reuse/reporting/image/single-score.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Total number of unresolved government cases in the system.

</td></tr><tr><td>

Cases opened per week

</td><td>

Line![](../../../reuse/reporting/image/line-trend.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Weekly trend of new government cases opened.

</td></tr><tr><td>

Open cases older than 30 days

</td><td>

Horizontal bar

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Distribution of government open cases older than 30 days.

</td></tr><tr><td>

Unassigned cases

</td><td>

Score![](../../../reuse/reporting/image/single-score.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Total number of government cases not yet assigned to agents.

</td></tr><tr><td>

Cases by case type

</td><td>

Pie

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Percentage of government cases by case type.

</td></tr><tr><td>

Open cases by stage and state

</td><td>

Pivot![](../../../product/public-sector/image/pivot.svg)

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Detailed summary of open government cases, arranged by stage and state.

</td></tr><tr><td>

Cases closed per week

</td><td>

Line![](../../../reuse/reporting/image/line-trend.svg)Line

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Weekly trend in government cases closed by agents.

</td></tr><tr><td>

Open Cases by Priority

</td><td>

Horizontal bar

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td><td>

Distribution of unassigned government cases by priority.

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting Solutions for Public Sector Digital Services](../../application-content-packs/concept/psds-content-pack.md)

