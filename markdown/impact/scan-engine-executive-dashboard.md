---
title: Scan Engine Executive dashboard
description: The Executive dashboard includes trend charts and the following overview modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-executive-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [Track Platform Health trends, Platform Health, Using Impact, Impact]
---

# Scan Engine Executive dashboard

The Executive dashboard includes trend charts and the following overview modules.

<table id="table_afw_4vz_chc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outstanding technical debt

</td><td>

-   The total time required to resolve existing technical debt on your platform, based on the effort of a single developer. It does not include time for testing, validation, or other stages of the software development life-cycle \(SDLC\).
-   The graph line shows the trend of technical debt over a certain time period.
-   The time period shown depends on available data, with a maximum of 90 days of information displayed.

</td></tr><tr><td>

Technical debt prevented

</td><td>

-   Reflects the amount of technical debt prevented from entering the instance because of the Scan Engine's real-time prevention.
-   The graph line shows the trend of prevented technical debt over a certain time period.
-   The time period shown depends on available data, with a maximum of 90 days of information displayed.

</td></tr><tr><td>

Platform Health Score

</td><td>

-   A 0–100 metric showing your overall instance platform risk across five weighted categories.
-   Combines Security, Performance, Manageability, Upgradeability, and User Experience risk independently so that higher severity violations carry more weight than cosmetic issues.
-   Each category is scored separately and unaffected by changes in other categories, giving you a stable indicator of true platform health without false shifts.

 For the complete calculation model and category weights, see [Platform Health score calculation model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-health-score-calculation.md).

</td></tr><tr><td>

Instance adoption risk

</td><td>

-   An assessment of the risk of adopting the latest ServiceNow instance version.
-   Risk factors are identified based on the current state of your instance's platform health, including quality, compliance, security, and other standards.
-   The three levels of adoption risk are low, medium, and high.

</td></tr><tr><td>

Cost and time savings from remediation

</td><td>

-   Reflects the cost savings and time savings your organization has gained by remediating findings through the Scan Engine.
-   Cost savings are based on avoided downtime, prevented data breach expenses, and other remediation benefits.
-   The chart shows current cost and time savings, as well as trends over time.

</td></tr></tbody>
</table>## Executive trend charts

The Executive dashboard includes the following trend charts.

|Trend chart|Description|
|-----------|-----------|
|Technical debt trend|A trend line showing the total outstanding technical debt over time, compared against the technical debt prevented by the Scan Engine.|
|Platform Health Score trend|A trend line showing your overall Platform Health score over time, with the five category scores displayed so you can track which risk areas are improving or worsening.|
|Instance adoption risk trend|A trend line showing changes in your adoption risk level over time.|
|Cost and time savings trend|A trend line showing cumulative cost and time savings gained through remediation efforts.|

## Data sources

Modules and trend charts on the Executive dashboard source data from the sn\_se\_scan\_result \[sn\_se\_scan\_result\] table.

|Modules|Trend charts|
|-------|------------|
|Outstanding technical debt|Technical debt trend|
|Technical debt prevented|Platform Health Score trend|
|Platform Health Score|Instance adoption risk trend|
|Instance adoption risk|Cost and time savings trend|
|Cost and time savings from remediation| |

