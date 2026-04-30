---
title: Working with setup topics
description: Setup topics are part of a standard conversation structure applied to all your conversations, such as the welcome greeting or fallback responses. Setup topics run at the appropriate spot in a conversation based on the context, keywords, or utterances entered by the user, and any conditions that are specified for the setup topic.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Setting up chat experiences for Virtual Agent users, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Working with setup topics

Setup topics are part of a standard conversation structure applied to all your conversations, such as the welcome greeting or fallback responses. Setup topics run at the appropriate spot in a conversation based on the context, keywords, or utterances entered by the user, and any conditions that are specified for the setup topic.

You define setup topics in a Virtual Agent Designer chat experience using the Custom Greetings and Setup option. A chat experience sets the context in which users run Virtual Agent. This context includes:

-   Setup topics applied to bot conversations.
-   A small list of topics, called promoted topics, initially displayed in the chat window.
-   AI Search configuration used to display AI Search results for your users.

For more information on chat experiences, see [Setting up chat experiences for Virtual Agent users](va-conversation-settings.md). For details on configuring a chat experience, see [Configure a Virtual Agent chat experience](../task/configure-default-chat-experience.md).

**Note:** Setup topics in conversations are discoverable \(via topic discovery\) only when they're [configured in a Virtual Agent chat experience](../task/configure-default-chat-experience.md) using the **Custom Greetings and Setup** option. If any setup topics are not included in a chat experience, those setup topics are not listed in the chat window's All Topics menu \(topic picker\) and cannot be discovered by Virtual Agent.

Setup topics run during a conversation as follows.

1.  Conversation beginning: Virtual Agent presents the Greeting topic and the list of available topics \(Virtual Agent capabilities\) that the user can select.

    **Note:** If you want the chat window to immediately take users to a live agent, do not select the Live Agent Support topic as a greeting. Instead, use the system method to [transfer to a live agent](transfer-to-live-agent.md).

2.  Conversation body: These setup topics are presented at different points in the conversation depending on the context:
    -   User requests help: Virtual Agent presents the Explore help topic \(Virtual Agent capabilities\).
    -   User enters a request or keyword that Virtual Agent doesn't understand: Virtual Agent presents the Fallback topic, unless the AI Search fallback topic is enabled.
    -   If the AI Search Fallback topic is enabled and the user enters a request or keyword but Virtual Agent can't find a matching topic or keyword, or finds too many topics to determine the matching topic: Virtual Agent runs AI Search to generate relevant search results for the user. If the AI Search results do not help the user, or if the AI Search Fallback setup topic is not activated, Virtual Agent runs the Fallback topic.
    -   An unrecoverable system error occurs during conversation: Virtual Agent runs the Error Handling topic, and then transfers the user to a live agent.
    -   User requests a transfer to live agent: Virtual Agent runs the Live Agent topic, which transfers the user to a live agent.
    -   After a task or user request is completed: Virtual Agent runs the Anything else topic to ask if the user wants to continue with another request or task.
3.  Conversation ending:
    -   If the user doesn't want further assistance after a task or the request is completed, Virtual Agent presents the Survey topic for feedback on the conversational experience.
    -   After the survey, Virtual Agent confirms that the feedback has been received, and runs the Closing topic to end the conversation.

The default setup topics are read-only and have topic names with a period at the end of the setup topic name, such as **Greeting**. You can create your own custom setup topics by duplicating a setup topic and changing it as needed. You can also change prompts or add other controls to the topic, just as you might when creating other topics.

If you want a closing message to be different from the default Closing topic, create a custom setup topic that contains the revised closing text. You also need to create an intent for that custom setup topic in the NLU model for setup topics, or define topic keywords in the Topic Properties page. You can then select the custom setup topic to be used in a custom chat experience instead of using a default setup topic.

The following table provides examples of the pre-built setup topics in the default chat experience.

<table id="table_h2k_tyr_5nb"><thead><tr><th>

Setup topic type

</th><th>

Setup topic name and description

</th></tr></thead><tbody><tr><td>

Anything else

</td><td>

Anything Else Topic. Virtual Agent asks users if they need further assistance.

 ![Anything else topic in Virtual Agent web client.](../images/setup-va-anything-else.png)

 If users select **Yes**, Virtual Agent returns a list of related items that it can help with.

</td></tr><tr><td>

Live agent

</td><td>

Live Agent Support. Tells users that a live agent transfer is in process:

 ![Live agent topic presented in Virtual Agent web client.](../images/setup-va-live-agent.png)

</td></tr><tr><td>

Error

</td><td>

Error Handling Topic. Displays a generic error message to the user when the Virtual Agent encounters a problem that it can't resolve \(unrecoverable system error\) and transfers the user to a live agent.

 ![The Virtual Agent chat window displays, "An recoverable error has occurred. Please stand by while I connect you to a live agent."](../images/va-error-transfer.png)

</td></tr><tr><td>

Greeting

</td><td>

Greetings. Starts a conversation by greeting users and giving them the option to enter a request or see the items that the Virtual Agent can assist with.

 ![Greeting topic in Virtual Agent web client.](../images/setup-va-greeting.png)

 **Note:** The pre-built setup topics include a personalized greeting called the Dynamic Greeting Topic, which welcomes the user by name. To change the default greetings topic, double click **Setup topic name** and then choose the personalized greeting from the list of available setup topics.

</td></tr><tr><td>

Survey

</td><td>

Virtual Agent Feedback topic.

 Gathers user feedback on the conversational experience with the Virtual Agent. The survey setup topic displays randomly in 33% of your Virtual Agent conversations.

 The survey topic includes an introductory sentence that admins can customize as needed. The survey then presents a choice list with options users can select to describe their experience.

![Survey feedback choice list showing Good, Neutral, and Bad reply options.](../images/va-survey-choice-list.png "Example survey feedback choices")

 After the users provide their feedback, a message confirms that their feedback has been received:

 ![Survey feedback received.](../images/va-survey-feedback-received.png)

 **Note:** To change the probability \(percentage\) that the survey setup topic occurs in your conversations, change the value in the **com.glide.cs.survey.probability** system property. To display the survey setup topic randomly in 50% of your Virtual Agent conversations, set the **Value** to 0.50.

</td></tr><tr><td>

Closing

</td><td>

Closing Conversation. Displays a closing message to the user that ends the conversation:

 ![Closing topic in Virtual Agent web client.](../images/setup-va-closing.png)

</td></tr><tr><td>

AI Search fallback

</td><td>

AI Search Fallback. When enabled, this setup topic uses AI Search search to generate fallback AI Search results when Virtual Agent can't find a matching intent or it finds too many intents and can't determine the appropriate topic to display to a user.

</td></tr><tr><td>

Fallback

</td><td>

Fallback Topic. Displays a standard message to the user when:

-   When virtual agent doesn't understand a user utterance or keyword and the AI Search fallback setup topic is not enabled in the chat experience. AI Search fallback topic was deactivated in the chat experience, and the virtual agent doesn't understand a user statement or keyword.
-   Users indicate that the AI Search results aren't helpful.

 ![Error handling topic and live agent transfer triggered by an unrecoverable system error.](../images/fallback.png)

</td></tr><tr><td>

Explore help

</td><td>

Virtual Agent Capabilities. Enables users to ask for assistance during a conversation and view a list of items that the Virtual Agent can assist with \(Virtual Agent capabilities\).

 ![Explore help topic presented in Virtual Agent web client.](../images/setup-va-capabilities.png)

</td></tr></tbody>
</table>-   **[Change text in the Show me everything button](../task/change-va-showme.md)**  
Configure the text in the **Show me everything** button displayed in the chat window to control the display of the initial greetings and the **Show me everything** button in Virtual Agent conversations. Edit the message in the System Properties \[sys\_properties\] table, or in a copy of the Greetings setup topic.
-   **[Hide or reveal the Show me everything button](../task/hide-reveal-showme-button.md)**  
Set properties to hide or reveal the **Show me everything** button in Virtual Agent conversations that use LLM \(large language model\) and NLU/Keyword \(Natural Language Understanding\) topic discovery.
-   **[Change the Virtual Agent greeting messages in the Greeting setup topic](../task/va-welcome-topic-selection-msgs.md)**  
The Virtual Agent greeting setup topic provides default greeting messages for your conversations. Customize these greetings by adding system properties that change the default welcome message and the top selection message prompting users to enter an issue or request.

**Parent Topic:**[Setting up chat experiences for Virtual Agent users](va-conversation-settings.md)

