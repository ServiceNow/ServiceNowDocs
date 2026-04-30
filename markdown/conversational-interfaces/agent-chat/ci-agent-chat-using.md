---
title: Using Agent Chat
description: Agent Chat enables live agents to have conversations with requesters and for managers to help agents and monitor them.Use shortcuts, known as quick actions, for common activities that are performed frequently.Agents can use Conversation Autopilot to display Virtual Agent topics during Agent Chat conversations. While the requester interacts with the Virtual Agent topics, agents can multitask and work on other items. Conversation Autopilot is not available for HR Service Delivery \(HRSD\).Use emojis in Agent Chat conversations to convey emotions to requesters. This helps requesters feel like they're having a conversation with a friend and builds customer brand loyalty.Use Dynamic Translation for Agent Chat \(DTAC\) to have a chat conversation with a requester who uses a different language.Send a message to a requester even when the requester isn't online while working on issues in Workspace. A long-running conversation between an an agent and a requester who are not online concurrently is called an asynchronous, or async, chat.
locale: en-US
release: xanadu
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2024-11-12"
reading_time_minutes: 10
keywords: [Using, Agent Chat, Virtual Agent, live, conversation]
breadcrumb: [Agent Chat, Conversational Interfaces]
---

# Using Agent Chat

Agent Chat enables live agents to have conversations with requesters and for managers to help agents and monitor them.

Workspace displays a chat inbox icon ![Chat inbox icon.](../../workspace/image/inbox-icon-pol.png) that agents use to enter chats. Agents set their status to **Available** or **Away** to open or close their inbox for chat requests. The icon displays numbers when chats are waiting to be answered.

The chat interface is integrated into the workspace so agents can chat while working onscreen with other features provided by the workspace.

![Chat with agent](../../workspace/image/chat-screen-pol.png)

The following sections explain how to use Agent Chat.

## Using quick actions in Agent Chat

Use shortcuts, known as quick actions, for common activities that are performed frequently.

In Agent Chat, an agent can insert a quick action in any of the following ways:

-   Enter a command after the forward slash \(/\).
-   Select the lightning bolt icon \(![Lightning bolt icon](../../workspace/image/lightning-bolt.png)\) and select a quick action from the menu.
-   Select the quick action button on the toolbar \(if available\).

For example, an agent can transfer a conversation to another queue by entering `/tq` in the message field.

![Initiating a queue transfer by typing](../../workspace/image/tq-typing.gif "Initiate a queue transfer by typing")

An agent can also initiate a queue transfer by selecting the lightning bolt icon and then selecting **/tq** from the menu.

![Initiating a queue transfer from the quick action menu](../../workspace/image/tq-menu.gif "Initiate a queue transfer from the quick action menu")

Alternatively, an agent can transfer to another queue by selecting the arrow button \(![Arrow icon](../image/arrow.png)\) on the toolbar.

![Initiating a queue transfer from the toolbar](../../workspace/image/tq-button.gif "Initiate a queue transfer from the toolbar")

**Note:** Agents must have the quickactions\_user role to use quick actions.

An agent can view the context relevant to a chat interaction. An agent can use a context quick action to show a card with context variables: sysparm\_portal, sysparm\_page, table, sys\_id, and sysparm\_language. The agent can initiate this quick action by entering `/context` in the message field.

![Context Quick Action](../../workspace/image/contex-quick-action.png "Display chat context details")

An agent can use the Now Assist context menu to generate a response to enter in a chat. The agent initiates this quick action by entering `/recommend` in the message input field. An error message appears if it takes too long to generate the recommended response or the LLM server isn't available.

### Parameters

Some quick actions require a secondary menu so that agents can further control the quick action. For example, after an agent initiates a queue transfer, the agent must select which queue to transfer to. The items that appear on the secondary menu are called parameters.

The following figure shows that, after an agent inserts a quick action to transfer to another queue, the agent sees a list of available queues. The default parameters for the quick actions are queues that are available to agents.

![Available queues parameters](../../workspace/image/queues-parameters.png)

To create a quick action that requires a secondary menu, you must define parameters for the quick action. For more information, see [Define a quick action parameter](ci-quick-actions-overview.md#).

## Automatically displaying topics with Conversation Autopilot

Agents can use Conversation Autopilot to display Virtual Agent topics during Agent Chat conversations. While the requester interacts with the Virtual Agent topics, agents can multitask and work on other items. Conversation Autopilot is not available for HR Service Delivery \(HRSD\).

While talking to a requester in an Agent Chat conversation, agents can start Conversation Autopilot by using autopilot quick actions to invoke Virtual Agent topics. Depending on the information entered by the requester, agents can search for a specific Virtual Agent topic and display it with parameters. The requester views the topic and responds as needed and Virtual Agent captures the requester’s input.

**Note:** For the best experience, enable the Agent Chat setting that turns on system messages during autopilot. For details, see [Setting up Agent Chat](../task/ac-configure-agent-chat.md).

### Configuring Autopilot

You must have the Glide Virtual Agent plugin and the Agent Chat plugin installed to view and access the quick action for Autopilot. Admins can setup which Virtual Agent topics are available to agents in Agent Chat.

**Note:** Admins must be able to configure a quick action based on their organization's business need and set it up for agents to use as required.

For information on using quick actions in Agent Chat, see [Using quick actions in Agent Chat](ci-agent-chat-using.md#).

### Using Autopilot

The agent is able to use quick actions to search for and invoke an Autopilot topic of their choice during their conversation with a requester. The agent can only select Autopilot topics that are relevant to the channel. For example, only topics optimized for SMS are selectable when conversing with a requester who is using SMS.

![Starting autopilot using the quick action](../image/autopilot-quick-action-start.png)

The agent is informed by system messages when an Autopilot topic has been initiated and ended. These messages can be configured by admins.

![Message to agent after autopilot has been started.](../image/autopilot-start-input.png)

### While Autopilot is on

While Autopilot is on, the requester can use the rich controls for text but agents see a read-only version of the rich controls rendered to the requester.

![Rich controls are read-only during autopilot.](../image/autopilot-no-rich-controls.png)

When Autopilot is in use, public chat with the requester is disabled, but agents can contact other agents and supervisors for help. If Agent Whisper is on, the **Private Chat** tab in Agent Whisper functions normally during Autopilot. While Autopilot is in use, the agent's capacity is not freed up and messaging actions configured by customers are disabled.

### When Autopilot is ended

The agent receives a desktop notification in the **Notifications** tab in Workspace stating that the Virtual Agent topic has ended or been completed by the requester. At this point, the agent resumes control of the conversation.

![Autopilot ended.](../image/autopilot-end-autopilot.png)

## Conveying emotions using emojis

Use emojis in Agent Chat conversations to convey emotions to requesters. This helps requesters feel like they're having a conversation with a friend and builds customer brand loyalty.

### Before you begin

Emojis must be enabled before agents can use them in Agent Chat. See [Setting up Agent Chat](../task/ac-configure-agent-chat.md) for instructions on enabling emojis.

Role required: admin

### Procedure

1.  While in an active chat, there are several ways to include an emoji:

    -   Select the Insert emoji icon ![smiley face icon](../image/smiley-icon.png) to display the emoji palette. Then select an emoji from the palette or search for an emoji by entering a name in the search bar of the emoji palette.
    ![Emoji palette.](../image/emoji-palette.png)

    -   Enter a colon followed by the first few characters of the emoji name. When the pop-up menu of emojis displays, select one.
    ![Short name list of emojis.](../image/emoji-enter-name.png)

    -   Enter a special character combination or short name which is automatically converted into an emoji after entering a space or enter.
    ![Enter emoji short name.](../image/emoji-enter-short-name.png)

2.  Display the short name of an emoji as a tooltip by positioning the cursor over the emoji.

    ![Tool tip displaying emoji short name.](../image/emoji-short-name.png)


## Conversing in a different language with Dynamic Translation for Agent Chat

Use Dynamic Translation for Agent Chat \(DTAC\) to have a chat conversation with a requester who uses a different language.

### Translation indicators

When DTAC is enabled, both the agent and the requester will see a banner at the top of the chat conversation that indicates the conversation is being translated. Bilingual agents can determine if they’re fluent enough in the requester’s language to temporarily turn off DTAC for individual chat sessions as needed.

![End user view and Agent view of chat window, showing Translation indicators for agents and requesters.](../image/translation-indicators.png)

### Dynamic translations control for bilingual agents

When a bilingual agent accepts a chat conversation to which they’re fluent in the requester’s language, DTAC is not necessary. With the Dynamic translations chat session control, agents can turn of DTAC for individual chat sessions.

Agents can select the ellipsis \(![Translation-indicator icon](../../dynamic-translation/image/Ellipses.png)\) at the bottom of the chat window then select the **Dynamic translations control** to the off position.

When DTAC is switched off, a notification displays at the top of the agent’s and the requester's chat windows, highlighting the change in status, for this chat session.

The translation capability is switched off for both the requester and the agent, for this specific chat session. The selection in one chat session does not affect the selection in other chat sessions and the agent can turn DTAC off and back on within one chat session.

![Dynamic translations control for bilingual agents.](../image/control-bilingual-agents.png)

### Troubleshoot translated messages

Translation services do not understand idioms or jargon and it is possible that some user messages are lost in translation. You can use the translation-indicator icon to view the requester’s original message and look up its meaning as needed.

You can navigate to the individual chat message and select the translation-indicator icon \(![Translation-indicator icon, displayed as a globe grid.](../../dynamic-translation/image/Globe.png)\) to see the requester’s original, untranslated message.

![Agent chat window with message banner indicating conversation will be translated from French.](../image/troubleshoot-translated-messages.png)

### Translated chat transcripts

Two chat transcripts are generated at the end of each DTAC chat session. One for the requester to download and save in the requester’s language. The other is the agent’s transcript which contains the text as seen in the agent’s chat window. If an agent used DTAC in part of the chat, the transcript contains both the translated and non-translated text. For more information, see [Chat transcript downloads for requesters](ci-chat-transcripts.md).

### Chat transferred from Virtual Agent

Once you accept a chat from a requester, you can see the chat history between the Virtual Agent and requester in their preferred language for more context.

![Transferring from virtual agent to live agent](../../dynamic-translation/image/transfer-va-live-agent.png)

### Attachments within DTAC

When inserting an attachment into a chat, DTAC does not translate the file name or the contents of the attachment.

## Sending an agent-initiated message during an async chat

Send a message to a requester even when the requester isn't online while working on issues in Workspace. A long-running conversation between an an agent and a requester who are not online concurrently is called an asynchronous, or async, chat.

### Before you begin

Role required: admin

### Procedure

1.  On the Interaction record, select **Compose Message**.

    The Compose message form displays for interactions that aren't Chat or Messaging.

2.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Channel|Messaging channel with which agents can initiate messages to connect with requesters. For async chat, select **mweb**.|
    |From|ID of the agent who is sending the message.|
    |To|ID of the requester who will receive the message.|
    |Message|Enter the message you want to send to the requester.|
    |Attachment|Select **Attach File** to specify a file to attach to the message.|

3.  Select **Send**.


**Related topics**  


[Asynchronous chat](../../virtual-agent/concept/async-chat.md)

[Configure asynchronous chat for the web channel](../../virtual-agent/task/configure-async-web.md)

