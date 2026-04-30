---
title: Virtual Agent Designer legacy Topics page
description: The Virtual Agent Designer legacy home page lists cards for available topics in your instance.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Virtual Agent, designer, legacy, topic, cards, page]
breadcrumb: [Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent Designer legacy Topics page

The Virtual Agent Designer legacy home page lists cards for available topics in your instance.

![Virtual Agent Designer Topics page that displays the available topics, topic blocks, and custom controls, as well as options for creating and managing topics.](../images/TopicPage.png "Legacy topic cards page")

Each topic is represented by a card on the topic page. A description of the topic \(from the **Properties** tab\) appears when you hover over the title, and all categories are shown when you hover over the list of tags.

![Hover over the name of a topic card to read its description from the Properties tab.](../images/topic-card-hover-1.png "Topic cards") ![Hover over the category tags of a topic card to see all categories associated with the topic.](../images/topic-card-hover-2.png "Topic cards") ![Topic card with the Promoted topic option highlighted under the More actions icon.](../images/promote-llm-topic.png "Topic cards")

<table id="table_lyh_wwg_rhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Localization Insights

</td><td>

Button that opens the Localization Insights dashboard. It shows reports of topics with their translation statuses. For more information, see [Localization Insights dashboard](https://www.servicenow.com/docs/access?context=localization-insights-dashboard&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

See Topic Recommendations

</td><td>

Button that opens Topic Recommendations \(if installed\). Review recommendations and manage jobs. For more information, see [Using Virtual Agent Topic Recommendations](../concept/va-topic-recommendations.md).

</td></tr><tr><td>

Manage languages

</td><td>

Button that opens the Manage languages page. You can view the localization status of an NLU model and request translations for the model and related topics.This field is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td>

Manage NLU/keyword test cases

</td><td>

Button that opens the Manage test cases page, where you can manage automated testing for Virtual Agent topics. For more information, see [Automated testing for Virtual Agent topics that use NLU topic discovery](../concept/automated-testing-va-topics.md).

</td></tr><tr><td>

Test Active Topics

</td><td>

Button that opens the chat test window, which runs active topics in the Virtual Agent chat widget.

 Use this feature to test and verify that your active topics work as intended.

</td></tr><tr><td>

Search by topic name

</td><td>

Option for finding a topic that matches the name or search string that you enter.

</td></tr><tr><td>

Explore additional topics

</td><td>

Link that opens the All prebuilt topics page, which shows prebuilt topics that are available when you activate their dependent spokes or plugins. For more information, see [Virtual Agent Designer All pre-built topics page](vad-additional-topics-list.md).

</td></tr><tr><td>

Topic Type

</td><td>

Filter for displaying Virtual Agent assets:

 -   **Topics**: Lists only topics \(and not blocks or custom controls\), including prebuilt topics.
-   **Topic Blocks**: Lists prebuilt and custom topic blocks.
-   **Setup Topics**: Lists topics that are basic conversational elements, such as the conversation greeting or closing.
-   **Small Talk Topics**: Lists topics that serve as casual conversations between the bot and end users, where the bot answers questions generally not related to the original task or issue.
-   **Custom Controls**: Lists custom controls that represent custom components used in a conversation.

By default, the Topics page lists all active \(published\) and inactive \(in development\) assets, unless you use filters to list only certain asset types.

</td></tr><tr><td>

Category

</td><td>

Filter that displays a list of topics belonging to a category that you specify. A category is a label that identifies a group of assets, such as setup topics or prebuilt topics for a particular business application.

 You can also define your own custom categories. For details, see [Create or modify custom Virtual Agent categories](../task/create-topic-category.md).

</td></tr><tr><td>

Status

</td><td>

Filter that displays a list of assets by their state:

 -   **Active**: Display only published assets
-   **Inactive**: Display only assets in development

</td></tr><tr><td>

NLU Language

</td><td>

Filter that is displayed only if you're using multi-language NLU models. Lists NLU -enabled topics by the language that you select.

 Enable the languages for the NLU service in [NLU settings](../task/configure-nlu-settings.md).

 This field is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td>

Channel

</td><td>

If other channels are configured for the instance, this filter lists topics by the channel \(chat client\) that you select. The default channels for Virtual Agent are the web chat client and the messaging integrations for Slack, Microsoft Teams, Workplace, and Facebook Messenger. Your instance may have other channels, such as SMS that were created using custom chat integrations.

</td></tr><tr><td>

Sort by

</td><td>

Filter that displays topics by the sort filter that you select:

 -   Name: Specified topic or asset.
-   Updated time: Recently updated topics.

</td></tr><tr><td>

Created by me

</td><td>

Option that, when enabled, displays only the topics that you created.

</td></tr><tr><td>

+ Create

</td><td>

Option that opens the Properties page to create a topic or topic element and define the topic properties.

</td></tr><tr><td>

Topic actions icon ![Topic actions icon.](../images/kebab-menu.png)

</td><td>

Icon that opens a drop-down menu with the following options:

 -   **Promote topic**: Adds a `Promoted` flag to the topic. Primary assistants only show promoted topics associated with them and not their secondary assistants' promoted topics. The option is deactivated and a tooltip appears when you try to promote any of the following:
    -   Setup topics
    -   Topic blocks
    -   Small talk topics
    -   Unpublished topics
    -   Any NLU/Keyword topics

**Note:** You can promote NLU topics in Conversational Interfaces settings, under **Virtual Agent Custom Greetings and Setup**. For more information, see [Configure a Virtual Agent chat experience](../task/configure-default-chat-experience.md).

-   **Demote topic**: Replaces the **Promote** option in a promoted topic, to remove the `Promoted` flag.
-   **Delete topic**: Opens a confirmation dialog box to delete the topic.

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer interface reference](../concept/vad-reference.md)

