---
title: Score search terms by inverse document frequency \(IDF\)
description: Enable term frequency–inverse document frequency \(TF-IDF\) to increase the search result scores of search terms that appear more frequently in a document, but less frequently in the whole collection of searchable documents.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing computes document scores using three components, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Score search terms by inverse document frequency \(IDF\)

Enable term frequency–inverse document frequency \(TF-IDF\) to increase the search result scores of search terms that appear more frequently in a document, but less frequently in the whole collection of searchable documents.

## Before you begin

To enable TF-IDF scoring, a text index must be present for the table. Make sure that text indexing is enabled for the table before changing the query mode. See [Configure a table for indexing and searching](configure-single-table-for-indexing.md#).

Role required: ts\_admin or admin

## About this task

Administrators can enable TF-IDF scoring on a table to improve search results. The Knowledge table \[kb\_knowledge\] has TF-IDF scoring enabled by default.

**Note:** This task requires that you regenerate an index and therefore should be done with system performance in mind. Regenerating an index may take a while to complete depending on table size and other factors. You may notice performance degradation or incomplete search results while the system regenerates the index.

## Procedure

1.  Navigate to the [system dictionary](../../data-dictionary-tables/concept/c_SystemDictionary.md) and open the entry for the desired table.

2.  In the **Attributes** related list, select **New**.

3.  In the **Attributes** field, select **Text search Enable IDF**.

4.  Select **Submit**.

    The **Enable IDF Score** check box in the table's text index record can now be configured.

5.  Navigate to **All** &gt; **System Definition** &gt; **Text Indexes**.

6.  Open the text index created for the table.

7.  Select **Enable IDF Score**.

8.  Under **Related Links**, select **Regenerate Document Frequency**.

    Regenerating document frequency is a one-time task. Regenerate document frequency when TF-IDF scoring is first enabled for a table.

9.  Configure the desired notification and select **OK**.


**Parent Topic:**[Zing computes document scores using three components](../concept/c_DocumentScoring.md)

**Related topics**  


[Set the relative weight of a field](t_ControlMatchRelevanceByField.md)

