---
title: Schedule suggestion pruning
description: Search Suggestions limits the number of auto-complete suggestions and search suggestions stored in the Search Suggestion \[sys\_search\_suggestion\] table to 500,000. A periodic pruning job removes the least relevant suggestions and increases the overall relevancy of suggestions.
locale: en-US
release: xanadu
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule suggestion pruning

Search Suggestions limits the number of auto-complete suggestions and search suggestions stored in the Search Suggestion \[sys\_search\_suggestion\] table to 500,000. A periodic pruning job removes the least relevant suggestions and increases the overall relevancy of suggestions.

## Before you begin

Role required: admin

## About this task

By default, the pruning job runs once a week and limits the Search Suggestion \[sys\_search\_suggestion\] table to 500,000 suggestions. Once the table reaches that limit, the pruning job removes the lowest-rated auto-complete suggestions and search suggestions to keep the maximum number of suggestions at 500,000. Pruning the least relevant suggestions improves the relevancy of the suggestions.

How often you run the pruning job might depend on how frequently you [generate suggestions from the Search Suggestion table](schedule-search-suggestion-builds.md), and how quickly the table exceeds 500,000 suggestions.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **Prune Search Suggestions** job.

3.  On the Scheduled Script Execution form, edit the following fields.

    |Field|Description|
    |-----|-----------|
    |Run|Frequency of execution for the pruning job. To execute the job manually, select **On Demand** and select **Execute Now**.|
    |Day|Day of the week to run the pruning job.|
    |Time zone|Time zone to use when interpreting the **Time** field value.|
    |Time|Time of day to run the pruning job. Specify hours \(00–23\), minutes \(00–59\), and seconds \(00–59\).|
    |Repeat interval|Interval between executions of the pruning job when **Run** is set to **Periodically**. Specify days \(01–07, where 01 is Sunday\), hours \(00–23\), minutes \(00–59\), and seconds \(00–59\).|
    |Conditional|Script to run when executing the pruning job.|

    **Note:** The fields on the form change with the choice of the **Run** value.

4.  Select **Update**.


