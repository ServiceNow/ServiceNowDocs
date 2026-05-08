---
title: Intelligent Search for CMDB
description: Use everyday natural language query \(NLQ\) in a search string to query for a set of CIs in the CMDB. Intelligent Search for CMDB, parses, resolves ambiguities, and converts your search string into a valid CMDB query. Complex search strings open fully constructed on a canvas of CMDB Query Builder where you can continue and refine, or run.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Intelligent Search for CMDB

Use everyday natural language query \(NLQ\) in a search string to query for a set of CIs in the CMDB. Intelligent Search for CMDB, parses, resolves ambiguities, and converts your search string into a valid CMDB query. Complex search strings open fully constructed on a canvas of CMDB Query Builder where you can continue and refine, or run.

Intelligent Search for CMDB is supported only on English language instances and isn't supported when the instance preferred language is set to a language other than English.

## Integration with CMDB Workspace

Intelligent Search for CMDB is integrated into the Home view in the CMDB Workspace store app. For more information, see:

-   [Home view in CMDB Workspace](cmdb-workspace-home-view.md) \(Intelligent Search section\) for details about how to use Intelligent Search, sample search strings, and helpful tips.
-   [CMDB Workspace](cmdb-workspace.md) for additional details about CMDB Workspace.

## Integration with Service Graph Workspace

Intelligent Search for CMDB is integrated into the Search and Explore view in the Service Graph Workspace store app. For more information, see:

-   [Explore and Search view in Service Graph Workspace](sg-workspace-search-explore-view.md), Search tab for details about how to use Intelligent Search, sample search strings, and helpful tips.
-   [Service Graph Workspace store app](sg-workspace.md) for additional details about Service Graph Workspace.

## Integration with CMDB Query Builder

Intelligent Search for CMDB is integrated with the [CMDB Query Builder](querying-cmdb.md) in the ServiceNow AI Platform. This integration is controlled by the system property **glide.cmdb.query.nlq.activated**, which is set to **true** by default. Intelligent Search for CMDB lets you use natural language processing in the CMDB Query Builder to find CIs and their relationships using Intelligent Search for CMDB functions.

## Using Intelligent Search for CMDB

Intelligent Search is tailored to the CMDB, searching only through the CMDB class hierarchy for tables, and for CIs and their relationships.

Use the Intelligent Search search field to construct a search string using everyday natural language. Your queries can span multiple CMDB classes and involve many CIs that are connected by different relationships. After resolving any ambiguities with table names or relationship types, Intelligent Search converts your search string into a query that the CMDB can run. The CMDB query is constructed dynamically as you type into the search box and spell checker is applied if needed. A dynamic list of relevant suggestions appears as you type, with items such as table names, matching single words or part phrases in the typed-in text.

Use Intelligent Search:

-   **Search tips**: Shows details and tips about the usage, and examples for single and multi-table search, advanced filtering, and relationships in Intelligent Search. The Relationships tab contains a link to the [CMDB Implicit Relationships](intelligent-search-cmdb.md#section_CMDB_Implicit_Relationships) table.
-   **Search**: Depending on whether the search string is already fully converted into a valid CMDB query and whether the search is for a single or multiple tables.

    -   If the search string has no ambiguities with the table name or relationships, then the query runs and the results appear in a list view format.

        If the constructed CMDB query contains more than a single table, then the **View in Query Builder** button appears. Click the button to open the [CMDB Query Builder](querying-cmdb.md) with your query fully constructed on the Query Builder canvas. You can use the Query Builder to continue editing the query.

    -   If there are any ambiguities with table names or relationship types in the search string, then the search string can't be converted into a valid CMDB query. In this case, the Refine your query dialog box appears to continue and parse your search string into a valid CMDB query. The dialog box contains suggested synonyms and labels for phrases in your search string. Use the drop-down lists to select the synonyms that match your intended search and then click **Go** to run the query.
    -   If Intelligent Search is unable to convert your search string into a valid CMDB query, then clicking **Search** does not generate any query results. Instead, a feedback form appears. Fill out the form and click **Submit Feedback** to send your feedback to ServiceNow analysis.
-   **Results Feedback**: Submit feedback to ServiceNow analysts, to express your assessment of the results. Choose descriptions that capture any gap between the results and your expected results, and add any helpful details.

## Sample searches

When you click the search box, the drop-down list of pre-defined sample searches appears. The list consists of more common searches, or searches that are more difficult to construct such as searches that involve application services. Run any of those searches to get started.

-   Sample searches are stored in the NLQ Sample Search \[sn\_cmdb\_ws\_nlq\_sample\_search\] table
-   Referenced tables are stored in the NLQ Sample Search Table \[sn\_cmdb\_ws\_nlq\_sample\_search\_table\] table

CMDB Admins \(sn\_cmdb\_admin user role\) can modify a sample search by directly editing its record in the NLQ Sample Search table. Click **All** and then in the Filter navigator, enter `sn_cmdb_ws_nlq_sample_search.list`. In the NLQ Sample Searches list view edit the record for a search that you want to modify.

Any modification to sample searches is reflected in CMDB Workspace,Service Graph Workspace, and the CMDB Query Builder.

## Synonyms

The NLQ Synonym \[nlq\_synonym\] table is pre-populated with synonyms for natural language strings for CMDB table and column names, and relationships. This table is used to match natural language search words to the CMDB query language. For example, the phrase ‘linux server’ has synonyms such as ‘Linux Server’, ‘Server’, and ‘Virtual Machine Instance’.

For details about viewing and adding synonyms customized to your business needs, see NLQ synonyms.

## CMDB Implicit Relationships

You can help Intelligent Search find more results by defining some of the relationships between classes as implicit relationships. Implicit relationships can be useful in queries that involve service offering and application services.

NLQ admins can create new implicit relationships by navigating to **All** &gt; **NLQ** &gt; **CMDB Implicit Relationships**.

An implicit relationship defines the relationship between two tables and includes any filters you want to apply. When creating an implicit relationship, you set the following items:

-   From table \(from\_table\): The class that acts as the parent
-   Filters: Conditions that are applied to the columns of the from\_table
-   To table: The class that acts as the child
-   Relationship: How the from\_table interacts with the to\_table. For example, Contains: Contained by means the from\_table contains the to\_table
-   Skipped table: The class that is implied and not captured by the CMDB Query Builder

For example, in CMDB Query Builder, you want to see your service offerings that have had a P1 incident in the last 10 days. However, if you were to type `show me all business service offerings with p1 incidents in the last 10 days`, NLQ wouldn't understand the relationship.

Implicit relationships are stored in the NLQ CMDB Implicit Relationship \[nlq\_cmdb\_implicit\_relationship\] table and are used in the CMDB Workspaceand in Service Graph Workspace, and if integrated, also in CMDB Query Builder.

For more information about NLQ in the ServiceNow AI Platform, see Natural Language Query \(NLQ\).

