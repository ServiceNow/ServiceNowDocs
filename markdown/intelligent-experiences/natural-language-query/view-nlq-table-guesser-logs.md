---
title: View NLQ Table Guesser logs
description: Use the Table Guesser logs to review the CMDB tables that were picked by NLQ in response to plain-language queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/natural-language-query/view-nlq-table-guesser-logs.html
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

2.  Select the personalize list icon \(\[Omitted image "List\_PersonalizeListIcon.png"\] Alt text: personalize list icon\) to display the columns **Matched words to table names** and **Confidence scores**.\[Omitted image "view-nlq-table-guesser-logs010V.png"\] Alt text: The list view of the NLQ Table Guesser Query Logs module with some example rows.

    The **Utterance** column shows the user's natural language query.

3.  Use the information in the **Matched words to table names** column for troubleshooting if needed.

    In this column's value field, the first word was found in the utterance. Next is a list of the CMDB tables that were matched to that word.


## What to do next

For more information on CMDB queries, see [Exploring CMDB Query Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/querying-cmdb.md).

**Parent Topic:**[Configuring NLQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/natural-language-query/configuring-nlq.md)

**Related topics**  


[Create an NLQ synonym]()

[Create an NLQ shortcut]()

[View NLQ logs]()

