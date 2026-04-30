---
title: Set up ITSM Virtual Agent
description: You can create and publish conversation topics in Virtual Agent Designer if you have administrator roles.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up, ITSM Virtual Agent, IT Service Management]
---

# Set up ITSM Virtual Agent

You can create and publish conversation topics in Virtual Agent Designer if you have administrator roles.

## Before you begin

Role required: admin

## About this task

[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) must be activated before you can use the ITSM Virtual Agent topic conversations. Users with the admin roles can activate Glide Virtual Agent \[com.glide.cs.chatbot\].

Install ITSM Virtual Agent and the ITSM NLU Model for Virtual Agent Conversations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Topics must be activated and published before your employees can use them. By default, the base system provides topics as inactive and unpublished. To view, duplicate, preview, or publish ITSM topics in the Virtual Agent Designer, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Procedure

1.  Activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\).

2.  Install ITSM Virtual Agent by requesting it from the ServiceNow Store.

3.  Review the ITSM-related conversation topics in Virtual Agent Designer.

4.  [Configure Natural Language Understanding \(NLU\) in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-nlu-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    ITSM Virtual Agent topics use ServiceNow NLU models. The English NLU models are activated by default. If you are using other languages, you must activate those NLU models manually. For details, see [Multilingual model management](https://www.servicenow.com/docs/access?context=multilingual-model-managent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

5.  Publish the ITSM Virtual Agent topics and their corresponding NLU models in Virtual Agent Designer.

    Publishing them in Virtual Agent Designer lets users run the conversations in your Virtual Agent support client.

    **Note:** You can't edit the provided topics. You can duplicate a provided topic and then edit it. You can also create additional topics. For complete details about activating and publishing conversation topics, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

6.  To test an active, published conversation topic, select the topic to test in Virtual Agent Designer and select **Test**.


**Parent Topic:**[Setting up ITSM Virtual Agent](../concept/setting-up-itsm-va.md)

