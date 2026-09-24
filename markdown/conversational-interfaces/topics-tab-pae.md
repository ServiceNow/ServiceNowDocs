---
title: \(Legacy\) Topics tab
description: Use the Topics tab in the Conversational Analytics dashboard to identify the best and underperforming topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/topics-tab-pae.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using, Conversational Analytics dashboard, Analyze Virtual Agent performance, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Topics tab

Use the **Topics** tab in the Conversational Analytics dashboard to identify the best and underperforming topics.

The **Topics** tab provides insights into which Virtual Agent \(VA\) topics are performing well and which aren’t. To use the Topics tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

\[Omitted image "Dashboard-Topics-2-pae.png"\] Alt text: Virtual Agent dashboard topics tab.

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

The Spokes indicator provides details of the spoke, actions, subflows, and topics that executed the spoke. Select a spoke on the chart to view the details of the spoke. For more information, see [\(Legacy\) Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/topic-spokes-subtab-pae.md).

-   **[\(Legacy\) Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/topic-spokes-subtab-pae.md)**  
Use the Spokes indicators to view details such as spoke usage, spoke actions, and subflows for the selected spoke.
-   **[\(Legacy\) Topic categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/category-page-pae.md)**  
Use the Category page in the Conversational Analytics dashboard to view the performance of Virtual Agent \(VA\) topics by the selected topic category.
-   **[\(Legacy\) Topic details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/topic-details-subtab-pae.md)**  
Use the Topic Details page in the Conversational Analytics dashboard to view key performance indicators of Virtual Agent \(VA\) topics.

**Parent Topic:**[\(Legacy\) Using the Conversational Analytics Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/use-the-dashboard-overview-pae.md)

