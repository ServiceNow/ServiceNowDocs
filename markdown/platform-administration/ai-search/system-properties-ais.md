---
title: AI Search system properties
description: Users with the admin role can configure the following system properties for AI Search by navigating to All System Properties AI Search .
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search system properties

Users with the admin role can configure the following system properties for AI Search by navigating to **All** &gt; **System Properties** &gt; **AI Search**.

<table id="table_qqp_qth_knb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Enable automatic switch over to a healthy AI Search node in the near datacenter** \(**glide.ais.ha.auto\_switch\_to\_near\_node**\)

</td><td>

Option to enable automatic switch over to a healthy AI Search node in the near datacenter.-   Type: true \| false
-   Default value: **true**
-   Supported values:
    -   **true**: The system automatically switches over to use an AI Search node in the near datacenter when its read health score equals or exceeds the **glide.ais.monitor.health\_threshold\_green** threshold.
    -   **false**: The system doesn't automatically switch over to an AI Search node in the near datacenter.
-   Location: **System Properties** &gt; **AI Search** \(AI Search High Availability section\)

</td></tr><tr><td>

**Enable automatic failover to an alternate AI Search node when the active node becomes unhealthy** \(**glide.ais.ha.enable\_auto\_failover**\)

</td><td>

Option to enable automatic failover to an alternate AI Search node when the active node becomes unhealthy.-   Type: true \| false
-   Default value: **true**
-   Supported values:
    -   **true**: The system automatically fails over to an alternate AI Search node if the active node's write health score drops below the **glide.ais.monitor.health\_threshold\_yellow** threshold.
    -   **false**: The system doesn't automatically fail over an active partition based on its health score.
-   Location: **System Properties** &gt; **AI Search** \(AI Search High Availability section\)

</td></tr><tr><td>

**Ingestion batcher queue memory size in MB** \(**glide.ais.ingestion.batcher\_queue\_memory\_size**\)

</td><td>

Size in MB of batcher queue for indexing of source record content.-   Type: integer
-   Default value: **20**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**Ingestion batcher queue length \(records\)** \(**glide.ais.ingestion.batcher\_queue\_size**\)

</td><td>

Maximum number of records on batcher queue for indexing of source record content.-   Type: integer
-   Default value: **1,000**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**glide.ais.ingestion.catalog\_variables\_filter\_query**

</td><td>

Encoded query string for a query that Catalog Item records must satisfy to be eligible for catalog variable content indexing.**Note:** This system property has no effect if **glide.ais.ingestion.index\_catalog\_variables** is set to **false**.

-   Type: string
-   Location: System Properties \[sys\_properties\] table \(record not present by default\)

 Changes to this system property's value don't take effect until you reindex content from the Catalog Item Table indexed source and indexed sources for other tables that extend the Catalog Item \[sc\_cat\_item\] table. For details on reindexing content from indexed sources, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md) and [Perform a full table index or reindex for multiple AI Search indexed sources](../task/index-multiple-sources-ais.md)

 For additional details on indexing of content from catalog variables, see [Activate indexing of catalog variable content on Catalog Item records](../task/activate-catalog-variable-indexing.md) and [Variable types supported by AI Search indexing](variable-types-ais-index.md). To learn about encoded query strings, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

**Ingestion dictionary batcher queue length \(records\)** \(**glide.ais.ingestion.dictionary\_term\_batcher\_queue\_size**\)

</td><td>

Maximum count of records on queue for addition of terms to a synonym, stop word, or typo handling dictionary.-   Type: integer
-   Default value: **1,000**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**Ingestion failure retry timeout in seconds** \(**glide.ais.ingestion.failure\_retry\_timeout**\)

</td><td>

Timeout period in seconds for indexing of content from a source record.-   Type: integer
-   Default value: **600**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**Ingestion feedback logger for error messages** \(**glide.ais.ingestion.feedback\_logger\_error**\)

</td><td>

Destination for AI Search ingestion feedback messages with the ERROR level.-   Type: string
-   Default value: **Sys Log**
-   Supported values:
    -   **None**: Don't log ingestion feedback messages with this level.
    -   **Sys Log**: Log ingestion feedback messages with this level to the .
    -   **File Log**: Log ingestion feedback messages with this level to a log file on the active AI Search node.
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**Ingestion feedback logger for informational messages** \(**glide.ais.ingestion.feedback\_logger\_info**\)

</td><td>

Destination for AI Search ingestion feedback messages with the INFO level.-   Type: string
-   Default value: **None**
-   Supported values:
    -   **None**: Don't log ingestion feedback messages with this level.
    -   **Sys Log**: Log ingestion feedback messages with this level to the .
    -   **File Log**: Log ingestion feedback messages with this level to a log file on the active AI Search node.
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**Ingestion feedback logger for minor error messages** \(**glide.ais.ingestion.feedback\_logger\_minor\_error**\)

</td><td>

Destination for AI Search ingestion feedback messages with the MINOR\_ERROR level.-   Type: string
-   Default value: **Sys Log**
-   Supported values:
    -   **None**: Don't log ingestion feedback messages with this level.
    -   **Sys Log**: Log ingestion feedback messages with this level to the .
    -   **File Log**: Log ingestion feedback messages with this level to a log file on the active AI Search node.
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**Ingestion feedback logger for warning messages** \(**glide.ais.ingestion.feedback\_logger\_warn**\)

</td><td>

Destination for AI Search ingestion feedback messages with the WARN level.-   Type: string
-   Default value: **Sys Log**
-   Supported values:
    -   **None**: Don't log ingestion feedback messages with this level.
    -   **Sys Log**: Log ingestion feedback messages with this level to the .
    -   **File Log**: Log ingestion feedback messages with this level to a log file on the active AI Search node.
-   Location: **System Properties** &gt; **AI Search** \(AI Search Ingestion Properties section\)

</td></tr><tr><td>

**glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles**

</td><td>

Option to allow indexing of searchable content from role-restricted catalog variables on Catalog Item records.**Note:** This system property has no effect if **glide.ais.ingestion.index\_catalog\_variables** is set to **false**.

-   Type: true \| false
-   Default value: **false**
-   Supported values:
    -   **false**: Prevent indexing of searchable content from catalog variables with role restrictions on Catalog Item records.
    -   **true**: Allow indexing of searchable content from catalog variables with role restrictions on Catalog Item records.
-   Location: System Properties \[sys\_properties\] table \(record not present by default\)

 Changes to this system property's value don't take effect until you reindex content from the Catalog Item Table indexed source and indexed sources for other tables that extend the Catalog Item \[sc\_cat\_item\] table. For details on reindexing content from indexed sources, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md) and [Perform a full table index or reindex for multiple AI Search indexed sources](../task/index-multiple-sources-ais.md)

 For additional details on indexing of content from catalog variables, see [Activate indexing of catalog variable content on Catalog Item records](../task/activate-catalog-variable-indexing.md) and [Variable types supported by AI Search indexing](variable-types-ais-index.md). To learn about encoded query strings, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

**glide.ais.ingestion.index\_catalog\_variables**

</td><td>

Option to allow indexing of searchable content from globally accessible catalog variables on Catalog Item records. To allow indexing of searchable content from catalog variables that require specific roles to access, see **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles**.

-   Type: true \| false
-   Default value: **false** in base system, **true** if Now Assist in AI Search application is installed
-   Supported values:
    -   **false**: Prevent indexing of searchable content from catalog variables on Catalog Item records.
    -   **true**: Allow indexing of searchable content from globally accessible catalog variables on Catalog Item records.
-   Location: System Properties \[sys\_properties\] table \(record not present by default\)

 Changes to this system property's value don't take effect until you reindex content from the Catalog Item Table indexed source and indexed sources for other tables that extend the Catalog Item \[sc\_cat\_item\] table. For details on reindexing content from indexed sources, see [Perform a full table index or reindex for a single AI Search indexed source](../task/index-single-source-ais.md) and [Perform a full table index or reindex for multiple AI Search indexed sources](../task/index-multiple-sources-ais.md)

 For additional details on indexing of content from catalog variables, see [Activate indexing of catalog variable content on Catalog Item records](../task/activate-catalog-variable-indexing.md) and [Variable types supported by AI Search indexing](variable-types-ais-index.md). To learn about encoded query strings, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

**Interval in seconds between AI Search node health status check requests** \(**glide.ais.monitor.health\_status\_check\_interval**\)

</td><td>

Interval in seconds between AI Search partition health status checks.-   Type: integer
-   Default value: **60**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Monitor Properties section\)

</td></tr><tr><td>

**Timeout period in seconds for AI Search node health status check request** \(**glide.ais.monitor.health\_status\_check\_timeout**\)

</td><td>

Timeout period in seconds for AI Search partition health status checks.-   Type: integer
-   Default value: **30**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Monitor Properties section\)

</td></tr><tr><td>

**Inclusive lower bound for GREEN \(healthy\) range of AI Search node health scores** \(**glide.ais.monitor.health\_threshold\_green**\)

</td><td>

Inclusive lower percentage bound for green partition health score range. The inclusive upper bound for this health score range is 100.-   Type: integer
-   Default value: **90**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Monitor Properties section\)

</td></tr><tr><td>

**Inclusive lower bound for YELLOW range of AI Search node health scores** \(**glide.ais.monitor.health\_threshold\_yellow**\)

</td><td>

Inclusive lower percentage bound for yellow partition health score range. The non-inclusive upper bound for this health score range is set by the **glide.ais.monitor.health\_threshold\_green** property value. The red partition health score range includes all scores below this property value. If the health score for an active partition drops into the red range, and if **glide.ais.ha.enable\_auto\_failover** is set to **true**, AI Search failover on the partition.

-   Type: integer
-   Default value: **50**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Monitor Properties section\)

</td></tr><tr><td>

**Maximum request count per search query for AI Search node** \(**glide.ais.query.max\_request\_count\_per\_search**\)

</td><td>

Maximum number of requests that an AI Search node can process per search query.-   Type: integer
-   Default value: **10**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Query Properties section\)

</td></tr><tr><td>

**Search query result count multiplier for AI Search node** \(**glide.ais.query.requested\_rows\_multiplier**\)

</td><td>

Result-count multiplier for search queries that use the late binding security implementation. The system multiplies the search query's minimum desired result count by this factor before requesting records from the AI Search node. Extra records replace any search results removed by the late-binding security implementation. For example, with the default value of **3**, a search query that uses the late binding security implementation and expects at least 10 results produces a request to the AI Search node for 30 matching records. The final result set includes the first 10 of these records that the user can access.

 Lower values improve search query performance but may reduce the search result count below the requested minimum.

-   Type: integer
-   Default value: **3**
-   Location: **System Properties** &gt; **AI Search** \(AI Search Query Properties section\)

</td></tr><tr><td>

**Boolean search operator to use when a search query includes multiple terms** \(**glide.ais.query.search\_operator**\)

</td><td>

Boolean search operator to use when a search query includes multiple terms. When using the AND \(conjunctive\) operator, search only finds records that include all search query terms and phrases. When using the OR \(disjunctive\) operator, search finds records that include any search query term or phrase.

-   Type: string
-   Default value: **AND then OR 2+ key terms**
-   Supported values:
    -   **AND then OR 2+ key terms**: Search using the AND operator. If the search query contains more than two search terms after stop word removal and returns less than one full page of results, automatically resubmit it using the OR operator.

The resubmitted search query only finds records that contain at least half \(rounded up\) of the terms and phrases in the OR expression.

**Note:** When you view the **glide.ais.query.search\_operator** record on the System Property \[sys\_properties\] table, this value appears as **AND\_OR\_ENHANCED**.

    -   **AND then OR query**: Search using the AND operator. If the search query returns less than one full page of results, automatically resubmit it using the OR operator.

The resubmitted search query only finds records that contain at least half \(rounded up\) of the terms and phrases in the OR expression.

**Note:** When you view the **glide.ais.query.search\_operator** record on the System Property \[sys\_properties\] table, this value appears as **AND\_OR**.

    -   **OR query**: Search using the OR operator.
    -   **AND query**: Search using the AND operator.

**Note:** This value is not displayed on the AI Search system properties page, but can be set when editing the **glide.ais.query.search\_operator** record on the System Property \[sys\_properties\] table.

-   Location: **All** &gt; **System Properties** &gt; **AI Search** \(AI Search Query Properties section\)

</td></tr><tr><td>

**Force AI Search to use late binding for ACL evaluation** \(**glide.ais.security.force\_late\_binding**\)

</td><td>

Option to force use of the late binding security implementation for all search queries. For descriptions of the early binding and late binding security implementations, see [Content security in AI Search](../concept/content-security-ais.md).

-   Type: true \| false
-   Default value: **false**
-   Supported values:
    -   **true**: The system uses the late binding security implementation for all search queries.
    -   **false**: The system uses the early binding security implementation for search queries. If search results include scripted ACLs, or if early binding encounters an error, the system switches to use the late binding security implementation.
-   Location: **System Properties** &gt; **AI Search** \(AI Search Security Properties section\)

**Note:** You can enable the late binding security implementation for all search results from a particular indexed source by setting the **Force Late Binding** field to **true** for the indexed source.

</td></tr><tr><td>

**Enable global language fallback** \(**glide.ais.translate.enable\_global\_language\_fallback**\)

</td><td>

Option to enable matching of translated documents in the instance locale's language as well as the user's session language. For example, suppose a user searches from a Japanese user session on an instance with the default US English locale. With the default system property value of **false**, this search only matches knowledge articles in Japanese. If the system property value is set to **true**, the same search matches articles in both Japanese and English.

 To learn more about translated document matching, see [Searching translated content](../concept/searching-translated-content-ais.md). For details on instance locales, see [Configuring locales](../../localization/concept/c_DefineLocales.md#).

 -   Type: true \| false
-   Default value: **false**
-   Supported values:
    -   **true**: AI Search matches translated documents in the instance locale's language as well as the user's session language.
    -   **false**: AI Search only matches translated documents in the user's session language.
-   Location: **System Properties** &gt; **AI Search** \(AI Search Multi-Language Support section\)

</td></tr><tr><td>

**glide.mlpredictor.ml\_x\_snc\_global\_global\_6eedb38234bf5010f877396127c8ffee.predict.request\_timeout**

</td><td>

Timeout period for ML predictions used in Genius Result processing. If Genius Result processing time exceeds this value for a search query, no Genius Result answers are displayed in the search query results.

-   Type: integer
-   Default value: **1000**
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

**query.maxDictionaryTermLength**

</td><td>

Character length limit for stop word and synonym dictionary terms. AI Search ignores dictionary terms that exceed this length limit.-   Type: integer
-   Default value: **256**
-   Location: System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

