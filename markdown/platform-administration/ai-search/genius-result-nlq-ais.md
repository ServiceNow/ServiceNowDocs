---
title: NLQ Genius Results
description: NLQ \(Natural Language Query\) Genius Results use NLQ processing to surface relevant results from tables that match your search query. Each NLQ Genius Result answer card displays a preview of records from matching tables. You can navigate to a matching table's list view or the CMDB workspace directly from the Genius Result answer card.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# NLQ Genius Results

NLQ \(Natural Language Query\) Genius Results use NLQ processing to surface relevant results from tables that match your search query. Each NLQ Genius Result answer card displays a preview of records from matching tables. You can navigate to a matching table's list view or the CMDB workspace directly from the Genius Result answer card.

NLQ Genius Results don't use indexed sources when finding tables that match your query. You don't need to define a table as an indexed source to make it eligible to appear in NLQ Genius Result answers.

When computing NLQ Genius Result answers, AI Search identifies tables that match your search using the following NLQ query types:

-   Natural language queries similar to the ones made using Analytics Center. To learn more about Analytics Center table query capabilities, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).
-   Natural language queries similar to the ones made using the Configuration Management Database \(CMDB\). These CMDB queries only match tables that aren't defined as indexed sources. For more information about CMDB table query capabilities, see [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

AI Search combines the results from these query types when creating NLQ Genius Result answer cards. As a result, a single NLQ Genius Result answer card may contain tables returned by Analytics Center queries, CMDB queries, or both.

For more information about NLQ processing, see [Natural Language Query](https://www.servicenow.com/docs/access?context=natural-language-query&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Answer card format

The NLQ Genius Result answer card shows different results depending on how many tables your search matched.

-   **Search matches a single table**

    When your search only matches one table, the answer card's preview list displays up to five records from that table. To see more records from the table, select **View full table**.

    ![NLQ Genius Result answer card showing preview records from a single table that matched your query, with answer type, View full table link, About link, and thumbs-up and thumbs-down feedback links.](../image/genius-result-nlq-one-table.png)

-   **Search matches multiple tables**

    When your search matches multiple tables, the answer card displays the matching tables as pills or as entries in a drop-down list. You can select any of the matching tables to preview.

    The preview list displays up to five records from the selected table. To see more records from the table, select **View full table**.

    ![NLQ Genius Result answer card showing pills for multiple tables that matched your search, along with preview records from selected pill.](../image/genius-result-nlq-multiple-tables.png)

-   **Multiple search terms match CMDB tables**

    When multiple terms in your search match CMDB tables, the answer card displays **Refine and preview** controls. A drop-down list appears for each search term that matches one or more CMDB tables. Use the drop-down lists to refine your results by selecting a CMDB table for each matching search term.

    The preview list displays records from a CMDB workspace smart search for the selected tables, including their connecting relationships. To see more records from the chosen tables, select **View full table**.

    ![NLQ Genius Result answer card showing drop-down lists for multiple search terms that matched CMDB tables, along with joined preview records from selected tables.](../image/genius-result-nlq-cmdb-multi-match.png)


## Viewing full tables

When you select **View full table** in an NLQ Genius Result answer card, the action performed depends on how the matching table was found. The default actions are as follows.

-   If the table was found by an Analytics Center table query, the system displays it in list view.
-   If the table was found by a CMDB table query, the system displays it in the [CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Search administrators can customize these actions. For more information, see the [Configure navigation actions for NLQ Genius Result answer cards](../task/configure-nav-action-nlq-grs.md) section.

## Review feedback

Some NLQ Genius Result answers show `NLQ supported by AI` as their answer type, indicating that they used artificial intelligence to help find tables that matched your search query. Because these answers are automatically generated, you should review them for accuracy.

To provide review feedback on an NLQ Genius Result answer, select one of the thumb icons shown on the answer card. If the answer's information is accurate, select the thumbs up icon ![](../image/genius-result-feedback-positive.png). If the answer's information isn't accurate, select the thumbs down icon ![](../image/genius-result-feedback-negative.png).

Your feedback helps ServiceNow improve future versions of this Genius Result configuration.

## Limitations

Like the other base system Genius Result configurations, NLQ Genius Results only support searches in English.

NLQ Genius Results rely on Natural Language Query processing, which can increase the time required to return results on the first search for a given set of terms. Consider this performance impact before enabling NLQ Genius Results in any of your AI Search applications.

NLQ Genius Results don't support the following table query options:

-   Grouping of table query results
-   Rendering of table query results as pie charts or bar charts
-   Trend and single score visualizations
-   Keywords that return results in non-list formats, such as `total`, `count`, or `average`

-   **[Display NLQ Genius Result answers in Service Portal search applications](../task/display-nlq-gr-service-portal-apps.md)**  
Configure the system to display search result preview lists for NLQ Genius Result answers in Service Portal search applications.
-   **[Configure navigation actions for NLQ Genius Result answer cards](../task/configure-nav-action-nlq-grs.md)**  
Configure the navigation actions that trigger when a user selects **View full table** on an NLQ Genius Result action card. Each navigation action includes a redirection payload and can optionally include filters for a table's name, the NLQ source that returned the table, or the search profile used by the search application.
-   **[System properties for NLQ Genius Results](../reference/sys-properties-nlq-gr.md)**  
A system property determines whether the system displays search result preview lists for NLQ Genius Result answers in Service Portal search applications.

**Parent Topic:**[Genius Result configurations in the base system](default-genius-result-configs-ais.md)

