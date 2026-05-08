---
title: View NLQ Table Guesser logs
description: Use the Table Guesser logs to review the CMDB tables that were picked by NLQ in response to plain-language queries.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring NLQ, Natural Language Query, Enable AI experiences]
---

# View NLQ Table Guesser logs

Use the Table Guesser logs to review the CMDB tables that were picked by NLQ in response to plain-language queries.

## Before you begin

This module is read-only.

Role required: nlq\_admin.

## About this task

When a plain-language request for CMDB data is parsed by NLQ, the system tries to determine the specific tables the user intended. The system's guesses, including confidence levels, are recorded in the NLQ Table Guesser logs module \[nlq\_table\_guesser\_log\].

Review these logs to troubleshoot which CMDB tables were inferred by NLQ.

**Note:** This list is read-only for NLQ admins. There are no buttons or actionable functions in the UI.

## Procedure

1.  Navigate to **All** &gt; **NLQ** &gt; **Table Guesser Logs**.

2.  Select the personalize list icon \(![personalize list icon](../../../common/image/List_PersonalizeListIcon.png)\) to display the columns **Matched words to table names** and **Confidence scores**.![The list view of the NLQ Table Guesser Query Logs module with some example rows.](../images/view-nlq-table-guesser-logs010V.png)

    The **Utterance** column shows the user's natural language query.

3.  Use the information in the **Matched words to table names** column for troubleshooting if needed.

    In this column's value field, the first word was found in the utterance. Next is a list of the CMDB tables that were matched to that word.


## What to do next

For more information on CMDB queries, see Exploring CMDB Query Builder.

**Parent Topic:**[Configuring NLQ](../concept/configuring-nlq.md)

**Related topics**  


[Create an NLQ synonym](create-nlq-synonym.md)

[Create an NLQ shortcut](create-nlq-shortcut.md)

[View NLQ logs](view-nlq-logs.md)

