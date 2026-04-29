---
title: Funnels tab
description: Funnels provide cumulative filtering of conversation flows. Using funnels, you can identify whether your conversation flows are performing effectively when users chat with Virtual Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Funnels tab

Funnels provide cumulative filtering of conversation flows. Using funnels, you can identify whether your conversation flows are performing effectively when users chat with Virtual Agent.

**Note:** Funnels is accessible only to users who have funnels created prior to upgrading to the new dashboard. Users with funnels created in the legacy dashboard can view the analytics related to funnels and edit the funnels in the new dashboard, however, creation of funnels is no longer supported.

![Select the Funnels option on the menu to view the Funnels page.](../images/funnels-page.png "Funnels page")

![Video link to Funnels demo.](../../conversational-interfaces/image/icon-video-link.png) [Funnels demo](https://www.youtube.com/watch?v=YMAaTSzPhwM&t=714s) Watch this video for an overview of Funnels.

## Overview of funnels

Funnels filter conversation flows using steps that are defined when a user creates the funnel.

A funnel can contain up to 10 filtering steps for a conversation flow. Each subsequent step further refines the results from the previous step. This type of cumulative filtering helps you to easily narrow down on the data of interest at each step of the conversation flow.

When you run a funnel for a particular date range, the system displays the following metrics that show the number of users at each step:

-   The percentage and number of users who have used the specified conversation flow.
-   The percentage and number of users who proceeded to the next conversation step specified in the funnel.
-   The percentage of users who dropped off at a particular conversation step.
-   The percentage and number of users who completed all specified conversation steps in the flow.
-   The biggest drop-off point or step where users left the conversation flow.

Each step in a funnel consists of the following:

-   Field: The item on which the step is evaluated.
-   Operator: A list of operators that is contextually generated based on the selected field.
-   Value: A text entry field or a list that is contextually generated based on the selected field.

## Use case for funnels

Consider an example scenario where an admin has to get insights about how Virtual Agent is handling user queries in a conversation flow. To review the efficiency of the conversation flow, the admin might look for information such as the following:

-   What percentage or number of users have interacted with Virtual Agent.
-   Out of the users who interacted with Virtual Agent, what percentage or number of users have followed a specific node in the topic during the conversation.
-   Out of the users who used the specific node, what number of users requested for a transfer to a live agent.

For example, see the following funnel for fetching metrics on a conversational flow that provides software access.

![The filter specifies the Software Access standard topic in which the Drive Flow Executed topic node has run and the user requested a transfer to a live agent.](../images/drive.png "Funnel")

Here, the funnel has three filtering steps:

-   Step 1 fetches users who have followed the **Software Access** topic while interacting with the Virtual Agent.
-   Out of the retrieved users from step 1, step 2 fetches users who requested for a drive access in the **Drive Flow Executed** node.
-   Out of the retrieved users from step 2, step 3 fetches users who requested transferring to a live agent.

## Metrics for funnels

Using Funnels, you can easily filter conversation flows and get information as metrics. Metrics indicate what percentage or number of users are active at each step of the conversation flow.

You can improve the conversation flows based on the performance metrics derived from using funnels. The metrics help identify opportunities for improving conversation flows so that Virtual Agent can handle your user queries better.

![The metrics show the percentage and number of users who made it through the steps and the step that experienced the biggest drop-off point for users.](../images/funnels-metrics.png "Metrics for funnels")

## Other benefits of using funnels

You can compare the performance of previous and current conversation flows. Funnels show metrics for the specified date range. Additionally, it shows the comparison for the same number of days in the date range prior to the specified start date. You can know the increase or decrease in users who have made through all the steps.

![The change from previous metrics displays at the bottom of the card. For example, the percentage of users may display as a 25% increase from the previous 8 days.](../images/prev-metrics.png "Previous metrics")

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

