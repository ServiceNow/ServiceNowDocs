---
title: Deprecated Benchmarks dashboard
description: The Benchmarks dashboard shows KPI data, performance trends, and indicator scorecards.
locale: en-US
release: australia
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Benchmarks, IT Service Management]
---

# Deprecated Benchmarks dashboard

The Benchmarks dashboard shows KPI data, performance trends, and indicator scorecards.

**Note:** For information about the new Benchmarks dashboard, see [New Benchmarks Dashboard](c_NewuiDashboard.md).

The Benchmarks KPI dashboard view displays all the KPIs and can be accessed through Service Portal.

Features include:

-   Ability to show KPIs in either list or card view.
-   Downloadable reports of KPI list and all charts in PDF format.
-   Ability to filter data by type of industry, number of users, MSPs, or geographic region \(the filter is retained when switching between KPI view and trend view\).

    **Note:** Only Managed Service Providers \(MSP\) can view the global MSP aggregate score data.

-   Color-coded KPI data \(the favorable comparison results for your instance are in green, while red favors global data\).
-   Monthly change percentage calculation of your instance from the previous month.
-   Ability to view six months of historical KPI data.
-   Ability to display time values in hours or days \(using the **sn\_bm\_client.dashboard\_display\_unit** system property\).

**Note:** Service Portal must be installed to view the Benchmarks dashboard.

![Benchmarks Dashboard](../image/BenchmarksDashboard.png)

## Percentile rank

The exact standing of the KPI for your company within your participating peer group is indicated by percentile rank. A KPI percentile rank of 90% indicates that your instance outperforms 90% of the instances participating in that KPI group.

**Note:** A high percentile rank does not always indicate a desirable result.

For certain KPIs a higher ranking is preferred \(% of incidents resolved using KB articles\), but for others it is not \(% of emergency changes\). The meaning of your percentile ranking should be interpreted based on the direction of the KPI being analyzed.

<table id="table_och_ydn_gbb"><thead><tr><th rowspan="2">

KPI

</th><th colspan="2" align="center">

Direction\(Percentile rank goal\)

</th></tr><tr><th align="center">

Minimize

</th><th align="center">

Maximize

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3" align="left">

Incident

</td></tr><tr><td>

% of high priority incidents resolved

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% of incidents resolved on first assignment

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

% of incidents resolved within SLA

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

% of reopened incidents

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Average time to resolve a high priority incident

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Average time to resolve an incident

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Number of incidents created per user

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Problem

</td></tr><tr><td>

% of high priority problems

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% of incidents resolved by problem

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

Average time to close a problem

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Change

</td></tr><tr><td>

% of emergency changes

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% of failed changes

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Average time to close a change

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Service Catalog

</td></tr><tr><td>

% of closed requests with breached SLAs

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Average time to fulfill a request

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Number of requests created per user

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Knowledge

</td></tr><tr><td>

% of incidents resolved using KB articles

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

Number of knowledge article views per user

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

ITSM Virtual Agent

</td></tr><tr><td>

% call deflection

</td><td>

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

% of incidents auto-resolved

</td><td>

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Other

</td></tr><tr><td>

Average customer satisfaction

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

Number of requesters per fulfiller

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

CMDB

</td></tr><tr><td>

% of duplicate CIs

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% of non-compliant CIs

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% of stale CIs

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Security Incident Response

</td></tr><tr><td>

% of critical and high priority security incidents

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Vulnerability Response

</td></tr><tr><td>

Average critical vulnerability age

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Average vulnerability age

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td align="center">

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Virtual Agent

</td></tr><tr><td>

% of users using Virtual Agent

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% conversation handed over to a live agent

</td><td>

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

Virtual Agent CSAT score

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Success Dashboard

</td></tr><tr><td>

Self-solved %

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Call deflection %

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Structured tickets %

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

Customer satisfaction survey scores

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

MTTR – Average mean time to resolution

</td><td>

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

Breached SLA %

</td><td>

![no.](../image/icon-error-red-x.png)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td></tr><tr><td>

First assignment resolution

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% Automated resolutions

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% KB - Self-solved \(count\)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% VA - Self-solved \(count\)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% Call deflection when self-solved \(count\)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% VA ticket submissions \(count\)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr><tr><td>

% Catalog ticket submissions \(count\)

</td><td align="center">

![yes.](../image/icon-check-mark-green.png)

</td><td>

![no.](../image/icon-error-red-x.png)

</td></tr></tbody>
</table>## Top Performers

You can compare the customer's Benchmark score to analyze your performance against the top-ten percentile in a cohort.

## ITSM dashboards

ITSM dashboards are a central place for ITSM users to monitor ongoing ITSM operations. These dashboards contain data visualizations to help you improve your business processes and practices.

Access the dashboards under **Self-Service** &gt; **Dashboards**. To view detailed information, hover over any report graphic.

<table id="table_e5m_lt4_qbb"><thead><tr><th>

Dashboard

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

IT Manager

</td><td>

Overview reports and IT service analysis reports

</td><td>

-   Incident Manager
-   SLA Manager
-   pa\_admin

</td></tr><tr><td>

IT Agent

</td><td>

Agent work and agent group work reports, and prioritized workload

</td><td>

-   itil
-   itil\_admin
-   pa\_admin

</td></tr><tr><td>

IT Executive

</td><td>

Customer service, performance, and risk map reports

</td><td>

-   itil
-   itil\_admin
-   pa\_admin

</td></tr></tbody>
</table>-   **[View benchmark KPI data \(deprecated\)](../task/t_ViewBenchKPIData.md)**  
Benchmarks KPI data is shown in Service Portal. Data includes values for your company instance, and for global data.
-   **[Benchmarks KPI performance trend and recommendations \(deprecated\)](bench-kpi-trend-recommend.md)**  
The Benchmarks KPI performance chart trend view shows your KPI performance comparison with global data, and provides recommendations to implement for improved performance of your KPI.
-   **[Drill down within benchmark KPI data \(deprecated\)](../task/t_ViewBenchKPIIndScore.md)**  
You can drill down within benchmark KPI data for further analysis within Performance Analytics.

**Parent Topic:**[Benchmarks](../reference/r_Benchmarks.md)

