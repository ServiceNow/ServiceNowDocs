---
title: Set up Virtual Agent for Universal Request
description: Use Virtual Agent \(VA\) capabilities to provide a better user experience for your chat channel using the ServiceNow Natural Language Understanding \(NLU\) model. Publish and use the default Virtual Agent topics for Universal Request.
locale: en-US
release: zurich
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Universal Request, Configure, Universal Request, Employee Service Management]
---

# Set up Virtual Agent for Universal Request

Use Virtual Agent \(VA\) capabilities to provide a better user experience for your chat channel using the ServiceNow® Natural Language Understanding \(NLU\) model. Publish and use the default Virtual Agent topics for Universal Request.

## Before you begin

To use VA capabilities, you must activate the following plugins:

-   Activate the Universal Request: Virtual Agent Conversations plugin \(com.snc.universal\_request.va\) to set up and use Virtual Agent in Universal Request. This plugin installs the Virtual Agent topics that must be made active. By default, the topics are set to inactive.
-   Activate the Universal Request: NLU Model for Virtual Agent Conversations plugin \(com.snc.universal\_request.nlu\) to set up and use the NLU model for Virtual Agent conversations.

Role required: admin

## About this task

Activate the Virtual Agent topics for Universal Request.

You can also copy and modify the default topics or create your own topics to use during the chatbot conversations. For more information on creating a topic, see [Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Enter `Universal Request` in the **Category** field.

    The following topics and topic blocks are displayed:

    -   Employee Help Request \(Template\)
    -   Track Universal Request Status \(Template\)
    -   Update UR \(Template\)
3.  Select the **Employee Help Request \(Template\)** topic to open it.

4.  On the header section, select **Publish**.

    The topic is made available and active in the chat window.

5.  Repeat this procedure to open and publish the Track Universal Request Status \(Template\) and Update UR \(Template\) topics.


-   **[Enable Natural Language Understanding model for Universal Request topic](nlu-model-setup-ur.md)**  
Apply the Natural Language Understanding vocabulary in the Universal Request application to help the system to understand human-expressed language.

**Parent Topic:**[Configuring Universal Request](../concept/configure-ur.md)

