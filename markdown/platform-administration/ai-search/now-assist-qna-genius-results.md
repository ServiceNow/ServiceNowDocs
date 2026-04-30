---
title: Now Assist Q&amp;A Genius Results
description: Now Assist Q&amp;A Genius Results use the Now LLM Service to generate concise, actionable answers from knowledge article results in Service Portal, Virtual Agent, Employee Center, and global searches.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 8
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Now Assist Q&amp;A Genius Results

Now Assist Q&amp;A Genius Results use the Now LLM Service to generate concise, actionable answers from knowledge article results in Service Portal, Virtual Agent, Employee Center, and global searches.

**Important:** Starting with the Now Assist in AI Search 11 release, the Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will remain available but will not be updated or supported. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](now-assist-multi-content-qna-genius-results.md).

## Now Assist Q&amp;A Genius Results overview

Now Assist Q&amp;A Genius Results send the most relevant knowledge articles from your search to the Now LLM Service, which generates answer snippets from the articles' HTML fields.

Each Now Assist Q&amp;A Genius Result answer card displays up to three generated answer snippets. For reference, the answer card also includes a link you can select to view the source knowledge articles.

The following example shows a Now Assist Q&amp;A Genius Result answer card containing a snippet summarizing a knowledge article. Select the answer card's **View article** action link to view the full knowledge article.

![Now Assist Q&A answer card showing generated answer banner, knowledge article summary snippet, source knowledge article title, View article action link, information link, and thumbs-up and thumbs-down feedback links.](../image/genius-result-q-a-nas.png "Sample Now Assist Q&A answer card")

**Note:** Because the Now Assist Q&amp;A Genius Result answer is automatically generated, it's a good idea to review it for accuracy. You can provide feedback on the answer by selecting the thumbs-up icon ![](../image/genius-result-feedback-positive.png) if the generated answer is accurate, or the thumbs-down icon ![](../image/genius-result-feedback-negative.png) if it's not. Your feedback helps ServiceNow improve future versions of this Genius Result configuration.

Now Assist Q&amp;A Genius Results use semantic vector search and legacy keyword search to find knowledge articles that best match the meaning and intent of your search query. For more details on semantic vector search, see [Semantic vector search in AI Search](semantic-search-ais.md).

The Now Assist Q&amp;A Genius Result configuration replaces the original Q&amp;A Genius Result configuration from the base system. The base system's Q&amp;A Genius Result configuration extracts answers from knowledge articles using internal routines instead of using the Now LLM Service. To learn more about the base system's Q&amp;A Genius Result configuration, see [Q&amp;A Genius Results](genius-result-q-a-ais.md).

## Enabling Now Assist Q&amp;A Genius Results

You can enable Now Assist Q&amp;A Genius Results in your AI Search portals and mobile applications using the Now Assist in AI Search Setup module. For details on this procedure, see [Enable Now Assist Genius Results in AI Search portals and mobile applications](../task/enable-now-assist-gr-ais-apps.md).

To use Now Assist Q&amp;A Genius Results in global search, you can enable the Now Assist Q&amp;A Genius Result configuration in the AI Search for Next Experience application. For details on this procedure, see [Enabling Now Assist Q&amp;A Genius Results](enabling-now-assist-qa-grs.md#).

**Note:** When you activate Now Assist Q&amp;A Genius Results in a search application, they're available to all users who search using that application.

## Limitations

By default, Now Assist Q&amp;A Genius Results only support English-language searches. Administrators can enable support for other languages by activating Dynamic Translation. To learn more about how content and answers are translated, see [Dynamic Translation for Now Assist Q&amp;A Genius Results](dynamic-translation-na-gr.md). For more details on Dynamic Translation, see [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md).

Knowledge articles that are boosted or promoted by result improvement rules are more likely to appear as Now Assist Q&amp;A Genius Results, but aren't guaranteed to appear.

**Note:** The Knowledge search property settings don't affect Now Assist Q&amp;A Genius Results. For more information on these settings, see [Knowledge search properties](https://www.servicenow.com/docs/access?context=r_KnowledgeProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

If you have the External Content Connectors ServiceNow® Store application installed, Now Assist Q&amp;A Genius Results exclude search results retrieved from external content source systems when generating answers.

## Answer snippet creation for Now Assist Q&amp;A Genius Results

AI Search uses the Now LLM Service to create each Now Assist Q&amp;A answer snippet from a knowledge article record's HTML fields. Each Now Assist Q&amp;A answer card can include up to three snippets. These snippets may all be generated from the same source article or from different source articles.

Now LLM Service automatically determines which elements of a knowledge article's text to include in a Now Assist Q&amp;A answer snippet. You can't configure the criteria for this behavior.

The Now LLM Service summarizes and abstracts content from the knowledge articles' text fields. Answer snippets displayed on Now Assist Q&amp;A Genius Result answer cards may not exist word for word in the source records.

Both AI Search content retrieval and the Now LLM Service are continually improving, so Now Assist Q&amp;A results for specific queries may vary over time. Because results from the Now LLM Service are non-deterministic, you should expect a higher answer variability compared to the base system's Q&amp;A Genius Results.

## Interaction with other search features

The following table describes the interactions between Now Assist Q&amp;A Genius Results and other search features.

<table id="table_qx4_4vz_nrb"><thead><tr><th>

Feature

</th><th>

Interaction with Now Assist Q&amp;A Genius Results

</th></tr></thead><tbody><tr><td>

[Result improvement rules](result-improvement-rules-ais.md)

</td><td>

When computing Now Assist Q&amp;A Genius Result answers for a search query, AI Search applies result improvement rules normally. The effects depend on the result improvement rule's action, as follows:

-   **block**: Now Assist Q&amp;A Genius Results don't generate answers from blocked records.
-   **boost** or **promote**: Boosted and promoted records are more likely to be used when generating Now Assist Q&amp;A Genius Result answers.

</td></tr><tr><td>

[Stop words](stop-words-ais.md)

</td><td>

Now Assist Q&amp;A Genius Results use a blend of semantic vector search, which doesn't support stop words, and keyword-based search. AI Search only removes stop words from keyword-based searches, so Now Assist Q&amp;A Genius Result answers may not reflect your stop words settings.

</td></tr><tr><td>

[Synonyms](synonyms-ais.md)

</td><td>

Now Assist Q&amp;A Genius Results use a blend of semantic vector search, which doesn't support synonyms, and keyword-based search. AI Search expands synonyms in keyword-based searches, so your synonyms are likely to improve the relevancy of Now Assist Q&amp;A Genius Result answers.

</td></tr><tr><td>

[Typo handling](typo-handling-ais.md)

</td><td>

When computing Now Assist Q&amp;A Genius Result answers for a search query, AI Search corrects misspelled terms in the query.

</td></tr></tbody>
</table>-   **[Enabling Now Assist Q&amp;A Genius Results](enabling-now-assist-qa-grs.md#)**  
As a search administrator, you can use the Now Assist Q&amp;A Genius Results skill in AI Search portals and mobile applications by enabling Now Assist Q&amp;A Genius Results in search profiles. You can also use the skill in global search by enabling Now Assist Q&amp;A Genius Results in the AI Search for Next Experience application.
-   **[Define a query filter for Now Assist Q&amp;A Genius Results](../task/define-qry-fltr-now-assist-qna-gr.md)**  
Define a Java regular expression pattern that a search must match to be eligible for triggering Now Assist Q&amp;A Genius Results. Searches that don't match this pattern don't return Genius Result answers from Now Assist Q&amp;A Genius Results.
-   **[Change the minimum search term count for Now Assist Q&amp;A Genius Results](../task/set-min-srch-terms-now-assist-qna.md)**  
Specify the minimum number of terms that a search must contain to be eligible for triggering Now Assist Q&amp;A Q&amp;A Genius Results. Searches with fewer terms don't return Now Assist Q&amp;A Genius Result answers.
-   **[Dynamic Translation for Now Assist Q&amp;A Genius Results](dynamic-translation-na-gr.md)**  
Dynamic Translation improves the international search experience for knowledge article content. When Dynamic Translation is activated, AI Search can generate Now Assist Q&amp;A Genius Result answers from non-English knowledge articles. Dynamic Translation also enables AI Search to translate Now Assist Q&amp;A Genius Result answers into the search user's language.
-   **[Caching for Now Assist Q&amp;A Genius Results](caching-now-assist-q-a-gr.md#)**  
AI Search provides two query-time caches to improve search performance for Now Assist Q&amp;A Genius Results. Caching enables AI Search to return previously generated Now Assist Q&amp;A Genius Result answers without submitting knowledge articles to the Now LLM Service for answer generation.

**Parent Topic:**[Configuring Now Assist in AI Search](configuring-now-assist-ais.md)

