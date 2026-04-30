---
title: Administering AI Search
description: Learn how AI Search features and behavior affect indexing and search. Gain insight into AI Search behavior by reviewing log messages, ingestion history for indexed sources, and session debugging messages.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-28"
reading_time_minutes: 3
breadcrumb: [AI Search, Search administration, Configure core features, Administer]
---

# Administering AI Search

Learn how AI Search features and behavior affect indexing and search. Gain insight into AI Search behavior by reviewing log messages, ingestion history for indexed sources, and session debugging messages.

## AI Search and performance testing

Understand how the AI Search topology affects performance testing on instances created with System Clone.

**Warning:**

Be careful when testing AI Search performance in cloned non-production instances. The same dedicated AI Search nodes handle search query traffic from all of your instances. As a result, search queries on non-production instances may impact search query performance in your production instance.

-   **[Lemma and Unicode normalization](lemma-unicode-normalization-ais.md)**  
AI Search normalizes inflected words and Unicode glyphs during indexing and at search query time. Normalization improves search recall and enables users to find content with variant forms of their search query terms.
-   **[Internationalization support for AI Search](international-language-support-ais.md)**  
AI Search supports indexing and search in all languages offered by the ServiceNow AI Platform®. Search linguistic features are supported in Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese.
-   **[Machine learning relevancy in AI Search](machine-learning-relevancy-ais.md)**  
AI Search displays the most relevant search results for a query first. Machine learning automatically tunes search result relevancy scoring for search experiences based on aggregated user interactions.
-   **[Content security in AI Search](content-security-ais.md)**  
AI Search filters search query results and displays only records that the currently logged in user can access.
-   **[Encrypted fields in AI Search](encrypted-fields-ais.md)**  
AI Search excludes source record fields encrypted with Encryption Support or Edge Encryption.
-   **[Semantic vector search in AI Search](semantic-search-ais.md)**  
Semantic vector search allows the Now LLM Service to find results based on how similar they are in meaning to your search terms. Now Assist Q&amp;A Genius Results and Now Assist in Virtual Agent use semantic vector search to improve recall with natural language interpretation of search queries.
-   **[AI Search logging and debugging](logging-debugging-ais.md)**  
Review AI Search logs and history to analyze performance and diagnose issues. View log messages and ingestion history, or use session debugging to capture detailed messages for a user session.
-   **[Search Preview UI for AI Search](search-preview-ui-new.md)**  
The Search Preview UI enables you to test AI Search queries using settings from a selected search application configurationor search profile. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.
-   **[Diagnose search result access issues using the Search Preview UI](../task/diagnose-srch-result-access-ais.md)**  
Use the Search Preview UI and the AI Search High Security administrator elevated privilege role to determine whether filters prevent a search user from viewing a specific search result in the AI Search index.
-   **[Debug search source and content security filters](../task/debug-search-filters-ais.md)**  
Use the Session Log to view search source and content security filters applied to results for a search query. Administrators can use this approach to verify search source filters and content security settings.
-   **[Debug external content security filters for a ServiceNow AI Platform user](../task/debug-ext-security-perms-user-ais.md)**  
Use the Session Log to view the set of externally defined user and group access permission filters associated with the current ServiceNow AI Platform user. Administrators can use this approach to verify that the proper user mappings exist for the current user.
-   **[Review record counts for indexed sources](../task/record-counts-indexed-sources-ais.md)**  
Understand where your indexed content originates by viewing record counts for your indexed sources in the AI Search Indexed Source Statistics table.
-   **[Search query parameter evaluation framework](srch-qry-parm-eval-fw-ais.md#)**  
AI Search performs A/B test evaluations that compare result relevancy for alternate sets of search query parameter values. These evaluations determine the models that AI Search uses for machine learning relevancy and for Q&amp;A Genius Results.

**Parent Topic:**[AI Search](overview-ais.md)

