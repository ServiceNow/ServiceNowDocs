---
title: Legacy - Use filters in the Conversation tab
description: You can filter out conversation for a deeper understanding.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-08"
reading_time_minutes: 5
keywords: [Legacy, filters, Conversation, tab, Virtual Agent, VA Success, fallback, Live Agent, transfer, filter editor]
breadcrumb: [Legacy - Conversations tab, Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Use filters in the Conversation tab

You can filter out conversation for a deeper understanding.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

## Filtering using list options

You use the list options to filter the conversations.

**Note:** The dashboard converts the dates to UTC, which might not match the dates in the conversations list.

|Option|Description|
|------|-----------|
|All|Lists all conversations.|
|VA Success|List all conversations that are considered successful. You can edit the default formula that defines successful conversations by using formula overrides. For more information, see [Legacy - Create custom override definitions](../task/set-up-custom-definitions.md). In the base system, the default formula is set as a percentage of conversations that did not escalate to a live agent, did not have negative feedback, and contained a topic that went through to the last node.|
|Fallback|Lists all conversations where Virtual Agent didn't understand the user and used fallback text to prompt the user for additional information.|
|Live Agent Transfer|Lists all conversations where Virtual Agent transferred the user to a live agent.|

## Filtering using the Filter Editor

To filter the conversations, select **View/edit filter** and use the condition builder in the Filter Editor pop-up window. You can either select a default filter from the list or create a new filter condition. For example, the following image shows a condition in the Filter Editor pop-up window. This condition lists conversations that use the **Pizza Order** topic, and that have the **Pizza Type** topic node \(a static choice control\) in which the user has selected the **Pepperoni** value.

![Filter Editor showing static choice values. Conditions are defined for a Standard Topic containing Pizza Order, Topic Node containing Pizza Type, and Selected Value of Pepperoni.](../images/filter-cond.png "Condition using a static choice value")

Another example condition is shown in the following image. This condition lists conversations that use the **Pizza Order** topic and that have the **Confirm** topic node \(a boolean control\) in which the user has selected the **true** value.

![Filter Editor showing Boolean values. Conditions are defined for a Pizza Order standard topic, with Topic Node containing Confirm, and Selected Value of true.](../images/confirm-va.png "Condition using a boolean value")

The condition builder consists of the following:

-   Field: A list based on relevant tables. For more information about the field options, see [Field options in the Filter Editor](conversation-tab-filtering.md#section_zpm_12c_xpb).
-   Operator: A list of operators that is contextually generated based on the selected field.
-   Value: A text entry field or a list that is contextually generated based on the selected field.

To add a dependent condition in the condition builder, either select **or** or **and**. To filter the conversations list using the condition, select **Run**.

To remove a condition, select the delete icon ![Delete icon](../images/delete-icon.png) next to the condition.

To save a condition that you created in the condition builder, select **Save Filter**. In the Save Filter pop-up window, specify a name for the condition. Users having the Chat Analytics Viewer \(chat\_analytics\_viewer\) role can select and modify your saved filters.

![Saved condition in the Filter Editor.](../images/condition-saved.png "Saved condition")

## Field options in the Filter Editor

|Option|Description|
|------|-----------|
|Channel|Conversations that used the specified channel.|
|Conversation Time|Conversations within the specified date and time.|
|Duration|Conversations within the specified time duration. You can edit the definition of duration to be a session duration, rather than an active messaging duration. For more information, see [Legacy - Create custom override definitions](../task/set-up-custom-definitions.md).|
|End State|Conversations with the specified state that is based on how conversations ended. The values for the end states are stored in the Interactions \[interactions\] table. For more information, see [Virtual Agent interaction records](va-interactions.md).|
|Events|Specific events that are triggered in a conversation.|
|Favorite|Conversations that are marked as favorite. You can also mark a conversation as favorite in the User Details page. For more information, see [Legacy - User Details page](user-page.md).|
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

**Parent Topic:**[Legacy - Conversations tab](conversation-tab.md)

