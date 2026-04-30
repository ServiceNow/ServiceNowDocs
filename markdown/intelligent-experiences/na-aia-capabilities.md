---
title: Now Assist AI agents capabilities
description: Lists the features supported by Now Assist AI agents, including configuration options and functional capabilities.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-08"
reading_time_minutes: 2
breadcrumb: [AI agents best practices, Explore, Now Assist AI agents, Enable AI experiences]
---

# Now Assist AI agents capabilities

Lists the features supported by Now Assist AI agents, including configuration options and functional capabilities.

## Invoke Conversations with AI Agent Background Channel

The AI Agent Background Channel helps you to invoke AI Agent or agentic workflow execution from the Workspace. Use the AI Agent Background Channel associated with the AI Agent Background Provider to invoke conversations. The AI Agent Background Provider is based on the Custom Adapter Framework from Virtual Agent. For more information, see [Configure a provider for your custom chat integration](https://www.servicenow.com/docs/access?context=create-provider-va-cccif&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

Create a channel identifier in the Provider Channel Identities table \[sys\_cs\_provider\_application\] to add any additional conversational capabilities to your own provider application and get a new inbound ID that allows for customization. For more information, see [Create a channel identifier for your custom chat integration](https://www.servicenow.com/docs/access?context=create-channel-id-va-cccif&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

To start a conversation, trigger the flow using the sn\_aia.AiAgentRunttimeUtil\(\).startAiAgentConversation\(request\) API in the Script Include \(sys\_script\_include\) of the AIAgentBackgroundProvider and select **Run Script**. When the Script execution status indicates Success, the conversation begins in the order of utterances defined in the Script.

Conversations that are invoked for executing an AI agent are logged in the Execution Plans \[sn\_aia\_execution\_plan\] table. Open the conversation record to confirm the device type as **AI Agent Background**. Open the execution record to see the **Execution Tasks**, **Messages**, and the **Tools Executions** used to execute the AI agent.

You can also see the entire execution steps on the AI Agent Studio Testing page by copying the execution plan record's \[sys\_Id\] and testing it. On the **Chat responses** tab, in the AI agent decision logs, you can see the AI agent details and the tools it used to resolve the issue.

## Interactive and Non-interactive AI agents

The Interactive AI agents reach out to users for information when there is a fallback in the execution process, and the AI agent re-triggers the flow.

The Non-interactive AI agents do not reach out to the user at any fallback stage in the execution process. When the AI agent needs user information, it takes the dynamic prompt approach using the ReAct layer, where the prompt of the ReAct will change based on the execution mode of the AI agent or agentic workflow. Therefore, in the Non-interactive execution, the reach fallback options do not have to collect input from a user as a fallback option. However, the output of the AI agent or agentic workflow will still need to be presented to the user, and in any execution failure scenario, a message in the Now Assist panel or Virtual Agent is shown.

To implement the Non-interactive execution, the **Execution Mode** field is added in the Execution Plans \[sn\_aia\_execution\_plan\] table, where the execution mode can be **Interactive** or **Non Interactive** based on the given runtime parameter.

You can run the AI agents and agentic workflows concurrently in the AI Agent Background Channel and in Non-interactive mode where the background execution allows AI agents to operate with any chat panel like Now Assist panel or Virtual Agent.

## Multilingual support

You can leverage multilingual support for AI agents across languages for better translation quality to:

-   Tune system prompts for native translations.
-   Implement dynamic translation strategies when native support is unavailable.
-   Provide extensive testing via automated and manual evaluations.

