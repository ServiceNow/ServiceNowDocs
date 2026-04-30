---
title: Limitations to generating data visualizations
description: While Analytics Generation is designed to handle a wide range of queries and scenarios, certain cases are currently not supported or only partially supported.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use Analytics Generation, Analytics Generation, Platform Analytics]
---

# Limitations to generating data visualizations

While Analytics Generation is designed to handle a wide range of queries and scenarios, certain cases are currently not supported or only partially supported.

<table id="table_nzf_txn_zbc"><thead><tr><th>

Query contents

</th><th>

Example

</th><th>

Limitation

</th></tr></thead><tbody><tr><td>

Chart type

</td><td>

"Show me a line chart of open incidents for the last 3 months."

</td><td>

Only the following chart types are supported:-   Scores: single score, dial, gauge
-   Bar: horizontal and vertical bars
-   Pie/donut
-   Time series: area, line, column, scatter, spline, step
-   Simple list

</td></tr><tr><td>

Data source

</td><td>

"Show me open problems"

</td><td>

Only table data sources in the Task table hierarchy are supported.

</td></tr><tr><td>

Multiple Group By conditions

</td><td>

"Show me open incidents by group and state."

</td><td>

Analytics Generation will produce results, but only the first 'group by' clause \(group\) will be considered. The second 'group by' clause \(state\) will be ignored in the current output.

</td></tr><tr><td>

Multiple time periods

</td><td>

"Show me open incidents last week, month, and year."

</td><td>

Analytics Generation is currently unable to process queries that request data for multiple time periods simultaneously. Only one time period can be handled at a time.

</td></tr><tr><td>

Conflicting or complementary conditions

</td><td>

"Show me resolved and unresolved cases last week."

</td><td>

Analytics Generation detects only the first condition \(resolved\) under the state column. The second condition \(unresolved\) is misinterpreted and may be incorrectly mapped to another column or ignored.

</td></tr><tr><td>

Multiple data tables

</td><td>

“Show me high priority incidents, problems and changes”

</td><td>

Analytics Generation identifies only the first table and ignores the other ones.

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

**Parent Topic:**[Use Analytics Generation](../task/use-dv-generation.md)

