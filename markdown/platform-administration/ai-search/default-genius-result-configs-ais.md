---
title: Genius Result configurations in the base system
description: Preconfigured AI Search Genius Result configurations display concise, actionable answers derived from high-relevancy search results. These configurations return Genius Result answers for Catalog Items, tables, users, and Knowledge articles that match your search.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Genius Result configurations in the base system

Preconfigured AI Search Genius Result configurations display concise, actionable answers derived from high-relevancy search results. These configurations return Genius Result answers for Catalog Items, tables, users, and Knowledge articles that match your search.

The base system includes multiple Genius Result configurations.

**Note:** You can link the base system's Genius Result configurations to your own search profiles. You can't modify these Genius Result configurations, but you can clone them and modify the cloned configurations.

-   **[Catalog Item Genius Results](genius-result-catalog-item-ais.md)**  
Catalog Item Genius Results display top search results from the Catalog Item \[sc\_cat\_item\] table. Each answer card shows a single Catalog Item record. You can create a request for the Catalog Item directly from the answer card.
-   **[NLQ Genius Results](genius-result-nlq-ais.md)**  
NLQ \(Natural Language Query\) Genius Results use NLQ processing to surface relevant results from tables that match your search query. Each NLQ Genius Result answer card displays a preview of records from matching tables. You can navigate to a matching table's list view or the CMDB workspace directly from the Genius Result answer card.
-   **[People Genius Results](genius-result-people-ais.md)**  
People Genius Results display top search results from the User \[sys\_user\] table. Each People Genius Result answer card shows a single user record. You can view the user's full profile directly from the answer card.
-   **[Q&amp;A Genius Results](genius-result-q-a-ais.md)**  
Q&amp;A Genius Results display top search results extracted from HTML fields of records on the Knowledge \[kb\_knowledge\] table and tables that extend it. Each Q&amp;A Genius Result answer card shows a topic snippet and an answer snippet extracted from a single Knowledge article. You can view the full article directly from the answer card.

**Parent Topic:**[Genius Results](genius-results-ais.md)

