---
title: New Benchmarks Dashboard
description: The Benchmarks dashboard displays KPI data, performance trends, and indicator scorecards.
locale: en-US
release: zurich
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analyze, Benchmarks, IT Service Management]
---

# New Benchmarks Dashboard

The Benchmarks dashboard displays KPI data, performance trends, and indicator scorecards.

The Benchmarks KPI dashboard view displays all the KPIs and can be accessed through Service Portal.

The dashboard features include the following:

-   KPIs are shown in either the list or card view.
-   Downloadable reports of the KPI list are available in PDF format.
-   Data is filtered by type of industry, number of users, Managed Service Providers \(MSPs\), or geographic region \(the filter is retained when switching between the KPI view and trend view\).

    **Note:** Only MSPs can view the global MSP aggregate score data.

-   The performance against the global data is shown with a thumbs up or thumbs down representation.
-   Depending on the subscription, six months to two years of historical KPI data can be viewed.
-   Time values can be displayed in hours or days using the **sn\_bm\_client.dashboard\_display\_unit** system property.

**Note:** The new Benchmarks dashboard is available from the ServiceNow store.

![Benchmarks Dashboard](../image/Newuidashboard.png)

## Percentile rank

The exact standing of the KPI for your company within your participating peer group is indicated by percentile rank. A KPI percentile rank of 90% indicates that your instance standing for that KPI is greater than 90% of the instances participating in that group.

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
</table>