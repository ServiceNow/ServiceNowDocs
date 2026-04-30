---
title: Configure a provider for your custom chat integration
description: Create a new provider for your custom chat integration. Providers are defined in the Connections \[sys\_cs\_provider\] table.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create conversational custom chat integration, Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure a provider for your custom chat integration

Create a new provider for your custom chat integration. Providers are defined in the Connections \[sys\_cs\_provider\] table.

## Before you begin

[Create a new channel for your custom chat integration](create-channel-va-cccif.md).

Role required: admin

## About this task

Configure a new provider for each integration that you set up.

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_provider.list` in the filter.

2.  On the Connections page, select **New Custom**.

3.  On the form, fill in the fields.

<table id="table_lpr_zvq_ktb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your provider application. For example: `VA SMS Twilio Adapter`

</td></tr><tr><td>

Provider attributes action

</td><td>

Name of the provider attributes action script. The provider attributes action script can return a Provider auth token, a user identifier, user input, and context variables.

</td></tr><tr><td>

Response processor action

</td><td>

Name of the response processor action script. The Response processor action script performs platform actions. For example, updating a message status based on the response received for an outbound message.

</td></tr><tr><td>

Version

</td><td>

The version of the provider. The framework is able to send the expected inputs to actions and subflows and handle the expected outputs. There are 2 versions:-   **1.0.0**: The assumed version unless explicitly defined on the provider.
-   **1.1.0**: The `outbound_token` input parameter \(from the provider channel identity\) was added to invocations of the sender subflow/action.


</td></tr><tr><td>

HTML to Image conversion required

</td><td>

Option to convert an HTML bot response into an image and link. Used for chat interfaces that do not support HTML rendering.

</td></tr><tr><td>

Allow account linking

</td><td>

Option to link your account to an existing ServiceNow® profile.

</td></tr><tr><td>

Channel

</td><td>

Channel that this provider supports and the one to which the integration is being built.

</td></tr><tr><td>

Sender action

</td><td>

The sender action script. The sender action script bundles the request and then sends the response via Workflow Studio or Integration Hub asynchronously.

</td></tr><tr><td>

Sender subflow

</td><td>

The sender subflow bundles the request and sends the response via Workflow Studio \(FD\) or Integration Hub \(IH\) asynchronously.

​

</td></tr><tr><td>

Contextual action

</td><td>

Name of the contextual action script. The contextual action script supports custom contextual actions.

</td></tr></tbody>
</table>4.  Click **Submit**.

    ![Custom chat integration.](../images/custom-chat-int.png)


## What to do next

[Set up message authentication for your custom chat configuration](set-up-msg-auth-va-cccif.md)

**Parent Topic:**[Create a Virtual Agent conversational custom chat integration](create-adapter-for-virtual-agent.md)

