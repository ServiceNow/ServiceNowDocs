---
title: Setting up ITSM Virtual Agent Lite
description: Setup ITSM Virtual Agent Lite using to use the read-only, pre-built conversation topics for your most common ITSM self-service cases. For example, you can connect your users with a virtual agent to check ticket status, search the knowledge base, and report an issue.
locale: en-US
release: yokohama
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM Virtual Agent Lite, IT Service Management]
---

# Setting up ITSM Virtual Agent Lite

Setup ITSM Virtual Agent Lite using to use the read-only, pre-built conversation topics for your most common ITSM self-service cases. For example, you can connect your users with a virtual agent to check ticket status, search the knowledge base, and report an issue.

## Before you begin

Role required: admin or virtual\_agent\_admin

## About this task

Virtual Agent Lite is a subset of the features available in Virtual Agent. Virtual Agent Lite is automatically activated. You don't need a subscription for Virtual Agent Lite.

Users with the admin or virtual\_agent\_admin role can activate the required plugins:

-   ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\) plugin

    Activates the read-only conversation topics for basic ITSM self-service.

-   The Service Management Virtual Agent Core \(com.glideapp.sm\_va\_core\) plugin

    Provides core functionality for Service Management Virtual Agent. This plugin is automatically activated with the ITSM Virtual Agent Conversation Topics Lite plugin.


## Procedure

1.  Activate the ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\) plugin to access the pre-built ITSM Virtual Agent Lite conversation topics.

2.  Review the **ITSM Self Service Lite** read-only conversation topics in Virtual Agent Designer.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    2.  In the **Category** drop-down box, select **ITSM Self Service Lite**.

3.  Select an available topic to open it.

    The conversation topic template opens in Virtual Agent Designer.

4.  Select **Inactive** in the header bar, and slide the toggle switch to **Active**.

    **Note:** Deactivate a topic by selecting **Active** and sliding the toggle switch to the inactive position.

5.  Select **Publish** to publish the topic.

    **Note:** For details about activating and publishing conversation topics, see [Getting started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

6.  Test an active, published conversation topic, by selecting the topic you want to test in Virtual Agent Designer and selecting **Test**.


-   **[ITSM Virtual Agent Lite pre-built topics](../reference/itsm-virtual-agent-lite-topics.md)**  
ITSM Virtual Agent Lite includes several pre-built, read-only topic conversations you can use to set up a virtual agent for your end users.

**Parent Topic:**[ITSM Virtual Agent Lite](../concept/itsm-virtual-agent-lite.md)

