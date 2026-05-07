---
title: Configuring AI Search
description: Plan and configure your AI Search implementation.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring AI Search

Plan and configure your AI Search implementation.

## AI Search configuration overview

<table id="table_nhp_vgd_2nb"><thead><tr><th>

Configuration stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Assign roles to AI Search administrators and users](../task/assign-ais-admin-role.md)

</td><td>

Assign the ais\_admin role to users who need to create, read, update, and delete content indexing and search settings for AI Search. Assign the ais\_high\_security\_admin elevated privilege role to users who need to access High Security settings for AI Search.

 Assign the search\_application\_admin to users who need to create, read, update, and delete search application configurations.

</td></tr><tr><td>

[Define indexed sources](indexed-sources-ais.md)

</td><td>

Create and configure an indexed source for each ServiceNow AI Platform® table that has content you want to make searchable. Index source tables to add their searchable content to the AI Search index. The base system includes pre-configured indexed sources for the Catalog Item, Knowledge, and User tables.

</td></tr><tr><td>

[Define search sources](search-sources-ais.md)

</td><td>

Apply filter conditions to indexed sources to define search sources that users can access in your search experiences. The base system includes pre-configured search sources that reference the default indexed sources.

</td></tr><tr><td>

[Define search profiles](defining-search-profiles-ais.md)

</td><td>

Create and publish a search profile for each distinct search experience that you want to offer in search applications. Specify the data that users can search by linking search sources to the search profile. Control search behavior by configuring synonyms, stop words, typo handling settings, Genius Results, and result improvement rules. The base system includes pre-configured search profiles for use with Service Portal, Now Mobile, and the AI Search Assist Service Portal widget.

</td></tr><tr><td>

[Define search application configurations](defining-search-app-cfgs-ais.md)

</td><td>

Create a configuration for each ServiceNow AI Platform application that supports AI Search. Select a search profile for the application to use. Configure application-specific search settings. The base system includes pre-configured search application configurations for Service Portal, Virtual Agent, and the AI Search Assist Service Portal widget.

</td></tr><tr><td>

[Enable and configure AI Search in ServiceNow AI Platform applications](enable-configure-apps-ais.md)

</td><td>

Specify AI Search as the search engine in supported ServiceNow AI Platform applications. Select a search application configuration for each application to use and configure available search UX settings.

</td></tr><tr><td>

[Create a custom search matcher for global search](../task/create-search-matcher-ais.md)

</td><td>

Optionally configure exact-match global searches that only match results from a specified column \(field\) on a particular ServiceNow AI Platform table.

</td></tr></tbody>
</table>## Using guided setup to implement AI Search

Guided setup provides a sequence of tasks that help you configure AI Search on your ServiceNow instance. To open AI Search guided setup, navigate to **All** &gt; **AI Search** &gt; **Guided Setup**.

For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

-   **[Assign roles to AI Search administrators and users](../task/assign-ais-admin-role.md)**  
Grant users the ais\_admin, ais\_external\_content, ais\_high\_security\_admin, and search\_application\_admin roles so they can configure and manage settings and content for AI Search and search applications.
-   **[Activate the Platform Multimodal Service plugin](../task/activate-platform-multimodal-service-plugin.md)**  
Enable automatic generation of searchable captions for images found in indexed attachments.
-   **[Indexed sources in AI Search](indexed-sources-ais.md)**  
Indexed sources designate ServiceNow AI Platform® tables and external document sets with alphanumeric text and string field content that you want to make searchable. AI Search ingests text and string fields from table records or external documents and stores their searchable alphanumeric content in its search index.
-   **[Search sources in AI Search](search-sources-ais.md)**  
Define search sources to make your searchable content available in search experiences. Choose an indexed source and configure optional filter conditions to limit the content that users can search.
-   **[Search profiles in AI Search](defining-search-profiles-ais.md)**  
Search profiles contain settings for a search experience, including synonyms, stop words, typo handling, Genius Results, and result improvement rules. Define a search profile for each unique search experience that you want to offer in a ServiceNow AI Platform® application. Publish search profiles to make them available in your search applications.
-   **[Search application configurations](defining-search-app-cfgs-ais.md)**  
A search application configuration specifies the search engine and settings to use for search in a ServiceNow AI Platform® application. When you choose AI Search as an application's search engine, you can select a search profile for the application and configure its search result display and refinement settings.
-   **[Activate fuzzy numeric search in AI Search](../task/activate-fuzzy-numeric-search-ais.md)**  
Activate fuzzy numeric search to let users find indexed records by their Number field values without needing to enter alphabetic prefixes or leading zeroes.
-   **[Configure EVAM display settings for search results in AI Search applications](../task/configure-search-result-card-opts.md)**  
Customize display settings for Search Result EVAM \(Entity View Action Mapping\) cards in portal and non-portal AI Search applications.
-   **[Enabling and configuring AI Search in ServiceNow AI Platform applications](enable-configure-apps-ais.md)**  
Configure and use the AI Search engine in the Customer Service Management, Now Mobile, Service Portal, and Virtual Agent applications.
-   **[Create a custom search matcher for global search](../task/create-search-matcher-ais.md)**  
Customize the global search experience to return exact match search results from a specified table and column \(field\). You can configure custom search matchers for search terms with prefixes followed by numbers, such as `INT470271`, or for numeric search terms with delimiter characters, such as `525-326-3827` or `2016/01/08`.
-   **[Domain separation and AI Search](ai-search-domain-separation.md)**  
Domain separation is unsupported for the AI Search application tables, but user search queries respect domain restrictions from indexed ServiceNow AI Platform® table records. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Indexing and searching external content in AI Search](external-content-ais.md)**  
With a subscription for the External Content for AI Search plugin, you can enable AI Search users to search content and metadata from documents in external repositories and remote tables.

**Parent Topic:**[AI Search](overview-ais.md)

