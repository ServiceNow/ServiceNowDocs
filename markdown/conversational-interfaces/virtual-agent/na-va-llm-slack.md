---
title: Using ServiceNow Otto for Virtual Agent conversations with Slack
description: ServiceNow Otto provides a large language model \(LLM\)-based conversational experience in your conversations with a Virtual Agent bot or a self-configured bot that is integrated with Slack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/na-va-llm-slack.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Using ServiceNow Otto for Virtual Agent conversations with Slack

ServiceNow Otto provides a large language model \(LLM\)-based conversational experience in your conversations with a Virtual Agent bot or a self-configured bot that is integrated with Slack.

## Integrating Slack with Virtual Agent

To enable a bot with ServiceNow Otto, you must first integrate your Virtual Agent bot or a self-configured bot with Slack.

-   To integrate Slack with Virtual Agent, see [Integrating ServiceNow Virtual Agent with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-integ-slack.md).

-   To integrate Slack with a self-configured bot, see [Integrating a self-configured bot with Slack workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-integ-single-slack.md).


## Conversational experience with ServiceNow Otto in Slack

ServiceNow Otto provides a new AI Search experience in channels with the following features:

-   **Legal Disclaimer**

    The first message in a conversation with ServiceNow Otto displays a legal disclaimer indicating that it is an AI-generated message followed by the ServiceNow Otto greeting message and LLM-enabled topics.

    \[Omitted image "legal-disclaimer-msg-slack.png"\] Alt text: LLM-based conversation with ServiceNow Otto displaying the legal disclaimer and greeting.

    The Legal disclaimer message is managed by the **support-system-action** provider property defined in the \[sys\_cs\_custom\_adapter\_property\] table. By default, the value of the provider property is set to **true**.

-   **Pagination and Search**

    You can navigate through multiple pages of choices and search for specific items or users, using the Search bar.

    When you select an LLM-enabled topic, the Search bar is displayed along with the available choices related to the selected topic and the **More options** button. You can either search for an item or user using the Search bar or pick an item or user from the choices available. If you want to look for more available options, you can navigate to the next page using the **More Options** button. If you would like to go back to the previously listed choices, you can use the **Previous Options** button.

    \[Omitted image "search-and-pagination-slck.png"\] Alt text: LLM based conversation with ServiceNow Otto displaying the Search and Pagination features.

    If you have searched for a user or an item, the choices related to your search term are displayed. You can either select from the choices available or reset the search and pagination.

    **Tip:** You can reset the pagination and search by selecting Enter in the Search bar.

    The pagination and search capabilities are managed by the following provider properties:

    -   **picker\_pagination\_experience\_supported**: Enables the pagination experience in your LLM conversations with ServiceNow Otto. The default value of this property is **true**.
    -   **picker\_pagination\_limit**: Sets the page limit value for an adapter for displaying the choices. The maximum page limit value that can be set for an adapter is **100**.

        For example, if a topic has fewer than 100 choices available and the limit is set to 100, then the **More Options** button is not displayed. If a topic has more than 100 choices available when the limit is set to 100, then the **More Options** button is displayed.

-   **Generative AI QnA card**

    Use this feature to ask questions and get answers from ServiceNow Otto in a card format. The response is displayed with a sparkle image, the legal disclaimer, and the citation about the question asked.

    \[Omitted image "slack-QnA-card-llm.png"\] Alt text: ServiceNow Otto displaying the question and answer card with the sparkle image, legal disclaimer, and the description and citation for the question asked.


**Note:** When using ServiceNow Otto in Slack, users can provide quick feedback on the AI-generated Virtual Agent responses by selecting the thumbs up \( \[Omitted image "llm-thumbs-up-like.png"\] Alt text:\)or thumbs down \( \[Omitted image "llm-thumbs-down-dislike.png"\] Alt text:\) icons.

For more information about enabling LLM for your bots that are integrated with Slack, see [Enable ServiceNow Otto for Virtual Agent in Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/enable-na-llm-slack.md).

-   **[Enable ServiceNow Otto for Virtual Agent in Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/enable-na-llm-slack.md)**  
Enable large language model \(LLM\) conversational experiences with ServiceNow Otto in your Slack integration.
-   **[Synthesized response in Slack conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/slack-synthesized-response.md)**  
Synthesized responses in Slack conversations are results that are summarized as a single response, allowing users to see information in a conversational way.

**Parent Topic:**[Conversational Integration with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/mssg-slack.md)

