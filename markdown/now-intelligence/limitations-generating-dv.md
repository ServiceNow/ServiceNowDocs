---
title: Limitations to generating data visualizations
description: While data visualization generation is designed to handle a wide range of queries and scenarios, certain cases are not supported or only partially supported.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generate visualizations, Platform Analytics in the Now Assist panel, Now Assist in Platform Analytics, Platform Analytics]
---

# Limitations to generating data visualizations

While data visualization generation is designed to handle a wide range of queries and scenarios, certain cases are not supported or only partially supported.

<table id="table_nzf_txn_zbc"><thead><tr><th>

Query contents

</th><th>

Example

</th><th>

Limitation

</th></tr></thead><tbody><tr><td>

Visualization type

</td><td>

"Show me a heatmap of open incidents by creation date"

</td><td>

Only the following visualization types are supported:-   Scores: single score, dial, gauge
-   Bar: horizontal and vertical bars
-   Donut, pie, and semi-donut
-   Time series: area, line, column, scatter, spline, step
-   List

</td></tr><tr><td>

Data source

</td><td>

"Show me open asset contracts"

</td><td>

Only table data sources listed in the Semantic Table Configuration table are supported. See [Add a table to the semantic data layer](../task/add-table-semantic-layer.md#).

</td></tr><tr><td>

Multiple Group By conditions

</td><td>

"Show me open incidents by group and state."

</td><td>

Data visualization generation will produce results, but only the first 'group by' clause \(group\) will be considered. The second 'group by' clause \(state\) will be ignored in the current output.

</td></tr><tr><td>

Multiple time periods

</td><td>

"Show me open incidents last week, month, and year."

</td><td>

Data visualization generation is currently unable to process queries that request data for multiple time periods simultaneously. Only one time period can be handled at a time.

</td></tr><tr><td>

Conflicting or complementary conditions

</td><td>

"Show me resolved and unresolved cases last week."

</td><td>

Data visualization generation detects only the first condition \(resolved\) under the state column. The second condition \(unresolved\) is misinterpreted and may be incorrectly mapped to another column or ignored.

</td></tr><tr><td>

Multiple data tables

</td><td>

“Show me high priority incidents, problems and changes”

</td><td>

Data visualization generation identifies only the first table and ignores the other ones.

</td></tr><tr><td>

Non-English queries

</td><td>

--

</td><td>

Only English is supported

</td></tr><tr><td>

Technical dashboards

</td><td>

--

</td><td>

Data visualizations can be added only to dashboards that are created in the inline editor. Technical dashboards are not supported.

</td></tr></tbody>
</table>## Possible ways to circumvent limitations

-   Simplify your queries by focusing on one 'group by' clause at a time.
-   Specify a single time period per query.
-   Avoid multiple conditions in a single query.

**Parent Topic:**[Generate visualizations in the Now Assist panel](../task/use-dv-generation.md)

