---
title: Scan Engine Team Lead dashboard
description: The Team Lead dashboard includes trend charts and the following overview modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-team-lead-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [Track Platform Health trends, Platform Health, Using Impact, Impact]
---

# Scan Engine Team Lead dashboard

The Team Lead dashboard includes trend charts and the following overview modules.

<table id="table_hrx_lll_fhc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total team technical debt

</td><td>

The amount of development time required to resolve all findings for the team.

</td></tr><tr><td>

Unapproved exceptions

</td><td>

The number of exceptions currently waiting to be approved or rejected.

</td></tr><tr><td>

Health score

</td><td>

-   The health score is a 0–100 metric reflecting your team's instance platform risk. It combines five independent category scores using fixed category weights so that higher severity findings influence the score more heavily than cosmetic issues.
-   Each category's score is computed independently and never affected by changes in other categories.
-   Each check compares its findings to a fixed reference point established when the definition was authored, not to the largest finding count in the scan. This ensures that fixing one issue never distorts the weight of an unrelated finding or shifts a category's score.
-   For a complete explanation of the four-step calculation model, category weights, and formulas, see [Platform Health score calculation model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-health-score-calculation.md).
-   The health score represents the percentage of definition occurrences used across the platform that did not return any findings.

 Definition occurrences refers to the total number of times a definition has been executed by the Scan Engine to generate findings.

</td></tr><tr><td>

Active scan engine definitions

</td><td>

The number of definitions currently being used by the Scan Engine.

</td></tr><tr><td>

Technical debt by category

</td><td>

The estimated amount of development time required to resolve all findings within each category for the entire team.

</td></tr><tr><td>

Open findings by developer

</td><td>

-   All open findings sorted by each developer on the team.
-   The value in the center is the total number of open findings for all selected developers.
-   Select a name to add or remove the developer from the chart.

</td></tr></tbody>
</table>## Team Lead trend charts

The Team Lead dashboard includes the following trend charts.

|Chart|Description|
|-----|-----------|
|Health Score trend|A trend line showing how your team's Platform Health score changes over time. The chart also displays the current individual category scores, so you can track which areas are improving or degrading.|
|Team technical debt trend|A trend line showing the total development time required to resolve all open findings for your team over time.|
|Technical debt by category trend|A stacked trend line showing technical debt broken down by category, so you can see which categories are driving the most effort.|

## Team Lead module data sources

|Module|Source table|
|------|------------|
|Total team technical debt|sn\_se\_summary\_scan\_detail|
|Unapproved exceptions|sn\_se\_exception|
|Health score|sn\_se\_scan\_result|
|Active definitions|sn\_se\_definition|
|Tech debt by category|sn\_se\_summary\_scan\_detail|
|Open findings by developer|sn\_se\_summary\_scan\_detail|

|Trend chart|Source table|
|-----------|------------|
|Health Score trend|sn\_se\_scan\_result|
|Team technical debt trend|sn\_se\_summary\_scan\_detail|
|Technical debt by category trend|sn\_se\_summary\_scan\_detail|

