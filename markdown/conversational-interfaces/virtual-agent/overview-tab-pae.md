---
title: Overview tab
description: Use the Overview tab to view key indicators that help you evaluate the performance of Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Overview tab

Use the Overview tab to view key indicators that help you evaluate the performance of Virtual Agent.

The **Overview** tab is the landing page for the dashboard. The visualizations in the **Overview** tab are important indicators of how VA is performing. You must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role to use the **Overview** tab.

**Note:** Now Assist in Virtual Agent Analytics appears in the left navigation only when you have [Now Assist in Virtual Agent](../../now-assist-in-va/concept/now-assist-in-va-landing.md) enabled.

![Virtual agent analytics dashboard overview tab](../images/vaa-next-exp-overview-pae.png)

<table id="table_lhm_1qk_4rb"><thead><tr><th>

Indicators

</th><th>

Descriptions

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

Cumulative number of unique active end users \(not agents\) who used the conversational interface. Select the indicator to drill down to the list of users.

</td></tr><tr><td>

Conversations

</td><td>

Count of all interactive conversations initiated from the Virtual Agent.Select the indicator to drill down to the list of conversations.

</td></tr><tr><td>

VA success

</td><td>

Percentage of conversations that were completed without escalation and with an intended topic flow.Completed conversations are those that reach the end of a Virtual Agent topic or conversation, are closed by the user, or are automatically closed.

Completed without escalation means that the conversation was not routed to a live agent, and the user did not give negative feedback. \(Feedback types include negative, positive, neutral, and no feedback.\)

Select the chart to drill down to the conversations that were completed successfully.

</td></tr><tr><td>

Topic flows completed

</td><td>

Percentage of topics that end users completed till the last node out of all topics invoked and ran.

</td></tr><tr><td>

Topic Category - Complete

</td><td>

Number of completed conversations shown per topic category. Select a topic category on the bar chart to drill down to the topic category details.

</td></tr><tr><td>

Topic Category - Incomplete

</td><td>

Number of incomplete conversations shown per topic category. Select a topic category on the bar chart to drill down to the topic category details.

</td></tr><tr><td>

Topic - Complete

</td><td>

Number of occurrences per topic when the user completed to the last node. Select a topic on the bar chart to drill down to the topic details.

</td></tr><tr><td>

Topic - Incomplete

</td><td>

Number of occurrences per topic where users abandoned the conversation before the topic reached the last node. Select a topic on the bar chart to drill down to the topic details.

</td></tr><tr><td>

User feedback

</td><td>

Feedback results categorized as good, bad and neutral. The feedback results are calculated from the Feedback Setup topic.**Note:** A user with Chat Analytics Admin role can change how frequently the Feedback Setup topic shows after the completion of chat using the system properties.

Select a feedback result on the chart to drill down to the list of conversations associated with the feedback.

</td></tr><tr><td>

Channels

</td><td>

Number of conversations executed across the configured channels of the Virtual Agent.Select a channel on the chart to drill down to the list of conversations associated with the channel.

</td></tr><tr><td>

Conversation end state

</td><td>

Number of conversations that have ended in the out-of-the-box conversation end state.Select a Conversation end state on the chart to drill down to the list of conversations associated with the Conversation end state.

</td></tr></tbody>
</table>Typical actions on the **Overview** tab include:

-   Selecting a deflection configuration to view the deflection indicators such as deflection count, deflection patter, and KB Breakdown.
-   Selecting the visualized data, for example, a bar in a bar chart, to get additional information about the data.
-   Changing the date range of the data displayed.

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

