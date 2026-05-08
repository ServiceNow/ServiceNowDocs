---
title: Now Assist Actions Genius Results
description: Now Assist Actions Genius Results display actionable answers showing Catalog Items and Virtual Agent topics that match your search query. AI Search matches records based on their similarity to your search's intent and meaning instead of looking for exact term matches.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Now Assist Actions Genius Results

Now Assist Actions Genius Results display actionable answers showing Catalog Items and Virtual Agent topics that match your search query. AI Search matches records based on their similarity to your search's intent and meaning instead of looking for exact term matches.

**Important:** Starting with the Now Assist in AI Search 11 release, the Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](now-assist-multi-content-qna-genius-results.md).

Now Assist Actions Genius Results send content from your search's most relevant Catalog Item records and Virtual Agent topic records to the Now LLM Service. The Now LLM Service ranks and filters the selected records' content for display.

A Now Assist Actions Genius Result answer card can display content from up to three records. AI Search uses semantic vector search and legacy keyword search to select records that best match the meaning and intent of your search query. For more details on semantic vector search, see [Semantic vector search in AI Search](semantic-search-ais.md).

## Supported record types

In Service Portal, Now Assist Actions Genius Results only operate on Catalog Items. In Virtual Agent, Now Assist Actions Genius Results operate on Virtual Agent topics as well as on Catalog Items. To learn more about Virtual Agent topics, see Virtual Agent.

In Virtual Agent, Now Assist Actions Genius Results rank Catalog Item and Virtual Agent topic records using a unified relevancy scoring scheme. As a result, Now Assist Actions Genius Result answers may display records of either type in any order.

## Activating Now Assist Actions Genius Results

To enable the Now Assist Actions skill in an AI Search application, you can link the Now Assist Actions Genius Result configuration to your search profile for the search application. For details on this procedure, see [Link a Genius Result configuration to a search profile](../task/link-gr-search-profile-ais.md).

For AI Search portal applications, you can enable Now Assist Genius Results using the Now Assist in AI Search Setup page. For more information on this approach, see [Enable Now Assist Genius Results in AI Search portals and mobile applications](../task/enable-now-assist-gr-ais-apps.md).

**Note:** When you activate Now Assist Actions Genius Results in a search application, they're available to all users who search using that application.

## Limitations

Now Assist Actions Genius Results are only supported in Service Portal and Virtual Agent.

By default, Now Assist Actions Genius Results only support English-language searches. Administrators can enable support for other languages by activating Dynamic Translation. To learn more about how answers are translated, see [Dynamic Translation for Now Assist Actions Genius Results](dynamic-translation-na-actions-gr.md). For more details on Dynamic Translation, see [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md).

If you have the External Content Connectors ServiceNow® Store application installed, Now Assist Actions Genius Results exclude search results retrieved from external content source systems when generating answers.

## Interaction with other search features

The following table describes the interactions between Now Assist Actions Genius Results and other search features.

<table id="table_qx4_4vz_nrb"><thead><tr><th>

Feature

</th><th>

Interaction with Now Assist Actions Genius Results

</th></tr></thead><tbody><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

When computing Now Assist Actions Genius Result answers for a search query, AI Search applies result improvement rules normally. The effects depend on the result improvement rule's action, as follows:

-   **block**: Now Assist Actions Genius Results don't return blocked records as answers.
-   **boost** or **promote**: Boosted and promoted records are more likely to be returned as Now Assist Actions Genius Result answers.

</td></tr><tr><td>

[Stop words](stop-words-ais.md)

</td><td>

Now Assist Actions Genius Results use a blend of semantic vector search, which doesn't support stop words, and keyword-based search. AI Search only removes stop words from keyword-based searches, so Now Assist Actions Genius Result answers may not reflect your stop words settings.

</td></tr><tr><td>

[Synonyms](synonyms-ais.md)

</td><td>

Now Assist Actions Genius Results use a blend of semantic vector search, which doesn't support synonyms, and keyword-based search. AI Search expands synonyms in keyword-based searches, so your synonyms are likely to improve the relevancy of Now Assist Actions Genius Result answers.

</td></tr><tr><td>

[Typo handling](typo-handling-ais.md)

</td><td>

When computing Now Assist Actions Genius Result answers for a search query, AI Search corrects misspelled terms in the query.

</td></tr></tbody>
</table>-   **[Dynamic Translation for Now Assist Actions Genius Results](dynamic-translation-na-actions-gr.md)**  
Dynamic Translation improves the international search experience for Catalog Items and Virtual Agent topics. When Dynamic Translation is activated, AI Search can translate searches into English before matching Catalog Items and Virtual Agent topics for inclusion in Now Assist Actions Genius Result answers, and can translate generated answers into the search user's language.

**Parent Topic:**[Configuring Now Assist in AI Search](configuring-now-assist-ais.md)

