---
title: AI Search dashboard
description: The AI Search dashboard summarizes AI Search indexed documents, configuration settings in use, and search query traffic. An interactive filter enables users to select the time frame for analysis of search query traffic.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search dashboard

The AI Search dashboard summarizes AI Search indexed documents, configuration settings in use, and search query traffic. An interactive filter enables users to select the time frame for analysis of search query traffic.

![AI Search dashboard showing AI Search Index tab.](../image/adv-ais-mgmt-dashboard-index-index.png "AI Search dashboard - AI Search Index tab")

![AI Search dashboard showing AI Search Query tab.](../image/adv-ais-mgmt-dashboard-index-query.png "AI Search dashboard - AI Search Query tab")

To access the dashboard, navigate to **All** &gt; **AI Search** &gt; **AI Search Analytics** &gt; **Search Index Analytics**.

**Note:** If the dashboard displays a `Read operation on table '<name>' from scope 'Advanced AI Search Management Tools' was denied` informational message, ask your administrator to perform the steps described in [Create a cross-scope access privilege for the AI Search dashboards](ais-dashboards-cross-scope-access.md) for the listed table.

## Required ServiceNow AI Platform® roles

To view or edit the dashboard, you must have the ais\_admin role.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|AI Search administrator|Reviews indexed record counts and follows search query traffic trends for AI Search.|

## Data visualizations

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TotalIndexed Documents

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

sn\_ais\_admin\_tools\_st\_ai\_search\_index\_analytics\_latest\_index\_stats

</td><td>

Shows the total number of records indexed by AI Search. **Note:** Because search source filters can exclude indexed records, this number may exceed the total number of searchable records in the index.

</td></tr><tr><td>

Documents by Indexed Source

</td><td>

Donut ![](../../performance-analytics/image/donut-icon.png)

</td><td>

sn\_ais\_admin\_tools\_ai\_search\_dashboard\_total\_indexed\_documents

</td><td>

Shows the number of records indexed by AI Search, grouped by indexed source. To drill down and view the number of records for an indexed source grouped by source table, select the graph segment for that indexed source. Refresh the report to return to the top-level view.

 **Note:** Because search source filters can exclude indexed records, the number of records reported for an indexed source may exceed the total number of searchable records from that indexed source.

</td></tr><tr><td>

Search Profiles

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

ais\_search\_profile

</td><td>

Shows the number of search profiles defined in AI Search.

</td></tr><tr><td>

Indexed Sources

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

ais\_datasource

</td><td>

Shows the number of indexed sources defined in the AI Search index.

</td></tr><tr><td>

Search Applications

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

sys\_search\_context\_config

</td><td>

Shows the number of search application configurations defined that use the AI Search search engine.

</td></tr><tr><td>

Dictionaries

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

ais\_dictionary

</td><td>

Shows the number of synonym and stop word dictionaries defined in AI Search.

</td></tr><tr><td>

Configured Genius Results

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

ais\_genius\_result\_configuration

</td><td>

Shows the number of Genius Result configurations defined in AI Search.

</td></tr><tr><td>

Results Improvement Rules

</td><td>

Single Score ![](../../../reuse/reporting/image/single-score.svg)

</td><td>

ais\_rule

</td><td>

Shows the number of result improvement rules defined in AI Search.

</td></tr><tr><td>

Documents by Search Profile

</td><td>

Bar ![](../../performance-analytics/image/column-icon.png)

</td><td>

sn\_ais\_admin\_tools\_ai\_search\_dashboard\_documents\_by\_search\_profile

</td><td>

Shows the number of indexed records searchable through each search profile defined in AI Search.

</td></tr><tr><td>

IndexedDocuments by Month

</td><td>

Bar ![](../../performance-analytics/image/column-icon.png)

</td><td>

sn\_ais\_admin\_tools\_ai\_search\_dashboard\_documents\_by\_month

</td><td>

Shows the number of newly indexed records grouped by month.

</td></tr></tbody>
</table>|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Queries by Search Profile|Donut ![](../../performance-analytics/image/donut-icon.png)|sys\_search\_event|Shows the number of search queries in the selected time frame, grouped by search profile used.|
|Queries by Language|Donut ![](../../performance-analytics/image/donut-icon.png)|sys\_search\_event|Shows the number of search queries in the selected time frame, grouped by query language \(ServiceNow AI Platform language context\).|
|Queries Run Against Index|Line ![](../../performance-analytics/image/line-icon.png)|sys\_search\_event|Shows the number of search queries in the selected time frame, grouped by month.|

