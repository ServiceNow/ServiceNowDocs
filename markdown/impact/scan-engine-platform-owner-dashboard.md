---
title: Scan Engine Platform Owner dashboard
description: The Platform Owner dashboard includes trend charts and the following overview modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-platform-owner-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 2
breadcrumb: [Track Platform Health trends, Platform Health, Using Impact, Impact]
---

# Scan Engine Platform Owner dashboard

The Platform Owner dashboard includes trend charts and the following overview modules.

<table id="table_lyk_4jl_fhc"><thead><tr><th>

Information module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Outstanding findings

</td><td>

The number of unresolved findings identified by the Scan Engine that have not been addressed.

</td></tr><tr><td>

Health score

</td><td>

-   A 0–100 metric reflecting your instance's overall platform risk.
-   Combines five independent category scores — using fixed category weights so that higher severity findings influence the score more heavily than cosmetic issues.
-   Each category's score is computed independently and never affected by changes in other categories.
-   Each check compares its findings to a fixed reference point established when the definition was authored, not to the largest finding count in the scan. This ensures that fixing one issue never distorts the weight of an unrelated finding or shifts a category's score.

 For a complete explanation of the four-step calculation model, category weights, and formulas, see [Platform Health score calculation model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-health-score-calculation.md).

</td></tr><tr><td>

Lines of code scanned

</td><td>

-   The total number of lines of code analyzed by the Scan Engine.
-   Includes all script field code and any scanned base system records.

</td></tr><tr><td>

In progress update sets

</td><td>

The number of unfinished update sets currently being worked on by developers.

</td></tr><tr><td>

Findings by impact to instance

</td><td>

-   The total findings for the instance, grouped by impact to instance.
-   Impacts to instance range from 1 \(minor impact\) to 10 \(significant impact\). You can select a bar on the chart to list the findings for that impact to the instance in a new browser tab.

</td></tr><tr><td>

Open findings by team

</td><td>

-   All available teams configured on the instance through the **Team Leads** related list on the **Scan Engine Properties** page.
-   Select a team from the list to show their corresponding information in the module and trend charts.
-   The number next to the team name is the number of open findings held by that team.

</td></tr></tbody>
</table>## Platform Owner trend charts

The Platform Owner dashboard includes the following trend charts.

|Chart|Description|
|-----|-----------|
|Health Score trend|A trend line showing how your overall Platform Health score changes over time. The chart also displays the current individual category scores, so you can track which areas are improving or degrading.|
|Outstanding findings trend|A trend line showing the total number of unresolved findings over time.|
|Lines of code scanned trend|A trend line showing the volume of code analyzed by the Scan Engine over time.|

## Platform Owner module data sources

|Module|Source table|
|------|------------|
|Outstanding findings|sn\_se\_summary\_scan\_detail|
|Health score|sn\_se\_scan\_result|
|Lines of code scanned|sn\_se\_scan\_result|
|In progress update sets|sn\_se\_scan\_result|
|Findings by impact to instance|sn\_se\_summary\_scan\_detail|
|Open findings by team|sn\_se\_summary\_scan\_detail|

|Trend chart|Source table|
|-----------|------------|
|Health Score trend|sn\_se\_scan\_result|
|Outstanding findings trend|sn\_se\_summary\_scan\_detail|
|Lines of code scanned trend|sn\_se\_scan\_result|

