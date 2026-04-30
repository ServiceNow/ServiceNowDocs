---
title: Topics tab
description: Use the Topics tab in the Conversational Analytics dashboard to identify the least and best performing topics.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Topics tab

Use the **Topics** tab in the Conversational Analytics dashboard to identify the least and best performing topics.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

The **Topics** tab provides insights into which Virtual Agent \(VA\) topics are performing well and which aren’t. You can also select multiple topic categories using the **Select Categories** dropdown to visualize data based on your selection. To use the Topics tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

![Virtual Agent dashboard topics tab.](../images/Dashboard-Topics-2.png)

## Worst performing topics

The Worst performing topics chart provides multiple ways of detecting chat topics that didn't work. The horizontal axis lists the chat topics. The subtabs include:

-   Least used—The topics used least in chats.
-   Incomplete—The topics the user abandoned without resolution.
-   Transfer to Live Agent—The topics the user couldn't resolve with Virtual Agent. So, the user transferred to a live agent.

## Best performing topics

The topics in this chart are performing well. The horizontal axis lists the topics. The count on the vertical axis varies depending on the subtab selected:

-   Most Used—Number of times users used a topic.
-   Complete—Number of times users completed a topic without the assistance of a live agent.

## Spokes used

For more information about the spokes used, see [Legacy - Spokes](topic-spokes-subtab.md).

## List of topics

The **Topics** page list the topics used in the date range specified in the Conversational Analytics Dashboard.

![Virtual Agent dashboard list of topics.](../images/dashboard-list-of-topics.png)

|Topic information|Description|
|-----------------|-----------|
|Correct NLU Prediction %|Percentage of times this topic name was predicted correctly out of all times this topic name was predicted. A correct prediction means that VA showed that a predicted topic and a user selected it.|
|Initiated %|Percentage of times this topic ran out of all the topics that ran.|
|Incomplete %|Percentage of times the user didn't reach the last node in the topic out of all times this topic ran. For example, if the 2 users didn't complete all the nodes in a topic but 8 other users did, the incomplete percentage would be 20%.|
|Transfer to Live Agent %|Percentage of occurrences where this topic transferred from VA to a live agent out of all the time this topic ran.|

## List of topic blocks

The **Topic Blocks** page list the topic blocks used in the date range specified in the Conversational Analytics Dashboard.

![Virtual Agent Topic Blocks page showing list of topics.](../images/dashboard-list-of-topic-blocks.png)

The chart shows the number of times each topic block was executed.

-   **[Legacy - Topic categories](category-page.md)**  
Use the Category page in the Conversational Analytics dashboard to see the performance of Virtual Agent \(VA\) topics divided into categories.
-   **[Legacy - Topics details](topic-details-subtab.md)**  
Use the Topic Details page in the Conversational Analytics dashboard to see the details of the Virtual Agent \(VA\) topics.
-   **[Legacy - Spokes](topic-spokes-subtab.md)**  
Use the Spokes page to see the details of the spoke actions and subflows for the Virtual Agent \(VA\) topic.

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)

