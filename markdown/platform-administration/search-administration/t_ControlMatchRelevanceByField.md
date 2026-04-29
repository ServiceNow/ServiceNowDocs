---
title: Set the relative weight of a field
description: To improve search results, the Zing search engine assigns to each potential match a numeric score that represents its relevancy to the query.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zing computes document scores using three components, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set the relative weight of a field

To improve search results, the Zing search engine assigns to each potential match a numeric score that represents its relevancy to the query.

## Before you begin

Text indexing must be enabled for the table containing the fields you want to modify the relative weight for. To learn about enabling text indexing for a table, see [Configure a table for indexing and searching](configure-single-table-for-indexing.md#).

Role required: admin

## About this task

Administrators can control the relative importance of a match for each field in a table with the ts\_weight attribute. The majority of fiends have no ts\_weight attribute. Zing treats these fields as having weight 1 when scoring search matches.

The following fields have ts\_weight attribute values by default:

-   kb\_knowledge.number = 50
-   kb\_knowledge.short\_description = 10
-   kb\_knowledge.meta = 10
-   task.number = 50
-   task.short\_description = 10

When scoring records, Zing compares the relative weights of fields that produced search term matches. For example, if the **Title** field has `ts_weight=50` and the **Description** field has `ts_weight=10`, then a match in **Title** is 5 times as relevant as a match in **Description** and 50 times as relevant as a field without the ts\_weight attribute.

**Note:** To view the complete scoring system, see [Document Scoring](../concept/c_DocumentScoring.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Open the system dictionary record for the field's table and column.

    For example, to modify the ts\_weight for the kb\_knowledge.number field, open the dictionary record with **Table** "kb\_knowledge" and **Column name** "number".

3.  In the Dictionary Entry form's **Attributes** field, perform one of the following steps:

    -   If a ts\_weight attribute appears in the list of attributes, change its integer value to the relative weight you want to set for the field.
    -   If no ts\_weight attribute appears in the list, add a new `ts_weight=<value>` comma-separated list entry, where &lt;value&gt; is the relative weight you want to set for the field.
4.  Select **Update**.

5.  Refresh the table's text index:

    1.  Open the system dictionary record for the field's table.

        The table's system dictionary record is the one with the table name as its **Table** value, an empty **Column name** field, and "Collection" as its **Type** value.

    2.  On the Dictionary Entry form, select the **Generate Text Index** link in the Related Links section.


## Result

Once Zing finishes regenerating the text index for the table, search result scoring uses your new relative weights for fields.

**Parent Topic:**[Zing computes document scores using three components](../concept/c_DocumentScoring.md)

**Related topics**  


[Score search terms by inverse document frequency \(IDF\)](enable-IDF-scoring.md)

