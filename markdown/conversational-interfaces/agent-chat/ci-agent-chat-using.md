---
title: Using Agent Chat
description: Agent Chat enables live agents to have conversations with requesters and for managers to help agents and monitor them.Use shortcuts, known as quick actions, for common activities that are performed frequently.Agents can use Conversation Autopilot to display Virtual Agent topics during Agent Chat conversations. While the requester interacts with the Virtual Agent topics, agents can multitask and work on other items. Conversation Autopilot is not available for HR Service Delivery \(HRSD\).Use emojis in Agent Chat conversations to convey emotions to requesters. This helps requesters feel like they're having a conversation with a friend and builds customer brand loyalty.Use Dynamic Translation for Agent Chat \(DTAC\) to have a chat conversation with a requester who uses a different language.Send a message to a requester even when the requester isn't online while working on issues in Workspace. A long-running conversation between an an agent and a requester who are not online concurrently is called an asynchronous, or async, chat.Use the action bar in chat interaction records to access a range of actions that help manage and respond to records efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/agent-chat/ci-agent-chat-using.html
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
keywords: [Using, Agent Chat, Virtual Agent, live, conversation]
breadcrumb: [Agent Chat, Conversational Interfaces]
---

# Using Agent Chat

Agent Chat enables live agents to have conversations with requesters and for managers to help agents and monitor them.

Workspace displays a chat inbox icon \[Omitted image "inbox-icon-pol.png"\] Alt text: that agents use to enter chats. Agents set their status to **Available** or **Away** to open or close their inbox for chat requests. The icon displays numbers when chats are waiting to be answered.

The chat interface is integrated into the workspace so agents can chat while working onscreen with other features provided by the workspace.

\[Omitted image "chat-screen-pol.png"\] Alt text: Chat with agent

The following sections explain how to use Agent Chat.

## Using quick actions in Agent Chat

Use shortcuts, known as quick actions, for common activities that are performed frequently.

In Agent Chat, an agent can insert a quick action in any of the following ways:

-   Enter a command after the forward slash \(/\).
-   Select the lightning bolt icon \(\[Omitted image "lightning-bolt.png"\] Alt text: Lightning bolt icon\) and select a quick action from the menu.
-   Select the quick action button on the toolbar \(if available\).

For example, an agent can transfer a conversation to another queue by entering `/tq` in the message field.

\[Omitted image "tq-typing.gif"\] Alt text: Initiating a queue transfer by typing

An agent can also initiate a queue transfer by selecting the lightning bolt icon and then selecting **/tq** from the menu.

\[Omitted image "tq-menu.gif"\] Alt text: Initiating a queue transfer from the quick action menu

Alternatively, an agent can transfer to another queue by selecting the arrow button \(\[Omitted image "arrow.png"\] Alt text: Arrow icon\) on the toolbar.

\[Omitted image "tq-button.gif"\] Alt text: Initiating a queue transfer from the toolbar

**Note:** Agents must have the quickactions\_user role to use quick actions.

An agent can view the context relevant to a chat interaction. An agent can use a context quick action to show a card with context variables: sysparm\_portal, sysparm\_page, table, sys\_id, and sysparm\_language. The agent can initiate this quick action by entering `/context` in the message field.

\[Omitted image "contex-quick-action.png"\] Alt text: Context Quick Action

An agent can use Now Assist context menu to generate a response to enter in a chat. The agent initiates this quick action by entering `/recommend` in the message input field. An error message appears if it takes too long to generate the recommended response or the LLM server isn't available.

### Parameters

Some quick actions require a secondary menu so that agents can further control the quick action. For example, after an agent initiates a queue transfer, the agent must select which queue to transfer to. The items that appear on the secondary menu are called parameters.

The following figure shows that, after an agent inserts a quick action to transfer to another queue, the agent sees a list of available queues. The default parameters for the quick actions are queues that are available to agents.

\[Omitted image "queues-parameters.png"\] Alt text: Available queues parameters

To create a quick action that requires a secondary menu, you must define parameters for the quick action. For more information, see [Define a quick action parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-quick-actions-overview.md).

## Automatically displaying topics with Conversation Autopilot

Agents can use Conversation Autopilot to display Virtual Agent topics during Agent Chat conversations. While the requester interacts with the Virtual Agent topics, agents can multitask and work on other items. Conversation Autopilot is not available for HR Service Delivery \(HRSD\).

While talking to a requester in an Agent Chat conversation, agents can start Conversation Autopilot by using autopilot quick actions to invoke Virtual Agent topics. Depending on the information entered by the requester, agents can search for a specific Virtual Agent topic and display it with parameters. The requester views the topic and responds as needed and Virtual Agent captures the requester’s input.

**Note:** For the best experience, enable the Agent Chat setting that turns on system messages during autopilot. For details, see [Setting up Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ac-configure-agent-chat.md).

### Configuring Autopilot

You must have the Glide Virtual Agent plugin and the Agent Chat plugin installed to view and access the quick action for Autopilot. Admins can setup which Virtual Agent topics are available to agents in Agent Chat.

**Note:** Admins must be able to configure a quick action based on their organization's business need and set it up for agents to use as required.

For information on using quick actions in Agent Chat, see [Using quick actions in Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-agent-chat-using.md).

### Using Autopilot

The agent is able to use quick actions to search for and invoke an Autopilot topic of their choice during their conversation with a requester. The agent can only select Autopilot topics that are relevant to the channel. For example, only topics optimized for SMS are selectable when conversing with a requester who is using SMS.

\[Omitted image "autopilot-quick-action-start.png"\] Alt text: Starting autopilot using the quick action

The agent is informed by system messages when an Autopilot topic has been initiated and ended. These messages can be configured by admins.

\[Omitted image "autopilot-start-input.png"\] Alt text: Message to agent after autopilot has been started.

### While Autopilot is on

While Autopilot is on, the requester can use the rich controls for text but agents see a read-only version of the rich controls rendered to the requester.

\[Omitted image "autopilot-no-rich-controls.png"\] Alt text: Rich controls are read-only during autopilot.

When Autopilot is in use, public chat with the requester is disabled, but agents can contact other agents and supervisors for help. If Agent Whisper is on, the **Private Chat** tab in Agent Whisper functions normally during Autopilot. While Autopilot is in use, the agent's capacity is not freed up and messaging actions configured by customers are disabled.

### When Autopilot is ended

The agent receives a desktop notification in the **Notifications** tab in Workspace stating that the Virtual Agent topic has ended or been completed by the requester. At this point, the agent resumes control of the conversation.

\[Omitted image "autopilot-end-autopilot.png"\] Alt text: Autopilot ended.

## Conveying emotions using emojis

Use emojis in Agent Chat conversations to convey emotions to requesters. This helps requesters feel like they're having a conversation with a friend and builds customer brand loyalty.

### Before you begin

Emojis must be enabled before agents can use them in Agent Chat. See [Setting up Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ac-configure-agent-chat.md) for instructions on enabling emojis.

Role required: admin

### Procedure

1.  While in an active chat, there are several ways to include an emoji:

    -   Select the Insert emoji icon \[Omitted image "smiley-icon.png"\] Alt text: smiley face icon to display the emoji palette. Then select an emoji from the palette or search for an emoji by entering a name in the search bar of the emoji palette.
    \[Omitted image "emoji-palette.png"\] Alt text: Emoji palette.

    -   Enter a colon followed by the first few characters of the emoji name. When the pop-up menu of emojis displays, select one.
    \[Omitted image "emoji-enter-name.png"\] Alt text: Short name list of emojis.

    -   Enter a special character combination or short name which is automatically converted into an emoji after entering a space or enter.
    \[Omitted image "emoji-enter-short-name.png"\] Alt text: Enter emoji short name.

2.  Display the short name of an emoji as a tooltip by positioning the cursor over the emoji.

    \[Omitted image "emoji-short-name.png"\] Alt text: Tool tip displaying emoji short name.


## Conversing in a different language with Dynamic Translation for Agent Chat

Use Dynamic Translation for Agent Chat \(DTAC\) to have a chat conversation with a requester who uses a different language.

### Translation indicators

When DTAC is enabled, both the agent and the requester will see a banner at the top of the chat conversation that indicates the conversation is being translated. Bilingual agents can determine if they’re fluent enough in the requester’s language to temporarily turn off DTAC for individual chat sessions as needed.

\[Omitted image "translation-indicators.png"\] Alt text: End user view and Agent view of chat window, showing Translation indicators for agents and requesters.

### Dynamic translations control for bilingual agents

When a bilingual agent accepts a chat conversation to which they’re fluent in the requester’s language, DTAC is not necessary. With the Dynamic translations chat session control, agents can turn of DTAC for individual chat sessions.

Agents can select the ellipsis \(\[Omitted image "Ellipses.png"\] Alt text: Translation-indicator icon\) at the bottom of the chat window then select the **Dynamic translations control** to the off position.

When DTAC is switched off, a notification displays at the top of the agent’s and the requester's chat windows, highlighting the change in status, for this chat session.

The translation capability is switched off for both the requester and the agent, for this specific chat session. The selection in one chat session does not affect the selection in other chat sessions and the agent can turn DTAC off and back on within one chat session.

\[Omitted image "control-bilingual-agents.png"\] Alt text: Dynamic translations control for bilingual agents.

### Troubleshoot translated messages

Translation services do not understand idioms or jargon and it is possible that some user messages are lost in translation. You can use the translation-indicator icon to view the requester’s original message and look up its meaning as needed.

You can navigate to the individual chat message and select the translation-indicator icon \(\[Omitted image "Globe.png"\] Alt text: Translation-indicator icon, displayed as a globe grid.\) to see the requester’s original, untranslated message.

\[Omitted image "troubleshoot-translated-messages.png"\] Alt text: Agent chat window with message banner indicating conversation will be translated from French.

### Translated chat transcripts

Two chat transcripts are generated at the end of each DTAC chat session. One for the requester to download and save in the requester’s language. The other is the agent’s transcript which contains the text as seen in the agent’s chat window. If an agent used DTAC in part of the chat, the transcript contains both the translated and non-translated text. For more information, see [Chat transcript downloads for requesters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-chat-transcripts.md).

### Chat transferred from Virtual Agent

Once you accept a chat from a requester, you can see the chat history between the Virtual Agent and requester in their preferred language for more context.

\[Omitted image "transfer-va-live-agent.png"\] Alt text: Transferring from virtual agent to live agent

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


[Asynchronous chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/async-chat.md)

[Configure asynchronous chat for the web channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-async-web.md)

## Using the action bar in chat interaction records

Use the action bar in chat interaction records to access a range of actions that help manage and respond to records efficiently.

The action bar includes the following actions:

-   End Chat: Enables an agent to end the chat conversation.

    **Note:** In contact-center-as-a-service \(CCaaS\) powered chats, End Chat is replaced with Leave Chat, which enables an agent to leave the chat conversation without ending it for other agents.

-   Discuss: Opens a pop-up window to start a Sidebar discussion.
-   Create Case: Creates a new case record.
-   Save: Saves changes to the interaction record.
-   More Actions: Perform additional actions such as creating a request or associating a record.
    -   Create Consumer: Creates a new Consumer record in a subtab.
    -   Create Request: Creates a new Request record in a subtab and adds the record to the Related Tasks related list.
    -   Associate Record: Opens a new record in a subtab that the agent can use to link a record to the current interaction. This new record is displayed in the Related Tasks related list.

**Note:** The specific actions available are determined by factors such as the user role and other attributes.

