---
title: Configuring assistants overview
description: Use Assistant Designer to build and optimize large language model \(LLM\) assistants for your conversational needs. Assistant Designer is a centralized assistant administrator experience that allows you to create and manage both chat and voice assistants.
locale: en-US
release: yokohama
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-04-21"
reading_time_minutes: 3
breadcrumb: [Now Assist in Virtual Agent, Conversational Interfaces]
---

# Configuring assistants overview

Use Assistant Designer to build and optimize large language model \(LLM\) assistants for your conversational needs. Assistant Designer is a centralized assistant administrator experience that allows you to create and manage both chat and voice assistants.

## Before you begin

See [Assistant Designer](../concept/assistant-designer.md).

Role required: virtual\_agent\_admin or admin

## About this task

An admin can create and configure more than one chat or voice assistant within [Assistant Designer](../concept/assistant-designer.md).

For chat assistants, a primary assistant can be linked to one or more secondary assistants. The linkage enables a primary assistant to use search sources from secondary assistants, enhancing its functionality and efficiency. For more information on primary and secondary assistants, see [LLM assistants](../concept/llm-assistants.md). If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.

Each assistant can have more than one display experience, using either the standard chat or enhanced chat experience, depending on the display experience that's configured. Enhanced chat offers a conversational search experience that seamlessly integrates Virtual Agent chat with search results. For more information, see [Standard chat](../concept/nava-standard-chat.md) or [Enhanced chat](../concept/nava-enhanced-chat.md). For a comparison of the two, see [Using Now Assist in Virtual Agent](../concept/using-now-assist-in-va.md).

When configuring a chat assistant, notes throughout the procedures show where there are differences between the setup for Now Assist in Virtual Agent assistants and the setup for Now Assist panel assistants. Additional Now Assist panel assistants can’t be created.

For voice assistants, a voice assistant can be mapped to one or more AI agents. The linkage enables a voice assistant to leverage agentic capabilities to resolve user queries over phone.

## Procedure

1.  To access assistants in [Assistant Designer](../concept/assistant-designer.md), navigate to **All** &gt; **Assistant Designer** &gt; **Assistants** tab.

    The **Assistants** tab in [Assistant Designer](../concept/assistant-designer.md) can also be accessed from different entry points.

<table id="table_b1j_2hm_w2c"><thead><tr><th>

Entry point

</th><th>

Accessing assistants

</th></tr></thead><tbody><tr><td>

**All** &gt; **Conversational Interfaces** &gt; **Assistants**

</td><td>

Select **Manage assistants**.![Manage assistants links to Assistant Designer.](../image/NAinVA-assistants-home-122025.png "CI Admin view")

</td></tr><tr><td>

**All** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Platform**

</td><td>

Select the **Set up Now Assist in Virtual Agent** link. ![Now Assist skills for Platform.](../image/NAinVA-na-admin-platform-May.png "Now Assist Admin console > Platform view")

</td></tr></tbody>
</table>2.  To view and create chat or voice assistants, see [View assistants](view-assistants.md).


## What to do next

See [View assistants](view-assistants.md).

