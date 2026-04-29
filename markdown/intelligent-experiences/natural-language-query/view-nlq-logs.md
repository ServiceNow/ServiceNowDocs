---
title: View NLQ logs
description: Review NLQ logs to see how the system has handled your users' plain-language requests. Use log records from attempted requests to expand NLQ synonyms or shortcuts.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring NLQ, Natural Language Query, Enable AI experiences]
---

# View NLQ logs

Review NLQ logs to see how the system has handled your users' plain-language requests. Use log records from attempted requests to expand NLQ synonyms or shortcuts.

## Before you begin

Role required: nlq\_admin, pa\_analyst, or admin

## About this task

Every natural language query is logged in the **NLQ Query Logs** table \[nlq\_query\_log\]. Each log entry provides details such as the table that was queried, whether the query succeeded, and how the results were generated. Other available fields include the following.

-   Output Source: how the results were generated. The value **BNF** indicates a rules-based method. The value **GAI** indicates the Now LLM Service \(fallback\) method.
-   Source: the location from which the query was initiated. The value **AC** indicates Analytics Overview. The value **CMDB\_WS** indicates CMDB Workspace.
-   Utterance: the original natural-language request which triggered NLQ.

## Procedure

1.  Navigate to **All** &gt; **NLQ** &gt; **Logs**.

    ![NLQ Query Logs list.](../images/view-nlq-logsT1.png)

2.  Select the value in the **Utterance** column to open the full log entry.

    ![Gif of a full NLQ log entry.](../images/view-nlq-logsW2.gif)


## What to do next

Based on your users' attempted queries, consider adding more [synonyms](create-nlq-synonym.md) or [shortcuts](create-nlq-shortcut.md).

**Parent Topic:**[Configuring NLQ](../concept/configuring-nlq.md)

**Related topics**  


[Create an NLQ synonym](create-nlq-synonym.md)

[Create an NLQ shortcut](create-nlq-shortcut.md)

[View NLQ Table Guesser logs](view-nlq-table-guesser-logs.md)

