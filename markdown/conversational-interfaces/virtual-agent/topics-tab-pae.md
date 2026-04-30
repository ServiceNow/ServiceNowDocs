---
title: Topics tab
description: Use the Topics tab in the Conversational Analytics dashboard to identify the best and underperforming topics.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Topics tab

Use the **Topics** tab in the Conversational Analytics dashboard to identify the best and underperforming topics.

The **Topics** tab provides insights into which Virtual Agent \(VA\) topics are performing well and which aren’t. To use the Topics tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

![Virtual Agent dashboard topics tab.](../images/Dashboard-Topics-2-pae.png)

## Best performing topics

The Best performing topics indicators show topics that are performing well. The horizontal axis lists the topics. The count on the vertical axis refers to the number of times the topic was invoked by VA.

-   Most Used—Topics that were least invoked by VA in conversations.
-   Complete—Number of times VA completed the topic without transferring to a live agent.

## Underperforming topics

The Underperforming topics indicators show topics that didn't perform well. The horizontal axis lists the topics. The count on the vertical axis refers to the number of times the topic was invoked by VA.

-   Least used— Topics that were least invoked by VA in conversations.
-   Incomplete—The topics the user abandoned without resolution.
-   Transfer to Live Agent—The topics that were transferred to a live agent because VA couldn't resolve user's query.

## Spokes

The Spokes indicator provides details of the spoke, actions, subflows, and topics that executed the spoke. Select a spoke on the chart to view the details of the spoke. For more information, see [Spokes](topic-spokes-subtab-pae.md).

-   **[Spokes](topic-spokes-subtab-pae.md)**  
Use the Spokes indicators to view details such as spoke usage, spoke actions, and subflows for the selected spoke.
-   **[Topic categories](category-page-pae.md)**  
Use the Category page in the Conversational Analytics dashboard to view the performance of Virtual Agent \(VA\) topics by the selected topic category.
-   **[Topics details](topic-details-subtab-pae.md)**  
Use the Topic Details page in the Conversational Analytics dashboard to view key performance indicators of Virtual Agent \(VA\) topics.

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

