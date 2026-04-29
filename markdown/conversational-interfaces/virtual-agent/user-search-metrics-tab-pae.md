---
title: Using user search metrics with Virtual Agent
description: By using user search metrics with the Virtual Agent application, you can see your users' queries and the results from their searches. With these metrics, you can identify the areas where you can improve Virtual Agent to offer more meaningful search results.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Using user search metrics with Virtual Agent

By using user search metrics with the Virtual Agent application, you can see your users' queries and the results from their searches. With these metrics, you can identify the areas where you can improve Virtual Agent to offer more meaningful search results.

Use the **User Search Metrics** tab in the Conversational Analytics dashboard to view key indicators about the queries that users searched on and the corresponding search results. By using this tab, you can get the answers to the following questions:

-   Which search results were not useful to the users?
-   Which queries did not have any search results?
-   Which were the most common queries from users?
-   Which search results did the users select most often?

To access the **User Search Metrics** tab, you must have the chat analytics admin role or the chat analytics viewer role. The following example shows the data included in the **User Search Metrics** tab.

![Conversational Analytics dashboard user search metrics tab.](../images/dashboard-user-search-metrics-pae.png "User Search Metrics tab")

## AI Search

Virtual Agent topics may use AI search to suggest helpful resources to the user. When a user enters a query, AI search provides the most relevant results by using intelligent query features. To know more about AI search, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) . To integrate Virtual Agent with AI Search, see [Improving the user experience with AI Search](va-ai-search.md).

## Contextual Search

Contextual search matches keywords to an existing database search to find potential matches to a query. Virtual Agent topics may use contextual search to resolve queries. For more information, see [Maximizing code reuse with topic blocks](topic-blocks-overview.md).

## Topic Links

Some Virtual Agent topics have links to useful resources that are embedded within them. When a user invokes one of these topics, the link shows up without having to do any back-end search.

## User Search information

The following table describes user search indicators visualized on the **User Search Metrics** tab.

|Visualization|Description|
|-------------|-----------|
|Total number of queries with no clicks|Number of queries that users did not click on any of the search results provided.|
|Top 10 queries with no clicks|Most commonly asked queries where users did not click on any of the search results provided.|
|Total number of queries with no results|Number of queries that did not yield any search result.|
|Top 10 queries with no results|Most commonly asked queries that did not yield any search results.|
|Total number of queries|Total number of queries handled by Virtual Agent.|
|Top 10 queries|Most commonly asked queries.|
|Total number of search results clicked|Number of search results that users clicked on.|
|Top 10 search results clicked|Search results that users clicked on the most.|

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

