---
title: Set up Virtual Agent for Universal Request integration with Microsoft Teams
description: Publish the default Virtual Agent topics \(conversation flows\) so that they can be used in the Universal Request integration with Microsoft Teams application.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Universal Request integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Set up Virtual Agent for Universal Request integration with Microsoft Teams

Publish the default Virtual Agent topics \(conversation flows\) so that they can be used in the Universal Request integration with Microsoft Teams application.

## Before you begin

To use Virtual Agent capabilities, you must activate the following plugins:

-   Universal Request: Virtual Agent Conversations plugin \(com.snc.universal\_request.va\) to set up and use Virtual Agent in Universal Request. This plugin installs the Virtual Agent topics that must be made active. By default, the topics are set to inactive.
-   Universal Request: NLU Model for Virtual Agent Conversations plugin \(com.snc.universal\_request.nlu\) to set up and use the NLU model for Virtual Agent conversations.

Role required: admin

## About this task

Activate the Virtual Agent topics for Universal Request.

You can also clone and modify the default topics or create your own topics to use during the chatbot conversations. For more information on creating a topic, see Create a Virtual Agent topic.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the **Category** field, enter `Universal Request`.

    The following topics and topic blocks are displayed:

    -   Employee Help Request \(Template\)
    -   Employee Help Request \(Teams Template\)
    -   Track Universal Request Status \(Template\)
    -   Update UR \(Template\)
3.  Click the **Employee Help Request \(Teams Template\)** topic to open it.

4.  On the header section, select **Publish**.

    The topic is made available and active in the chat window.

    **Note:** This topic has the same functionality as the **Employee Help Request \(Template\)** topic, but is specially configured for Microsoft Teams.

5.  Repeat this procedure to open and publish the **Track Universal Request Status \(Template\)** topic.

    **Note:** If you have already published the **Track Universal Request Status \(Template\)** topic for Universal Request, you can skip this step.


**Parent Topic:**[Configure Universal Request integration with Microsoft Teams](../concept/ur-ms-teams-config-ur.md)

