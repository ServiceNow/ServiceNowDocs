---
title: Legacy - Using user search metrics with Virtual Agent
description: By using user search metrics with the Virtual Agent application, you can see your users' queries and the results from their searches. With these metrics, you can identify the areas where you can improve Virtual Agent to offer more meaningful search results.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Using user search metrics with Virtual Agent

By using user search metrics with the Virtual Agent application, you can see your users' queries and the results from their searches. With these metrics, you can identify the areas where you can improve Virtual Agent to offer more meaningful search results.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

Use the **User Search Metrics** tab in the Conversational Analytics dashboard to see the key details about the queries that your users searched on and their search results. By using this tab, you can get the answers to the following questions:

-   Which search results were not useful to the users?
-   Which queries did not have any search results?
-   Which were the most common queries from users?
-   Which search results did the users select most often?

**Note:** You can also use Financial Services Remote Tables to view user-search data in Dashboards. For more information, see [Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

To access the **User Search Metrics** tab, you must have the chat analytics admin role or the chat analytics viewer role. The following example shows the data included in the **User Search Metrics** tab.

![Virtual Agent Analytics user search metrics tab.](../images/dashboard-user-search-metrics.png "User Search Metrics tab")

## AI Search

Virtual Agent topics may use AI search to suggest helpful resources to the user. When a user enters a query, AI search provides the most relevant results by using intelligent query features. To know more about AI search, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) . To integrate Virtual Agent with AI Search, see [Improving the user experience with AI Search](va-ai-search.md).

## Contextual Search

Contextual search matches keywords to an existing database search to find potential matches to a query. Virtual Agent topics may use contextual search to resolve queries. For more information, see [Maximizing code reuse with topic blocks](topic-blocks-overview.md).

## Topic Links

Some Virtual Agent topics have links to useful resources that are embedded within them. When a user invokes one of these topics, the link shows up without having to do any back-end search.

## User Search information

The following table describes the summarized User Search information that is visualized on the **User Search Metrics** tab.

|Visualization|Description|
|-------------|-----------|
|Queries with no clicks|Queries that users did not click on any of the search results. Total % refers to the number of queries with no clicks expressed as a percentage of total number of queries with no clicks.|
|Queries with no results|Queries that did not yield any search result. Total % refers to the number of queries with no results expressed as a percentage of total number of queries with no results.|
|Trending queries|Queries that users most commonly asked. Total % refers to the number of trending queries expressed as a percentage of total number of trending queries.|
|Trending content|Search results that most users clicked on. Total % refers to the number of trending search results users clicked on expressed as a percentage of total number of trending search results.|

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)

