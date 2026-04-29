---
title: Chief Digital Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Digital Officer \(CDO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Digital Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs all three kinds of indicators, Automated, Formula, and Manual. For more information about configuring indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Formula indicators](../../performance-analytics/concept/formula-indicators.md)
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

Sentiment

</td><td>

cSAT

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Sentiment

</td><td>

Responders

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Usage

</td><td>

MAU

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Usage

</td><td>

Hits

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Operations

</td><td>

P1 Incidents

</td><td>

 

</td><td>

Automated

</td><td>

Source: IncidentsConditions: Closed on This month and Priority = 1 - Critical

</td></tr><tr><td>

Operations

</td><td>

CDO: % incidents resolved in time

</td><td>

 

</td><td>

Formula

</td><td>

\(\[\[CDO: Number of incidents resolved in time / By month SUM +\]\] / \[\[CDO :Number of incidents resolved that should have been resolved in time / By month SUM +\]\]\) \* 100

</td></tr><tr><td>

Transformation

</td><td>

Self service %

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Transformation

</td><td>

Automation %

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Outcome

</td><td>

Cost Savings

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr><tr><td>

Outcome

</td><td>

Total Spend

</td><td>

 

</td><td>

Manual

</td><td>

 

</td></tr></tbody>
</table>