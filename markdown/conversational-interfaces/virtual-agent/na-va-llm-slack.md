---
title: Now Assist in Virtual Agent with Slack
description: The Now Assist provides you with the large language model \(LLM\)-based conversational experience during your conversations with a Now Virtual Agent bot or a Self-configured bot that is integrated with Slack.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Conversational Integration with Slack, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Now Assist in Virtual Agent with Slack

The Now Assist provides you with the large language model \(LLM\)-based conversational experience during your conversations with a Now Virtual Agent bot or a Self-configured bot that is integrated with Slack.

To enable a bot with LLM-based capabilities and experience the LLM-based conversations with Now Assist, you must first integrate your Now Virtual Agent bot or a Self-configured bot with Slack.

## Integrating Slack with Virtual Agent

You can integrate Virtual Agent with Slack either with the Now Virtual Agent bot or a Self-configured bot.

To integrate Slack with the Now Virtual Agent, see [Integrating ServiceNow Virtual Agent with Slack](va-integ-slack.md).

To integrate Slack with a Self-configured bot, see [Integrating a Self-configured bot with Slack workspace](va-integ-single-slack.md).

## Conversational experience with Now Assist in Slack

The Now Assist provides a new AI Search experience in channels with the following features:

-   **Legal Disclaimer**

    The first message in a conversation with Now Assist displays a legal disclaimer indicating that it is an AI-generated message followed by the Now Assist greeting message and LLM-enabled topics.

    ![LLM-based conversation with Now Assist displaying the legal disclaimer and greeting.](../images/legal-disclaimer-msg-slack.png "Legal Disclaimer")

    The Legal disclaimer message is managed by the **support-system-action** provider property defined in the \[sys\_cs\_custom\_adapter\_property\] table. By default, the value of the provider property is set to **true**.

-   **Pagination and Search**

    You can navigate through multiple pages of choices and search for specific items or users, using the Search bar.

    When you select an LLM-enabled topic, the Search bar is displayed along with the available choices related to the selected topic and the **More options** button. You can either search for an item or user using the Search bar or pick an item or user from the choices available. If you want to look for more available options, you can navigate to the next page using the **More Options** button. If you would like to go back to the previously listed choices, you can use the **Previous Options** button.

    ![LLM based conversation with Now Assist displaying the Search and Pagination features.](../images/search-and-pagination-slck.png "Pagination and Search")

    If you have searched for a user or an item, the choices related to your search term are displayed. You can either select from the choices available or reset the search and pagination.

    **Tip:** You can reset the pagination and search by selecting Enter in the Search bar.

    The pagination and search capabilities are managed by the following provider properties:

    -   **picker\_pagination\_experience\_supported**: Enables the pagination experience in your LLM conversations with Now Assist. The default value of this property is **true**.
    -   **picker\_pagination\_limit**: Sets the page limit value for an adapter for displaying the choices. The maximum page limit value that can be set for an adapter is **100**.

        For example, if a topic has fewer than 100 choices available and the limit is set to 100, then the **More Options** button is not displayed. If a topic has more than 100 choices available when the limit is set to 100, then the **More Options** button is displayed.

-   **Generative AI QnA card**

    Use this feature to ask questions and get answers from Now Assist through LLM in a card format. The response is displayed with a sparkle image, the legal disclaimer, and the citation about the question asked.

    ![Now Assist displaying the question and answer card with the sparkle image, legal disclaimer, and the description and citation for the question asked.](../images/slack-QnA-card-llm.png "Generative AI QnA card")


For more information about enabling LLM for your bots that are integrated with Slack, see [Enable Now Assist in Virtual Agent for Slack](../task/enable-na-llm-slack.md).

