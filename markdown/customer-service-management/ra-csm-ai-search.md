---
title: AI search in Recommended Actions
description: Enable agents to use AI search in Recommended Actions to find relevant resources or resolutions for customer issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# AI search in Recommended Actions

Enable agents to use AI search in Recommended Actions to find relevant resources or resolutions for customer issues.

AI search results and genius results are displayed in the Search tab of the Recommended Actions component in the contextual side panel. Agents can initiate actions from the search cards directly to resolve an issue.

![AI search results and genius result in the search tab within the Recommended Actions component.](../image/ra-card-ai-search.png)

The search results from the configured search sources are displayed in the form of cards. These cards are previews of search records. You can select the card to view the record details or directly take actions through the cards. The most relevant answers are displayed as top results in the form of genius result cards.

AI search harnesses advanced machine learning algorithms and natural language processing capabilities to comprehend user queries and provides the most relevant search results that can be employed to resolve issues effectively. For more information on:

-   AI search and its features, see AI Search.
-   enabling AI search for Next Experience, see Enable AI Search for Next Experience.

## AI search features

-   Highlights search query terms that appear in the search results.
-   Displays the most relevant results first with machine learning relevancy. Machine learning automatically tunes and improves the search result relevancy score for each search profile based on the answers agents select.
-   Displays the best answers as genius result cards.

## AI search benefits

-   Maximizes efficiency: Use AI search integration to reduce task resolution time and improve agent productivity.
-   Leverages contextual intelligence: Make the most of context-aware searching to provide accurate and timely responses.
-   Provides summarization: Configure genius results to get large language model-based knowledge summarization to align with your content and information needs.

## Configuring AI search in Recommended Actions

Steps to configure AI search in Recommended Actions include enabling the AI search tab, mapping the AI search results with guidance inputs, and customizing the Recommended Actions component. Advanced customization options include adjusting the number of results to view on a page, identifying genius results to add to the search profile, and configuring search sources. For more information, see [Configuring AI search in Recommended Actions](ra-configuring-ai-search.md).

## Using AI search in Recommended Actions

Enable customer service agents to use AI search for faster access to relevant information and take appropriate actions to resolve customer issues. For more information, see [Use AI search in Recommended Actions to resolve cases](../task/nba-use-ai-search.md).

-   Accessing AI search: Agents can access the AI search tab in the contextual side panel of the workspace.
-   Finding context-aware results: Agents can enter their search queries in the search bar. AI search uses natural language processing to understand user queries and considers task context to produce relevant results.
-   Showing AI search results: Review AI search results and take actions directly from the search cards.
-   Showing genius results: Agents can view the most relevant results at the top based on criteria defined in the genius results configuration, drawing their attention to the most relevant information first.
-   Narrowing search results: Agents can select a search source from the **Search filter** field to display results only from that search source and then return to viewing all matching records.
-   Viewing results count: The search tab shows counts of the total number of matching search results. The search filters show the number of matching results for each search source.

    **Note:** Search results displayed and the total search count may vary due to security permissions or if the search result has already been executed. The executed guidances are added to the Activity stream and moved to the Actions history. Executed guidances will be included in the total search count but will not show up in the search results.


