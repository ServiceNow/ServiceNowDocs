---
title: Display relevant and actionable search results
description: AI Search provides users with clear answers for their search queries.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Explore, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Display relevant and actionable search results

AI Search provides users with clear answers for their search queries.

-   **Hit highlighting**

    AI Search highlights search query terms that appear in search results. This highlighting enables users to see which query terms contributed to record matches.

-   **Display the most relevant results first with machine learning relevancy**

    AI Search orders search results in decreasing order of relevancy. Machine learning automatically tunes and improves search result relevancy scoring for each search profile based on aggregated user interaction data and A/B testing evaluations of live search traffic.

    Machine learning relevancy is automatically enabled and not configurable, though search administrators can exclude specific search profiles from automatic relevancy-model updates. For more details on automatic relevancy score tuning, see [Machine learning relevancy in AI Search](machine-learning-relevancy-ais.md).

-   **Display the best answers as actionable Genius Result cards**

    Configure Genius Results to analyze search query intent and put the best answers first. Search users can read a Knowledge article, view a user's profile or organization chart, or request a Catalog Item directly from a Genius Result answer card.

    Search administrators can link Genius Results to search profiles, modify their settings, and create new configurations. To learn more about Genius Results configurations, see [Genius Results](genius-results-ais.md).

-   **Boost, block, or promote search results**

    Define result improvement rules with configurable trigger conditions. A rule can boost search result relevancy based on the search query or user context, or can block or promote specific results for a particular search query.

    Search administrators define result improvement rules in search profiles. For details on creating rules and configuring their boost, block, or promote actions, see [Result improvement rules](result-improvement-rules-ais.md). AI Search supports result improvement rules for Brazilian Portuguese, Dutch, English, Finnish, French, French - Canada, German, Italian, Japanese, Korean, Norwegian \(Bokmål\), Polish, Portuguese, Simplified Chinese, Spanish, Swedish, and Traditional Chinese search queries.


**Parent Topic:**[Exploring AI Search](explore-ais.md)

