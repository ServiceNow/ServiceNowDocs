---
title: Set global text search properties
description: Administrators can control how global text search behaves with system properties.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set global text search properties

Administrators can control how global text search behaves with system properties.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Global Text Search**.

2.  Review the values for the following global text search properties and change them as needed.

<table id="table_kxg_qzk_ddb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Enable Global Text Search** \(**glide.ui.text\_search.enable**\)

</td><td>

Option to enable global search in Core UI and UI15.-   Type: Boolean
-   Default value: **true**
-   Supported values:
    -   **true**: Global search is enabled in Core UI.
    -   **false**: Global search is disabled in Core UI.
**Note:** When Next Experience is enabled, this system property has no effect. To enable or disable the Unified Navigation search field in Next Experience, set the **glide.ui.polaris.global\_search** system property described in [Next Experience system properties](https://www.servicenow.com/docs/access?context=pol-sys-properties&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

**List of roles \(comma-separated\) that can use the Global Text Search capability** \(**glide.ui.can\_search**\)

</td><td>

Comma-separated list of user roles that allow access to global search. To enable global search for users with a role, add the role to this list.-   Type: String
-   Default value: **itil, text\_search\_admin, admin**


</td></tr><tr><td>

**List of tables \(comma-separated\) that won't appear as options when setting up Global Text Search tables** \(**glide.ui.no\_text\_search**\)

</td><td>

Comma-separated list of tables that don't appear as options when defining text search groups for Core UI. Examples are system or maintenance tables.-   Type: String
-   Default value: **sys\_audit, sys\_event, ecc\_queue, ecc\_event, syslog, syslog\_transaction, sys\_journal\_field, sys\_audit\_relation, ecc\_agent\_log, ecc\_mi\_result, sysrule\_escalate\_history, sys\_user\_token, sys\_time\_dimension, sys\_attachment\_doc, sys\_audit\_delete**


</td></tr><tr><td>

**Number of Global Text Search matches returned per table** \(**glide.ui.text\_search.rowcount**\)

</td><td>

Maximum number of matching records previewed for each table on the global text search results page. Users can select a table to see all matching results for that table.-   Type: Integer
-   Default value: 10
**Note:** This system property only controls the global text search preview limit in Core UI. In Next Experience UI, you can set the global search preview limit by editing the **Now Experience Search Configuration** record in the Workspace Global Search Configurations \[sys\_aw\_global\_search\_config\] table.

</td></tr><tr><td>

**Global Text Search background color for Knowledge Base results** \(**css.textsearch.kb.background.color**\)

</td><td>

Background color for Knowledge article global text search results. This property only affects display of results on the legacy global search results page.-   Type: String
-   Default value: **\#f0f7f9**


</td></tr><tr><td>

**Global Text Search background color for Catalog results** \(**css.textsearch.catalog.background.color**\)

</td><td>

Background color for Catalog global text search results. This property only affects display of results on the legacy global search results page.-   Type: String
-   Default value: **\#ffffdd**


</td></tr><tr><td>

**Form view to use for Global Text Search exact match - blank means Default view** \(**glide.ui.text\_search.match\_view**\)

</td><td>

Name of the form view that global text search uses to display exact match results. If no value is specified, global text search uses the default form view. For information on creating and managing views, see [View management](https://www.servicenow.com/docs/access?context=view-management-overview&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

-   Type: String
-   Default value: \(empty\)


</td></tr><tr><td>

**List and form view to use for Global Text Search results. Blank means default view** \(**glide.ui.text\_search.view**\)

</td><td>

Name of the list view that global text search uses to format results for each searched table. If no value is specified, global text search uses the default list view. For information on creating and managing views, see [View management](https://www.servicenow.com/docs/access?context=view-management-overview&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

-   Type: String
-   Default value: **text\_search**


</td></tr><tr><td>

**Query method for global text search. Run a query for each table, for each base class \(parent table\), against a single index regardless of table \(requires text index regeneration\), or let GlideRecord handle the query \(simple\). With the Zing text search engine, the preferred value is "simple"** \(**glide.ir.query\_method**\)

</td><td>

Query method to use for global text search.**Note:** The **base**, **single**, and **table** values aren't supported. Leave this system property set to its default **simple** value.

-   Type: Choice list
-   Default value: **simple**
-   Available values:
    -   **base**: Run a search query for each base class. This value is no longer supported.
    -   **simple**: Let GlideRecord handle the search query.
    -   **single**: Run a search query against a single text search index. To use this method, you must regenerate text search indexes. This value is no longer supported.
    -   **table**: Run a search query for each searchable table. This value is no longer supported.


</td></tr><tr><td>

**The maximum number of results that will be returned during a text index search. This limits the number of records that will be extracted from the text index and displayed** \(**glide.lucene.base\_result\_max**\)

</td><td>

Maximum number of results that global text search will return when searching a text search index.**Note:** When the query method is set to **simple**, this property is ignored.

-   Type: Integer
-   Default value: 100


</td></tr><tr><td>

**The maximum number of entries that will be retrieved from the text index. Only the table that is involved will be returned from the text index for all entries that are between the value specified for maximum results and this value. This is done so that it can be indicated that more results exists for any given table that are going to be displayed** \(**glide.lucene.base\_hits\_max**\)

</td><td>

Maximum number of entries that global text search will retrieve from a text search index.**Note:** When the query method is set to **simple**, this property is ignored.

-   Type: Integer
-   Default value: 500


</td></tr><tr><td>

**Number of simultaneous processes \(1 to 16\) used when searching though multiple groups in a global search** \(**glide.ts.global\_search.parallelism**\)

</td><td>

Number of concurrent threads global text search uses when searching multiple search groups. Each search group requires one thread.Set this value to yield optimal results for your search group configuration. For example, if you have five search groups and four threads, the first four groups run in parallel and the fifth group starts when one of the first four groups finishes. This setup may work well if one of the groups is much larger than another. Similarly, if you have five search groups, setting this value higher than five yields no benefits.

-   Type: Integer
-   Default value: 4


</td></tr></tbody>
</table>3.  Select **Save**.

    The business rule **Text Search Property Change Rationally** validates the new values and aborts the update if they are outside its acceptable ranges.

4.  To set the maximum number of matches to display for a wildcard search term, follow these steps.

    1.  [Open the System Properties table](../../reference-pages/reference/r_AvailableSystemProperties.md#) and search for the property **glide.ts.max\_wildcard\_expansion**.

        |Field|Description|
        |-----|-----------|
        |Name|glide.ts.max\_wildcard\_expansion|
        |Description|Maximum number of matches for a wildcard search term that are allowed as unambiguous.|
        |Type|Integer|
        |Default value|500|

    2.  Edit the **Value**.

        If a wildcard search matches more words than this value, the system displays a message asking the user to refine the search.

    3.  Select **Update**.

5.  To set the Zing text search stemming language, follow these steps.

    1.  Install the internationalization \(i18n\) plugin for the language you want to stem text search terms in.

    2.  [Add a new system property](../../reference-pages/reference/r_AvailableSystemProperties.md#), **glide.ts.stemming\_language**:

<table id="table_krx_crr_2jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

glide.ts.stemming\_language

</td></tr><tr><td>

Description

</td><td>

Language to use for text search stemming. For details on stemming, see [Zing matches derived words with stemming](../concept/stemming-matches-derived-words.md).

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Values supported

</td><td>

-   English
-   French
-   German


</td></tr><tr><td>

Default value

</td><td>

English

</td></tr></tbody>
</table>    3.  To make tables use the new stemming language for text search, manually regenerate their text search indexes.

        For details on this procedure, see [Regenerate a text index for a table](t_RegenerateATextIndexForATable.md).

6.  To enable and configure fallback number search for exact matches, follow these steps.

    **Note:** Fallback number search is disabled by default. When it's enabled, if a global text search finds no exact match for a record number, the system searches a list of specified tables for matches. This additional search can make global text searches take longer, so enable fallback number search only if you need it.

    1.  To enable fallback number search, [add a new system property](../../reference-pages/reference/r_AvailableSystemProperties.md#), **glide.ui.text\_search.enable\_fallback\_number\_search**:

<table id="table_pfs_xdm_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

glide.ui.text\_search.enable\_fallback\_number\_search

</td></tr><tr><td>

Description

</td><td>

Option to enable fallback number search for use when global text search finds no exact matches for a record number.**Note:** Fallback number search can make global text searches take longer. Enable the option only if you need it.

</td></tr><tr><td>

Type

</td><td>

Boolean

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr></tbody>
</table>    2.  To configure the list of tables searched by fallback number search, [add a new system property](../../reference-pages/reference/r_AvailableSystemProperties.md#), **glide.ui.text\_search.fallback\_table\_list**:

<table id="table_ep1_c2m_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

glide.ui.text\_search.fallback\_table\_list

</td></tr><tr><td>

Description

</td><td>

Comma-separated list of names of tables to search when performing fallback number search. Use the special value **all** to search all tables that have prefixes defined in the Number \[sys\_number\] table.

**Note:** Increasing the number of tables to search may increase the time required for fallback number search. Test any changes to this system property before putting them into production.

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Default value

</td><td>

task,kb\_knowledge

</td></tr></tbody>
</table>
-   **[Configure parallel processing of search groups](t_ConfigureParallelProcessing.md)**  
To improve performance, only activate search groups and tables that are necessary to meet business needs.
-   **[Revert to the legacy global search UI](revert-to-legacy-global-search.md#)**  
Disable the dynamic global search UI to preserve customizations you made to the legacy global search UI.

**Parent Topic:**[Global search finds records from multiple tables](../concept/c_GlobalTextSearch.md)

**Related topics**  


[Global search displays a page of matching results](../concept/global-search-polaris-ui.md#)

[Text search views control format of global search results for tables](../concept/text-search-view-formats-results.md)

[Search settings filter and group global search results by table](../concept/search-settings-filter-group-table.md#)

[Global search displays exact matching records](../concept/exact-matches-global-search.md#)

[Global search displays your most recent search queries and results in Next Experience UI](../concept/global-search-recent-queries-results.md)

[Set the preview limit for global or workspace search in Next Experience UI](set-app-preview-limit-polaris-ui.md)

[Hide per-table search result counts in Next Experience UI](hide-result-counts-polaris-ui.md)

[Add a workspace application to the Unified Navigation search context menu](add-app-search-context-polaris-ui.md)

[Global text search suggestions](../reference/r_GlobalTextSearchSuggestions.md)

