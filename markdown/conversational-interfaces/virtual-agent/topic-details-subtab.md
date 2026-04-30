---
title: Legacy - Topics details
description: Use the Topic Details page in the Conversational Analytics dashboard to see the details of the Virtual Agent \(VA\) topics.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Topics tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Topics details

Use the Topic Details page in the Conversational Analytics dashboard to see the details of the Virtual Agent \(VA\) topics.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

## Get additional information about the topics

You can select the visualized data selecting the topic from the list. Details about the data you selected displays.

![Virtual Agent Analytics Dashboard topic details sub-tab.](../images/dashboard-topic-details-2.png)

**Note:** The Y axis is evenly divided over 10 increments. If there are fewer than ten values on the Y axis, some values repeat, for example, five 1's in the previous image.

Use the list menu to display one of the chat interactions in the topic you selected. This page shows:

-   **Topic Usage**—The number of times the topic was used each day.

    You can display the number of occurrences and user sessions of the selected topic by selecting **Download**.

    ![Event occurrences table showing date, event name, number of occurrences, and sessions.](../images/dashboard-topic-tab-instances-2.png)

    In this example, one chat session happened on 2020-12-16.

-   **Topic completion**—Number of times the user went to the final node in the topic.
-   **Live Agent Transfer**—Number of VA chats transferred to a live agent.
-   **Last Visited Node**—Last nodes users visited before leaving the chat.

    The presumption is the user gave up after the last node they visited.


**Parent Topic:**[Topics tab](topics-tab.md)

