---
title: Legacy - Spokes
description: Use the Spokes page to see the details of the spoke actions and subflows for the Virtual Agent \(VA\) topic.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Topics tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Spokes

Use the Spokes page to see the details of the spoke actions and subflows for the Virtual Agent \(VA\) topic.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

## Spokes used

The **Spokes used** chart shows which spokes, actions, and subflows were used and how often. In Virtual Agent, conversations contain topics, topics contain spokes, and spokes contain spoke actions or subflows. Selecting a spoke from the list displays the following details.

![Virtual Agent Analytics dashboard with Global spoke usage, Actions and Subflows, and Topics charts.](../images/dashboard-spoke-used-2.png)

The three charts show:

-   **Spoke Usage**—The number of times the specified spoke ran each day.

    You can display the number of occurrences and user sessions of the selected topic by selecting **Download**.

    ![Event occurrences table showing date, event name, number of occurrences, and sessions.](../images/dashboard-topics-tab-instances-2.png)

-   **Actions and Subflows**—Within the specified spoke, which actions and subflows were executed. In the previous **Actions and Subflows** chart, one action, Create Freeform VTB was triggered 22 times.
-   **Topics**—Which topics executed the spoke. The horizontal axis in the **Topics** chart shows the topics that triggered the spoke. The vertical axis shows how many times the topic triggered the spoke.

**Parent Topic:**[Topics tab](topics-tab.md)

