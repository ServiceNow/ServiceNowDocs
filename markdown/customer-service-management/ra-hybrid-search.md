---
title: Hybrid search in Recommended Actions
description: Hybrid search combines keyword-based and semantic search to surface more relevant results in CSM Configurable Workspace, helping agents find KB articles and guided actions even when their phrasing does not match article content exactly.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-07"
reading_time_minutes: 2
keywords: [Hybrid search, Hybrid search in Recommended Actions, Semantic search, Hybrid search in AI search]
breadcrumb: [AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Hybrid search in Recommended Actions

Hybrid search combines keyword-based and semantic search to surface more relevant results in CSM Configurable Workspace, helping agents find KB articles and guided actions even when their phrasing does not match article content exactly.

Unlike keyword-only search, which requires exact term matches, hybrid search understands the context and intent behind a query. Agents using CSM Configurable Workspace will see more contextually relevant KB articles and guided actions in the AI search tab of the Recommended Actions contextual side panel.

## How it works

When an agent performs a search in the AI search tab of the Recommended Actions in CSM Configurable Workspace, Recommended Actions processes the query using a hybrid approach:

-   Keyword matching — returns results based on exact or close term matches.
-   Semantic matching — uses AI to interpret the meaning and context of the query.

The two methods are combined to rank results, improving relevance without requiring agents to rephrase queries or use specific terminology.

## Hybrid search results

For example, a search for `My system keeps freezing` now returns relevant KB articles such as titled `Troubleshooting application performance degradation`, even if they do not use the word "freezing" — a query that previously returned no results with keyword-only search. With Hybrid Search, the article is surfaced because the search understands that freezing, lagging, and performance degradation describe the same problem. For more information on hybrid search, see [Hybrid search in AI Search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Default behavior

The **Enable hybrid search** check box on the **\[CSM AIS\] Configurable Workspace Search Config** record is set to `true` by default in the base system. No admin configuration is required to activate this feature. As an admin, you can disable hybrid search in the CSM Configurable Workspace by navigating to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **\[CSM AIS\] Configurable Workspace Search** and deselecting the **Enable hybrid search** check box.

This configuration is specific to the CSM AI search application. Search configurations for portals or other workspaces are managed separately. If you do not find the **Enable hybrid search** check box for other workspaces, see the [KB2735151](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2735151) article to know how to enable hybrid search when the hybrid search check box is not available on the search configuration record.

**Note:** When Hybrid Search is active, the total result counts and facet counts are not displayed in the search results tab of the Recommended Actions contextual side panel. Hybrid Search applies to KB article and guided action results surfaced in the Recommended Actions panel within CSM Configurable Workspace.

