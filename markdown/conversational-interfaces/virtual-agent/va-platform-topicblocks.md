---
title: Virtual Agent pre-built topic blocks for NLU
description: Virtual Agent provides pre-built topic blocks that topic authors or admins can use to perform specific platform-related functions or tasks in bot conversations. For example, certain topic blocks enable you to check agent availability or generate AI Search results.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
keywords: [Virtual Agent, pre-built, topic, blocks, AI Search, Agent Availability]
breadcrumb: [Maximizing code reuse with topic blocks, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent pre-built topic blocks for NLU

Virtual Agent provides pre-built topic blocks that topic authors or admins can use to perform specific platform-related functions or tasks in bot conversations. For example, certain topic blocks enable you to check agent availability or generate AI Search results.

## Overview of pre-built topic blocks

Certain pre-built topic blocks are included automatically with the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin and Virtual Agent Lite. If you're using Virtual Agent Lite, you have read access to the topic blocks but you can't create topic blocks or add them to calling topics.

You can duplicate pre-built topic blocks and modify the duplicates by using Virtual Agent Designer. For information about working with topic blocks and how to add them to calling topics, see [Maximizing code reuse with topic blocks](../concept/topic-blocks-overview.md) and [Add a reusable topic block to a calling topic or topic block](../task/add-topic-blocks-to-topic.md).

The following sections describe the input and output parameters for calling different types of platform topic blocks. The topic block input parameters are passed from the calling topic, and the output parameters are returned from the topic block to the calling topic.

**Note:** Upgrades to the default topic blocks are not applied to the duplicated topic blocks.

## Agent Availability topic block

Use this topic block to get relevant live agent information for use in agent handoff conversations. This information includes agent availability, wait time \(how long before an agent is available\), and queue information. You can use the information returned, such as a long wait time for an agent, to initiate a case or customer callback.

This topic block requires the Agent Chat \(com.glide.interaction.awa\) plugin, which includes Advanced Work Assignment.

The following table lists the output parameters for this topic block.

|Parameter|Description|
|---------|-----------|
|agentAvailable|Agent availability. The value is true if an agent is available for this queue. Otherwise, the value is false.|
|supportQueue|sys\_id of the queue that is associated with the conversation. The value is null if an agent is not available or if there is no associated queue.|
|waitingTime|Average numeric wait time for the queue. The value is null if an agent is not available.|

## Deflection topic block

Use the deflection topic block in Virtual Agent conversation topics to track the issues that Virtual Agent helped to resolve or actually resolved for a user.

For example, the pre-built Auto Resolution Virtual Agent topic uses a deflection topic block to track deflections. For more information, see [Using the deflection topic block to track deflections in Virtual Agent](../concept/deflections-virtual-agent.md).

The following table lists the input parameters for this topic block.

<table id="table_pzw_vlb_lpb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deflection Configuration

</td><td>

Group of deflection patterns.

</td></tr><tr><td>

Deflection Pattern

</td><td>

Deflection pattern in the deflection configuration that you have chosen.

</td></tr><tr><td>

Activity Table

</td><td>

Table where the deflection activity occurs. This table is associated with the primary activity table. For more information, see [Create deflection configurations and patterns](../task/set-up-deflection-settings-va.md).

</td></tr><tr><td>

Activity Ids

</td><td>

List of comma-separated activity system IDs. For example, incident ID or task ID. You can also add output from the AI Search or Contextual Search topic block to create a link between a deflection occurrence and the content that contributed to the same deflection.

</td></tr></tbody>
</table>## FAQ Conversation Builder topic block

Use this topic block to build bot conversations that use your existing FAQ content. With this topic block, you can enable topic authors to build simple conversations by using existing [knowledge articles](https://www.servicenow.com/docs/access?context=knowledge-article-templates&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) that are published in the FAQ template or by using Q&amp;A data that was imported from sources such as [spreadsheets](https://www.servicenow.com/docs/access?context=t_TranslateTheInterface&version=zurich&pubname=zurich-platform-administration&section=t_ImportATranslationFromExcel&ft:locale=en-US).

The FAQ Conversation Builder topic block uses [contextual search](https://www.servicenow.com/docs/access?context=configuring-contextual-search&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to find an appropriate match in the FAQ content. FAQ content is access-controlled based on requester role, access rights, and context.

Activate the [Knowledge Management Advanced](https://www.servicenow.com/docs/access?context=activate-knowledge-advanced-plugin&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) plugin to use the FAQ Knowledge template.

**Note:** The default length of an FAQ snippet that is returned in the conversation is 400 characters. The snippet length includes the HTML tags and links that are used in the snippet. To change the snippet length, change the value in the **com.glide.cs.faq.display\_size** system property. In addition to applying the specified length, the system applies word-wrap logic to prevent words and links in the snippet from being truncated arbitrarily.

The following tables list the input and output parameters for this topic block.

|Parameter|Description|
|---------|-----------|
|query|Search term or phrase that is passed to the topic block. Select **Input Variables** or **Script Variables**.|
|portal|Context for the search. Select **Input Variables** or **Script Variables**.|
|kb\_knowledge|Knowledge base for the search. Select **Input Variables** or **Script Variables**.|

|Parameter|Description|
|---------|-----------|
|Results\_Returned|Boolean value that indicates whether any results were returned from the query.|
|Results\_Helpful|Boolean value that indicates whether the user found the results helpful.|

## Form Content Popup topic block

Use this topic block to open a form in a popup window from the chat widget. Once the user submits the required information, the record appears as a card in the Virtual Agent chat window. If a new record is created, the sys ID for that record is sent to the server so that the Virtual Agent topic has that information. For information about creating a pop-up window from a link, see [Create a smart link preference](../../conversational-interfaces/task/create-smart-link-preference.md).

|Parameter|Description|
|---------|-----------|
|sysId|Sys ID of the record you want to display from the table specified in the **table** parameter. If you don't want a specific record, enter `-1`to create a new record.|
|table|Name of the table you want to query or create a record in.|
|view|Name of a view that you created for the table. If not specified, the default view is used.|

## Geolocation topic block

Use this topic block to retrieve information about the location of users, if the users agree to that. Before the topic block is called in a conversation, the users are asked if they want their location to be known. For example, the users see a prompt similar to the following:

![Dialog box with block and allow buttons, and message from anonymized website requesting to know user's location.](../images/allow-or-block-location-info.png "User permission prompt")

Users can choose to block the request or allow their location to be known. If the users click **Allow**, they are later asked if they would like to share their location.

The following tables list the input and output parameters for this topic block.

<table id="table_mtq_dsk_x4b"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

permissionPrompt \(String\)

</td><td>

Text asking permission to use the user's location. This text is shown to the user.

</td></tr><tr><td>

isGeoPermissionGrantedForNextUse

</td><td>

Boolean value that determines if users have granted permission to retrieve their location coordinates if this request is asked more than once during the conversation. The variable can be set as follows:-   **True**: Don't display permission prompt again because the user has granted permission on this device.
-   **False**: Display the permission prompt because the user has either denied permission or has allowed the coordinates to be retrieved one time only.

</td></tr></tbody>
</table><table id="table_ycq_ksk_x4b"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Latitude

</td><td>

Latitude coordinates.

</td></tr><tr><td>

Longitude

</td><td>

Longitude coordinates.

</td></tr><tr><td>

errormessage

</td><td>

Message that is associated with the error if there are any errors.

</td></tr><tr><td>

errortype

</td><td>

Variable that is returned from the topic block. Types of errors include:-   PERMISSION\_DENIED
-   POSITION\_UNAVAILABLE
-   TIMED\_OUT
-   UNKNOWN\_ERROR

</td></tr><tr><td>

status

</td><td>

Variable that is returned from the topic block. The status can be:-   OK: Location coordinates were retrieved successfully.
-   ERROR: Retrieval was unsuccessful.

</td></tr></tbody>
</table>## Pause topic block

Use this topic block to create a pause to control the pacing of a conversation. To end users, this feedback is seamless and is displayed as a typing indicator.

For example, if the chat generated a list of knowledge base links, you may want to add a delay before continuing the conversation to give your end user time to read the information.

The Pause topic block appears on the Utilities section of the palette for easier access.

The following table lists the input parameter for this topic block.

<table id="table_f5k_c5h_dpb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Seconds

</td><td>

Number of seconds to wait before continuing the chat. The maximum value allowed is 60 seconds.If the value entered is 30 seconds \(the default value\) or less, the block should unpause in near real time. If the value entered is greater than 30 seconds, expect the unpause to occur with a maximum latency of +30 seconds. For example, if you set the value to 31 seconds, it could take up to 61 seconds to unpause \(at most\).

</td></tr></tbody>
</table>## Run AI Search topic block

**Note:** If you're upgrading from Rome or a prior release, you must replace the legacy AI Search topic block with the Run AI Search topic block in order for it to work.

Use this topic block to generate AI Search results in a conversation. This block doesn't require specific input parameters from a calling topic because it is controlled by the AI Search application in Virtual Agent. The default Virtual Agent Search Application and EVAM configuration set in the [chat experience](../concept/va-conversation-settings.md) control how AI Search results are displayed in conversations.

For information about how Virtual Agent uses AI Search, see [Improving the user experience with AI Search](../concept/va-ai-search.md). To learn more about Virtual Agent chat experiences and how to configure them, see [Customizing a Virtual Agent chat experience](../concept/va-conversation-settings.md).

You can control certain aspects of the Run AI Search topic block:

-   Optionally customize the AI Search experience - You can customize the search experience by creating a custom Search Application Configuration to be used by the topic block, rather than the default Virtual Agent Search Application Configuration. The Search Application Configuration defines the search results returned in the conversation. For details on using a custom Search Application Configuration in the topic block, see [Create a custom AI Search experience for Virtual Agent conversations](../task/create-va-aisearch-application.md).

    To use the default Virtual Agent configuration for AI Search, leave the **Search Application Configuration** field empty in the Topic Block Properties sheet when you're adding the Run AI Search topic block to a topic.

-   Specify an AI Search flow action timeout value - The AI Search flow action in the topic block automatically times out at 10 seconds. You can change the length of time before this flow action times out by [adding the system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) **com.glide.cs.fdih.atlassearch.timeout** and setting these fields to change the timeout value:

<table id="table_xdm_ryb_dxb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the system property name: `com.glide.cs.fdih.atlassearch.timeout`

</td></tr><tr><td>

Description

</td><td>

Enter an explanation for this property: `AI Search action timeout (in seconds)`

</td></tr><tr><td>

Type

</td><td>

Select `integer`.

</td></tr><tr><td>

Value

</td><td>

Enter the number of seconds before the AI Search action times out. The default value is 10 seconds.

</td></tr></tbody>
</table>
The following tables list the input and output parameters for this topic block. For the output parameters, you have the option to deactivate any of the variables returned by the topic block.

|Parameter|Description|
|---------|-----------|
|search\_term|Phrase entered by a user during the conversation.|

|Parameter|Description|
|---------|-----------|
|genius\_results|Variable that identifies the Genius Results returned.|
|search\_results|Variable that identifies the regular search results \(multi-list output\) returned.|
|search\_metadata|Variable that identifies the search result metadata used for click metrics in Conversational Analytics, such as the search term used, query language, and more.|

## Runtime Language Detection topic block

Use this topic block to detect the user’s language during a conversation and switch to that language mid-conversation if the language is supported in the ServiceNow AI Platform.

For example, in conversations where guest users are interacting with the bot in a language different from the current conversation language, you can use this topic block to change the language accordingly. This topic block enables your bot to:

-   Detect the language in conversations across all supported Virtual Agent channels.
-   Determine if the language is supported in the ServiceNow AI Platform, and if so, ask the user whether to switch to the detected language.
-   Switch to the detected language during the conversation if the user agrees to the switch.

Activate the Virtual Agent Language Detection and Translation plugin \[com.glide.cs.runtime\_language\_detection\_translation\] to use this topic block.

The following table lists the input parameters for this topic block.

<table id="table_gbz_hpw_dsb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

utterance \(String\)

</td><td>

Text entered by the user.

</td></tr><tr><td>

Change language \(Boolean\)

</td><td>

Option that displays a message to the user that does the following:-   Indicates the bot has detected that the user is typing in a different language.
-   Asks whether to continue the conversation in the supported language. If the user responds yes, the conversation changes to the supported language.

</td></tr></tbody>
</table>