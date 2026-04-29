---
title: Chief Financial Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Financial Officer \(CFO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Financial Officer Dashboard indicators

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

Indicator source / Formula calculation / Additional conditions

</th></tr></thead><tbody><tr><td>

Portfolio Health

</td><td>

Variance by portfolio

</td><td>

 

</td><td>

Formula

</td><td>

\[\[PPM - Planned Cost\]\]-\[\[PPM - Actual Cost\]\]

</td></tr><tr><td>

Portfolio Health

</td><td>

PPM - Number of Active Projects With negative ROI

</td><td>

 

</td><td>

Automated

</td><td>

PPM.projects.activeCondition: Planned ROI % &lt; 0

</td></tr><tr><td>

Software Investment

</td><td>

% Spend in Use

</td><td>

 

</td><td>

Formula

</td><td>

100-\(\(\[\[Potential Savings\]\]+\[\[Over-licensed Amount\]\]\)/\[\[Software Spend\]\]\*100\)

</td></tr><tr><td>

Software Investment

</td><td>

Potential savings

</td><td>

 

</td><td>

Automated

</td><td>

SAM Removal Candidates Weekly-   Condition: Active = true
-   Calculation: Sum \(potential\_savings\)

</td></tr><tr><td>

Software Investment

</td><td>

Actual Savings Year-to-date

</td><td>

 

</td><td>

Automated

</td><td>

SAM Inactive Removal Candidates Monthly-   Additional conditions: State = Closed Complete and Closed on This month
-   Calculation: Sum \(potential\_savings\)

</td></tr><tr><td>

Procurement

</td><td>

Purchase Line Total Negotiated Savings

</td><td>

 

</td><td>

Formula

</td><td>

\[\[Purchase Line Negotiated Savings\]\] - \[\[Parent Line Negotiated Savings\]\]

</td></tr><tr><td>

Procurement

</td><td>

Number of Open Negotiations

</td><td>

 

</td><td>

Automated

</td><td>

Source: Negotiation.Open

</td></tr><tr><td>

Audit &amp; Risk

</td><td>

Total Net Loss

</td><td>

 

</td><td>

Automated

</td><td>

Risk.Event.Non.Rejected-   Condition: Event type = Financial Impact
-   Calculation: Sum \(net\_amount\)

</td></tr><tr><td>

Audit &amp; Risk

</td><td>

\# of events with impact &gt; 1 M

</td><td>

 

</td><td>

Automated

</td><td>

Risk.Event.Non.RejectedAdditional conditions: Event type = Financial Impact and Gross loss &gt; $1,000,000.00

</td></tr></tbody>
</table>