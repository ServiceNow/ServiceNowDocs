---
title: Associate user profiles with agent-initiated messages
description: Use scripted extension points to call custom scripts for associating user profiles with agent-initiated messages.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Agent-Initiated Messaging Interface, Configure, Agent Chat, Conversational Interfaces]
---

# Associate user profiles with agent-initiated messages

Use scripted extension points to call custom scripts for associating user profiles with agent-initiated messages.

## Before you begin

Install the Agent-Initiated Messaging Interface application. For more information, see [Install agent-initiated messaging interface](install-agent-init-messg.md).

Role required: admin

## About this task

An agent can compose messages from an interaction of type other than Message in the CSM Configurable Workspace. By default, the AgentMessagingInteractionUserDocument script include is available for retrieving user profiles associated with consumers and customer contacts in an interaction record.

By using extension points, you can easily integrate customizations without having to alter the base code. You can extend standard base functionality using customized scripts. For more information, see Using extension points to extend application functionality.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and select **sn\_agent\_initiated.AgentInitiatedMessagingUserDocument**.

3.  On the Extension Point form, either modify a script include to use the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point or create and register a custom script include.

    -   Create and register a custom script include.
    -   Modify the existing script include by going to the Implementations related list and selecting a script include in the **Class** column.

        **Note:** By default, the AgentMessagingInteractionUserDocument script include that use the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point is available for the Agent-Initiated Messaging Interface application. This script include is configured to retrieve user profiles associated with consumers and customer contacts from the Interaction \[interaction\] table record.

4.  Associate user profiles for an agent-initiated messages by adding the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point to the script include.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

    |Customization|Implementation|
    |-------------|--------------|
    |Associate a table record from which the message was initiated|Include the isValidForTableRecord method in the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point.|
    |Retrieve the user details associated with the table record from which the message was initiated|Include the getUserDocument method in the sn\_agent\_initiated.AgentInitiatedMessagingUserDocument extension point.|

    **Note:** Based on the table record set in the isValidForTableRecord method, the user details are retrieved for sending agent-initiated messages in the getUserDocument method.

5.  On the Extension Point form, click **Update**.


**Parent Topic:**[Configuring Agent-Initiated Messaging Interface](../concept/config-agent-init-messg-interface.md)

