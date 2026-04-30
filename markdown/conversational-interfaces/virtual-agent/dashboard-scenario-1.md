---
title: Trying out the dashboard
description: Use this tutorial to get familiar with the Conversational Analytics Dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Legacy - Exploring the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Trying out the dashboard

Use this tutorial to get familiar with the Conversational Analytics Dashboard.

## Before you begin

Role required: Chat Analytics Viewer \(chat\_analytics\_viewer\)

**Note:** This tutorial is intended for use in your own instance. Test instances can be used but may not provide meaningful feedback unless they contain pre-loaded data.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Conversational Analytics** &gt; **Virtual Agent Dashboard**.

    The **Overview** tab on the dashboard appears. The **Topic flows completed** scorecard shows that the number of users completing all the nodes in a topic has decreased. I'd like to know why.

2.  In the **Topics** visualization, click **Incomplete**.

    ![Incomplete topics displayed in Virtual Agent dashboard.](../images/dashboard-topics-incomplete.png)

    I see that users did not complete the **Testing Topic** the most times, 14. So, I want to find out where the user got lost.

3.  Click the **Testing Topic** bar to drill down on that topic.

    The Topic details page opens. In the **Total completion** scorecard, the example shows that Virtual Agent \(VA\) resolved 15 conversations but couldn't resolve 5 conversations. The **Live Agent Transfer** scorecard shows that no one transferred to a live agent. The **Last visited node** scorecard shows the three nodes in the topic where the user abandoned the conversation: **Start**, **Testing**, and **link to requested screen**. Review those nodes to clarify the communication or add a different intent.

    ![The Topics > Topic details subtab shows topic usage, topic completion, live agent transfers, and the last visited node.](../images/testing-topic-details.png)

    No conversations in this topic transferred from VA to a live agent. But I wonder if there are topics where users did transfer.

4.  Click the **Conversations** tab.

    The **Conversations** tab displays all the conversations within the specified date range. I decide to use filters to see only the conversations that VA transferred to a live agent.

5.  Select **Live Agent Transfer**.

    I notice that the condition builder automatically entered the filter parameters, setting **Type** to **VA to LA**.

    ![Conversation filter editor showing "Type is any of VA to LA".](../images/dashboard-conversation-filter-2.png).

    I'd like to know which topic node the user last visited before transferring to a live agent.

6.  Click a conversation date.

    The conversation details appear.

7.  Expand the **Greetings** action in the **Timeline** tab.

    I see that the last node the user visited was **Send Topic Picker**. Now, I know I should revise that node in that topic.

    ![Conversation details Timeline tab with greetings topic details open.](../images/dashboard-conversation-failed-2.png)

    I decide to see which topics are working better.

8.  Select the **VA Success** filter.

    The list contains conversations that VA was able to resolve. Perhaps I want to find out if the problem resolution took too long.

9.  To add a condition, click **View/edit filter** and use the condition builder in the Filter Editor pop-up window. You can either select a default filter from the list or create a new filter condition.

10. Select **Duration** for the condition, the greater-than sign for the operator, enter 180 for the number of seconds, and click **Run**.

    The list shows VA conversations that lasted over three minutes. It's a small percentage of all the conversations. So, I conclude the topic is working well.

    Finally, I want to know which topics are most and least used so I know what topics to prioritize.

11. Click the **Topics** tab.

    The Topics page shows the best and worst performing topics.

    ![Virtual Agent conversation Topics tab displaying best and worst performing topics.](../images/dashboard-topics-tab-2.png)


**Parent Topic:**[Legacy - Exploring the Conversational Analytics Dashboard](../concept/dashboard-explore-dashboard.md)

