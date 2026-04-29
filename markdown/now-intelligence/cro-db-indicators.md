---
title: Chief Risk Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Risk Officer \(CRO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Risk Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs all three kinds of indicators, Automated, Formula, and Manual. For more information about configuring indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Manual indicators](../../performance-analytics/task/t_CreateAManualIndicator.md)

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

Enterprise Risks

</td><td>

Entities at highest risk

</td><td>

sn\_cro\_dashboard

</td><td>

Automated

</td><td>

Entities at highest risk

</td></tr><tr><td>

Enterprise Risks

</td><td>

Net loss \(YTD\)

</td><td>

sn\_cro\_dashboard

</td><td>

Automated

</td><td>

Net loss \(YTD\)Calculation: Sum \(net\_amount\)

</td></tr><tr><td>

Enterprise Risks

</td><td>

Total Risks

</td><td>

sn\_cro\_dashboard

</td><td>

Automated

</td><td>

Total RisksCondition: Active = true

</td></tr><tr><td>

Enterprise Risks

</td><td>

Active Risk

</td><td>

sn\_risk

</td><td>

Automated

</td><td>

Active.Risk

</td></tr><tr><td>

Enterprise Issues

</td><td>

All Open Issues

</td><td>

sn\_grc

</td><td>

Automated

</td><td>

All Open Issues Quarterly

</td></tr><tr><td>

Enterprise Issues

</td><td>

All Unassigned Issues

</td><td>

sn\_grc

</td><td>

Automated

</td><td>

All Issues QuarterlyConditions: Assigned to is empty and Created on This quarter

</td></tr><tr><td>

Enterprise Issues

</td><td>

Issues Aging Indicator

</td><td>

 

</td><td>

Automated

</td><td>

All Open Issues QuarterlyConditions: Actual start date isn’t empty and Actual end date isn’t empty and Actual end date is more than 0 Hours after Actual start date

</td></tr><tr><td>

Enterprise Issues

</td><td>

Issues resolved

</td><td>

sn\_grc

</td><td>

Automated

</td><td>

Resolved Issues

</td></tr><tr><td>

Internal Audits

</td><td>

Open Audit Issue

</td><td>

sn\_audit

</td><td>

Automated

</td><td>

All Open Issues QuarterlyCondition: Top task Number starts with ENG

</td></tr><tr><td>

Internal Audits

</td><td>

Failed Controls

</td><td>

sn\_audit

</td><td>

Automated

</td><td>

Controls.With.Failed.ControlTest

</td></tr><tr><td>

Compliance

</td><td>

Authority document compliance score percentage daily

</td><td>

sn\_compliance

</td><td>

Automated

</td><td>

GRC document compliance status-   Conditions: Name Class = Authority document and Name Functional domain CONTAINS IT risk and compliance
-   Calculation: Average \(compliance\_score\)

</td></tr><tr><td>

Compliance

</td><td>

Policy Compliance Score Percentage

</td><td>

sn\_compliance

</td><td>

Automated

</td><td>

All Active Policies MonthlyCalculation: Average \(compliance\_score\)

</td></tr><tr><td>

Compliance

</td><td>

Authority document compliance score percentage

</td><td>

sn\_compliance

</td><td>

Automated

</td><td>

All Active Authority documents MonthlyCalculation: Average \(compliance\_score\)

</td></tr><tr><td>

BCM Governance

</td><td>

\# of global crisis events

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

BCM Governance

</td><td>

\# of global emergency response events

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

BCM Governance

</td><td>

Plan status

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

BCM Governance

</td><td>

Tests completed

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr></tbody>
</table>