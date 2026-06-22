---
title: Benchmark KPIs
description: You can enable or disable a benchmark KPI, and customize KPI conditions. Integration with Performance Analytics provides daily data collection and drill down capabilities on KPI data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/benchmarks/c\_BenchKPIConfig-cf.html
release: australia
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Reference, Benchmarks, IT Service Management]
---

# Benchmark KPIs

You can enable or disable a benchmark KPI, and customize KPI conditions. Integration with Performance Analytics provides daily data collection and drill down capabilities on KPI data.

Benchmarks offers ITSM, ITOM, Virtual Agent, Security Operations KPIs, Success Dashboard, and Strategic Portfolio Management.

**Note:** Upgrading Benchmarks does not change KPI status or configuration from the previous release. New KPIs are enabled by default.

Benchmarks uses anonymous, aggregated usage data from customers who have opted in to calculate global and industry benchmarks. The KPIs in the Benchmarks application are performance analytics indicators that only collect the usage count data, for example, the total number of incidents in a month, based on the monthly aggregates. During data collection, the Benchmarks application does not consider any other details such as description of incidents, or information about requests, changes, or applications.

The participating customer count for each cohort bucket in Industry Category, User Size, and Three geo regions aggregates are large enough to calculate monthly benchmarks values and to maintain full anonymity. To further ensure data anonymity, the Benchmarks user interface allows you to use only one filter at a time.

## Benchmarks KPI categories

Benchmarks supports KPIs from other ServiceNow applications such as ITSM, ITOM, Security Operations, Conversational Interfaces, Success Dashboard, and Strategic Portfolio Management. For more information, see Benchmark KPIs.

## ITSM KPIs

<table id="table_ovv_mj4_gbb"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Note:** In some environments, KPIs involving resolved incidents may require further configuration to retrieve resolved incident data.

</td></tr><tr><td>

% of high priority incidents resolved

</td><td>

\[Number of priority 0 \(P0\) and priority 1 \(P1\) incidents resolved during the month\] / \[Total number of incidents resolved during the same month\]

 Incident count is generated from the Incident table.

**Note:** The definition of P0 and P1 incidents is likely to vary per participant. Your P0 and P1 incidents may or may not be similar to the incidents of others. For comparison, the metrics provided in this report represent the average of all participants.

</td></tr><tr><td>

% of incidents resolved on first assignment

</td><td>

\[Number of incidents resolved on first assignment during the month\] / \[Total number of incidents resolved during the same month\]

 First assignment is when the **Reassignment Count** field is 0 for the incident.

</td></tr><tr><td>

% of incidents resolved within SLA

</td><td>

\[Number of incidents with met SLAs resolved during the month\] / \[Total number of incidents resolved during the same month\]

 Met SLAs are calculated from the task\_sla table for incidents resolved during the month.

</td></tr><tr><td>

% of reopened incidents

</td><td>

\[Number of incidents resolved during the month that were reopened\] / \[Total number of incidents resolved during the same month\].

 Reopened is when the **Reopen Count** field is greater than 0 for the incident.

</td></tr><tr><td>

Average time to resolve a high priority incident

</td><td>

\[Sum of the duration of all high priority incidents resolved during the month\] / \[Total number of high priority incidents resolved during the same month\]

 -   Duration is the length of time from creation to resolution.
-   High priority incidents include priority 0 \(P0\) and priority 1 \(P1\).

</td></tr><tr><td>

Average time to resolve an incident

</td><td>

\[Sum of the duration of all incidents resolved during the month\] / \[Total number of incidents resolved during the same month\]

 Duration is the length of time from creation to resolution.

</td></tr><tr><td>

Number of incidents created per user

</td><td>

Number of incidents per user created during the month. Global value is the average of all participating customers per user.

</td></tr></tbody>
</table><table id="table_zw4_jxn_b1b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of high priority problems

</td><td>

\[Number of high priority problems closed during the month\] / \[Total number of problems closed during the same month\]

 High priority problems include priority 0 \(P0\) and priority 1 \(P1\).

</td></tr><tr><td>

% of incidents resolved by problem

</td><td>

\[Number of incidents resolved during the month that are associated with a problem\] / \[Total number of incidents resolved during the same month\]

</td></tr><tr><td>

Average time to close a problem

</td><td>

\[Sum of the duration of all problems closed during the month\] / \[Total number of problems closed during the same month\]

 Duration is the length of time from creating to closure.

</td></tr></tbody>
</table><table id="table_ljl_nxn_b1b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of emergency changes

</td><td>

\[Number of emergency changes closed during the month\] / \[Total number of all changes closed during the same month\]

 All changes include standard, normal, and emergency.

</td></tr><tr><td>

% of failed changes

</td><td>

\[Number of unsuccessful changes during the month\] / \[Total number of all changes closed during the same month\]

</td></tr><tr><td>

Average time to close a change

</td><td>

\[Sum of the duration of all changes closed during the month\] / \[Total number of all changes closed during the same month\]

 -   Duration shows the length of time from creating to closure.
-   All changes include standard, normal, and emergency.

</td></tr></tbody>
</table><table id="table_w3h_v5n_b1b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of closed requests with breached SLAs

</td><td>

\[Number of closed requests with breached SLAs during the month\] / \[Total number of closed requests during the same month\]

 Breached SLAs are calculated from the task\_sla table for requests closed during the month.

</td></tr><tr><td>

Average time to fulfill a request

</td><td>

\[Sum of the duration for Service Catalog requests fulfilled during the month\] / \[Total number of Service Catalog requests fulfilled in the same month\]

 -   **Duration** is the length of time from creation to closure.
-   **Number of Service Catalog requests fulfilled** is the count of the number of records in the sc\_req\_item table, which were closed within a month.

</td></tr><tr><td>

Number of requests created per user

</td><td>

Number of requests per user created during the month.

</td></tr></tbody>
</table><table id="table_dly_x5n_b1b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of incidents resolved using KB articles

</td><td>

\[Number of incidents with KB articles resolved during the month\] /

 \[Total number of incidents resolved during the same month\]

</td></tr><tr><td>

Number of knowledge articles views per user

</td><td>

Number of knowledge article views per user during the month.

-   **Knowledge base views** are generated from the sys\_view\_count table.
-   **Global** value is the average of all participating customers per user.

</td></tr></tbody>
</table><table id="table_rsg_1f3_ktb"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% call deflection

</td><td>

\[The number of incidents and requests created using Virtual Agent \] / \[Total numbers of incidents and requests created\]

 The number of times, in percentage, the incident, or request was submitted using Virtual Agent. This is determined by the [deflection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/deflections-virtual-agent.md) pattern added in the Virtual Agent topic.

</td></tr><tr><td>

% of incidents auto-resolved

</td><td>

\[The number of incidents auto-resolved by Virtual Agent \] / \[Total number of incidents resolved\]

 The number of times, in percentage, incidents were automatically resolved using automated workflows or by [Issue Auto Resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/auto-resolution-va.md).

</td></tr></tbody>
</table><table id="table_yws_1qy_fbb"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Average customer satisfaction

</td><td>

\[Sum of normalized metric values of all survey instances taken during the month\] /

 \[Total number of survey instances taken during the same month\]

-   Table: metric\_results.
-   Survey: Customer Satisfaction Survey.
-   Metric value is normalized as per category weights.

**Note:** This KPI uses the base system Customer Satisfaction Survey.

If you're using a different survey to collect user feedback, you can customize the KPI definition.

</td></tr><tr><td>

Number of requests per fulfiller

</td><td>

\[Number of active requester \(non-ITIL\) users during the month\] /

 \[Total number of active ITIL users during the same month\]

</td></tr></tbody>
</table>## ITOM KPIs

<table id="table_oh2_1vn_b1b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of duplicate CIs

</td><td>

\[Number of duplicate CIs during the month\] / \[Total number of CIs during the same month\]

 Duplicate CIs are calculated using the cmdb\_health\_scorecard table.

**Note:** The definition of duplicate CIs is likely to vary per participant. Your duplicate CIs definition may or may not be similar to the definitions of others. For comparison, the metrics provided in this report represent the average of all participants.

</td></tr><tr><td>

% of non-compliant CIs

</td><td>

\[Number of CI audit failures during the month\] / \[Total number of CIs audited during the same month\]

 Non-compliant CIs are calculated using the cmdb\_health\_scorecard table.

**Note:** The definition of CI compliance audits is likely to vary per participant. Your CI compliance audit definition may or may not be similar to the definitions of others. For comparison, the metrics provided in this report represent the average of all participants.

</td></tr><tr><td>

% of stale CIs

</td><td>

\[Number of stale CIs during the month\] / \[Total number of CIs during the same month\]

 Stale CIs are calculated using the cmdb\_health\_scorecard table.

**Note:** The definition of stale CIs is likely to vary per participant. Your stale CIs definition may or may not be similar to the definitions of others. For comparison, the metrics provided in this report represent the average of all participants.

</td></tr></tbody>
</table>## Conversational Interfaces KPIs

<table id="table_ow2_2ny_ktb"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of users using Virtual Agent

</td><td>

\[Total number of users using Virtual Agent \] / \[Total number of active users\]

 Percentage of unique users who are using Virtual Agent to handle everyday tasks and requests.

</td></tr><tr><td>

% conversation handed over to a live agent

</td><td>

\[Number of conversations assigned to a live agent\] / \[Total number of conversations\]

 The percentage of virtual agent conversations that were redirected to handle everyday tasks and requests.

</td></tr><tr><td>

Virtual Agent CSAT score

</td><td>

Uses the daily average score of the surveys conducted to analyze the quality of user interactions with Virtual Agent conversations.

</td></tr></tbody>
</table>## Security Operations KPIs

<table id="table_nlc_sr4_ndb"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of critical and high priority security incidents

</td><td>

\[Number of critical and high priority security incidents created during the month\] / \[Total number of all security incidents created during the same month\]

</td></tr></tbody>
</table><table id="table_kgw_yrk_h2b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Average critical vulnerability age

</td><td>

\[Summed age of critical vulnerable items\] / \[Number of critical vulnerable items\]

</td></tr><tr><td>

Average vulnerability age

</td><td>

\[Summed age of vulnerable items\] / \[Number of vulnerable items\]

</td></tr><tr><td>

Average vulnerability per asset

</td><td>

\[Sum of active vulnerable items\] / \[Total number of scanned configuration items\]

</td></tr><tr><td>

VI mean time to remediate \(MTTR\)

</td><td>

\[Sum of duration of closed vulnerable items\] / \[Total number of closed vulnerable items displayed as a 30-day running average\]

</td></tr><tr><td>

% of remediation efficiency

</td><td>

\[Number of vulnerable Items items closed during a month\] / \[Number of new or reopened vulnerable items in the same month\]

</td></tr></tbody>
</table>## Success Dashboard KPIs

<table id="table_okv_rp3_1vb"><thead><tr><th>

KPI

</th><th>

Formula

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Self-solved %

</td><td>

\[Self-solved \(VA\) + Self-solved \(KB\) + Automated resolutions\] / \[Total Tickets Resolution + Self-solved \(VA\) + Self-solved \(KB\)\] \*100

</td><td>

Self-solved percentage is calculated based on the daily average number of times your users achieved resolution without agent intervention. It includes numbers from the following items:-   Self-solved using Virtual Agent.
-   Self-solved using Knowledge articles.
-   Automated resolutions. This could be, for example, incidents that were auto-resolved using Virtual Agent.

</td></tr><tr><td>

Call deflection %

</td><td>

\[Catalog ticket submissions + VA ticket submissions + Self-solved \(VA\) + Self-solved \(KB\)\] / \[Total tickets submitted + Self-solved \(VA\) + Self-solved \(KB\)\] \* 100

</td><td>

Call deflection is calculated per day based on the number of times requestors performed the following actions without Tier 1 agent intervention:-   Ticket submissions using Service Catalog
-   Ticket submissions using Virtual Agent
-   Self-solved using Virtual Agent
-   Self-solved using Knowledge articles

</td></tr><tr><td>

Structured tickets %

</td><td>

\[Structured tickets completed\]/\[Total Ticket resolutions\]\*100

</td><td>

Total number of tickets successfully completed and closed for the report range that has a pre-defined or guided intake and fulfillment process. This could be, for example, a requested item fulfillment or an HR Case where payroll ambiguity was resolved.

</td></tr><tr><td>

Customer satisfaction survey scores

</td><td>

\[ITSM Customer Satisfaction Score\] + \[Virtual agent Customer Satisfaction score\]

</td><td>

Average of customer satisfaction scores based on the surveys conducted after the issue was resolved.**Note:** Both ITSM Customer Satisfaction score and VA Customer Satisfaction score are normalized with the base as 10.

</td></tr><tr><td>

MTTR – Average mean time to resolution

</td><td>

\[Time to resolve\]/\[Issues resolved\]/24

</td><td>

Average time, in days, between the day, a ticket was created and the day it was closed.

</td></tr><tr><td>

Breached SLA %

</td><td>

\[Issues resolved with breached SLAs\]/\[Issues resolved\]\*100

</td><td>

Percentage of issues resolved after the SLA was breached.

</td></tr><tr><td>

First assignment resolution

</td><td>

\[Tickets resolved without reassignment\]/\[Issues resolved\]\*100

</td><td>

Tickets resolved without having to reassign to an agent.

</td></tr><tr><td>

% Automated resolutions

</td><td>

\(\[\[Automated resolutions\]\]/\[\[Self solved - percentage \(denominator\)\]\]\)\*100

</td><td>

Total number of tickets successfully completed and closed using the automated workflows, or by Issue Auto Resolution, or by Password Reset web/windows application.

</td></tr><tr><td>

% KB - Self-solved \(count\)

</td><td>

\(\[\[KB - Self-solved \(count\)\]\]/\[\[Self solved - percentage \(denominator\)\]\]\)\*100

</td><td>

Total number of tickets successfully completed and closed by reading the knowledge articles. This is determined when users read knowledge article\(s\) and do not create a ticket in a 24-hour window.

</td></tr><tr><td>

% VA - Self-solved \(count\)

</td><td>

\(\[\[VA - Self-solved \(count\)\]\]/\[\[Self solved - percentage \(denominator\)\]\]\)\*100

</td><td>

Total number of automated conversations that resolved the issue. This is determined by the deflection node instrumented in the Virtual Agent topic.

</td></tr><tr><td>

% Call deflection when self-solved \(count\)

</td><td>

\(\[\[Call deflection when self-solved \(count\)\]\]/\[\[Call deflection - percentage \(denominator\)\]\]\)\*100

</td><td>

Total number of issues or requests solved using the Virtual Agent and Knowledge Base articles that resulted in call deflection.

</td></tr><tr><td>

% VA ticket submissions \(count\)

</td><td>

\(\[\[VA ticket submissions \(count\)\]\]/\[\[Call deflection - percentage \(denominator\)\]\]\)\*100

</td><td>

Total number of times the ticket was submitted using the Virtual Agent. This is determined by the deflection node instrumented in the Virtual Agent topic.

</td></tr><tr><td>

% Catalog ticket submissions \(count\)

</td><td>

\(\[\[Catalog ticket submissions \(count\)\]\]/\[\[Call deflection - percentage \(denominator\)\]\]\)\*100

</td><td>

Total number of tickets \(cases, incidents, requested items and so on\) submitted using the Service Catalog in Service Portal or NOW mobile.

</td></tr></tbody>
</table>For more information on Success Dashboard KPI definitions and formulas, see [ITSM Success Dashboard indicators KPI definitions and formulas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-success-dashboard-indicators/sd-kpi-formulae.md)

## Strategic Portfolio Management KPIs

Benchmarks supports Strategic Portfolio Management KPIs. For more information, see [SPM Benchmarking KPIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/benchmarks-for-strategic-portfolio-management/spm-benchmarking-kpis.md).

## Benchmarks data transfer

Your Benchmarks score data is automatically uploaded to ServiceNow on the third day of the month. Global scores are automatically downloaded to your instance on the 11th day of the month.

You can manually upload or download scores beyond those days of the month \(on demand\) by executing the Benchmarks scores scheduled jobs through the **System Definition** &gt; **Scheduled Jobs** navigation item.

-   Upload the benchmark scores \(automatically runs on the first day of the month\)
-   Download the benchmark scores \(automatically runs on the ninth day of the month\)

These on-demand scheduled jobs are useful if, for any reason, there was a failure in the automatic upload or download scores process and it is after the cutoff dates. You can also run a scheduled job to generate six months of historical data.

## Email notification

Users with the Benchmarks admin \(sn\_bm\_client.benchmark\_admin\) and Benchmarks data viewer \(sn\_bm\_client.benchmark\_data\_viewer\) roles automatically receive email notification regarding availability of monthly scores, historical data recalculation, and new KPIs. You must have system admin \(admin\) role to modify the email recipient list.

-   An email containing notification information is sent when the monthly global data is available. Monthly results \(your instance results, and global results\) are downloaded to the customer instance mid month.
    -   Subject: New Monthly Benchmarks report is available now
    -   Body: ServiceNow Benchmarks has been updated with &lt;month&gt; data. You can see the updated Benchmarks by viewing the Benchmarks Dashboard &lt;Benchmarks Dashboard Portal link&gt;.
-   An email containing notification information is sent when historical data for the past six months is recalculated.
    -   Subject: Historical Global Benchmarks scores have been refreshed
    -   Body: The global Benchmarks scores of last six months have been recalculated with improved data quality. You can see the updated Benchmarks by visiting Benchmarks Dashboard &lt;Benchmark Dashboard Portal Link&gt;.
-   An email containing notification information is sent when an updated KPI version is introduced \(with some fixes, for example\).
    -   Subject: One or more Benchmarks KPI versions have changed
    -   Body: The latest Benchmarks scores have a new version of following KPIs with improved data quality.

        &lt; KPI name&gt;.

        You can see the updated Benchmarks by visiting Benchmarks Dashboard &lt;Benchmark Dashboard Portal Link&gt;.


Benchmarks notification emails are accessed using the **System Settings** &gt; **Notifications** navigation menu.

