---
title: Activate Virtual Agent
description: You can activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) if you have the admin role. This plugin automatically activates other necessary plugins if they are not already active.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Activate Virtual Agent

You can activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) if you have the admin role. This plugin automatically activates other necessary plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

You must have a subscription for Virtual Agent before you can activate the Glide Virtual Agent plugin.

<table id="table_hyz_kkt_w2b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conversational Analytics\[com.sn.conversational.analytics\]

</td><td>

Enables the ServiceNow Conversational Analytics app.**Note:** Subsequent updates for the Conversational Analytics app must be installed from the ServiceNow Store.

</td></tr><tr><td>

Integration - Multiple Provider Single Sign-On Installer\[com.snc.integration.sso.multi.installer\]

</td><td>

Enables authentication for multiple identity providers \(IDPs\) using SAML or OpenID connect\(OIDC\).

</td></tr><tr><td>

Localization Framework Installer\[com.glide.localization\_framework.installer\]

</td><td>

Provides the framework for localization of Virtual Agent conversations.

</td></tr><tr><td>

NLU Model for Virtual Agent Setup Topics\[com.glide.cs.nlu.topics\]

</td><td>

Installs the NLU model for Virtual Agent Setup topics.

</td></tr><tr><td>

Proxy Agent to the ServiceNow Natural Language Understanding Server\[com.glide.nlu.intent.discovery\]

</td><td>

Activates the connection to the ServiceNow NLU server for NLU intent discovery. Used by Virtual Agent and other clients. Activates:-   NLU Workbench - Core \[com.glide.nlu\]
-   Predictive Intelligence \[com.glide.platform\_ml\]
-   Proxy agent for connecting to NLU providers \[com.glide.nlu.proxy\] - Proxy agent for connecting to NLU providers

</td></tr><tr><td>

Proxy Agent to the IBM Watson Natural Language Understanding server\[com.glide.nlu.ibmwatson.intent.discovery\]

</td><td>

Activates the IBM Watson Assistant Intent and Entity integration, which enables Virtual Agent to use intents, entities, and utterances defined in IBM Watson Assistant.

</td></tr><tr><td>

Proxy Agent to the Microsoft LUIS Natural Language Understanding server\[com.glide.nlu.msluis.intent.discovery\]

</td><td>

Activates the Microsoft LUIS integration, which enables Virtual Agent to use intents, entities, and utterances defined in the Microsoft Language Understanding Intelligent Service \(LUIS\).

</td></tr><tr><td>

Proxy Agent to the Google Dialogflow ES Natural Language Understanding server\[com.glide.nlu.googledialogflow.es.intent.discovery\]

</td><td>

Activates the Google Dialogflow ES integration, which enables Virtual Agent to use intents, entities, and utterances defined in Google Dialogflow ES.

</td></tr><tr><td>

Topic Recommendations \[com.snc.va\_topic\_recommender\]

</td><td>

Enables the ServiceNow Topic Recommendations app.**Note:** Subsequent updates for the Topic Recommendations app must be installed from the ServiceNow Store.

</td></tr><tr><td>

Virtual Agent integration with actionable notificationscom.glide.cs.actionable.notification

</td><td>

Enables ServiceNow actionable notifications on Virtual Agent channels.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel. For more information, see [Request a plugin](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`


## What to do next

Activate [additional Virtual Agent plugins](../reference/additional-va-plugins.md) for related features, such as the plugins for predefined Virtual Agent topics.

-   **[Installed with Virtual Agent](../reference/installed-wth-virtual-agent.md)**  
Various types of components are installed with activation of the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin, including tables and user roles.
-   **[Additional plugins for Virtual Agent](../reference/additional-va-plugins.md)**  
After activating Virtual Agent, you can activate additional plugins to enable other features for conversation design.
-   **[Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models](../reference/prebuilt-topics-ITSM.md)**  
Prebuilt Virtual Agent conversations \(topics\), reusable topic blocks, and ServiceNow NLU models are available for the Virtual Agent platform and various business applications, such as Customer Service Management, HR Service Delivery, IT Service Management, and more.

**Parent Topic:**[Configuring Virtual Agent](../concept/configure-virtual-agent.md)

