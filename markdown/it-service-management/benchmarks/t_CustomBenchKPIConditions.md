---
title: Link or customize a benchmark KPI
description: You can customize KPI conditions to fit the needs of your organization better.
locale: en-US
release: yokohama
product: Benchmarks
classification: benchmarks
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Benchmark KPIs, Benchmarks, IT Service Management]
---

# Link or customize a benchmark KPI

You can customize KPI conditions to fit the needs of your organization better.

## Before you begin

The Benchmarks admin role does not provide application-specific roles. Therefore, although a Benchmarks admin can access a KPI through the Benchmarks application, changes to KPI conditions require the role specific to the KPI application.

For example, a Benchmarks admin cannot modify conditions for the knowledge base KPI \(Knowledge Use \[kb\_use\] table\), SLA KPI \(Task SLA \[task\_sla\] table\), ITOM KPIs \(CMDB Health Scorecard \[cmdb\_health\_scorecard\] table\), Security Operations KPIs \(Vulnerable Item \[sn\_vul\_vulnerable\_item\], or Security Incident \[sn\_si\_incident\] tables\) from within Benchmarks without specific access granted to those tables \(knowledge\_admin, sla\_admin, asset, or sn\_si.special\_access roles\).

Role required: sn\_bm\_client.benchmark\_admin

## About this task

Customizing KPI conditions is useful to adjust the criteria to more accurately represent the data that your company is interested in.

For example, if your implementation does not use priority 1 incidents, you can change the criteria for high priority KPIs from 1 to 0, which returns more accurate data for your organization.

**Note:** It takes one to two months for aggregate monthly data to accurately reflect changes made to KPI conditions. For example, changes made within the month include a combination of data:

-   Data for the previous condition \(up until the date the condition was changed\)
-   Data for the new condition from that date forward

For further analysis, you can link a Performance Analytics indicator that you are already using to the corresponding Benchmarks indicator to see breakdowns, in addition to individual scores, when drilling down on KPI data.

For example, link **Number of resolved incidents by first assigned group** to **Benchmark: Number of incidents resolved on first assignment** to view breakdown values by priority, assignment group, and category.

**Note:** Individual scores are shown by default but you must have [Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) to use linking to show breakdowns.

## Procedure

1.  Navigate to **All** &gt; **Benchmarks** &gt; **Setup** and click a KPI to access the KPI conditions.

    ![Number of high-priority incidents resolved](../image/BenchConditions.png)

2.  Change the conditions, as appropriate.

3.  To link a Performance Analytics indicator to a Benchmarks indicator, follow the procedure in [Link an automated indicator to a benchmark](https://www.servicenow.com/docs/access?context=link-automated-indicator-benchmark&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

<table id="table_aqj_hjl_tfb"><thead><tr><th>

Benchmarks KPI

</th><th>

Formula

</th><th>

Performance Analytics KPI

</th></tr></thead><tbody><tr><td>

Number of active users

</td><td>

--

</td><td>

Benchmark: Number of active users

</td></tr><tr><td>

Total time to close changes

</td><td>

--

</td><td>

Benchmark: Total time to close changes

</td></tr><tr><td>

% of failed changes

</td><td>

\[Number of unsuccessful changes during the month\] /

 \[Total number of all changes closed during the same month\]

</td><td>

Benchmark: % of failed changes

</td></tr><tr><td>

Number of unsuccessful changes

</td><td>

--

</td><td>

Benchmark: Number of unsuccessful changes

</td></tr><tr><td>

Number of changes closed

</td><td>

--

</td><td>

Benchmark: Number of changes closed

</td></tr><tr><td>

% of emergency changes

</td><td>

\[Number of emergency changes closed during the month\] /

 \[Total number of all changes closed during the same month\]

</td><td>

Benchmark: % of emergency changes

</td></tr><tr><td>

Number of emergency changes closed

</td><td>

--

</td><td>

Benchmark: Number of emergency changes closed

</td></tr><tr><td>

Average time to close a change

</td><td>

\[\[Benchmark: Total time to close changes\]\] /

 \[\[Benchmark: Number of changes closed\]\]

</td><td>

Benchmark: Average time to close a change

</td></tr><tr><td>

% of stale CIs

</td><td>

Monthly average.

</td><td>

Benchmark: % of stale cis

</td></tr><tr><td>

% of duplicate CIs

</td><td>

Monthly average.

</td><td>

Benchmark: % of duplicate cis

</td></tr><tr><td>

% of non-compliant CIs

</td><td>

Monthly average.

</td><td>

Benchmark: % of non-compliant cis

</td></tr><tr><td>

Average time to resolve a high priority incident

</td><td>

\[\[Benchmark: Total time to resolve high priority incidents\]\]/

 \[\[Benchmark: Number of high priority incidents resolved\]\]

</td><td>

Benchmark: Average time to resolve a high priority incident

</td></tr><tr><td>

% of incidents resolved within SLA

</td><td>

\(\[\[Benchmark: Number of resolved incidents with SLAs\]\] - \[\[Benchmark: Number of resolved incidents with breached SLAs\]\]\) /

 \[\[Benchmark: Number of resolved incidents with SLAs\]\] \* 100

</td><td>

Benchmark: % of incidents resolved within SLA

</td></tr><tr><td>

Total number of incidents resolved by problem

</td><td>

--

</td><td>

Benchmark: Total number of incidents resolved by problem

</td></tr><tr><td>

Number of incidents closed that were re-opened

</td><td>

--

</td><td>

Benchmark: Number of incidents closed that were re-opened

</td></tr><tr><td>

Number of high priority incidents

</td><td>

--

</td><td>

Benchmark: Number of high priority incidents resolved

</td></tr><tr><td>

Average time to resolve an incident

</td><td>

\[\[Benchmark: Total time to resolve an incident\]\] /

 \[\[Benchmark: Number of incidents resolved\]\]

</td><td>

Benchmark: Average time to resolve an incident

</td></tr><tr><td>

Number of resolved incidents with SLAs

</td><td>

--

</td><td>

Benchmark: Number of resolved incidents with SLAs

</td></tr><tr><td>

Number of incidents created per user

</td><td>

\[\[Benchmark: Number of incidents created / By month SUM\]\]/

 \[\[Benchmark: Number of active users / By month AVG\]\]

</td><td>

Benchmark: Number of incidents created per user

</td></tr><tr><td>

Total time to resolve high priority incidents

</td><td>

--

</td><td>

Benchmark: Total time to resolve high priority incidents

</td></tr><tr><td>

% of high priority incidents

</td><td>

\[\[Benchmark: Number of high priority incidents resolved\]\] /

 \[\[Benchmark: Number of incidents resolved\]\] \* 100

</td><td>

Benchmark: % of high priority incidents

</td></tr><tr><td>

Number of incidents created

</td><td>

--

</td><td>

Benchmark: Number of incidents created

</td></tr><tr><td>

Number of incidents resolved with attached KB articles

</td><td>

--

</td><td>

Benchmark: Number of incidents resolved with attached KB articles

</td></tr><tr><td>

Number of resolved incidents with breached SLAs

</td><td>

--

</td><td>

Benchmark: Number of resolved incidents with breached SLAs

</td></tr><tr><td>

Total number of incidents

</td><td>

--

</td><td>

Benchmark: Number of incidents resolved

</td></tr><tr><td>

Number of incidents resolved on first assignment

</td><td>

--

</td><td>

Benchmark: Number of incidents resolved on first assignment

</td></tr><tr><td>

% of incidents resolved on first assignment

</td><td>

\[\[Benchmark: Total time to resolve an incident\]\] /

 \[\[Benchmark: Number of incidents resolved\]\]

</td><td>

Benchmark: % of incidents resolved on first assignment

</td></tr><tr><td>

Total time to resolve incidents

</td><td>

--

</td><td>

Benchmark: Total time to resolve an incident

</td></tr><tr><td>

% of reopened incidents

</td><td>

\[\[Benchmark: Number of incidents closed that were re-opened\]\] /

 \[\[Benchmark: Number of incidents closed \]\] \* 100

</td><td>

Benchmark: % of reopened incidents

</td></tr><tr><td>

Number of incidents closed

</td><td>

--

</td><td>

Benchmark: Number of incidents closed

</td></tr><tr><td>

Number of knowledge article views

</td><td>

--

</td><td>

Benchmark: Number of knowledge article views

</td></tr><tr><td>

Number of knowledge base views per user

</td><td>

\[\[Benchmark: Number of knowledge article views / By month SUM\]\]/

 \[\[Benchmark: Number of active users / By month AVG\]\]

</td><td>

Benchmark: Number of knowledge base views per user

</td></tr><tr><td>

% of incidents resolved using KB articles

</td><td>

\[\[Benchmark: Number of incidents resolved with attached KB articles\]\] /

 \[\[Benchmark: Number of incidents resolved\]\] \* 100

</td><td>

Benchmark: % of incidents resolved using KB articles

</td></tr><tr><td>

Number of survey instances

</td><td>

--

</td><td>

Benchmark: Number of survey instances

</td></tr><tr><td>

Number of active ITIL users

</td><td>

--

</td><td>

Benchmark: Number of active ITIL users

</td></tr><tr><td>

Normalized customer satisfaction

</td><td>

--

</td><td>

Benchmark: Normalized customer satisfaction

</td></tr><tr><td>

Average customer satisfaction

</td><td>

\[\[Benchmark: Normalized customer satisfaction\]\] /

 \[\[Benchmark: Number of survey instances\]\]

</td><td>

Benchmark: Average customer satisfaction

</td></tr><tr><td>

Number of requesters per fulfiller

</td><td>

\(\[\[Benchmark: Number of active users\]\] - \[\[Benchmark: Number of active ITIL users\]\]\) /

 \[\[Benchmark: Number of active ITIL users\]\]

</td><td>

Benchmark: Number of requesters per fulfiller

</td></tr><tr><td>

% of high priority problems

</td><td>

\[\[Benchmark: Number of high priority problems closed\]\] /

 \[\[Benchmark: Number of problems closed\]\] \* 100

</td><td>

Benchmark: % of high priority problems

</td></tr><tr><td>

Total time to close problems

</td><td>

--

</td><td>

Benchmark: Total time to close problems

</td></tr><tr><td>

% of incidents resolved by problem

</td><td>

\[\[Benchmark: Total number of incidents resolved by problem\]\] /

 \[\[Benchmark: Number of incidents resolved\]\] \* 100

</td><td>

Benchmark: % of incidents resolved by problem

</td></tr><tr><td>

Number of high priority problems closed

</td><td>

--

</td><td>

Benchmark: Number of high priority problems closed

</td></tr><tr><td>

Number of problems closed

</td><td>

--

</td><td>

Benchmark: Number of problems closed

</td></tr><tr><td>

Average time to close a problem

</td><td>

\[\[Benchmark: Total time to close problems\]\] /

 \[\[Benchmark: Number of problems closed\]\]

</td><td>

Benchmark: Average time to close a problem

</td></tr><tr><td>

% of critical and high priority security incidents

</td><td>

\[\[Benchmark: Number of Critical and High Priority Security Incidents\]\] /

 \[\[Benchmark: Number of Security Incidents\]\] \* 100

</td><td>

Benchmark: % of critical and high priority security incidents

</td></tr><tr><td>

Number of critical and high priority security incidents

</td><td>

--

</td><td>

Benchmark: Number of Critical and High Priority Security Incidents

</td></tr><tr><td>

Number of security incidents

</td><td>

--

</td><td>

Benchmark: Number of Security Incidents

</td></tr><tr><td>

Number of requests created

</td><td>

--

</td><td>

Benchmark: Number of requests created

</td></tr><tr><td>

Number of requests closed

</td><td>

--

</td><td>

Benchmark: Number of requests closed

</td></tr><tr><td>

Average time to fulfil a request

</td><td>

\[\[Benchmark: Total time to fulfil requests\]\]/

 \[\[Benchmark: Number of requests closed\]\]

</td><td>

Benchmark: Average time to fulfil a request

</td></tr><tr><td>

Number of closed requests with SLAs

</td><td>

--

</td><td>

Benchmark: Number of closed requests with SLAs

</td></tr><tr><td>

Number of requests created per user

</td><td>

\[\[Benchmark: Number of requests created / By month SUM\]\]/

 \[\[Benchmark: Number of active users / By month AVG\]\]

</td><td>

Benchmark: Number of requests created per user

</td></tr><tr><td>

Number of closed requests with breached SLAs

</td><td>

--

</td><td>

Benchmark: Number of closed requests with breached SLAs

</td></tr><tr><td>

Total time to fulfil requests

</td><td>

--

</td><td>

Benchmark: Total time to fulfil requests

</td></tr><tr><td>

% of closed requests with breached SLAs

</td><td>

\[\[Benchmark: Number of closed requests with breached SLAs\]\] /

 \[\[Benchmark: Number of closed requests with SLAs\]\] \* 100

</td><td>

Benchmark: % of closed requests with breached SLAs

</td></tr><tr><td>

Number of critical vulnerability items

</td><td>

--

</td><td>

Benchmark: Number of critical vulnerability items

</td></tr><tr><td>

Number of vulnerability items

</td><td>

--

</td><td>

Benchmark: Number of vulnerability items

</td></tr><tr><td>

Average vulnerability age

</td><td>

\[\[Benchmark: Summed age of vulnerable items\]\] /

 \[\[Benchmark: Number of vulnerability items\]\]

</td><td>

Benchmark: Average age of vulnerable items

</td></tr><tr><td>

Average critical vulnerability age

</td><td>

\[\[Benchmark: Summed age of critical vulnerable items\]\] /

 \[\[Benchmark: Number of critical vulnerability items\]\]

</td><td>

Benchmark: Average age of critical vulnerable items

</td></tr><tr><td>

Summed age of critical vulnerable items

</td><td>

--

</td><td>

Benchmark: Summed age of critical vulnerable items

</td></tr><tr><td>

Summed age of vulnerable items

</td><td>

--

</td><td>

Benchmark: Summed age of vulnerable items

</td></tr></tbody>
</table><table id="table_fpm_t3x_4tb"><thead><tr><th>

Benchmarks KPI

</th><th>

Formula

</th><th>

Performance Analytics KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Call Deflection \(VA Triaged and Created\)

</td><td>

--

</td><td>

Benchmark: Call Deflection \(VA Triaged and Created\)

</td><td>

Incidents created using Virtual Agent and tracked using the **ITSM VA–Triage and Created** deflection pattern.

</td></tr><tr><td>

Call Deflection \(VA Catalog Analytics\)

</td><td>

--

</td><td>

Benchmark: Call Deflection through VA \(Catalog Analytics\)

</td><td>

Requests created using Virtual Agent and tracked every time Virtual Agent referred a catalog for submission.

</td></tr><tr><td>

% Call Deflection

</td><td>

\(\[\[Benchmark: Call Deflection \(VA Triaged and Created\)\]\] + \[\[Benchmark: Call Deflection through VA \(Catalog Analytics\)\]\]\) / \(\[\[Benchmark: Number of requests created\]\] + \[\[Benchmark: Number of incidents created\]\]\) \* 100

</td><td>

Benchmark: % VA Deflection

</td><td>

The number of times the Virtual Agent automatically resolved incidents or completed requests.

</td></tr><tr><td>

IAR \(Intercept &amp; Resolved\)

</td><td>

--

</td><td>

Benchmark: VA IAR \(Intercept &amp; Resolved\)

</td><td>

Incidents that were resolved using **ITSM VA-Intercept &amp; Resolved** deflection pattern.

</td></tr><tr><td>

VA Self Resolved

</td><td>

--

</td><td>

Benchmark: VA Self Resolved

</td><td>

Every time the user was able to self-solve incident resolution or complete requests using **ITSM VA-Self Resolving** deflection pattern.

</td></tr><tr><td>

Number of incidents resolved

</td><td>

--

</td><td>

Benchmark: Number of incidents resolved

</td><td>

The total number of incidents resolved.

</td></tr><tr><td>

% of incident that were auto-resolved using VA

</td><td>

\(\[\[Benchmark: VA IAR \(Intercept &amp; Resolved\)\]\] + \[\[Benchmark: VA Self Resolved\]\]\) / \(\[\[Benchmark: Number of incidents resolved\]\] + \[\[Benchmark: VA Self Resolved\]\]\) \* 100

</td><td>

Benchmark: % of incident that were auto-resolved using VA.

</td><td>

Percentage of incidents that were auto-resolved using Virtual Agent.

</td></tr><tr><td>

Number of monthly users of VA

</td><td>

--

</td><td>

Benchmark: Number of monthly users of VA

</td><td>

Number of monthly users who are using Virtual Agent.

</td></tr><tr><td>

% of users using Virtual Agent

</td><td>

\[\[Benchmark: Number of monthly users of VA\]\] / \[\[Benchmark: Number of active users\]\] \* 100

</td><td>

Benchmark: % of users using Virtual Agent

</td><td>

Percentage of users in the organization using Virtual Agent as an engagement channel.

</td></tr><tr><td>

Number of VA conversations handed over to an agent

</td><td>

--

</td><td>

Benchmark: Number of VA conversation handed over to an agent

</td><td>

Conversations that were not resolved by the Virtual Agent and had to be handed off to a live agent.

</td></tr><tr><td>

Total conversations in VA

</td><td>

--

</td><td>

Benchmark: Total conversations in VA

</td><td>

All conversations that occurred in the Virtual Agent.

</td></tr><tr><td>

% ofVA conversations handed over to live agent

</td><td>

\[\[Benchmark: Number of VA conversation handed over to an agent\]\] / \[\[Benchmark: Total conversations in VA\]\] \* 100

</td><td>

Benchmark: % of VA conversations handed over to live agent

</td><td>

Number of times, in percentage, that the conversation was handed off to an agent.

</td></tr><tr><td>

VA normalized Satisfaction score

</td><td>

--

</td><td>

Benchmark: VA normalized Satisfaction score

</td><td>

Overall, total normalized score of all the surveys conducted for Virtual Agent conversations.

</td></tr><tr><td>

VA survey instances

</td><td>

--

</td><td>

Benchmark: VA survey instances

</td><td>

Total number of surveys that an agent responded to for assessing the satisfaction score.

</td></tr><tr><td>

Virtual Agent CSAT score

</td><td>

\[\[Benchmark: VA normalized Satisfaction score\]\]/\[\[Benchmark: VA survey instances\]\]

</td><td>

Benchmark: VA CSAT score

</td><td>

Average Virtual Agent satisfaction score.

</td></tr></tbody>
</table>
**Parent Topic:**[Benchmark KPIs](../concept/c_BenchKPIConfig.md)

