---
title: Installed with Virtual Agent
description: Various types of components are installed with activation of the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin, including tables and user roles.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Activate Virtual Agent, Activate and get started, Virtual Agent, Conversational Interfaces]
---

# Installed with Virtual Agent

Various types of components are installed with activation of the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Plugins installed

The following table lists the plugins that are installed when you activate Virtual Agent.

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
</table>## Roles installed

With the Virtual Agent Administrator \[virtual\_agent\_admin\] role, users can create and manage topics \(bot conversations\), using Virtual Agent Designer.

-   If using Natural Language Understanding, the NLU admin role is included.
-   If the Virtual Agent admin is granted access to AI Search-related tables, the search application administrator role \[search\_application\_admin\] is included.
-   If the Virtual Agent admin is granted access to Entity View Action Mapper tables, the EVAM admin role \[evam\_admin\] is included.
-   For multilanguage support, the localization\_requestor role is included by default. For more information, see [Localization Framework roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/roles-localization-framework.md) .
-   For more information on the roles contained in virtual\_agent\_admin, see [Virtual Agent roles](VA-roles.md#).

## Users installed

The Glide Conversation Server plugin \(com.glide.cs\) automatically installs a virtual agent user \(virtual.agent\) in the User \[sys\_user\] table. Ongoing [Virtual Agent interactions](../concept/va-interactions.md) are assigned to this virtual agent user. If you're using Advanced Work Assignment \(AWA\), interactions assigned to the virtual agent user are not routed by AWA. The virtual agent user is also used in the default web chat branding settings to associate a virtual agent user profile with a bot avatar.

## Tables installed

<table id="table_nrw_wtr_k2b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Adapter Configurations\[sys\_cs\_adapter\_configuration\]

</td><td>

Stores records for default keywords, labels, and message values for third-party messaging integrations.

</td></tr><tr><td>

Adapter Configuration Page\[sys\_cs\_adapter\_configuration\_page\]

</td><td>

Stores the configuration for third-party messaging integrations. This table is the root table for:-   Configurations - Slack Integration \[sys\_cs\_adapter\_configuration\_page\_slack\]
-   Configurations - Teams Integration \[sys\_cs\_adapter\_configuration\_page\_teams\]
-   Configurations - Workplace Integration \[sys\_cs\_adapter\_configuration\_page\_workplace\]
-   Configurations - Facebook Messenger Integration \[sys\_cs\_adapter\_configuration\_page\_messenger\]

</td></tr><tr><td>

Adapter Message\[sys\_cs\_adapter\_message\]

</td><td>

Stores adapter messages.

</td></tr><tr><td>

Brandings\[sys\_cs\_branding\_setup\]

</td><td>

Stores different branding configurations for the web-based chat client used in an instance.

</td></tr><tr><td>

Client Adapter\[sys\_cs\_client\_adapter\]

</td><td>

Stores each adapter state.

</td></tr><tr><td>

Consumer Channel\[sys\_cs\_consumer\_channel\]

</td><td>

Stores consumer channel information.

</td></tr><tr><td>

Consumer Device Context\[sys\_cs\_consumer\_device\_context\]

</td><td>

Stores consumer device context information.

</td></tr><tr><td>

Context Topics\[sys\_cs\_context\_topic\]

</td><td>

Stores different configurations for determining the appropriate conversation topic displayed to end users based on their pre-chat survey answers.

</td></tr><tr><td>

Conversation\[sys\_cs\_conversation\]

</td><td>

Stores a record for each conversation on the instance. Each record includes the Conversation Task \[sys\_cs\_conversation\_task\] and Conversation Message \[sys\_cs\_message\] related lists, which show all the topics run and associated messages presented in the conversation.

</td></tr><tr><td>

Conversation Consumer\[sys\_cs\_consumer\]

</td><td>

Stores a record representing the user in a conversation, and references the associated sys\_user record for that user.

</td></tr><tr><td>

Conversation Server Field Script Validators\[sys\_cs\_field\_script\_validator\]

</td><td>

Stores text format validation rules and default error messages. Read-only.

</td></tr><tr><td>

Custom Controls\[sys\_cs\_custom\_control\]

</td><td>

Identifies custom controls.

</td></tr><tr><td>

Custom Control Definitions \[sys\_cs\_custom\_control\_definition\]

</td><td>

Binds a client type \(for example, web or mobile\) to a custom control.

</td></tr><tr><td>

Conversation Media\[sys\_cs\_media\]

</td><td>

Media attached to conversations are stored in sys\_attachment, and associated to this table.

</td></tr><tr><td>

Conversation Message\[sys\_cs\_message\]

</td><td>

Stores a record for each message in a conversation. Shows the messages displayed for each topic in the conversation flow.

</td></tr><tr><td>

Conversation Server Connect Hand-off\[sys\_cs\_connect\_handoff\]

</td><td>

Stores mapping of Virtual Agent conversations and Connect/Workspace conversations.

</td></tr><tr><td>

Conversation Session\[sys\_cs\_session\]

</td><td>

Stores a record for each conversation.

</td></tr><tr><td>

Conversation Task\[sys\_cs\_conversation\_task\]

</td><td>

Stores a record for each conversation task. Each record shows the conversation flow, which can include multiple topics that are run during the conversation.

</td></tr><tr><td>

Conversation Task FDIH Invocations\[sys\_cs\_fdih\_invocation\]

</td><td>

Tracks the state of a call to a Workflow Studio action or subflow in a conversation.

</td></tr><tr><td>

Conversation Vendor\[sys\_cs\_vendor\]

</td><td>

Stores vendor information.

</td></tr><tr><td>

CS Consumer Account\[sys\_cs\_consumer\_account\]

</td><td>

Stores third-party user information.

</td></tr><tr><td>

Custom Greetings and Setup\[sys\_cs\_context\_profile\]

</td><td>

Stores a profile record for context-driven chat experiences. Contains customizations in the following child tables:-   Setup topics \[sys\_cs\_context\_profile\_topic\] - Stores the setup topics used for each setup topic type.
-   Promoted topics \[sys\_cs\_context\_profile\_promotion\] - Stores the topics that are highlighted in the Virtual Agent client.
-   Search Profiles \[sys\_cs\_context\_profile\_search\] - Stores the AI search profile for the associated chat experience.

</td></tr><tr><td>

Custom Controls\[sys\_cs\_custom\_control\]

</td><td>

Stores the custom input and response controls.

</td></tr><tr><td>

Custom Control Definitions\[sys\_cs\_custom\_control\_definition\]

</td><td>

Binds a client type \(for example web chat client\) to a custom control. Stores the channel, domain, and user interface component defined for a custom control.

</td></tr><tr><td>

General Settings\[sys\_cs\_general\_settings\]

</td><td>

Stores the records for the NLU configuration.

</td></tr><tr><td>

Live Agent Setup\[sys\_cs\_live\_agent\_setup\]

</td><td>

Stores the Live Agent setup with queue information.

</td></tr><tr><td>

Live Agent Support Queue Cache\[sys\_cs\_support\_queue\_cache\]

</td><td>

The database cache used for support queue wait times.

</td></tr><tr><td>

Open NLU Drivers\[open\_nlu\_driver\]

</td><td>

Stores the records of the NLU service providers used in the instance. Identifies the base system NLU provider and other services installed, such as IBM Watson NLU.

</td></tr><tr><td>

Open NLU Driver Http Connections\[open\_nlu\_driver\_http\_connection\]

</td><td>

Stores all the HTTP connection references for the NLU service provider.

</td></tr><tr><td>

Open NLU Driver Languages\[open\_nlu\_driver\_language\]

</td><td>

Lists the language codes for the NLU service providers \(ServiceNow NLU and IBM Watson Assistant\). Identifies the driver codes and associated languages.

</td></tr><tr><td>

Open NLU Predict Entity Feedbacks\[open\_nlu\_predict\_entity\_feedback\]

</td><td>

Stores the disposition taken by an application in response to an NLU entity prediction result. For example, in Virtual Agent the goal is to map a predicted NLU entity to an input variable in a Virtual Agent topic.

</td></tr><tr><td>

Open NLU Predict Intent Feedbacks\[open\_nlu\_predict\_intent\_feedback\]

</td><td>

Stores the disposition taken by an application in response to an NLU intent prediction result. For example, in Virtual Agent the goal is to map a predicted NLU intent to a Virtual Agent topic.

</td></tr><tr><td>

Published Topic\[sys\_cb\_design\_topic\]

</td><td>

Stores design topic definitions and references the runtime topic.

</td></tr><tr><td>

Session Binding\[sys\_cs\_session\_binding\]

</td><td>

Stores session binding and AMB channel information.

</td></tr><tr><td>

Configurations - Slack Integration\[sys\_cs\_adapter\_configuration\_page\_slack\]

</td><td>

Extends the sys\_cs\_adapter\_configuration\_page table. Stores the configuration for the Slack messaging application.

</td></tr><tr><td>

Configurations - Facebook Messenger Integration\[sys\_cs\_adapter\_configuration\_page\_messenger\]

</td><td>

Extends the sys\_cs\_adapter\_configuration page table. Stores the configuration for the Facebook Messenger messaging application.

</td></tr><tr><td>

Teams Adapter Configuration Page\[sys\_cs\_adapter\_configuration\_page\_teams\]

</td><td>

Extends the sys\_cs\_adapter\_configuration\_page table. Stores the adapter configuration for the Microsoft Teams messaging application.

</td></tr><tr><td>

Workplace Adapter Configuration Page\[sys\_cs\_adapter\_configuration\_page\_workplace\]

</td><td>

Extends the sys\_cs\_adapter\_configuration\_page table. Stores the adapter configuration for the Workplace messaging application.

</td></tr><tr><td>

Vendor Client Adapter Configuration\[sys\_cs\_vendor\_client\_adapter\_configuration\]

</td><td>

Stores the adapter configuration for third-party messaging applications.

</td></tr><tr><td>

Topic\[sys\_cb\_topic\]

</td><td>

Stores a record for each topic \(design-time definition\).

</td></tr><tr><td>

Topic\[sys\_cs\_topic\]

</td><td>

Stores an instance of a topic from sys\_cb\_topic at run time. Records on this table are cleaned every 12 hours.

</td></tr><tr><td>

Topic Category\[sys\_cb\_topic\_category\]

</td><td>

Stores all the categories that identify the different types of topics, such as setup topics and small talk topics. Also includes custom categories defined by admins.

</td></tr><tr><td>

Topic Library Usages\[sys\_cs\_topic\_library\_usage\]

</td><td>

Stores references to published topic blocks.

</td></tr><tr><td>

Vendor Context Configuration\[sys\_cs\_vendor\_context\_configuration\]

</td><td>

Stores vendor-specific device context information.

</td></tr><tr><td>

Virtual Agent Context\[sys\_cs\_virtual\_agent\_context\]

</td><td>

Stores Virtual Agent context variables.

</td></tr></tbody>
</table>## Properties installed

|Property|Description|
|--------|-----------|
|com.glide.cs.branding.msg\_delay|Minimum delay between bot messages|
|com.glide.cs.branding.type\_presence\_delay|Minimum delay before displaying typing animation|
|com.glide.cs.conversation\_faulted\_reason|Message that displays the following default message when a conversation has faulted: `It seems that you have left the conversation.`|
|com.glide.cs.general.error\_message|Generic error message|
|com.glide.cs.general.live\_agent\_handoff\_error\_message|Error message when no live agent has been set up|
|com.glide.cs.general.live\_agent\_handoff\_message|Message to display when handing over to a live agent|
|com.glide.cs.general.support\_email|General support email|
|com.glide.cs.general.support\_hours|General support hours|
|com.glide.cs.general.support\_phone|General support phone|
|com.glide.cs.global\_configuration|The sys\_id of the default configuration page \(sys\_cs\_configuration\_page\)|
|com.glide.cs.javascript.reserved\_words|Reserved words in JavaScript that should not be used as vaInputs names or vaVars names|
|com.glide.cs.live\_agent\_queue|The chat queue that users transfer to when a conversation transitions from a virtual agent to a live agent. This default queue is used unless the topic specifies a specific queue to use.|
|com.glide.cs.suggest.minimum\_characters|The minimum number of characters the user must enter in a keyword search before partial matching, phonetic matching, and spellcheck begin to function.|
|com.glide.cs.suggest.enable\_partial\_search|Enables partial matching searches on topic searches when set to true.|
|com.glide.cs.suggest.enable\_phonetic\_search|Enables phonetic searching on topic searches when set to true.|
|com.glide.cs.suggest.enable\_spell\_check|Enables alternate search spellings on topic searches when set to true.|

