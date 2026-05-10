---
title: Exploring Natural Language Query
description: NLQ is a ServiceNow AI Platform feature that is active by default. Use NLQ to query the data in your instance by entering plain language requests into the user interface.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 1
breadcrumb: [Natural Language Query, Enable AI experiences]
---

# Exploring Natural Language Query

NLQ is a ServiceNow AI Platform feature that is active by default. Use NLQ to query the data in your instance by entering plain language requests into the user interface.

ServiceNow® NLQ translates natural language user input into glide record queries. The queries are rendered into an executable structured format, such as a JavaScript Object Notation \(JSON\) file or a visual definition. The output, in whichever format, is the response to the user's request.

**Note:** When a user enters a request directly into the user interface \(UI\), the text of the request is called an utterance in tables such as NLQ logs.

NLQ is a ServiceNow AI Platform feature that is active by default and supports the following data operations:

-   Driving table suggestion​
-   Filtering​
-   Grouping and aggregations​
-   Sorting​
-   Data visualization \(single score, list, bar chart, pie chart, time series\)​
-   Business calendar
-   Single number
-   Multi-table

For more information, see [Using Natural Language Query](using-nlq.md).

NLQ doesn't support domain separation. It also doesn't support on-premise instances.

## Language support

NLQ supports American English by default. For all applications and features except CMDB, NLQ also supports queries in Spanish, French, French Canadian, German, and Japanese.

You must first activate the languages on your instance for NLQ to parse queries in those languages. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md).

## Using NLQ in other applications and features

Other ServiceNow® applications and features can consume NLQ functionality. See the following resources for more information.

<table id="table_bnd_lxw_xzb"><thead><tr><th>

Application or feature

</th><th>

Information

</th></tr></thead><tbody><tr><td>

Analytics Q &amp; A

</td><td>

[Create a report with Analytics Q&amp;A](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/t_CreateYourOwnReport.md)

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Query your CMDB data without needing to know table relationships or data structures.-   [Querying the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/querying-cmdb.md)
-   [Intelligent Search for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/intelligent-search-cmdb.md)

English is the only supported language for CMDB.

</td></tr><tr><td>

NLQ with AI Search in global search

</td><td>

[NLQ Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/genius-result-nlq-ais.md) in AI Search \(supports English only\)

</td></tr><tr><td>

List V2

</td><td>

Filter through any platform list by entering in a plain-language request.

</td></tr></tbody>
</table>