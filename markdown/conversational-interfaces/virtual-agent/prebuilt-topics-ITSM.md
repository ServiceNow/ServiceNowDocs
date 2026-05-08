---
title: Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models
description: Prebuilt Virtual Agent conversations \(topics\), reusable topic blocks, and ServiceNow NLU models are available for the Virtual Agent platform and various business applications, such as Customer Service Management, HR Service Delivery, IT Service Management, and more.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Install Virtual Agent plugins, Activate and get started, Virtual Agent, Conversational Interfaces]
---

# Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models

Prebuilt Virtual Agent conversations \(topics\), reusable topic blocks, and ServiceNow NLU models are available for the Virtual Agent platform and various business applications, such as Customer Service Management, HR Service Delivery, IT Service Management, and more.

These predefined conversations help users with common self-service tasks in each business area, such as creating or updating cases or providing answers to frequently asked questions. Prebuilt topic blocks are reusable components \(similar to subflows\) that perform a specific function or task and can be added to a conversation topic. Prebuilt NLU models define the business-specific language understanding needed for Virtual Agent to understand and process user requests. Each NLU intent in a model maps to a single Virtual Agent conversation topic.

## Summaries of prebuilt topics and topic blocks

For more information on the Virtual Agent prebuilt topics and topic blocks provided by various ServiceNow applications, refer to the documentation for those applications. For example, the CSM, HRSD, and ITSM applications provide information on their prebuilt topics in the following sections:

<table id="table_rmj_1s5_mhb"><thead><tr><th>

Predefined topics and topic blocks

</th><th>

Activation

</th></tr></thead><tbody><tr><td>

Customer Service Virtual Agent conversations

</td><td>

Plugin name: com.sn\_csm.virtualagent

 For more information about activating a plugin, see Activate a plugin.

</td></tr><tr><td>

Field Service Virtual Agent Conversations

</td><td>

Request the Field Service Virtual Agent Conversations and Field Service NLU Model for Virtual Agent Conversations apps from the ServiceNow Store.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Human Resources Virtual Agent conversations

</td><td>

Request the HR Service Delivery Virtual Agent Conversations app from the ServiceNow Store.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

ITSM Virtual Agent Conversations

</td><td>

Request ITSM Virtual Agent and the ITSM NLU Model for Virtual Agent Conversations from the ServiceNow Store.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Legal Virtual Agent Conversations

</td><td>

Request Legal Virtual Agent Conversations from the ServiceNow Store.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Virtual Agent Platform topics and topic blocks

-   [Virtual Agent Designer setup topics](../concept/working-setup-topics.md)
-   [Virtual Agent pre-built topic blocks for NLU](va-platform-topicblocks.md) \(such as Agent Availability, AI Search, and FAQ Conversation Builder\)

</td><td>

Plugin name: com.glide.cs.chatbot

 For more information about activating a plugin, see Activate a plugin.

</td></tr></tbody>
</table>**Note:** The plugins for the CSM, HR Service Delivery, and ITSM predefined conversations also install their prebuilt ServiceNow NLU models and topic blocks. The Glide Virtual Agent plugin installs the prebuilt NLU model for setup topics, as well as platform topic blocks.

After installing the plugins or apps, you can preview \(test\) the topics and topic blocks using Virtual Agent Designer. You can review the intents, utterances, and entities in the prebuilt NLU models using ServiceNow NLU Workbench or within Virtual Agent Designer if your NLU-enabled topics are associated with intents in ServiceNow NLU models.

## Working with prebuilt topics and topic blocks in Virtual Agent Designer

-   Previewing topics and topic blocks – After you install the plugins for prebuilt topics, admins or Virtual Agent admins can access the prebuilt topics and topic blocks in the Virtual Agent Designer home page. Select the topic and in the **Flow** tab, select **Test**. Review the conversation as it runs in the test window to determine the topics and topic blocks that you want to use.
-   Using prebuilt topics and topic blocks – Although prebuilt topics and topic blocks are read only and can't be changed, you can reuse them by [duplicating](../task/duplicate-virtual-agent-topic.md) and modifying them as needed. After you test a duplicated topic and are ready to deploy it to your Virtual Agent clients, [publish](../task/publish-virtual-agent-topic.md) the topic. Similarly, after testing a duplicated topic block, publish it to make it available for use in conversation \(calling\) topics.

For details on creating, testing \(previewing\), duplicating, and publishing a topic, see [Getting started with Virtual Agent Designer](conversation-designer-virtual-agent.md). For details on working with topic blocks, see [Maximizing code reuse with topic blocks](../concept/topic-blocks-overview.md).

## Working with prebuilt ServiceNow NLU models in ServiceNow NLU Workbench

-   Reviewing a prebuilt NLU model – After you install the plugins for predefined topics, you can view the prebuilt models in NLU Workbench. The prebuilt NLU models for ServiceNow applications define the intents, entities, and utterances used for the predefined topics. These models are also trained and published. You can also review the utterances for a prebuilt model in Virtual Agent Designer. However to copy a prebuilt model, you use NLU Workbench.
-   Duplicating prebuilt NLU models – Although prebuilt NLU models are read only and can't be edited, you can Duplicate an NLU model prebuilt NLU models to create your own NLU models and Import an NLU intent from prebuilt models or other NLU models that you create in NLU Workbench.

For details on creating, training, and publishing ServiceNow NLU models, see Natural Language Understanding.

