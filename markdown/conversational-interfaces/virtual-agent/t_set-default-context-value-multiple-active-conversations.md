---
title: Set a default NLU context value for multiple active conversations
description: Use consumer account context values to define where Virtual Agent messages are directed by default when using the multiple active conversations feature.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Default, context, Multiple active conversations, Virtual Agent, Agent Chat, portal]
breadcrumb: [Multiple active conversations for Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Set a default NLU context value for multiple active conversations

Use consumer account context values to define where Virtual Agent messages are directed by default when using the multiple active conversations feature.

## Before you begin

Define values for portal consumer contexts. For more information, see [Set NLU portal consumer context values for multiple active conversations](t_set-portal-consumer-context-values-multiple-active-conversations.md).

Configure context values that align Virtual Agent and your portals. See [Configure Agent Chat in a portal](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

Role required: virtual\_agent\_admin or admin.

## About this task

You can create as many context values as you need. One consumer account context must always be set to `Yes` to provide a default content area. The default acts as a fallback for the chat widget when the portal setup doesn’t include context. The default is also used as the context for mobile conversations, which only support one conversation at a time. Context values are stored in the Conversation Consumer Account Context \[sys\_cs\_consumer\_account\_context\] table. \(The CS Consumer Account \[sys\_cs\_consumer\_account\] table [Installed with Virtual Agent](../reference/installed-wth-virtual-agent.md) shows whether third-party users in your instance have a context assigned to them.\)

**Note:** These instructions are for configuring Natural Language Understanding \(NLU\) conversations. Large Language Model \(LLM\) conversations are configured for multiple active conversations based on portals, with no configuration necessary.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

2.  Under **multiple active conversations**, select **View settings**.

    **Note:** The delivered default value for consumer account contexts is `sp`.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_zxw_5d2_bxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the context value \(also used as reference in the backend\).

</td></tr><tr><td>

Short Description

</td><td>

Description for the context \(displayed on the Conversational Interfaces card when the default value is shown\).

</td></tr><tr><td>

Is Default Consumer Account Context

</td><td>

Option to make this context value the default for your Virtual Agent conversations.**Note:** Only one consumer account context can be set as the default. Setting a new one as a default automatically resets the last context to `False`.

</td></tr></tbody>
</table>5.  Select **Save**.


## What to do next

Activate the multiple active conversations system. For more information, see [Activate multiple active conversations in Virtual Agent](t_activate-multiple-active-conversations-va.md).

**Parent Topic:**[Multiple active conversations for Virtual Agent](../concept/c_multiple-active-conversations-va.md)

