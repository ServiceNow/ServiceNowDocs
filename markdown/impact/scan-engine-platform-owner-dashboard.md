---
title: Scan Engine Platform Owner dashboard
description: The Platform Owner dashboard includes trend charts and the following overview modules.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Analytics Dashboards, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine Platform Owner dashboard

The Platform Owner dashboard includes trend charts and the following overview modules.

<table id="table_lyk_4jl_fhc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outstanding findings

</td><td>

The number of unresolved findings identified by the Scan Engine that have not been addressed.

</td></tr><tr><td>

Health score

</td><td>

The health score represents the percentage of definition occurrences used across the platform that did not return any findings. It is calculated as:

 `1 - (F / D) * 100`

 -   F: The number of findings
-   D: The number of definition occurrences which is the total number of times a definition has been executed by the Scan Engine to generate findings.

</td></tr><tr><td>

Lines of code scanned

</td><td>

The total number of lines of code analyzed by the Scan Engine, including all script field code and any scanned base system records.

</td></tr><tr><td>

In progress update sets

</td><td>

The number of unfinished update sets currently being worked on by developers.

</td></tr><tr><td>

Findings by impact to instance

</td><td>

-   The total findings for the instance, grouped by impact to instance.
-   Impacts to instance range from 1 \(minor impact\) to 10 \(significant impact\). You can select a bar on the chart to list the findings for that impact to the instance in a new browser tab.

</td></tr><tr><td>

Open findings by team

</td><td>

All available teams configured on the instance through the **Team Leads** related list on the **Scan Engine Properties** page. You can select a team from the list to show their corresponding information in the module and trend charts. **Note:** The number next to the team name is the number of open findings held by that team.

</td></tr></tbody>
</table>## Platform Owner trend charts

The Platform Owner dashboard includes the following trend charts.

<table id="table_ugg_2kl_fhc"><thead><tr><th>

Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technical debt

</td><td>

-   The amount of development time required to resolve all findings.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Technical debt by team

</td><td>

-   A team's total technical debt, represented as the estimated amount of development time required to resolve all team findings.
-   You can configure the teams displayed on this chart in the Scan Engine properties.

</td></tr><tr><td>

Findings by team

</td><td>

-   The number of findings by team, classified by state and category.
-   Select a number to see the list of findings for that team in a new browser tab.

</td></tr><tr><td>

Findings by impact to instance

</td><td>

-   Findings listed in order of highest impact to your instance with the lowest time to resolve. Address these findings first to achieve the highest impact with the lowest effort.
-   Select any finding number to view its details in a new browser window.

</td></tr><tr><td>

Real time preventions

</td><td>

-   The findings that were corrected during development for each team.
-   The default time span for these preventions is 30 days. You can customize time spans using the date selector.

</td></tr><tr><td>

Real time preventions trend

</td><td>

-   All real-time preventions by a team during the selected time period. A real-time prevention is when the Scan Engine prevents a finding from being saved.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Findings by file type

</td><td>

-   A heatmap of findings by file type. Lets you quickly identify development areas that need the most attention.
-   Select a number in a cell to see the full list of violations for that file type/category.

</td></tr><tr><td>

Update sets

</td><td>

-   A list of update sets on all configured instances for the selected time period.
-   You can customize the time period using the date selector.
-   You can add and configure instances in the **My SN Instances** related list in the Scan Engine properties.

</td></tr><tr><td>

Exception reasons

</td><td>

The number of exception approval requests by status for each team.

</td></tr><tr><td>

Findings by suite

</td><td>

-   The number of findings by category, classified by suite.
-   Lets you identify findings within top-level suites and engage the relevant process owners.
-   Select a table entry to view the list of findings for that category in a new browser tab.

</td></tr></tbody>
</table>## Platform Owner dashboard data sources

The following tables show the data source for each module and trend chart in the Platform Owner dashboard.

**Note:** All components require either the impact.admin or impact.platform.owner role to use.

|Component|Data Source|
|---------|-----------|
|Outstanding findings|sn\_se\_scan\_result|
|Health score|sn\_se\_scan\_result|
|Lines of code scanned|sn\_se\_scan\_result|
|In progress update sets|sn\_se\_scan\_result|
|Findings by impact to instance|sn\_se\_summary\_scan\_detail|
|Open findings by team|sn\_se\_summary\_scan\_detail|

<table id="table_m2g_s44_nhc"><thead><tr><th>

Component

</th><th>

Data Source

</th></tr></thead><tbody><tr><td>

Technical debt

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Technical debt by team

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Findings by team

</td><td>

-   sn\_se\_summary\_scan\_detail
-   sn\_se\_summary\_resolved\_detail
-   sn\_se\_findings

</td></tr><tr><td>

Findings by impact to instance

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Real time preventions

</td><td>

sn\_se\_onsubmit\_prevention

</td></tr><tr><td>

Real time preventions trend

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Findings by file type

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Update sets

</td><td>

-   sn\_se\_scan\_result
-   sn\_se\_my\_sn\_instances

</td></tr><tr><td>

Exception reasons

</td><td>

sn\_se\_exception\_reason

</td></tr><tr><td>

Findings by suite

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr></tbody>
</table>