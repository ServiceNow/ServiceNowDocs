---
title: Chief Human Resources Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Chief Human Resources Officer \(CHRO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Human Resources Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs all three kinds of indicators, Automated, Formula, and Manual. For more information about configuring indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Formula indicators](../../performance-analytics/concept/formula-indicators.md)
-   [Manual indicators](../../performance-analytics/task/t_CreateAManualIndicator.md)

## Operations tab

<table id="table_zcc_dry_mgc"><thead><tr><th>

Column

</th><th>

Indicator

</th><th>

Source plugin

</th><th>

Indicator type

</th><th>

Indicator Source or Formula calculation

</th></tr></thead><tbody><tr><td>

Onboarding

</td><td>

Average age of closed onboarding cases

</td><td>

 

</td><td>

Formula

</td><td>

\[\[Summed duration of closed cases &gt; Lifecycle Event Type.Event type = Onboarding\]\]/\[\[Number of closed HR Cases &gt; Lifecycle Event Type.Event type = Onboarding\]\]/24

</td></tr><tr><td>

Care

</td><td>

Average age of closed cases

</td><td>

 

</td><td>

Formula

</td><td>

\[\[Summed duration of closed cases\]\]/\[\[Number of closed HR Cases\]\]/24

</td></tr><tr><td>

Care

</td><td>

Number of open cases

</td><td>

 

</td><td>

Automated

</td><td>

HR.Case.Open

</td></tr><tr><td>

Continuous Improvement

</td><td>

Number of open cases with breached SLAs

</td><td>

 

</td><td>

Automated

</td><td>

HR.Case.Open

</td></tr><tr><td>

Continuous Improvement

</td><td>

Number of unassigned open cases

</td><td>

 

</td><td>

Automated

</td><td>

HR.Case.OpenCondition: Assigned to is empty

</td></tr><tr><td>

Satisfaction

</td><td>

Average case survey score

</td><td>

 

</td><td>

Automated

</td><td>

HR.Case.Survey.MetricCalculation: Average \(amr\_actual\_value\)

</td></tr><tr><td>

Relations

</td><td>

ERCases.Open

</td><td>

 

</td><td>

Automated

</td><td>

ERCases.OpenCalculation: Count Distinct \(c\_sys\_id\)

</td></tr><tr><td>

Relations

</td><td>

ERCases.PastSLA

</td><td>

 

</td><td>

Automated

</td><td>

ERCases.OpenCalculation: SLA due &lt; Today

</td></tr></tbody>
</table>## People tab

All of the indicators on this tab are manual, meaning that they are based on data that you enter manually on the associated score sheet. For more information on populating manual indicators, see [Add or edit indicator scores manually](../../performance-analytics/task/t_ManuallyAddingScoresForIndicators.md).

|Column|Indicator|Source plugin|Indicator Type|Formula calculation|
|------|---------|-------------|--------------|-------------------|
|Grow|Headcount| |Manual| |
|Grow|Time to fill| |Manual| |
|Grow|Internal hires as a % of total hires| |Manual| |
|Grow|Time to fill trend| |Manual| |
|Develop|Ramp up completion rate| |Manual| |
|Develop|Training effectiveness| |Manual| |
|Develop|% of employees submitted goals| |Manual| |
|Develop|Promotion rate by job level| |Manual| |
|Diversify|DEI index| |Manual| |
|Diversify|Women representation| |Manual| |
|Diversify|Gender \(global women\) by job level| |Manual| |
|Diversify|Race and Ethnicity by job level| |Manual| |
|Empower|Regrettable attrition| |Manual| |
|Empower|Employee per HR staff| |Manual| |
|Empower|Persona mix| |Manual| |
|Empower|Hiring mix| |Manual| |
|Reward|Recognition| |Manual| |
|Reward|Rewards| |Manual| |
|Reward|Revenue per employee| |Manual| |
|Reward|OTE\(On Target Earnings\) per employee| |Manual| |

