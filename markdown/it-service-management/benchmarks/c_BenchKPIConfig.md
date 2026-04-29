---
title: Benchmark KPIs
description: You can enable or disable a benchmark KPI, and customize KPI conditions. Integration with Performance Analytics provides daily data collection and drill down capabilities on KPI data.
locale: en-US
release: australia
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Benchmarks, IT Service Management]
---

# Benchmark KPIs

You can enable or disable a benchmark KPI, and customize KPI conditions. Integration with Performance Analytics provides daily data collection and drill down capabilities on KPI data.

Benchmarks offers KPIs grouped in six categories. The categories are ITSM, ITOM, Security Operations, Success Dashboard, Conversational Interfaces, and Strategic Portfolio Management.

**Note:** Upgrading Benchmarks does not change KPI status or configuration from the previous release. New KPIs are enabled by default.

Benchmarks uses anonymous, aggregated usage data from customers who have opted in to calculate global and industry benchmarks. The KPIs in the Benchmarks application are performance analytics indicators that only collect the usage count data, for example, the total number of incidents in a month, based on the monthly aggregates. During data collection, the Benchmarks application does not consider any other details such as description of incidents, or information about requests, changes, or applications.

The participating customer count for each cohort bucket in Industry Category, User Size, and Three geo regions aggregates are large enough to calculate monthly benchmarks values and to maintain full anonymity. To further ensure data anonymity, the Benchmarks user interface allows you to use only one filter at a time.

## ITSM KPIs

<table id="table_ovv_mj4_gbb"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Note:** In some environments, KPIs involving resolved incidents may require further [configuration](../task/t_ConfigResIncBenchKPIs.md) to retrieve resolved incident data.

</td></tr><tr><td>

% of high priority incidents resolved

</td><td>

\[Number of priority 1 \(P1\) and priority 2 \(P2\) incidents resolved during the month\] / \[Total number of incidents resolved during the same month\]

 Incident count is generated from the Incident table.

**Note:** The definition of P1 and P2 incidents is likely to vary per participant. Your P1 and P2 incidents may or may not be similar to the incidents of others. For comparison, the metrics provided in this report represent the average of all participants.

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
-   High priority incidents include priority 1 \(P1\) and priority 2 \(P2\).

</td></tr><tr><td>

Average time to resolve an incident

</td><td>

\[Sum of the duration of all incidents resolved during the month\] / \[Total number of incidents resolved during the same month\]

 Duration is the length of time from creation to resolution.

</td></tr><tr><td>

Number of incidents created per user

</td><td>

Number of incidents per user created during the month.

 Global value is the average of all participating customers per user.

</td></tr></tbody>
</table><table id="table_zw4_jxn_b1b"><thead><tr><th>

KPI

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of high priority problems

</td><td>

\[Number of high priority problems closed during the month\] / \[Total number of problems closed during the same month\]

 High priority problems include priority 1 \(P1\) and priority 2 \(P2\).

</td></tr><tr><td>

% of incidents resolved by problem

</td><td>

\[Number of incidents resolved during the month that are associated with a problem\] / \[Total number of incidents resolved during the same month\]

</td></tr><tr><td>

Average time to close a problem

</td><td>

\[Sum of the duration of all problems closed during the month\] / \[Total number of problems closed during the same month\]

 -   Duration is the length of time from creating to closure.
-   Problems include priority 1 \(P1\) through priority 5 \(P5\).

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

 -   Duration is the length of time from creation to closure.
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

-   **Knowledge base views** are generated from the kb\_use table.
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

 The number of times, in percentage, the incident, or request was submitted using Virtual Agent. This is determined by the [deflection](https://www.servicenow.com/docs/access?context=deflections-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) pattern added in the Virtual Agent topic.

</td></tr><tr><td>

% of incidents auto-resolved

</td><td>

\[The number of incidents auto-resolved by Virtual Agent \] / \[Total number of incidents resolved\]

 The number of times, in percentage, incidents were automatically resolved using automated workflows or by [Issue Auto Resolution](https://www.servicenow.com/docs/access?context=auto-resolution-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

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

-   Table: asmt\_metric\_results.
-   Survey: Customer Satisfaction Survey.
-   Metric value is normalized as per category weights.

**Note:** This KPI uses the base system Customer Satisfaction Survey.

If you're using a different survey to collect user feedback, you can [customize the KPI definition](../task/t_CustomBenchKPIConditions.md).

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

Average % of duplicate CIs during the month.

 Duplicate CIs are calculated using the cmdb\_health\_scorecard table.

**Note:** The definition of duplicate CIs is likely to vary per participant. Your duplicate CIs definition may or may not be similar to the definitions of others. For comparison, the metrics provided in this report represent the average of all participants.

</td></tr><tr><td>

% of non-compliant CIs

</td><td>

Average % of non-compliant CIs during the month.

 Non-compliant CIs are calculated using the cmdb\_health\_scorecard table.

**Note:** The definition of CI compliance audits is likely to vary per participant. Your CI compliance audit definition may or may not be similar to the definitions of others. For comparison, the metrics provided in this report represent the average of all participants.

</td></tr><tr><td>

% of stale CIs

</td><td>

Average % of stale CIs during the month.

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

You must install the ITSM Success Dashboard application to access the Success Dashboard KPIs. For more information, see [Install ITSM Success Dashboard indicators](../../itsm-success-dashboard/task/install-success-dashboard.md).

<table id="table_okv_rp3_1vb"><thead><tr><th>

KPI

</th><th>

Formula

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Self-solved %

</td><td>

\[Self-solved \(VA, KB, QnA, Proactive Engagement\) + Automated resolutions\] / \[Total Tickets Resolution + Self-solved \(VA, KB, QnA, Proactive Engagement\) + Self service using Password Reset apps\]\*100

</td><td>

Self-solved percentage is calculated based on the daily average number of times your users achieved resolution without agent intervention. It includes numbers from the following items:-   Self-solved using Virtual Agent.
-   Self-solved using Knowledge articles.
-   Self-solved using QnA.
-   Self-solved using PE
-   Automated resolutions. This could be, for example, incidents that were auto-resolved using Virtual Agent.

</td></tr><tr><td>

Call deflection %

</td><td>

\[Catalog ticket submissions + VA ticket submissions + Self-solved \(VA, KB, QnA and Proactive Engagement\) + Self service using Password Reset apps\] / \[Total tickets submitted + Self-solved \(VA, KB, QnA and Proactive Engagement\) + Self service using Password Reset apps\]\*100

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

Count percentage of tickets that were completed and were structured. This could be, for example, a requested item fulfillment or an HR Case where payroll ambiguity was resolved.

</td></tr><tr><td>

Average CSAT \(Customer satisfaction survey\) scores

</td><td>

\[ITSM Customer Satisfaction Score\] + \[Virtual agent Customer Satisfaction score\]

</td><td>

Average of customer satisfaction scores based on the surveys conducted after the issue was resolved.**Note:** Both ITSM Customer Satisfaction score and VA Customer Satisfaction score are normalized with the base as 10.

</td></tr><tr><td>

MTTR – Average mean time to resolution

</td><td>

\[Time to resolve\]/\[Issues resolved\]/24

</td><td>

Mean time to resolve \(MTTR\) is calculated from daily average of the time between the ticket creation and ticket closure. Card displays average MTTR for the report range.

</td></tr><tr><td>

Breached SLA %

</td><td>

\[Issues resolved with breached SLAs\]/\[Issues resolved\]\*100

</td><td>

Breached Service Level Agreement \(SLA\) percentage is calculated from the daily average number of issues that were closed after having breached an SLA.

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

</td></tr><tr><td>

Productivity moments - Productivity in search per user

</td><td>

\[\[Productivity in search \(count\)\]\] / \[\[Average number of active users\]\]

</td><td>

Instances where ServiceNow capabilities like NLU, LLM, Knowledge Article, Walk-up experience, etc, helped either the agent or requester in improving their productivity.

</td></tr><tr><td>

Productivity moments - Productivity in routing per user

</td><td>

\[\[Productivity in routing \(count\)\]\] / \[\[Average number of active users\]\]

</td><td>

Instances where ServiceNow capabilities like NLU, LLM, Knowledge Article, Walk-up experience, etc, helped either the agent or requester in improving their productivity.

</td></tr><tr><td>

Productivity moments - Productivity in fulfilment per user

</td><td>

\[\[Productivity in fulfilment \(count\)\]\] / \[\[Average number of active users\]\]

</td><td>

Instances where ServiceNow capabilities like NLU, LLM, Knowledge Article, Walk-up experience, etc, helped either the agent or requester in improving their productivity.

</td></tr><tr><td>

Productivity moments - Productivity in knowledge article generation

</td><td>

\[\[Productivity in knowledge article generation\]\] / \[\[Average number of active users\]\]

</td><td>

Instances where ServiceNow capabilities like NLU, LLM, Knowledge Article, Walk-up experience, etc, helped either the agent or requester in improving their productivity.

</td></tr></tbody>
</table>For more information on Success Dashboard KPI definitions and formulas, see [ITSM Success Dashboard indicators KPI definitions and formulas](../../itsm-success-dashboard/concept/sd-kpi-formulae.md)

## Strategic Portfolio Management KPIs

Benchmarks supports Strategic Portfolio Management KPIs. You must install the [Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=it-business-management-bu-level&version=australia&pubname=australia-it-business-management&ft:locale=en-US) application to access the respective Benchmarks KPIs. For more information about the , see [SPM Benchmarking KPIs](https://www.servicenow.com/docs/access?context=spm-benchmarking-kpis&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

-   **[Configure KPI participation](../task/t_EnableABenchKPI.md)**  
Review and configure Benchmarks KPI participation by opting in or out of categorized KPIs.
-   **[Link or customize a benchmark KPI](../task/t_CustomBenchKPIConditions.md)**  
You can customize KPI conditions to fit the needs of your organization better.
-   **[Use Benchmarks data for value management analysis](../task/analyze-business-value-historical-data-benchmarks.md)**  
Manually collect historical Benchmarks data to analyze the benefits of year-over-year growth when you use the ServiceNow Benchmarks application.

**Parent Topic:**[Benchmarks](../reference/r_Benchmarks.md)

