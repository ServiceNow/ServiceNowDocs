---
title: Supported Virtual Agent and Agent Chat features for custom chat integrations
description: The chat integrations framework supports a multitude of Virtual Agent and Agent Chat features to provide a robust conversational experience.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Supported Virtual Agent and Agent Chat features for custom chat integrations

The chat integrations framework supports a multitude of Virtual Agent and Agent Chat features to provide a robust conversational experience.

## User authentication, authorization, and secure connection setup

-   **Synchronous authentication of messages**

    Provider authentication is synchronous. They will get an immediate response with the request successful or failure code. For configuration information, see .

    **Note:** As of the Paris release, asynchronous authentication is no longer supported.

-   **Account auto-linking**

    Allow a user's third-party account to be auto-linked to their ServiceNow® profile. This feature bypasses the prompt for the user to link their accounts manually. Without account linking, conversations will take place in Guest mode. For configuration information, see [Account linking in pre-built messaging integrations](va-adapter-autolinking.md).

-   **[Configure the output response REST endpoint and outbound authentication for the Virtual Agent API](../task/configure-response-endpoint-va-api.md)**

    Specify the outbound endpoint URL to which the Virtual Agent responses are posted and configure outbound authentication. For configuration information, see .

-   **Secure data transfer**

    Sensitive data such as passwords can be masked and transferred via the integration framework securely.

-   **Trusted media domains**

    Use trusted media domains to check the URLs of attachment files before uploading them. For configuration information, see [Set up trusted media domains for secure file upload](../task/ccif-secure-file-upload.md).


## Rich control transformation

Design a rich and unique conversational experience for a channel through rich control transformation via inbound and outbound transformation scripts. All standard rich controls are supported. For detailed information about Virtual Agent controls, see the following sections:

-   [Virtual Agent Designer user input controls](../reference/va-user-inputs.md)
-   [Virtual Agent Designer bot responses](../reference/va-bot-responses.md)
-   [Virtual Agent Designer utilities](../reference/va-utilities.md)

## Supported Virtual Agent chat features

No configuration or scripting required to implement these features in Custom Chat Integration Framework.

-   **Support for all standard Virtual Agent controls**
    -   Pass context variables, system parameters, or a user's time-zone along with user input.
    -   By default the Virtual Agent processes only one user request at a time. If a user sends a second request before the first request is finished, the second request is ignored. This does not apply when the user is connected to a live agent.
    -   Ignore duplicate requests from client.
-   **Topic discovery using keywords or Natural Language Understanding**

    Custom chat integrations can avail topic discovery via keywords or NLU depending on how Virtual Agent is set up on your instance.

-   **Standard chat and long-running conversations**

    Channels can be set up as either chat or messaging. For more information on long-running conversations, see [Using Asynchronous Chat in messaging channels](async-chat.md).

-   **[Custom Virtual Agent chat experiences](../task/configure-default-chat-experience.md)**

    Define a custom chat experience for a specific context in which your users run Virtual Agent.

-   **Dynamic translation**

    Display a message in chat client that messages are being translated if dynamic translation is enabled.

-   **[Customize Virtual Agent and Agent Chat system messages](../../conversational-interfaces/task/ac-change-system-messages.md)**

    System messages are a set of pre-built messages that can be served as bot response in common conversation scenarios such as greeting a user or transferring to a live agent. Admins can override the message text to suit their business needs.

-   **[Notifications](configuring-va-notifications.md)**

    Deliver both simple and actionable notifications via the integration framework.

-   **Standard timeouts for idle agent conversations**

    You can change the default timeout period for closing Virtual Agent and live agent conversations by adding the system property **com.glide.cs.conversation\_idle\_timeout**.

-   **[Virtual Agent interaction records](va-interactions.md)**

    The channel \(sys\_cs\_channel.Name\), channel type \(sys\_cs\_channel.Type\), provider \(sys\_cs\_provider.Name\), provider identifier name \(sys\_cs\_provider\_application.Name\) and provider channel id \(sys\_cs\_provider\_application.InboundID\) fields are available for reporting.

-   **API rate limiting**

    Ability to control the rate at which API calls are made via the platform rate limiting feature.

-   **API versioning**

    Specify the version of the provider. The framework is able to send the expected inputs to actions and subflows and handle the expected outputs. See [Configure a provider for your custom chat integration](../task/create-provider-va-cccif.md) for more information.

-   **Specify the default portal for URL navigation at the Provider Channel Identities level**

    For a provider channel, specify the portal in which chat links, including links in output cards and cards for Virtual Agent notifications and AI Search results, are opened. For details on setting the default portal in the Provider Channel Identities \[sys\_cs\_provider\_application\] table, see [Create a channel identifier for your custom chat integration](../task/create-channel-id-va-cccif.md). To learn more about URL navigation, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).


## Supported Agent Chat features

-   **Support for all standard live agent controls**
    -   Transfer to live agent from Virtual Agent or directly by user
    -   Persistent messages after live agent is initiated
    -   Interaction history \(chat transcripts\) for live agents
    -   Channel-level flag to initiate conversations with live agents, bypassing Virtual Agent
-   **Live agent status for end users**
    -   Agent availability
    -   Wait time for next agent
    -   Display agent name and avatar, if enabled in [Agent Chat settings](../../conversational-interfaces/task/ac-configure-agent-chat.md).
-   **Channel-level flag to initiate conversations with live agents, bypassing Virtual Agent**

    Enable the **Live Agent Only** option in the Messaging Channels \[sys\_cs\_channel\] table to route conversations directly to a live agent and skip the Virtual Agent conversation greeting. If an agent isn't available, the message **No agent available** is displayed to the user. For channel configuration information, see [Create a new channel for your custom chat integration](../task/create-channel-va-cccif.md).

-   **Pass the agent avatar and name if enabled in Agent Chat settings**

    When the **Agent Names and Avatars** field is enabled in Agent Chat settings, the Custom Chat Integration Framework supports the display of the agent name and avatar in the chat. For more information, see [Setting up Agent Chat](../../conversational-interfaces/task/ac-configure-agent-chat.md).

-   **Pre-chat and post-chat surveys**

    After an agent ends a chat, the post-chat survey runs automatically when the following criteria are met:

    -   The Virtual Agent Feedback setup topic is enabled.
    -   The chat service channel and the queues that your live agents support are configured in Advanced Work Assignment.

-   **[Message delivery order](../reference/ccci-message-delivery-order.md)**  
Control message delivery order by enabling the **Maintain message ordering** option in the Provider Channel \[sys\_cs\_provider\] table. You can view the message order and status in the Custom Adapter Message \[sys\_cs\_ca\_message\] table.
-   **[Virtual Agent action scripts](../reference/va-action-scripts.md)**  
You need to write a set of mandatory Workflow Studio action and subflow scripts to pass the user data to VACS, apply transformations and send the response back to your chat interface endpoint.
-   **[Set up trusted media domains for secure file upload](../task/ccif-secure-file-upload.md)**  
Virtual Agent uses trusted media domains to check the URLs of attachment files before uploading them. If a URL is not from a trusted domain, Virtual Agent will not upload the attachment.
-   **[Create bot messages](../task/create-bot-messages.md#)**  
Create channel-specific bot messages.
-   **[Integrate custom controls](../task/ccif-integrate-custom-controls.md)**  
Implement and leverage custom controls built using the custom control framework in your integration.
-   **[Multi-step responses](../reference/ccci-multi-step-responses.md)**  
An example of multi-step response is a set of images in a carousel or a date control.
-   **[Multi-response output controls](../reference/ccci-multi-flow-output-controls.md)**  
Implement controls that involve multiple steps to get user input.
-   **[Send previous control to client](../reference/send-previous-control-client.md)**  
Provide the ability to send previous control to client.
-   **[Implement a skip option](../reference/va-skip-option-script.md)**  
Use a rich control to provide the option for users to skip a question.
-   **[Pass branding to a chat client](../reference/va-ccif-pass-branding.md)**  
Pass custom branding to your custom chat integration.
-   **[Contextual actions for custom chat integrations](../reference/contextual-actions.md#)**  
Commands with a pre-defined behavior can be mapped to certain user-friendly keywords and passed as user input. This input is mapped to supported contextual actions for the most appropriate response in the chat.
-   **[Typing indicators](../reference/ccci-typing-indicators.md)**  
Display a typing indicator when a bot or live agent is preparing a response to a requester.

**Parent Topic:**[Creating conversational custom chat integrations in Virtual Agent](va-custom-adapter-framework.md)

