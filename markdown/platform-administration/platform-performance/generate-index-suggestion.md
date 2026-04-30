---
title: Generate an index suggestion for a slow query
description: Use the Index Suggestion Engine \(ISE\) to generate an index suggestion for a slow query. The ISE analyzes slow queries and provides index recommendations to improve execution time when possible.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Resolving slow queries, Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Generate an index suggestion for a slow query

Use the Index Suggestion Engine \(ISE\) to generate an index suggestion for a slow query. The ISE analyzes slow queries and provides index recommendations to improve execution time when possible.

## Before you begin

Role required: admin

## About this task

When the ISE generates an index suggestion for a slow query, it reviews query metrics and information from tables in the query. If the ISE doesn’t have the information required to generate an index suggestion, the system displays messages informing you about the data needed. These messages typically provide links for obtaining more information, such as updated query metrics or gathering column statistics from tables in the query. Sometimes the ISE might be unable to provide a recommended index for the query and lets you know why the suggestion can’t be generated.

## Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Stats** &gt; **Slow Queries**.

2.  In the Slow Queries table, select the query record for which you want to generate an index suggestion.

3.  In the Slow Queries record, select **Suggest Index**.

    If more information is needed to generate a suggestion, the system might display one or more messages with details for obtaining that information. After you respond to each message, select **Suggest Index**. Repeat this process until the ISE has the information required to generate the index suggestion.

    For example, the following information might be needed to generate a suggestion:

    -   Recent metrics—If the system displays a message indicating that query metrics are outdated, the message provides a link for obtaining the most recent metrics.
        -   Select the link to get the updated query metrics.
        -   Select **Suggest Index**.
    -   Column statistics—If the column statistics don’t exist for the query, the system displays a message asking you to schedule the Collect Column Stats job. You can choose to run the job at the default time when the system is less busy, or you can have the system collect the statistics immediately.
        -   If you schedule the Column Stats job to run later, the ISE generates the index suggestion after it collects the column statistics. After the column stats job runs, return to the Slow Queries record and select **Suggest Index**.
        -   If you choose to collect column stats immediately, the system displays the Collect Column Statistics progress indicator while it gathers column statistics. In the Slow Queries record, select **Suggest Index**.
    When the ISE successfully generates an index suggestion, the Index Suggestion record for the query shows the index **State** as **Suggested**.

4.  If you want to continue working with the index suggestion, select the next processing step.

    |Option|Description|
    |------|-----------|
    |**Export**|Downloads the index suggestion as an .xml file so that you can [export it to a non-production instance for testing and evaluation](export-index-suggestion.md).|
    |**Ignore**|Sets the index suggestion state to Ignore, which indicates that the index suggestion isn’t to be used. Index suggestions with an Ignore state are listed in the **Index Suggestions &gt; Done** view of the Index Suggestion table.|
    |**Schedule creation**|Opens the Schedule Index Creation window for [scheduling index creation](create-index-slowquery.md).|


**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

