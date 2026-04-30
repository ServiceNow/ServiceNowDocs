---
title: Activate Virtual Agent conversations with NLU
description: Integrate Natural Language Understanding \(NLU\) models with your Virtual Agent chatbot topics so that chatbots can analyze and understand the user's provided information. The chatbot can navigate the user to the right topic based on the inferred intent.
locale: en-US
release: zurich
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Virtual Agent Conversations, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Activate Virtual Agent conversations with NLU

Integrate Natural Language Understanding \(NLU\) models with your Virtual Agent chatbot topics so that chatbots can analyze and understand the user's provided information. The chatbot can navigate the user to the right topic based on the inferred intent.

## Before you begin

Role required: admin, virtual\_agent\_admin

## About this task

The Field Service NLU Model for Virtual Agent Conversations plugin \(com.sn\_fsm.nlu\) is automatically enabled when you enable the Field Service Virtual Agent Conversations plugin \(com.sn\_fsm.virtualagent\).

After enabling the plugin, you can view the following read-only intents for the Field Service NLU models in Studio:

-   My Upcoming Tasks
-   Show Nearby Tasks
-   Debrief Tasks

To use these intents, you must train and publish the predefined Field Service NLU for VA model. For more information, see [Train your NLU model](https://www.servicenow.com/docs/access?context=test-train-nlu-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Publish your NLU model](https://www.servicenow.com/docs/access?context=publish-nlu-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Enable ServiceNow NLU in Virtual Agent.

    For more information, see [Configure Natural Language Understanding in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-nlu-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

2.  Customize an intent by importing an existing intent from the Field Service NLU for Virtual Agent model.

    For more information, see [Import an NLU intent](https://www.servicenow.com/docs/access?context=import-nlu-intent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

3.  Link the NLU model with associated intents in the Virtual Agent topics.

    For more information, see [Natural Language Understanding in Virtual Agent](https://www.servicenow.com/docs/access?context=va-NLU&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


