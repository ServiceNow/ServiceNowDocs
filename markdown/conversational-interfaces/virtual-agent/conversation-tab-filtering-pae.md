---
title: Use filters in the Conversation tab
description: You can filter out conversation for a deeper understanding.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Conversation tab, filters, field options, filter editor]
breadcrumb: [Conversations tab, Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Use filters in the Conversation tab

You can filter out conversation for a deeper understanding.

## Filtering using the Filter Editor

To filter the conversations, select filter icon and select **Advanced view** button to use the filter editor. You can either select an existing filter from the list or create a new filter condition.

![Filter editor filter conditions.](../images/filter-editor-pae.png "Building filters in the filter editor")

The filter editor consists of the following:

-   Field: A list based on relevant tables. For more information about the field options, see [Field options in the Filter Editor](conversation-tab-filtering-pae.md#section_zpm_12c_xpb).
-   Operator: A list of operators that is contextually generated based on the selected field.
-   Value: A text entry field or a list that is contextually generated based on the selected field.

To add a dependent condition in the filter editor, either select **or** or **and**. To filter the conversations list using the condition, select **Update**.

To remove a condition, select the delete icon ![Delete icon.](../images/delete-icon.png) next to the condition.

To save a condition that you created in the condition builder, select **Save filter**. In the Save Filter pop-up window, specify a name for the filter. You can also set permissions for the filter in the Save Filter window. Users having the Chat Analytics Viewer \(chat\_analytics\_viewer\) role can select and modify saved filters.

## Field options in the Filter Editor

|Option|Description|
|------|-----------|
|Channel|Conversations that used the specified channel.|
|Conversation Time|Conversations within the specified date and time.|
|Duration|Conversations within the specified time duration. You can edit the definition of duration to be a session duration, rather than an active messaging duration. For more information, see [Create custom override definitions](../task/set-up-custom-definitions-pae.md).|
|End State|Conversations with the specified state that is based on how conversations ended. The values for the end states are stored in the Interactions \[interactions\] table. For more information, see [Virtual Agent interaction records](va-interactions.md).|
|Events|Specific events that are triggered in a conversation.|
|Feedback Result|Conversations for the specified feedback type.|
|Language|Conversations for the specified language based on the user's language setting.|
|Message Count|Conversations for the specified message count in the chat.|
|Provider Name|Conversations for the specified provider.|
|VA Success|Conversations resolved by the Virtual Agent.|
|Setup Topic Types|Conversations that used the specified setup topic type.|
|Topic Blocks|Conversations that used the specified topic block.|
|Topic Categories|Conversations that have topics which belong to a specified topic category.|
|Topic Count|Conversations that used the specified topic count. Each conversation can use multiple topics and this option filters conversations based on the count of topics used in it.|
|Topics|Conversations that used the specified topics in the chat.|
|Type|Conversations that are of the specified type such as live agent only or Virtual Agent only.|

**Parent Topic:**[Conversations tab](conversation-tab-pae.md)

