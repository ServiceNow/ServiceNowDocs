---
title: Platform Health score calculation model
description: Your Platform Health score is the foundation for understanding instance risk. The score reflects platform risk through a four-step, category-weighted calculation that combines findings into a single 0–100 health metric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/instance-health-score-calculation.html
release: brazil
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 3
keywords: [Instance Health Score, Platform Health, score calculation, category weights, Scan Engine]
breadcrumb: [Scan Engine reference, Impact reference, Impact]
---

# Platform Health score calculation model

Your Platform Health score is the foundation for understanding instance risk. The score reflects platform risk through a four-step, category-weighted calculation that combines findings into a single 0–100 health metric.

Each scoring category is evaluated independently, then combined into a single overall score using fixed category weights. A critical Security finding should not be weighted exactly the same as a cosmetic User Experience finding, and remediating a Performance issue should not alter your Upgradeability score.

|Step|What happens|Why it matters|
|----|------------|--------------|
|1. Fixed reference|Each check compares its own findings to a stable reference point established when the definition was authored, not to the largest finding count in that scan.|Fixing one check doesn't distort the weight of another.|
|2. Category scoring|Security, Performance, Manageability, Upgradeability, and User Experience are each scored independently, 0–100.|You can see exactly which category needs attention and why.|
|3. Weighted roll-up|Category scores combine into one overall Platform Health score, weighted by how much each category matters to your risk.|Security counts more than a cosmetic issue.|
|4. Same scope for Full and Delta|Full and delta scans count findings on the same instance-wide basis. See [Full and delta scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md) for more information on scans.|Your score means the same thing, regardless of scan type.|

## Formulas

Here are the four steps translated into the actual calculations.

<table id="table_formulas"><thead><tr><th>

Step

</th><th>

Formula

</th><th>

What it computes

</th></tr></thead><tbody><tr><td>

1. Magnitude

</td><td>

`Magnitude = min(2, 1 + ln(1+F) ÷ ln(1+R))`**Note:** Magnitude = 0 when F = 0, and is capped at 2 after F reaches R. This is the natural logarithm.

</td><td>

How widely a check fired, capped at 2× so one check can't dominate its category.

</td></tr><tr><td>

2. Weighted penalty

</td><td>

`Penalty = W × Magnitude`

</td><td>

The check's own contribution to its category's burden.

</td></tr><tr><td>

3. Category health

</td><td>

`CategoryHealth = clamp(100 × (1 − ΣPenalty ÷ ΣCeiling), 0, 100)`

</td><td>

A 0–100 health score for that category alone, unaffected by any other category.

</td></tr><tr><td>

4. Overall score

</td><td>

`Score = Σ (CategoryWeight × CategoryHealth)`

</td><td>

Category scores combined into one Platform Health score, weighted by importance.

</td></tr></tbody>
</table>Where:

-   F: The number of records a check found.
-   R: The check's stable reference point. R is not set per definition. It is a fixed tier: 10 for checks that return one finding for an entire table, 20,000 for all others.
-   W: The check's own weight, based on its severity and impact.
-   *Category Weight*: The category's share of overall risk, shown in the following category weights table.
-   ΣPenalty: The sum of all weighted penalties in that category.
-   ΣCeiling: 2 × W for every active check in the category, whether or not it fired.

## How categories are weighted

Category weighting reflects how much risk each area typically represents across the check library. These weights are applied only at the final roll-up step, so a change in one category's findings won't distort the calculated health of another category. See [Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-definitions.md) for their definitions.

|Category|Weighting|Description|
|--------|---------|-----------|
|Security|~40%|The highest-consequence category, encompassing breach risk, compliance violations, and access-control vulnerabilities.|
|Performance|~22%|Affects every user on the instance and compounds if left unaddressed.|
|Manageability|~19%|The largest category by volume, impacting administration and supportability.|
|Upgradeability|~9%|Smaller in volume but can block or delay ServiceNow release upgrades.|
|User Experience|~9%|Important to adoption and satisfaction, but carries the lowest urgency overall.|

**Note:** Publishing new definitions does not change the score on its own.

## Related concepts

For more information, see the following:

-   [Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-definitions.md) — Category definitions and their weights
-   [Scan Engine Executive dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-executive-dashboard.md)
-   [Scan Engine Platform Owner dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-platform-owner-dashboard.md)
-   [Scan Engine Team Lead dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-team-lead-dashboard.md)

**Parent Topic:**[Scan Engine reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-reference.md)

