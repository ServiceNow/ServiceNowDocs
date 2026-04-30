---
title: AI Search in mobile
description: The AI Search search engine in the Now Mobile platform enables users to find answers to issues and then proceed quickly with their tasks.
locale: en-US
release: xanadu
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Now Mobile, Employee Service Management]
---

# AI Search in mobile

The AI Search search engine in the Now Mobile platform enables users to find answers to issues and then proceed quickly with their tasks.

The mobile platform supports two search engines within applet launchers: AI Search and Zing.

AI Search uses user data sources \(people\), catalog items \(services\), and knowledge articles. The Zing search engine uses additional data sources not associated with AI Search, for example, user tasks and requests.

-   For more information on AI Search configuration, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   For more information about Zing configuration, see [Global search for mobile](https://www.servicenow.com/docs/access?context=mobile-search-config&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

**Note:** You cannot simultaneously use both AI Search and Zing search engines within the same search field. However, you can configure individual applet launchers to host a different search engine per applet. For more information, see [Add AI Search to a launcher screen](../task/aisearch-add-applet-launcher.md).

AI Search offers the following features:

-   Navigation tab filters - Filters help users narrow down results on a site.
-   Auto-complete - As the user enters text, AI Search predicts the query and helps formulate the user's question.
-   Recent and popular searches - When the user starts to search, two categories of search answers display: the user's personal search history and the most common queries by all users on the instance.
-   Auto-correct typos - Typos are auto-corrected based on indexed content. 
-   Synonym handling - The search engine also looks for words similar to the search term.
-   Genius cards and action items - Genius result cards display the most relevant answers and offer users the option to perform actions within the card, for example, adding buttons to make a call, send an email, or add to a shopping basket.

<table id="table_g5d_qck_j4b"><thead><tr><th>

Service category AI search

</th><th>

People category AI search

</th><th>

Knowledge category AI search

</th></tr></thead><tbody><tr><td>

![AI Search results from the services category.](../image/aisearch-catalog-callout-results.png "AI Search results from services category")

</td><td>

![AI Search results from the people category.](../image/aisearch-people-results.png "AI Search results from people category")

</td><td>

![AI Search results from the knowledge category.](../image/aisearch-knowledge-results.png "AI Search results from knowledge category")

</td></tr></tbody>
</table>-   **[Configure AI Search for mobile devices](../task/advanced-text-search-config-now.md)**  
Configure the Now Mobile search bar to use the AI Search search engine.
-   **[Customize AI Search results](../task/advanced-text-search-customize.md)**  
Customize AI Search results to provide users with a tailored search experience.
-   **[Add AI Search to a launcher screen](../task/aisearch-add-applet-launcher.md)**  
Configure your launcher screen to use the AI Search search engine.

**Parent Topic:**[Configuring Now Mobile](setup-mobile-employee.md)

