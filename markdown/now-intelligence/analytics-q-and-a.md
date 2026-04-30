---
title: Analytics Q&amp;A
description: You can make natural language queries related to indicators, tables, or columns from the Analytics Q&amp;A in the Analytics Center.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Analytics Center, Platform Analytics experience, Platform Analytics]
---

# Analytics Q&amp;A

You can make natural language queries related to indicators, tables, or columns from the Analytics Q&amp;A in the Analytics Center.

Analytics Q&amp;A supports the following languages:

-   English
-   French
-   Canadian French
-   Spanish
-   German
-   Japanese

This feature is not available in sessions that use an unsupported language.

**Note:** Analytics Q&amp;A is also available in the classic environment, in Report Designer. For more information, see [Create a report with Analytics Q&amp;A](../../reporting/task/t_CreateYourOwnReport.md#)

## Entering queries

![Image showing the line for entering queries, a link for pop-up examples, and a link to a keywords guide](../image/analytics-qna.png "Analytics Q&A before you enter a query")

As you type in a query, Analytics Q&amp;A suggests recent searches, indicators, tables, and columns that match what you have typed so far. Only the tables and columns to which you have access are shown.

![Five suggestions from typing in the word incident](../image/analytics-center-suggestions.png)

## Selecting from several likely tables

If Analytics Q&amp;A cannot determine which table you want, it shows you up to three likely tables. In the following screenshot, the user has asked for assets grouped by asset tag and displayed as a bar visualization. However, the system cannot determine whether the user is interested in the Asset \[alm\_asset\], the Key Value \[cmdb\_key\_value\], or the Tag \[label\] table.

![The three tables that the system thinks your query might be asking about](../image/analytics-center-table-guesser.png "Refining search to select table")

## Results

If your query is successful, Analytics Q&amp;A shows your result as whichever of the following visualizations you specified. If you do not specify a visualization, Analytics Q&amp;A determines which visualization is the most appropriate:

-   List
-   Trend
-   Single score
-   Bar
-   Pie

The results are subject to an ACL security check against your roles. Visualizations based on tables follow Reporting security. Visualizations based on Performance Analytics follow PA security.

The following example shows the results of a query where you specify a breakdown for grouping the results. Analytics Q&amp;A determines that the query matches an indicator. Because indicators show trends over time, Analytics Q&amp;A determines that a trend line is the appropriate visualization:

![Analytics Q&A results with details](../image/analytics-center-results-w-details.png "Analytics Q&A results")

If you do not want to see the change in scores over time, click **Click here to see only the current data**. Analytics Q&amp;A returns the current values on the underlying table instead of the indicator scores.

![The results of a successful query in the Analytics Q&A](../image/analytics-center-result.png "Analytics Q&A latest score results")

Hold your cursor over the chart to get more information about breakdowns. In a time series trend, you get the values for all the breakdowns on the selected day. In a column chart of the latest scores, you get the score of the breakdown you select. If the result is a visualization for an indicator, click on a value to open the indicator in KPI Details.

By default, you also see the following details if they apply:

-   Which table you are querying
-   The unit for the values
-   The data aggregation method
-   Which column you are grouping by
-   What date field you are measuring the trend by, and at what frequency
-   Which additional conditions you want to apply to your query

Lastly, you can send feedback on your query results by selecting thumbs up or down.

**Note:** If you only select one item from the suggestion or indicator or table, the feedback option is not available. By selecting only one item, you do not use the query parser. By not using the query parser, you do not create a query log. The feedback is attached to the query log, but the log must already exist.

## New queries

To make a new query or view a list of your KPIs, click **Back**. Returning to the Analytics Center updates your list of the last five successful queries.

## How to make a valid query

When you write a query, use special keywords to denote the type and range of information you are looking for, filters you want to apply, and other parameters. To see a full list of keywords and their uses, click **How can I improve my results?**.

You can ask your ServiceNow AI Platform administrator to add synonyms and semantic shortcuts for keywords. For more information, see [Create an NLQ synonym](https://www.servicenow.com/docs/access?context=create-nlq-synonym&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Create an NLQ shortcut](https://www.servicenow.com/docs/access?context=create-nlq-shortcut&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

![A guide you can open from the Analytics Q&A dialog that explains the keywords](../image/analytics-center-keywords.png "Keywords guide")

