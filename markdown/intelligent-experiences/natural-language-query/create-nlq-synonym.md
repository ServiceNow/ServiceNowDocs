---
title: Create an NLQ synonym
description: Add synonyms to improve the ability of NLQ to recognize the various ways your users request data. With synonyms, you can map commonly used words or terms to table columns.
locale: en-US
release: australia
product: Natural Language Query
classification: natural-language-query
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring NLQ, Natural Language Query, Enable AI experiences]
---

# Create an NLQ synonym

Add synonyms to improve the ability of NLQ to recognize the various ways your users request data. With synonyms, you can map commonly used words or terms to table columns.

## Before you begin

Role required: admin, nlq\_admin, or pa\_analyst

## About this task

NLQ synonyms enable you to map common words in your users' requests to the columns in your instance tables. When these words are detected in natural-language queries, NLQ replaces them with actual column and table names, then submits the formal query.

Several synonyms are provided in the base system, and you can add more for your use cases and business requirements. Review NLQ logs of actual user utterances to find possible synonyms to add. For more information, see [View NLQ logs](view-nlq-logs.md).

You can create a new synonym, or modify an existing synonym, as follows.

-   If any synonym already exists for your target table and column, you must add your new synonym to the current record. Separate multiple synonyms with a comma.
-   Synonyms can point to reference fields, using dot-walking. For more information, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).
-   Synonyms are case-insensitive in queries.
-   Synonyms can contain apostrophes and periods, but not commas.
-   Synonym records are associated to one table. You can use the same synonym term for more than one table, but you must create a record for each table.

## Procedure

1.  Ensure that you are in the application scope you want for your synonym, then navigate to **All** &gt; **NLQ** &gt; **Synonyms**.

2.  Select **New**.

    If you are updating an existing record, select its **Column name** in the list.

3.  On the form, fill in the fields.

<table id="table_yvv_mjw_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Synonym Type

</td><td>

Type of synonym.

-   **Table or Column**: Synonym for a value on a table or a specific column in that table.
-   **Record**: Synonym for a value on the CMDB tables \[cmdb\_rel\_type\_table\]. For more information, see [Querying the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/querying-cmdb.md).

**Note:** Supports cmdb\_rel\_type,cmdb\_group, cmdb\_ci\_service\_technical, cmdb\_ci\_service\_discovered, cmdb\_ci\_query\_based\_service tables.

</td></tr><tr><td>

Application

</td><td>

\[Read only\] Application scope that can use the synonym in a query. The default is **Global**.

 When creating a synonym, ensure that you are in the scope you want for the synonym.

</td></tr><tr><td>

Table

</td><td>

Source table.

 You can use the same term for more than one table, but you must create a synonym record for each table. The synonym's mapping is unique to the table.

</td></tr><tr><td>

Column name

</td><td>

Specific column on the source table.

</td></tr><tr><td>

Language

</td><td>

Language of the synonym. Should match the language of the source value.

</td></tr><tr><td>

Synonyms

</td><td>

Words or short phrases that the system should map to column names or tables, when converting the utterance to a formal query.

 Separate multiple synonyms with a comma.

</td></tr><tr><td>

Extend to All Child Tables

</td><td>

**Table or Column** type only.

 Select this option to make any child tables of the source table inherit the synonyms.

</td></tr></tbody>
</table>4.  Select **Submit** if new, or **Update** if you are modifying an existing record.


## Result

The new synonym is available to your users as soon as they refresh the browser window of the list.

## NLQ Synonym for the Active field

The following image shows an example of an NLQ synonym record for the **Active** field on a change request. The synonyms open and in progress are replaced by the term active when the system submits a query.

![NLQ synonym record form for a column synonym.](../images/create-nlq-synonymT1.png)

With this synonym record, a user can type `show open change requests` or `change requests in progress`and the system displays active change requests.

**Parent Topic:**[Configuring NLQ](../concept/configuring-nlq.md)

**Related topics**  


[Create an NLQ shortcut](create-nlq-shortcut.md)

[View NLQ logs](view-nlq-logs.md)

[View NLQ Table Guesser logs](view-nlq-table-guesser-logs.md)

