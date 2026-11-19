---
title: Actions Genius Results
description: Actions Genius Results display actionable answers showing Catalog Items and Virtual Agent topics that match your search query. AI Search matches records based on their similarity to your search's intent and meaning instead of looking for exact term matches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/now-assist-catalog-ordering-gr.html
release: brazil
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-11-10"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring ServiceNow Otto for AI Search, ServiceNow Otto for AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, ServiceNow AI Platform]
---

# Actions Genius Results

Actions Genius Results display actionable answers showing Catalog Items and Virtual Agent topics that match your search query. AI Search matches records based on their similarity to your search's intent and meaning instead of looking for exact term matches.

**Important:** Starting with the ServiceNow Otto for AI Search 11 release, the Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer ServiceNow Otto Summary Genius Results feature. For more details on this feature, see [ServiceNow Otto Summary Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md).

Actions Genius Results send content from your search's most relevant Catalog Item records and Virtual Agent topic records to the LLM. The LLM ranks and filters the selected records' content for display.

An Actions Genius Result answer card can display content from up to three records. AI Search uses semantic vector search and legacy keyword search to select records that best match the meaning and intent of your search query. For more details on semantic vector search, see [Semantic vector search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/semantic-search-ais.md).

## Supported record types

In Service Portal, Actions Genius Results only operate on Catalog Items. In Virtual Agent, Actions Genius Results operate on Virtual Agent topics as well as on Catalog Items. To learn more about Virtual Agent topics, see [Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent-landing-page.md).

In Virtual Agent, Actions Genius Results rank Catalog Item and Virtual Agent topic records using a unified relevancy scoring scheme. As a result, Actions Genius Result answers may display records of either type in any order.

## Activating Actions Genius Results

To enable the Actions skill in an AI Search application, you can link the Actions Genius Result configuration to your search profile for the search application. For details on this procedure, see [Link a Genius Result configuration to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/link-gr-search-profile-ais.md).

For AI Search portal applications, you can enable ServiceNow Otto® Genius Results using the ServiceNow Otto for AI Search Setup page. For more information on this approach, see [Enable ServiceNow Otto for AI Search Genius Results in AI Search portals and mobile applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/enable-now-assist-gr-ais-apps.md).

**Note:** When you activate Actions Genius Results in a search application, they're available to all users who search using that application.

## Limitations

Actions Genius Results are only supported in Service Portal and Virtual Agent.

By default, Actions Genius Results only support English-language searches. Administrators can enable support for other languages by activating Dynamic Translation. To learn more about how answers are translated, see [Dynamic Translation for Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/dynamic-translation-na-actions-gr.md). For more details on Dynamic Translation, see [Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-translation/dynamic-translation-overview.md).

If you have the External Content Connectors ServiceNow® Store application installed, Actions Genius Results exclude search results retrieved from external content source systems when generating answers.

## Interaction with other search features

The following table describes the interactions between Actions Genius Results and other search features.

<table id="table_qx4_4vz_nrb"><thead><tr><th>

Feature

</th><th>

Interaction with Actions Genius Results

</th></tr></thead><tbody><tr><td>

[Result improvement rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/result-improvement-rules-ais.md)

</td><td>

When computing Actions Genius Result answers for a search query, AI Search applies result improvement rules normally. The effects depend on the result improvement rule's action, as follows:

-   **block**: Actions Genius Results don't return blocked records as answers.
-   **boost** or **promote**: Boosted and promoted records are more likely to be returned as Actions Genius Result answers.

</td></tr><tr><td>

[Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/stop-words-ais.md)

</td><td>

Actions Genius Results use a blend of semantic vector search, which doesn't support stop words, and keyword-based search. AI Search only removes stop words from keyword-based searches, so Actions Genius Result answers may not reflect your stop words settings.

</td></tr><tr><td>

[Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/synonyms-ais.md)

</td><td>

Actions Genius Results use a blend of semantic vector search, which doesn't support synonyms, and keyword-based search. AI Search expands synonyms in keyword-based searches, so your synonyms are likely to improve the relevancy of Actions Genius Result answers.

</td></tr><tr><td>

[Typo handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/typo-handling-ais.md)

</td><td>

When computing Actions Genius Result answers for a search query, AI Search corrects misspelled terms in the query.

</td></tr></tbody>
</table>-   **[Dynamic Translation for Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/dynamic-translation-na-actions-gr.md)**  
Dynamic Translation improves the international search experience for Catalog Items and Virtual Agent topics.

**Parent Topic:**[Configuring ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/configuring-now-assist-ais.md)

