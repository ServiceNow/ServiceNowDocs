---
title: Exploring the Conversational Analytics dashboard in Platform Analytics experience
description: Use Conversational Analytics dashboard to improve Virtual Agent \(VA\) interactions with users. The dashboard provides insights into conversational data, and helps you refine topics and improve the deflection rate of VA.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Virtual Agent, Conversational, Platform, Analytics, improve, deflection, rate, dashboard, experience]
breadcrumb: [Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Exploring the Conversational Analytics dashboard in Platform Analytics experience

Use Conversational Analytics dashboard to improve Virtual Agent \(VA\) interactions with users. The dashboard provides insights into conversational data, and helps you refine topics and improve the deflection rate of VA.

## Conversational Analytics dashboard

Conversational Analytics dashboard provides insights into conversations so you can see how well Virtual Agent understood and resolved user issues. Virtual Agent keeps conversational data, that is, records of conversations with the users, and analytics data for up to two years. The dashboard contains indicators which, for example, reveal:

-   What percentage of users transfer from VA to a live agent
-   How to increase engagement rate and reduce user drop-offs
-   Whether the user reached the last node in a topic
-   Most and least used topics
-   Conversation details using advanced filters
-   How to optimize conversation design

![Virtual agent analytics overview tab](../images/vaa-next-exp-overview-pae.png)

## Key features

-   **Underperforming topics**

    See the underperforming VA topics to investigate and improve topic performance.

    ![Virtual Agent Underperforming topics section with visualizations for least used and incomplete topics.](../images/vaa-next-least-performing-topic-pae.png)

-   **Conversation details**

    Discover metadata about each VA interaction, including the user, chat duration, conversation type, and channel.

    ![Virtual Agent Analytics Dashboard conversation details tab.](../images/vaa-next-conversation-details-pae.png)


## Overview of Conversational Analytics dashboard

The following sections provide a high-level overview of how to use each section of the dashboard from the top down.

-   **Date range of data displayed**

    The **Start date** and **End date** fields at the top of the dashboard specify the data range of the data summarized on each page.

    ![Virtual Agent chat data ranges shown by start and end dates in year-month-day format.](../images/dashboard-top-dates-pae.png)

    All data is continually pushed from Virtual Agent to the dashboard in real time, and retained for up to two years.

    For information about setting the date range, see [Set the date range of the data](../task/use-the-dashboad.md).

    Certain data visualizations might not have data available for the start date and end date selected in the **Start date** and **End date** fields. In such cases, the indicator shows data for a start date and end date based on data availability within the selected date range.

-   **Getting detailed data**

    The **Overview** tab contains key indicators to help you evaluate the performance of VA. You can view more details in the following ways:

    -   Select a tab, for example, **Usage**.
    -   Select an indicator, for example, **Active VA users**.



-   **Dashboard tabs**

    |Tab|Description|
    |---|-----------|
    |Overview|View the key indicators of the performance of VA.|
    |Now Assist in VA|View key indicators to monitor the performance of Now Assist in Virtual Agent. This is visible only when Now Assist in Virtual Agent is enabled.|
    |Usage|View VA conversation usage, for example, the language and conversation type. You can also drill down to the list of conversations of a certain language or conversation type.|
    |Conversations|View conversation details and troubleshoot individual conversations. Advanced filtering enables you to filter the list of conversations by conversation type, duration, user, and language.|
    |Users|View how your users are conversing with VA. Advanced filtering enables you to filter the list by user, channel, and last conversation.|
    |Topics|View topic performance indicators. Some of the indicators are most and least used topics, topics corresponding to VA conversations that were transferred to a live agent, average length of conversations per topic, and topic blocks used.|
    |NLU Prediction|View NLU performance indicators such as number of times the NLU prediction model accurately understood the intent of the user's conversation or auto-selected a topic. The indicator links to the NLU Workbench if your instance includes NLU.|
    |Custom Events|View the number of custom chat events that you created using the Events page.|
    |Issue Auto-Resolution|View details about the number of user issues intercepted by the auto-resolution service and resolved by the Virtual Agent.|

-   **Virtual Agent activity**

    This area of the dashboard contains indicators that show Virtual Agent activity such as number of active users who interacted with the Virtual Agent, number of conversations initiated on the Virtual Agent, and so on.

    ![Virtual Agent analytics dashboard key performance indicators.](../images/vaa-next-virtual-agent-activity-pae.png)

    Selecting on the info icon displays the description of the indicator.

    Certain trend visualizations on the dashboard such as the trends in intent and topic matching do not support viewing monthly, weekly, and daily data.

-   **Virtual Agent performance**

    This area of the dashboard contains indicators such as topic performance and user feedback that show how well Virtual Agent topics performed and the feedback from the user.

    ![Virtual Agent analytics dashboard key performance indicators.](../images/vaa-next-virtual-agent-activity-pae.png)


**Parent Topic:**[Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md)

