---
title: Legacy - Topic categories
description: Use the Category page in the Conversational Analytics dashboard to see the performance of Virtual Agent \(VA\) topics divided into categories.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-14"
reading_time_minutes: 2
keywords: [Legacy, topic, categories, Category, Conversational Analytics, dashboard, Virtual Agent]
breadcrumb: [Topics tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Topic categories

Use the Category page in the Conversational Analytics dashboard to see the performance of Virtual Agent \(VA\) topics divided into categories.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

Topic categories group related conversation topics. Topics can belong to more than one category. Select the drop-down list to show the categories that you can display in the visualizations. The visualizations show the aggregate performance of Virtual Agent conversations that ran in the topics belonging to a category.

![Virtual Agent Analytics Category subtab.](../images/dashboard-category-page-2.png)

For more information about creating or modifying VA categories, see [Create or modify custom categories](../task/create-topic-category.md).

<table id="table_mpj_xvy_j4b"><thead><tr><th>

Visualization

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conversation end state

</td><td>

The number of users that reached a specific node in a topic in the VA category. In the example, six users reached the node labeled, **System closed VA - Auto Closed**. Use this field to see where topics stopped working for users.For definitions of each conversation end state, see [Virtual Agent interaction records](va-interactions.md).

</td></tr><tr><td>

Transfer to live agent

</td><td>

The number of users that transferred from VA to a live agent in that VA category. A high number indicates that the topic is not meeting user needs.

</td></tr><tr><td>

Topic usage trend

</td><td>

Number of topics users used in a specified topic category over the course of the date range. The example shows the number of topics per day users used in the IT category. Use this field to monitor updates to topics.

</td></tr><tr><td>

Channel

</td><td>

The application the user used to chat with VA in that topic category, for example, Slack or chat widget.

</td></tr><tr><td>

Channel usage trend

</td><td>

Number of users using a specified channel over the course of the date range for topics in that VA category.

</td></tr></tbody>
</table>**Parent Topic:**[Topics tab](topics-tab.md)

