---
title: Now Assist in Virtual Agent conversations with Microsoft Copilot
description: Use Now Assist plugins in Microsoft Copilot to connect with the Copilot by providing your bot or plugin name during your generative AI conversations.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 4
breadcrumb: [Integrating Now Assist in Virtual Agent with Microsoft Copilot, Use Now Assist in VA conversations with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Now Assist in Virtual Agent conversations with Microsoft Copilot

Use Now Assist plugins in Microsoft Copilot to connect with the Copilot by providing your bot or plugin name during your generative AI conversations.

## Copilot Conversations

**Note:** Custom Engine Agent \(CEA\) is replacing Declarative Agent \(DA\), the prior Microsoft Copilot integration. The CEA enables Virtual Agent to be discoverable by Microsoft Copilot, with full functional access to Now Assist in Virtual Agent and multi-turn conversations.

You must have version 10.1.1 or higher of the Microsoft Teams plugin to have CEA support. In version 10.2 of the Microsoft Teams plugin, streaming is inactive by default and CEA is active by default.

Demonstration of Now Assist and Microsoft Copilot capabilities.

The Copilot integration doesn’t follow a conversational flow like the Virtual Agent. It uses a non-conversational flow and provides synchronous responses with Now Assist that are primarily built on AI Search. Therefore, any search term that you input is passed to AI Search and the results are returned from AI Search. You're then able to render the response and share it as a card in Message Extension.

Sample prompts that you can use within Copilot:

-   `What is my laptop replacement policy?`
-   `Can you help me order a laptop?`

**Note:** Sample prompts are located in the manifest file, and are displayed in both Microsoft Copilot and Microsoft Teams. You can't customize the prompts or the **View prompts** control displayed in Answers Chat if you're using the pre-published Now Virtual Agent app. To customize prompts, use the self-configured bot. For more information, see [Setting up the Self-configured bot for using Microsoft Copilot](setup-self-bot-copilot.md).

To initiate a chat with Microsoft Copilot, you can @-mention the bot name and based on the input utterance, Copilot verifies that your request in the chat reaches the respective plugin's instance and a response is received.

![User using the @-mention feature in Copilot to invoke the bot.](../images/copilot-at-mention-bot-name.png)

You can also interact with the bot directly by selecting it from the Agents section on the right panel within Copilot instance. Interacting with the bot this way provides you with the same results or responses as you would receive them while you invoked it.

![Select your bot to interact with it directly within Copilot.](../images/select-bot-within-copilot.png)

You can use Now Assist to search for Knowledge Base articles, catalog items, and so on, and it provides results based on your input for the search. For example, if you searched for iPhone, you're presented with the list of generative AI Search results. You can pick an item from the list and share it with the user of your choice. The user who receives the catalog item shared by you can view it by selecting **View item**.

**Note:** You can configure the viewing experience of an item to either open it in a browser or within the Microsoft Teams tab if you're using Copilot only with your Self-configured bot.

![Catalog item shared with a user from Virtual Agent through Microsoft Copilot with an option to view.](../images/card-share-ms-copilot.png "View item")

## Now Assist capabilities in Copilot

With the Microsoft Copilot integration, you can initiate generative AI chat with Copilot. The following capabilities are available:

-   **Retrieve a Knowledge Base article**

    You can ask the Microsoft Copilot your questions and Copilot responds with detailed information about the questions asked along with a relevant Knowledge Base article for more information.

    ![Microsoft Copilot, providing the Knowledge Base article in response to the questions asked.](../images/msteams-copilot-kb.png "Retrieving a Knowledge Base article")

    **Note:** Any input request to Copilot that takes more than 15 seconds to respond will time out.

-   **Request a conversational catalog item**

    Use Microsoft Copilot to request a catalog item.

    ![Microsoft Copilot helping out with the Catalog item search.](../images/msteams-copilot-catalog-request.png "Requesting a catalog item")

    With Copilot, there’s no conversational flow, but when a conversational catalog is requested, Copilot hands off the chat to the Virtual Agent bot \(the Now Assist in Virtual Agent plugin that you used to connect with Copilot\) for continuing the conversation. When Copilot hands off the request to Virtual Agent, it sends a `Continuing the conversation from Copilot` message and invokes the conversational catalog that you requested from Copilot.

    ![Virtual Agent completes the request submission by continuing with the Copilot conversation.](../images/msteams-copliot-support-catlog-req.png "Continue conversation from Copilot")

-   **Transfer to a Live Agent chat**

    You can ask Copilot to connect you to a Now Assist Live Agent.

    You’re directed to the Now Assist Live Agent for live agent support.

    ![Microsoft Copilot responding to your request to connect to a live agent.](../images/copilot-live-agent-support.png)


## Declarative Agent experience in Copilot

You can add your Self-configured bot to Copilot and use them as declarative agents to meet your unique business needs and establish consistent and personalized experiences.

**Note:**

-   A Copilot license is no longer required in order to use the declarative agent.
-   Only bots for which the manifest package file is uploaded to Microsoft Teams can be enabled for use as declarative agents.

To add a bot to Copilot, login to your Microsoft Teams tenant and navigate to **Apps** &gt; **Features** &gt; **Agents** and select **Add** against the bot that you would like to add. Once the bot is added, it’s available for quick access from the Agents section within Copilot.

![Adding a bot to Copilot as a declarative Agent to use it for unique business needs.](../images/copilot-declarative-agent.png "Declarative Agent")

**Parent Topic:**[Integrating Now Assist in Virtual Agent with Microsoft Copilot](ms-copilot-na-va.md)

