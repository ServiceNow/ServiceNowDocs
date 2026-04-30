---
title: Legacy - Exploring the Conversational Analytics Dashboard
description: Use Conversational Analytics dashboard to improve Virtual Agent \(VA\) interactions with users. The dashboard provides deep insights into conversational data, and helps you refine topics and increase the percentage of issues resolved by VA.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-08"
reading_time_minutes: 6
keywords: [Legacy, Conversational, Dashboard, Virtual Agent, Analytics, topics, insights, visualization]
breadcrumb: [Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Exploring the Conversational Analytics Dashboard

Use Conversational Analytics dashboard to improve Virtual Agent \(VA\) interactions with users. The dashboard provides deep insights into conversational data, and helps you refine topics and increase the percentage of issues resolved by VA.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

## Virtual Agent Analytics

Virtual Agent keeps records of interactions with users for up to 90 days. The metrics extracted from the conversations are retained for a period of two years. The Conversational Analytics dashboard provides insights into those interactions so you can see how well Virtual Agent understood and resolved user issues. Dashboard metrics, for example, reveal:

-   What percentage of users transfer from VA to a live agent
-   How to increase engagement rate and reduce user drop-offs
-   Whether the user reached the last node in a topic
-   Most and least-used topics
-   Conversation details using advanced filters
-   How to optimize conversation design

![Virtual agent analytics overview tab](../images/vaa-next-exp-overview.png)

## Key Features

-   **Worst performing topics**

    See the worst-performing VA topics over a given time period.

    ![Virtual Agent worst performing topics dialog box, with Least Used tab active.](../images/vaa-next-least-performing-topic.png)

-   **Conversation details**

    Discover metadata about each VA interaction, including the user, the chat duration, and which node a user stopped at in a topic.

    ![Virtual Agent Analytics Dashboard conversation details tab.](../images/vaa-next-conversation-details.png)

-   **User insights**

    Get a history of a user's chats.

    ![Virtual Agent chat User details with multiple chat events shown.](../images/vaa-next-user-details.png)


## Overview of using dashboard sections

The following sections provide a high-level overview of how to use each section of the dashboard from the top down.

-   **Date range of data displayed**

    The **Start** and **End** dates at the top of the dashboard specify the data range of the data summarized on each page.

    ![Virtual Agent chat data ranges shown by start and end dates in year-month-day format.](../images/dashboard-top-dates.png)

    All data is continually pushed from Virtual Agent to the dashboard in real time, and retained for up to 3 months. The analytics dashboard can also accept conversation data up to 30 days old, to support scenarios involving temporary technical issues.

    All dates and times on the dashboard are UTC. Even though the conversation table lists conversation dates and times in different time zones, Virtual Agent \(VA\) converts them to UTC when displaying them on the dashboard. Additionally, if you select a preset date range, such as last week, the dates might be slightly different from what you expect.

    For information about setting the date range, see [Set the date range of the data](../task/use-the-dashboad.md).

    Certain data visualizations might not have data available for the start date and end date selected in the **Start** and **End** fields. In this case, the widget shows a start date and end date for the visualization based on the data availability within the selected date range.

-   **Getting detailed data**

    The **Overview** tab provides summaries of the data displayed on the other tabs. You can get to more detailed data in several ways:

    -   Select a tab, for example, **Usage**.
    -   Select the arrowhead in one of the cards.

        ![Virtual Agent active users widget.](../images/vaa-next-active-va-users.png)

    -   Select a visualization.

        ![Open graph in Virtual Agent expanded from Active users widget, with arrow indicator pointing to New Issue category.](../images/vaa-next-click-a-visualization.png)

-   **Dashboard tabs**

    |Tab|Description|
    |---|-----------|
    |Overview|Landing page for the dashboard that shows summary information for all the other tabs.|
    |Usage|Describes VA conversation usage, for example, the language of the conversations, their durations, and the types of conversations.|
    |Conversations|Summary information for a user's conversations. Advanced filtering enables you to filter by conversation nodes or topics, and get details about the conversation duration, the channel the conversation occurred in, and the number of messages exchanged. You can link to details about each conversation on this tab.|
    |Users|Lists the users who have had VA conversations. Advanced filtering provides analytics about usage frequency, by conversation, the duration of the conversation for each user, the user's first and last conversation, and the language used. You can link to user details from this tab, including their conversations.|
    |Topics|Shows metrics about topics used by VA in conversations. Metrics include how many VA conversations moved to a live agent, average length of conversations per topic, and topic blocks used.|
    |NLU Prediction|Shows the number of times the NLU prediction model accurately understood the intent of the user's conversation or auto-selected a topic. The chart links to the NLU Workbench if your instance includes NLU.|
    |Custom Events|Displays the number of custom chat events that you create using the Events page. If you don't create custom events, the tab content is empty.|
    |Funnels|Provides metrics for conversation flows.|
    |Issue Auto-Resolution|Displays information about the number of user issues intercepted by the auto-resolution service and resolved by the Virtual Agent.|

-   **Trends and scores**

    Many tabs use scorecards that show the current value for a data point, for example, the number of conversations currently online.

    ![Virtual Agent analytics Dashboard scorecard.](../images/vaa-next-virtual-agent-activity.png)

    Scorecards also show data trends, such as the increase or decrease of the data values over the date range specified on the dashboard. Hovering over the title of a scorecard displays a description of the scorecard.

    Certain trend visualizations on the dashboard such as the trends in intent and topic matching do not support viewing monthly, weekly, and daily data.

-   **Visualizing data**

    Many tabs show visualizations of the recorded VA data.

    ![Three Virtual Agent data visualization tabs displaying Category, Topics, and User Feedback data.](../images/vaa-next-virtual-agent-performance.png)

    The cards have a common setup.

    ![Virtual Agent chat dashboard general widget UI. Summarized Data, Data sets tabs, more information arrow, and data visualization areas of the card are highlighted.](../images/vaa-next-categories-summary.png)

    In each visualization, you can select:

    -   Subtabs to visualize different datasets in the visualization.
    -   Arrowhead icon ![arrowhead](../images/dashboard-arrowhead.png), which takes you to the corresponding tab that provides more detailed information.

        For example, select the arrowhead in the **Active Users** scorecard to go to the **Users** tab, which shows a list of users currently using VA chat.

        ![Virtual Agent active users widget.](../images/vaa-next-active-va-users.png)

    -   Select displayed data, such as a bar in a bar chart, to display detailed information about that data.

## Tutorial

Now that you are familiar with the user interface, you can [try the tutorial](../task/dashboard-scenario-1.md). It shows how the parts of the dashboard work together to provide insights for improving VA.

-   **[Trying out the dashboard](../task/dashboard-scenario-1.md)**  
Use this tutorial to get familiar with the Conversational Analytics Dashboard.

**Parent Topic:**[Legacy - Conversational Analytics Dashboard](VA-dashboard-landing-page.md)

