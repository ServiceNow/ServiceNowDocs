---
title: Managing the indexed sources from the AI Search Admin console
description: If you have the admin or ais\_admin role, you can create, view, or edit the indexed sources directly from the AI Search Admin console.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-02-04"
reading_time_minutes: 3
breadcrumb: [Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing the indexed sources from the AI Search Admin console

If you have the admin or ais\_admin role, you can create, view, or edit the indexed sources directly from the AI Search Admin console.

## Indexed sources overview

The indexed sources are the ServiceNow AI Platform® tables and external documents that you want to make searchable. AI Search then adds the content from these sources to its search index. The configuration for the indexed sources is shared by AI Search and other applications. For more information, see [Indexed sources in AI Search](indexed-sources-ais.md).

The following example shows the indexed sources configuration table on the **Shared Configuration** tab of the AI Search Admin console where you can view or edit the existing indexed sources or create indexed sources.

![AI Search Admin console Shared Configurations Indexed Sources view where you can view, edit, or create indexed sources for your AI Search enabled applications.](../image/indexed-source-adminconsole.png "Indexed sources table")

## Indexed sources table

The Indexed sources \(ais\_datasource\) configuration table displays the key details of the existing indexed source, such as the name, source table, type, status, and more.

<table id="table_rbg_jzr_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the indexed source.

</td></tr><tr><td>

Source table

</td><td>

ServiceNow AI Platform table to index.

</td></tr><tr><td>

Type

</td><td>

Type of the source table selected for indexing. It can be either an internal ServiceNow AI Platform table or an external document.

</td></tr><tr><td>

Overall status

</td><td>

Status of the indexed source:-   **Inactive**

The indexed source isn’t searchable and overrides other statuses.

-   **Never indexed**

The indexed source is active, but it has never been full indexed. This status can be combined with the **Reindex required** status.

-   **Index in progress**

The indexed source is being indexed manually.

-   **Reindex required**

The indexed source configuration is updated and the source must be indexed again.

-   **Active**

The index is active and no changes have been made to the configuration since the last full index was completed.


</td></tr><tr><td>

Indexing method

</td><td>

Methods that are used in information retrieval systems, such as AI Search, to organize and retrieve text-based data:-   **Keyword**

A method that helps to identify and index the specific keywords or phrases from the text.

-   **Semantic**

An advanced semantic vector search that goes beyond keywords. This method helps to understand the meaning or context of words within a document.


</td></tr><tr><td>

Semantic fields

</td><td>

Name of the fields that are configured to index for a semantic vector search.

</td></tr></tbody>
</table>-   **[Create an indexed source from the AI Search Admin console](../task/ais-admin-console-create-indexed-source.md)**  
Create an indexed source to make the content and metadata from the ServiceNow AI Platform table records that are searchable by using AI Search.
-   **[Define the semantic indexing configuration for an indexed source](../task/ais-admin-console-config-semantic-index.md)**  
Define the semantic indexing configuration for your indexed sources so that AI Search can analyze and understand your content accurately. By doing this process, you can help to ensure that you get more relevant search results.
-   **[Index the content from an indexed source for searchability](../task/ais-admin-console-start-content-indexing.md)**  
Enable AI Search to index the records from your source tables to make the content searchable.
-   **[Set up a field configuration for an indexed source](../task/ais-admin-console-setup-field-config-indexed-source.md)**  
Set up indexed source field configurations to control how AI Search indexes content for a specific field in your source table records.
-   **[Set up an indexed source attribute for indexing the search content](../task/ais-admin-console-setup-indexed-source-attributes.md)**  
Set up an indexed source attribute to control how AI Search indexes content for all records in a source table.

**Parent Topic:**[Using the AI Search Admin console](using-ais-admin-console.md)

