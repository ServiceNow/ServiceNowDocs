---
title: Transferring Virtual Agent conversations to a live agent
description: Manage live chat support, including the chat support interface used when a Virtual Agent conversation is transferred to a live agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Virtual Agent with a live agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Transferring Virtual Agent conversations to a live agent

Manage live chat support, including the chat support interface used when a Virtual Agent conversation is transferred to a live agent.

**Note:** The Glide Virtual Agent plugin \(com.glide.cs.chatbot\) automatically activates the Glide Conversation Server plugin \(com.glide.cs\) for chat support.

Conversations in Virtual Agent are transferred to a live agent in several ways. This transfer happens automatically when an unrecoverable error occurs, but it can also be triggered by a script in a topic, when a user manually selects that option, or when a user inputs the request during an LLM conversation.

-   **Automatic transfer to a live agent when an error occurs**

    When a conversation encounters an error, the conversation automatically transfers to a live agent.

    ![Virtual Agent chat window displaying, "An unrecoverable error has occurred. Please stand by while I connect you to a live agent."](../images/va-error-transfer.png)

    **Note:** If you don't plan to use Agent Chat, be sure to deactivate it in the Agent Chat settings. For more information, see [Setting up Agent Chat](../../conversational-interfaces/task/ac-configure-agent-chat.md).

-   **Automatic transfer to a live agent that is triggered by a script in a topic**

    In situations where you want a support agent to handle the conversation, you can create a script in your topic that uses the vaSystem.connectToAgent\(\) method. This method triggers a transfer to a live agent. This option can be useful for conversations involving negative customer sentiment, high priority requests, or requests outside the scope of your topic process. For example:

    ```
    (function execute() {
        if (vaInputs.urgency == 1 && vaInputs.impact == 3)
            if(vaSystem.isLiveAgentAvailable()) { 
               vaSystem.connectToAgent()
            }
        })()
    ```

    This script action control transfers the conversation to a live agent based on the incident impact and user urgency. The script uses the vaSystem.isLiveAgentAvailable\(\) method as follows:

    -   In Agent Workspace, the vaSystem.isLiveAgentAvailable\(\) method checks the queue schedule and whether agents are online.
    -   In Connect Support, the vaSystem.isLiveAgentAvailable\(\) method only checks the queue schedule.
    **Note:** The vaSystem.isLiveAgentAvailable\(\) method only checks whether agents are online, regardless of their skill set.

-   **Manual transfer to a live agent using the Contact support option**

    You can choose the **Contact support** option and then select **Contact Live Agent** to transfer the conversation to a live agent.

    **Note:** Users running a Virtual Agent messaging integration must enter the command `Hi` or `agent` to access the live agent transfer option. If your environment isn't configured for live agents, the `agent` command doesn't work. For more information, see [Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md).

    ![Virtual Agent chat window and contact support options.](../images/va-manual-transfer.png "Contact Support options in Virtual Agent")

-   **Manual transfer to a live agent in LLM conversations**

    In a Virtual Agent conversation using LLM topics, you can enter a statement such as `I need to talk to a live agent`, `transfer me to a live agent`, or other similar statements. The LLM then turns your chat over to an available live agent.


## How Virtual Agent conversation transfers work

For a user engaged in a Virtual Agent conversation, the switch to a live agent is a seamless transfer. When a transfer is triggered, either automatically or by a user manually, the conversation is automatically routed to the appropriate chat support interface, based on your [Agent Chat settings](../../conversational-interfaces/task/ac-configure-agent-chat.md). In Agent Chat settings, admins also define the general messages that users see during live agent transfers.

If you're using Agent Workspace, the conversation is automatically routed and assigned to an available live agent. If you're using Connect Support, the conversation is routed to the chat support queue that you specify.

**Note:** At least one live agent must be available when transferring from Virtual Agent, otherwise the end user is presented with a `no agents available` message and their conversation isn’t transferred.

-   **Transfer to a live agent in Agent Workspace**

    If you're using Agent Workspace, the Virtual Agent conversation is automatically transferred to a qualified available agent, based on the Chat service channel configuration and the queues that the agent supports, as defined in Advanced Work Assignment.

    For the user, the conversation with the agent continues in the Virtual Agent \(client\) interface. In Agent Workspace, the chat assignment appears in the agent's inbox. When an agent accepts the assignment, the agent joins the conversation and interacts with the user.

-   **Transfer to a live agent in Connect Support**

    If you're using Connect Support, the virtual agent conversation is routed to the appropriate chat support queue. For the user, the conversation with the agent continues in the Virtual Agent client interface. In Connect Support, the agent accepts the queue with the transferred user to join the conversation and interact with the user.

    In earlier releases, admins used the Chat Setup form to assign the default chat queues for Customer Service Management, HR Service Delivery, and IT Service Management or a global queue to which Virtual Agent conversations were automatically routed if default queues weren’t assigned. These queues, which admins defined in Connect Support, are stored in the Chat Queues \[chat\_queue\] table. If you're using Connect Support as the fulfiller interface and must change chat settings, see [Setting up Agent Chat](../../conversational-interfaces/task/ac-configure-agent-chat.md) for details.


## User sentiment

When configured, user sentiment analysis is performed on Virtual Agent and live agent conversations. The user sentiment is stored in the Interaction Insights \[sys\_cs\_interaction\_insight\] table. For details, see [Interaction Insights table](../../conversational-interfaces/reference/ci-interaction-insights-table.md).

**Parent Topic:**[Using Virtual Agent with a live agent](using-va-agent-chat.md)

