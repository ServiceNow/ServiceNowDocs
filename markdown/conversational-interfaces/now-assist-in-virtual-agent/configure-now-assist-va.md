---
title: Configuring Now Assist in Virtual Agent
description: Use Now Assist in Virtual Agent to provide a content-driven and search-driven generative AI experience for users.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 3
breadcrumb: [Now Assist in Virtual Agent, Conversational Interfaces]
---

# Configuring Now Assist in Virtual Agent

Use Now Assist in Virtual Agent to provide a content-driven and search-driven generative AI experience for users.

## Before you begin

An admin can configure Now Assist in Virtual Agent assistants and the default Now Assist panel assistants \(Platform and Developer\).

**Note:** The procedures in this admin guided setup show steps for configuring Now Assist in Virtual Agent assistants. Options may differ if you're configuring a Now Assist panel assistant.

If multiple Now Assist in Virtual Agent assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.

Assistants are accessed from three different entry points:

<table id="table_b1j_2hm_w2c"><thead><tr><th>

Entry point

</th><th>

Accessing assistants

</th></tr></thead><tbody><tr><td>

**All** &gt; **Conversational Interfaces** &gt; **Assistants**

</td><td>

See Procedure 1 [Create an assistant](create-assistant.md) to set up your assistant.

</td></tr><tr><td>

**All** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Platform**

</td><td>

Select the **Set up Now Assist in Virtual Agent** link. ![Now Assist skills for Platform.](../image/NAinVA-na-admin-platform-May.png "Now Assist Admin console > Platform view")

</td></tr><tr><td>

**All** &gt; **Now Assist Admin** &gt; **Now Assist Experiences** &gt; **Now Assist panel**

</td><td>

Select the **Manage Assistants** link.![Now Assist panel with link to Manage assistants.](../image/NAinVA-NAP-manage-assistants.png "Manage assistants from the Now Assist panel")

</td></tr></tbody>
</table>Role required: virtual\_agent\_admin or admin

## About this task

Admins can configure more than one Now Assist in Virtual Agent assistant with this guided setup. A primary assistant can be linked to one or more secondary assistants. The linkage enables a primary assistant to use search sources from secondary assistants, enhancing its functionality and efficiency. For more information on primary and secondary assistants, see [LLM assistants](../concept/llm-assistants.md).

Each assistant uses either standard chat or enhanced chat. Enhanced chat provides a conversational search experience that combines Now Assist in Virtual Agent chat with search results. For more information, see [Standard chat](../concept/nava-standard-chat.md) and [Enhanced chat](../concept/nava-enhanced-chat.md). For a comparison of the two, see [Using Now Assist in Virtual Agent](../concept/using-now-assist-in-va.md).

## Procedure

1.  [Create an assistant](create-assistant.md).

2.  [Assign Now Assist skills to an assistant](assign-na-skills-assistant.md).

3.  [Display your assistant on a portal or channel](display-assistant-portal-channel.md).

4.  [Add information sources to an assistant](add-info-sources-assistant.md).

5.  [Brand an assistant](brand-assistant.md).

6.  [Manage an assistant chat experience](manage-assistant-chat-experience.md).

7.  [Review assistant settings](review-assistant-settings.md).


