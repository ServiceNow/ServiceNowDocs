---
title: Exploring Natural Language Query
description: NLQ is a ServiceNow AI Platform feature that is active by default. Use NLQ to query the data in your instance by entering plain language requests into the user interface.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Natural Language Query, Enable AI experiences]
---

# Exploring Natural Language Query

NLQ is a ServiceNow AI Platform feature that is active by default. Use NLQ to query the data in your instance by entering plain language requests into the user interface.

![This image shows the NLQ data flow for user input and processing.](../images/nlq-architecture.png "NLQ data flow for user input and processing")

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

Note that you must first activate the languages on your instance for NLQ to parse queries in those languages. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Using NLQ in other applications and features

Other ServiceNow® applications and features can consume NLQ functionality. See the following resources for more information.

<table id="table_bnd_lxw_xzb"><thead><tr><th>

Application or feature

</th><th>

Information

</th></tr></thead><tbody><tr><td>

Analytics Q &amp; A

</td><td>

[Create a report with Analytics Q&amp;A](https://www.servicenow.com/docs/access?context=t_CreateYourOwnReport&version=australia&pubname=australia-now-intelligence&section=create-report-nlq&ft:locale=en-US)

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Query your CMDB data without needing to know table relationships or data structures.-   [Querying the CMDB](https://www.servicenow.com/docs/access?context=querying-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Intelligent Search for CMDB](https://www.servicenow.com/docs/access?context=intelligent-search-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

English is the only supported language for CMDB.

</td></tr><tr><td>

NLQ with AI Search in global search

</td><td>

[NLQ Genius Results](https://www.servicenow.com/docs/access?context=genius-result-nlq-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) in AI Search \(supports English only\)

</td></tr><tr><td>

List V2

</td><td>

Filter through any platform list by entering in a plain-language request.

</td></tr></tbody>
</table>