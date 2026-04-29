---
title: Scan Engine Team Lead dashboard
description: The Team Lead dashboard includes trend charts and the following overview modules.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Analytics Dashboards, Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine Team Lead dashboard

The Team Lead dashboard includes trend charts and the following overview modules.

<table id="table_hrx_lll_fhc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total team technical debt

</td><td>

The amount of development time required to resolve all findings for the team.

</td></tr><tr><td>

Unapproved exceptions

</td><td>

The number of exceptions currently waiting to be approved or rejected.

</td></tr><tr><td>

Health score

</td><td>

The health score represents the percentage of definition occurrences used across the platform that did not return any findings. It is calculated as:

 `1 - (F / D) * 100`

 Where F is the number of findings, and D is the number of definition occurrences.

 "Definition occurrences" refers to the total number of times a definition has been executed by the Scan Engine to generate findings.

</td></tr><tr><td>

Active scan engine definitions

</td><td>

The number of definitions currently being used by the Scan Engine.

</td></tr><tr><td>

Technical debt by category

</td><td>

The estimated amount of development time required to resolve all findings within each category for the entire team.

</td></tr><tr><td>

Open findings by developer

</td><td>

-   All open findings sorted by each developer on the team.
-   The value in the center is the total number of open findings for all selected developers.
-   Select a name to add or remove the developer from the chart.

</td></tr></tbody>
</table>## Team Lead trend charts

The Team Lead dashboard includes the following trend charts.

<table id="table_t33_wll_fhc"><thead><tr><th>

Chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technical debt

</td><td>

-   The amount of development time required to resolve all findings for the team.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Technical debt by developer

</td><td>

-   A developer's total technical debt, represented as the estimated amount of development time required to resolve all their findings.
-   You can configure the developers displayed in this chart in the Scan Engine properties.

</td></tr><tr><td>

Policy prioritized findings

</td><td>

-   Findings that have a Priority status within a policy. To view the policy, select the name in the policy column.
-   Select **View all findings** to view the list in a separate tab.

</td></tr><tr><td>

Findings by impact to instance

</td><td>

-   Findings listed in order of highest impact to your instance with the lowest time to resolve. Address these findings first to get the highest impact with the lowest effort.
-   Select a finding number to view it in a new browser window.

</td></tr><tr><td>

Findings by developer

</td><td>

-   The number of findings by developer, classified by category.
-   Select a table entry to view the list of findings for a given developer in a new tab.

</td></tr><tr><td>

Real time preventions

</td><td>

-   All real-time preventions by the team, for the selected time period. A real-time prevention is when the Scan Engine prevents a finding from being saved.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Unapproved exceptions

</td><td>

-   All requested exceptions, by developer, requiring the team lead's approval or rejection.
-   Select the box to the left of an exception to approve or reject it
-   Select a Source record entry to view it for an exception.

</td></tr><tr><td>

Real time preventions trend

</td><td>

-   All real-time preventions by each team developer, for the selected time period. A real-time prevention is when the Scan Engine prevents a finding from being saved.
-   You can customize the time period using the date selector.

</td></tr><tr><td>

Update sets

</td><td>

-   All current update sets for the configured instance over the selected time period.
-   You can customize the time period using the date selector.
-   To filter the list, select the filter in the column heading.
-   You can add and configure instances from the **My SN Instances** related list in the Scan Engine properties.

</td></tr></tbody>
</table>## Team Lead dashboard data sources

The following tables show the data source for each overview module and trend chart in the Team Lead dashboard.

**Note:** All components require either the impact.development.team.lead or impact.app.admin role to use.

| | |
|---|---|
|Total team technical debt|sn\_se\_summary\_scan\_detail|
|Unapproved exceptions|sn\_se\_exception\_reason|
|Health score|sn\_se\_scan\_result|
|Active definitions|sn\_se\_definition|
|Tech debt by category|sn\_se\_summary\_scan\_detail|
|Open findings by developer|sn\_se\_summary\_scan\_detail|

<table id="table_gf1_jr4_nhc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Technical debt

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Technical debt by developer

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Policy prioritized findings

</td><td>

sn\_se\_finding

</td></tr><tr><td>

Findings by impact to instance

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr><tr><td>

Findings by developer

</td><td>

-   sn\_se\_summary\_scan\_detail
-   sn\_se\_finding

</td></tr><tr><td>

Real time preventions

</td><td>

sn\_se\_onsubmit\_prevention

</td></tr><tr><td>

Unapproved exceptions

</td><td>

sn\_se\_exception\_reason

</td></tr><tr><td>

Update sets

</td><td>

sn\_se\_scan\_result

</td></tr><tr><td>

Real time preventions trend

</td><td>

sn\_se\_summary\_scan\_detail

</td></tr></tbody>
</table>**Note:** The Team Lead dashboard charts only include data for members underneath the defined team lead.

