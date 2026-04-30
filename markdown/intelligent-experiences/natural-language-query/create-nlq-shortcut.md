---
title: Create an NLQ shortcut
description: Create a semantic shortcut to help improve the ability of NLQ to recognize the various ways your users request data. Semantic shortcuts operate similarly to NLQ synonyms by mapping common words to columns, but for a selected table when certain conditions are met.
locale: en-US
release: yokohama
product: Natural Language Query
classification: natural-language-query
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring NLQ, Natural Language Query, Enable AI experiences]
---

# Create an NLQ shortcut

Create a semantic shortcut to help improve the ability of NLQ to recognize the various ways your users request data. Semantic shortcuts operate similarly to NLQ synonyms by mapping common words to columns, but for a selected table when certain conditions are met.

## Before you begin

Role required: admin, nlq\_admin, or pa\_analyst

## About this task

Like NLQ synonyms, semantic shortcuts enable you to map common words in your users' requests to the columns in your instance tables. When these words are detected in natural-language queries, NLQ replaces them with actual column and table names, then submits the formal query.

Semantic shortcuts provide a condition builder so that you can filter which records are covered by the terms you provide.

Some semantic shortcuts are provided in the base system, and you can add more for your use cases and business requirements. Review NLQ logs of actual user utterances to find possible terms to add. For more information, see [View NLQ logs](view-nlq-logs.md).

You can create a new shortcut, or modify an existing shortcut, as follows.

-   If any shortcut already exists for your target table and filter conditions, you must add your new shortcut to the current record. Separate multiple shortcuts with a comma.
-   Shortcuts can point to reference fields, using dot-walking. For more information, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
-   Synonyms are case-insensitive in queries.
-   Synonyms can contain apostrophes and periods, but not commas.
-   Synonym and shortcut records are associated to one table. You can associate the same synonym term to more than one table, but you must create a record for each table.

## Procedure

1.  Ensure that you are in the application scope that you want for your shortcut, then navigate to **All** &gt; **NLQ** &gt; **Semantic Shortcuts**.

2.  Select **New**.

    If you are updating an existing record, select its row in the list.

3.  On the form, fill in the fields.

<table id="table_wl2_w4w_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Source table.

 You can use the same term for more than one table, but you must create a record for each table. The synonym's mapping is unique to the table.

</td></tr><tr><td>

Conditions

</td><td>

Conditions on the source table that must be met for the synonym to work.

</td></tr><tr><td>

Synonyms

</td><td>

Words or phrases that the system should map to column names or tables, when converting the utterance to a formal query.

 Separate multiple synonyms with a comma.

</td></tr><tr><td>

Application

</td><td>

\[Read only\] Application scope that can use the synonym in a query. Default is **Global**. Ensure that you are in the target application scope for your shortcut before creating it.

</td></tr></tbody>
</table>4.  Select **Submit** if new, or **Update** if you are modifying an existing record.


## Result

The new shortcut is available to your users as soon as they refresh the browser window of the list.

## Semantic shortcut for Incident backlog

The following image shows an example of a semantic shortcut used on incident records. Incidents contain the Assigned to field. Using the condition builder, you can provide synonyms for when the field is empty. When NLQ detects unassigned and backlog in your users' input, it replaces them with the SQL clause `assigned_toISEMPTY`.

![New record form for an NLQ Semantic Shortcut.](../images/create-nlq-shortcutT1.png)

A user can enter `show me incident backlog` or `unassigned incidents` and the system displays incidents with an empty Assigned to field.

**Parent Topic:**[Configuring NLQ](../concept/configuring-nlq.md)

**Related topics**  


[Create an NLQ synonym](create-nlq-synonym.md)

[View NLQ logs](view-nlq-logs.md)

[View NLQ Table Guesser logs](view-nlq-table-guesser-logs.md)

