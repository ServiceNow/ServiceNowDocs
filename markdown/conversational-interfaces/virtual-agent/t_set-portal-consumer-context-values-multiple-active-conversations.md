---
title: Set NLU portal consumer context values for multiple active conversations
description: Use context values to determine which portals receive certain messages and notifications for users in that portal.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using multiple active conversations in Virtual Agent, Configure, Virtual Agent, Conversational Interfaces]
---

# Set NLU portal consumer context values for multiple active conversations

Use context values to determine which portals receive certain messages and notifications for users in that portal.

## Before you begin

Activate Virtual Agent. For more information, see [Activate Virtual Agent](activate-virtual-agent.md).

Configure your Agent Chat system for your portal or portals. See [Configure Agent Chat in a portal](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) for more information.

Role required: virtual\_agent\_admin or admin

## About this task

With consumer context added to a portal configuration, that portal acts as context for multiple active conversations with Virtual Agent.

**Note:** These instructions are for configuring Natural Language Understanding \(NLU\) conversations. Large Language Model \(LLM\) conversations are configured for multiple active conversations based on portals, with no configuration necessary.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**.

2.  Select the Agent Chat Configuration for which you want to set the context value.

3.  In the Server Script window, add the line `consumer_account_context: 'VALUE'`, replacing `VALUE` with your desired consumer account context.

    ![Service Portal agent chat configuration form](../images/portal-consumer-context-values-mac-02.png "Server script example")

    **Note:**

    The syntax of the account context line depends on how the configuration is set up. For example, some configurations use an equal sign versus a colon. In the case of the **esc** context, there are also two relevant chat configurations.

    Values that are defined or created in a script aren’t displayed to an admin as a selection for use elsewhere in the system.

4.  Select **Update**.


## What to do next

Set a default context for your conversations. See [Set a default NLU context value for multiple active conversations](t_set-default-context-value-multiple-active-conversations.md) for more information.

**Parent Topic:**[Using multiple active conversations in Virtual Agent](../concept/c_multiple-active-conversations-va.md)

