---
title: Legacy - Overview tab
description: Use the Overview tab to get a snapshot of some of the information collected in the Conversational Analytics dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [Legacy, Overview, tab, Conversational Analytics, dashboard, Chat Analytics Viewer, chat\_analytics\_viewer]
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Overview tab

Use the Overview tab to get a snapshot of some of the information collected in the Conversational Analytics dashboard.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

The **Overview** tab is the landing page for the dashboard. It provides a summary of the information on all the other dashboard tabs. To use the **Overview** tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

**Note:** Now Assist in Virtual Agent Analytics appears in the left navigation only when you have Now Assist in Virtual Agent enabled.

![Virtual agent analytics dashboard overview tab](../images/vaa-next-exp-overview.png)

For directions about using the widgets on the **Overview** tab, see [Explore the Virtual Agent Analytics Dashboard](dashboard-explore-dashboard.md).

<table id="table_lhm_1qk_4rb"><thead><tr><th>

Visualisation

</th><th>

descriptions

</th></tr></thead><tbody><tr><td>

Deflection Count

</td><td>

Number of deflection occurrences measured by the execution count of the Deflection topic block. A deflection occurs when Virtual Agent resolves or helps to resolve an issue for a user.

</td></tr><tr><td>

Deflection Pattern

</td><td>

Number of deflections per deflection patterns.

</td></tr><tr><td>

KB Breakdown

</td><td>

Titles of KB articles with the number of times they were presented as part of deflections.

</td></tr><tr><td>

Active VA users

</td><td>

Cumulative number of unique active end users \(not agents\) who used the conversational interface.

</td></tr><tr><td>

Conversations

</td><td>

Count of all interactive conversations initiated from the Virtual Agent.

</td></tr><tr><td>

VA success

</td><td>

Percentage of conversations that were completed without escalation and with an intended topic flow.Completed conversations are those that reach the end of a Virtual Agent topic or conversation, are closed by the user, or are automatically closed.

 Completed without escalation means that the conversation was not routed to a live agent, and the user did not give negative feedback. \(Feedback types include negative, positive, neutral, and no feedback.\)

</td></tr><tr><td>

Topic flows completed

</td><td>

Percentage of topics that end users completed till the last node out of all topics invoked and ran.

</td></tr><tr><td>

Categories

</td><td>

Number of completed conversations shown per the Topic Category.

</td></tr><tr><td>

Topics

</td><td>

Number of occurrences when the user completed to the last node or left a conversation midway through for each topic.

</td></tr><tr><td>

User feedback

</td><td>

Feedback Results categorized as good, bad and neutral. The Feedback results are calculated from the Feedback Setup Topic.**Note:** Analytics Administrator can change how frequently the Feedback Setup topic show post-chat by changing the system properties.

</td></tr><tr><td>

Channels

</td><td>

Number of conversations executed across the configured channels of the Virtual Agent.

</td></tr><tr><td>

Conversation end state

</td><td>

Number of conversations that have ended in the OOTB Conversation End state.

</td></tr></tbody>
</table>Typical actions on the **Overview** tab include:

-   Selecting the arrowhead icon ![Carat](../images/dashboard-carat.png) in any of the widgets to open other dashboard tabs that display more detailed information.
-   Selecting the visualized data, for example, a bar in a bar chart, to get additional information about the data.
-   Changing the date range of the data displayed.
-   Selecting a tab inside one of the widgets to change the set of data displayed. For example, in **Categories** bar chart, select the **Incomplete** tab.

**Note:** Your **Overview** tab might look different because [it can be configured](../task/edit-overview-tab.md).

-   **[Edit the Overview page](../task/edit-overview-tab.md)**  
Add or subtract the widgets on the **Overview** page to suit your users.

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)

