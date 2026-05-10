---
title: Using Now Assist in Virtual Agent conversations with Microsoft Teams
description: The Now Assist provides you with the large language model \(LLM\)-based conversational experience during your conversations with a Now Virtual Agent bot or a Self-configured bot that is integrated with Microsoft Teams.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Using Now Assist in Virtual Agent conversations with Microsoft Teams

The Now Assist provides you with the large language model \(LLM\)-based conversational experience during your conversations with a Now Virtual Agent bot or a Self-configured bot that is integrated with Microsoft Teams.

To enable a bot with LLM-based capabilities and experience the LLM-based conversations with the Now Assist, you must first integrate your Now Virtual Agent bot or a Self-configured bot with Microsoft Teams.

## Integrating Microsoft Teams with Virtual Agent

You can integrate Virtual Agent with Microsoft Teams either with your Now Virtual Agent bot or the Self-configured bot.

To integrate Microsoft Teams with the Now Virtual Agent, see [Integrate Virtual Agent with Microsoft Teams](../task/va-integ-msteams.md).

To integrate Microsoft Teams with a Self-configured bot, see [Integrating Virtual Agent with Microsoft Teams using the self-configured bot](va-integ-teams-self-configured-bot.md).

## Conversational experience with Now Assist in Microsoft Teams

The Now Assist provides a new AI Search experience in channels with the following features:

-   **Legal Disclaimer**

    The first message in a conversation with Now Assist displays a legal disclaimer indicating that it is an AI-generated message followed by the Now Assist greeting message and LLM-enabled topics.

    ![LLM-based conversation with Now Assist displaying the legal disclaimer and greeting.](../images/msteams-llm-legal-disclaimer.png "Legal Disclaimer")

    ![LLM-based conversation with Now Assist displaying the list of LLM topics.](../images/msteams-llm-topics.png "LLM Topics")

-   **Pagination and Search**

    You can navigate through multiple pages of choices and search for specific items or users, using the Search bar.

    ![LLM based conversation with Now Assist displaying the Search and Pagination features.](../images/msteams-llm-search-pagination.png "Pagination and Search")

    When you select an LLM-enabled topic, the Search bar is displayed along with the available choices related to the selected topic and the **More options** button. You can either search for an item or user using the Search bar or pick an item or user from the available choices. If you want to look for more available options, you can navigate to the next page using the **More Options** button. If you would like to go back to the previously listed choices, you can use the **Previous Options** button.

    If you have searched for a user or an item, the choices related to your search term are displayed. You can either select from the choices available or reset the search and pagination.

    **Tip:** You can reset the Pagination and Search by selecting Enter in the Search bar.

    The Pagination and Search capabilities are managed by the following provider properties:

    -   **picker\_pagination\_experience\_supported**: Enables the pagination experience in your LLM conversations with Now Assist. The default value of this property is **true**.
    -   **picker\_pagination\_limit**: Sets the page limit value for an adapter for displaying the choices. The maximum page limit value that can be set for an adapter is **100**.

        For example, if a topic has fewer than 100 choices available and the limit is set to 100, then the **More Options** button is not displayed. If a topic has more than 100 choices available when the limit is to 100, then the **More Options** button is displayed.

-   **Generative AI QnA card**

    Use this feature to ask questions and get answers from Now Assist through LLM in a card format. The response is displayed with a sparkle image, the legal disclaimer, and the citation about the question asked.

    ![Now Assist displaying the question and answer card with the sparkle image, legal disclaimer, and the description and citation for the question asked.](../images/msteams-llm-QnA-card.png "Generative AI QnA Card")


For more information about enabling LLM for your bots integrated with Microsoft Teams, see .

-   **[Integrating Now Assist in Virtual Agent with Microsoft Copilot](ms-copilot-na-va.md)**  
Integrate your Now Assist Virtual Agent with Microsoft Copilot using Conversational Integration with Microsoft Teams to leverage the generative AI conversational experience.
-   **[Synthesized response in Microsoft Teams conversations](msteams-synthesized-response.md)**  
Conversational Integration with Microsoft Teams is designed to provide new and rich user experience with synthesized responses using Large Language Models \(LLM\) based results summarized in a single response for users to see information in a conversational way, and avoid browsing through carousels.

**Parent Topic:**[Conversational Integration with Microsoft Teams](teams-conv-integration.md)

