---
title: Content security in AI Search
description: AI Search filters search query results and displays only records that the currently logged in user can access.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer]
---

# Content security in AI Search

AI Search filters search query results and displays only records that the currently logged in user can access.

Content security is automatically enabled and isn't configurable.

## Indexed security features

When indexing records from ServiceNow AI Platform® tables, AI Search preserves the following access control settings:

-   Role-based field-level [access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) \(ACLs\)
-   Non-scripted conditional ACLs
-   Scripted table-level ACLs
-   [Before Query business rules](https://www.servicenow.com/docs/access?context=bp-before-query-business-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Domain separation](ai-search-domain-separation.md)
-   [User criteria](https://www.servicenow.com/docs/access?context=t_CreateAUserCriteriaRecord&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for records indexed from the Knowledge \[kb\_knowledge\] and Catalog Item \[sc\_cat\_item\] tables

AI Search doesn't support scripted field-level ACLs or conditional field-level ACLs.

## Early and late binding security implementations for search queries

At query time, AI Search filters search results by evaluating user access to indexed tables and records. The filtering implementation used depends on the security features present on tables and records that match the search query.

<table id="table_a3q_bz4_5mb"><thead><tr><th>

Content security implementation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Early binding

</td><td>

Default content security implementation that incorporates security filters into the search query. The system adds relevant security filters for the user to each search query. To appear in the search results, records must match the search query and pass all security filters.

 Early binding security supports non-scripted ACLs, Before Query business rules, and domain separation, plus user criteria for records indexed from the kb\_knowledge and sc\_cat\_item tables. If a search matches records that have table-level scripted ACLs, the search query automatically falls back to use late binding security.

 **Note:** If an early binding filter produces an error, the search query automatically falls back to use late binding security.

</td></tr><tr><td>

Late binding

</td><td>

More computationally expensive alternate content security implementation that post-filters search query results. The system applies security filters to the search query just as early binding security does. After retrieving records that match the filtered query, it invokes the [GlideRecord.canRead\(\)](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) method for each record. To appear in the search results, records must match the search query, pass all security filters, and return **true** for the API method.

 Late binding security supports all indexed security features.

 By default, late binding security serves as a fallback mechanism for early binding security. You can override this default behavior in the following ways:

-   To make AI Search use late binding security for all results from an indexed source, set the value of that indexed source's **Force Late Binding** field to **true**.
-   To make AI Search use late binding security for all search results, set the value of the **Force AI Search to use late binding for ACL evaluation** \(**glide.ais.security.force\_late\_binding**\) system property to **true**.

 If AI Search applies late binding security to any results from an indexed source used by a facet, the list of available filter selections for the facet changes. When this happens, the facet only displays field values found in the current page of search results. For details on facets, see [Create a facet in an AI Search application configuration](../task/create-facet-ais.md).

 When you enable search result counts for facets in a search application, the counts indicate the number of results that matched the user's search. Late binding security can remove results after they’re counted, causing the actual number of displayed results to be lower than the count. For more information on search result counts for facets, see [Show search result counts for facets on the results page for a search application](../task/display-result-counts-ais.md).

</td></tr></tbody>
</table>## Content security for external content

AI Search preserves access permissions when ingesting external documents. You can alias ServiceNow AI Platform users to the externally defined users and groups specified in these access permissions. AI Search constructs content security filters for external document records from these permissions and aliases.

To learn about using AI Search with external data sources, see [Indexing and searching external content in AI Search](external-content-ais.md). For full details on external content security, see [External content security for AI Search](external-content-security-ais.md).

**Parent Topic:**[Administering AI Search](administer-ais.md)

