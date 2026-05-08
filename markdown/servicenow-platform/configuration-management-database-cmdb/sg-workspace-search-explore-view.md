---
title: Explore and Search view in Service Graph Workspace
description: Search through CMDB tables without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation. Use natural language with the AI-driven search to search the CMDB and related data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Explore, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Explore and Search view in Service Graph Workspace

Search through CMDB tables without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation. Use natural language with the AI-driven search to search the CMDB and related data.

## Access

Navigate to **Workspaces** &gt; **Service Graph Workspace**, and then in the navigation panel, select the Explore and Search icon.

Role required: sn\_cmdb\_user, sn\_cmdb\_editor, or sn\_cmdb\_admin

## Explore

Explore classes and CIs using one of the following exploration modes:

-   **Contexts**

    The top-level contexts expand into a hierarchy of contexts \(where classes are grouped by categories\). As you expand navigation entries, the next level of contexts appears.

    This option is available only if the Service Graph Workspace - Content store app is installed. The Service Graph Workspace - Content app automatically installs all its dependent apps, such as the Data Model Navigator store app. The Service Graph Workspace - Content store app and its dependent apps enable the **Explore by contexts** option, and provide the contexts definitions and the quick class filters used in the CI list views.

-   **Classes**

    The top-level contexts expand into lists of classes.

    If the Service Graph Workspace - Content store app isn't installed, then **Explore by classes** is the only mode of exploration available. In this case, existing CMDB groups definitions in which type = **CMDB Workspace** are used to organize the navigation panel. For more information, see [CMDB groups](cmdb-groups.md#).


In either exploration mode, you can drill-down to see a list of CIs that belongs to the selected context or CMDB group.

In the CIs list view you can:

-   Use the class quick filters to filter the list of the CIs by fields. Only filters that are common to all the CI classes in the list, appear \(if there are none, then no class quick filters appear\).
-   Select a CI to open it in CI Form. For more information, see [Manage CI details using CI Form in Service Graph Workspace](ci-form-sg-workspace.md).

## Search

Select the Search tab to search through the service graph data. Search provides the following modes of operation where depending on system configurations and usage, each mode might produce different search results:

-   **AI search**

    Lets you access a Now Assist AI-driven search using natural language. Now Assist analyzes your search utterance to determine the optimum search method, shows the results, and then lets you refine the search using natural language in the Now Assist panel.

    To access all of the functionality, including follow up questions, the following requirements must be met:

    -   Role: sn\_cmdb\_user and now\_assist\_panel\_user
    -   This skill is available starting with the [Now Assist for CMDB](now-assist-landing-cmdb.md) version 3.0 store app, which must be installed
    -   The Now Assist skill Search result classifier, must be activated
    For more information, see [Search the Service Graph database using natural language](../../now-assist-cmdb/task/na-cmdb-skill-search-result-classfy.md).

-   **Intelligent Search**

    Lets you use Natural Language Query \(NLQ\) search capabilities provided by [Intelligent Search for CMDB](intelligent-search-cmdb.md).


If the Now Assist store app and the Search result classifier skill requirements for AI search aren't met, the system defaults to using Intelligent Search to search service graph data.

## Intelligent Search

Accessible to: CMDB Admin, CMDB Editor, CMDB User.

Lets you use Natural Language Query \(NLQ\) search capabilities provided by [Intelligent Search for CMDB](intelligent-search-cmdb.md). Use the input field to construct a search string using everyday language. As you type, a dynamic list of relevant suggestions appears, with items matching single words or part phrases in the typed-in text, such as table names.

You can:

-   Select **Search tips** to see tips about constructing search strings. See details about the usage, examples for single and multi-table search, advanced filtering, and relationships in Intelligent Search.
-   Select **Search** to either run the query if the search string is already fully converted into a valid CMDB query, or to open the Refine your query dialog box.
    -   If the search string has no ambiguities with the table name or relationships, then the query runs and the results appear in a list view format.

        Only the first 100 results of the query appear in the results pane.

        -   Select **Load More Results** to view the next set of 100 results.
        -   Select **Load All Results** to view the rest of the query results, up to the number specified by the [glide.cmdb.query.max\_results\_limit](../reference/cmdb-querybldr-sysproprties.md) system property \(10,000 by default\).
        If the constructed CMDB query contains more than a single table, then the **View in Query Builder** button appears. Select the button to open the [CMDB Query Builder](querying-cmdb.md) with your query fully constructed on the Query Builder canvas. You can use the Query Builder to continue editing the query.

    -   If there are any ambiguities with table names or relationship types in the search string, then the search string can't be converted into a valid CMDB query. In this case, the Refine your query dialog box appears letting you select from suggested CI classes and continue to parse your search string into a valid CMDB query. Those suggested CI classes are based on phrases in your search string. Use the drop-down lists to select the CI classes that match your intended search and then select **View search results** to run the query.
    -   If Intelligent Search is unable to convert your search string into a valid CMDB query, then selecting **Search** doesn't generate any query results. Instead, a feedback form appears. Fill out the form and select **Submit Feedback** to record your feedback for your CMDB Admin to review.
-   Use the Sample searches list to get you started in running a pre-defined search. This list consists of more common searches, or searches that are more difficult to construct such as searches that involve service instances \(application services\).
-   Use the Your recent searches list to rerun a previous search.
-   Select **Results Feedback** to submit feedback on the search results for your CMDB Admin to review.

For more details about using NLQ with Intelligent Search, see [Intelligent Search for CMDB](intelligent-search-cmdb.md).

Alternatively, you can select **Use conditional search instead** to use a basic condition builder functionality where you can specify conditions to search for CIs of a specific class.

You can:

-   Select **New condition set** to add a condition phrase.
-   Select **Related List Condition** to add a condition phrase for related lists.
-   Select **Search** to search through the CMDB.
-   Add and then adjust the **sn\_cmdb\_ws.list.record\_count\_limit** system property to limit the record count summation and so to minimize the performance impact of that operation. The record count shows on the Conditional search page, for example, above the results list. For more information about adding and modifying that system property, see [Components installed with Service Graph Workspace](../reference/installed-with-sg-workspace.md).

In the results list, select a CI to see its details in [CI Form](ci-form-sg-workspace.md).

<table id="table_tdz_dnw_v5b"><thead><tr><th>

UI activity

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

-   Mapped Application Service
-   Application Service
-   Application Service Group
-   Dynamic CI Group
-   Tag Based Service

</td><td>

app\_service\_user role

</td></tr><tr><td>

-   Business Service
-   Technical Service
-   Application Service Outage

</td><td>

service\_viewer role

</td></tr></tbody>
</table>