---
title: Chief Information Security Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Information Security Officer \(CISO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Information Security Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs Automated and Formula indicators. For more information about configuring these indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Formula indicators](../../performance-analytics/concept/formula-indicators.md)

<table id="table_zcc_dry_mgc"><thead><tr><th>

Column

</th><th>

Indicator

</th><th>

Source plugin

</th><th>

Indicator type

</th><th>

Indicator Source / Formula calculation / Additional conditions

</th></tr></thead><tbody><tr><td>

Risk Exposure

</td><td>

Total Risks

</td><td>

sn\_ciso\_dashboard

</td><td>

Automated

</td><td>

Source: RisksConditions: Active = true

</td></tr><tr><td>

Risk Exposure

</td><td>

Net Loss

</td><td>

sn\_ciso\_dashboard

</td><td>

Automated

</td><td>

Source: Risks-   Conditions: Created on This year or Acceptance end date on This year
-   Calculation: Sum \(calculated\_ale\)

</td></tr><tr><td>

Compliance

</td><td>

Authority document compliance score percentage

</td><td>

sn\_compliance

</td><td>

Automated

</td><td>

Source: All Active Authority documents MonthlyCalculation: Average \(compliance\_score\)

</td></tr><tr><td>

Compliance

</td><td>

Policy Compliance Score Percentage

</td><td>

sn\_compliance

</td><td>

Automated

</td><td>

Source: All Active Policies MonthlyCalculation: Average \(compliance\_score\)

</td></tr><tr><td>

Security Incidents

</td><td>

Overdue Security Incidents

</td><td>

sn\_ciso\_dashboard

</td><td>

Automated

</td><td>

Active Security IncidentsConditions: expected\_end&lt;javascript:gs.beginningOfToday\(\)

</td></tr><tr><td>

Security Incidents

</td><td>

\[CISO\] Average monthly close time of security incidents

</td><td>

sn\_sir\_analytics

</td><td>

Formula

</td><td>

Calculation: \[\[Average close time of security incidents / By month SUM +\]\]

</td></tr><tr><td>

Security Incidents

</td><td>

SI - Total Incident Count

</td><td>

sn\_sir\_analytics

</td><td>

Automated

</td><td>

Source: SI - Impacted Services

</td></tr><tr><td>

Vulnerabilities

</td><td>

Non-Deferred Overdue Critical Vulnerable Items

</td><td>

sn\_vul\_analytics

</td><td>

Automated

</td><td>

Risk rating = 1 - Critical and Remediation target &lt; Today and State not in Deferred

</td></tr><tr><td>

Vulnerabilities

</td><td>

Vulnerable Items Mean Time to Remediate

</td><td>

sn\_vul\_analytics

</td><td>

Formula

</td><td>

\[\[Total Duration of Closed Vulnerable Items\]\] / \[\[Closed Vulnerable Items\]\]

</td></tr><tr><td>

Vulnerabilities

</td><td>

Vulnerable Items

</td><td>

sn\_vul\_analytics

</td><td>

Automated

</td><td>

Source: VI.Active

</td></tr><tr><td>

Audits

</td><td>

Overdue Audit Tasks

</td><td>

sn\_ciso\_dashboard

</td><td>

Automated

</td><td>

Source: Open Audit TasksConditions: Planned end date &lt; Today

</td></tr><tr><td>

Audits

</td><td>

Open audit tasks

</td><td>

sn\_ciso\_dashboard

</td><td>

Automated

</td><td>

Source: Open Audit Tasks

</td></tr></tbody>
</table>