---
title: Assign Now Assist skills to an assistant
description: Turn on and assign Now Assist skills to your assistant.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 2
breadcrumb: [Configuring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Assign Now Assist skills to an assistant

Turn on and assign Now Assist skills to your assistant.

## Before you begin

[Create an assistant](create-assistant.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Assign Now Assist skills to your assistant.

    **Note:** For Now Assist panel assistant \(Platform\), Now Assist Mult-Turn Catalog Ordering skill isn't available. For Now Assist panel assistant \(Developer\), only Now Assist Topic skill is available.

    ![Activate Now Assist skills for the Virtual Agent.](../image/NAinVA-skills3-052025.png "Conversational skill status")

    At the top of the page, the name of your Virtual Agent assistant appears. The table shows the following columns: Skill name, LLM service provider, and Alert.

    By default, all global skill types, except subflows and actions, are turned on in the Now Assist Admin console. If a global skill type is turned off, an alert appears in the Alert column at the assistant level. The alert indicates that a global skill type must be activated in the Now Assist Admin console.

    To turn a global skill type on or off, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). To deactivate a skill across the entire instance, select **Manage skills**. One or more skills must be active.

    The default Now Assist in Virtual Agent assistant is assigned Now Assist Q&amp;A, Now Assist Multi-Turn Catalog Ordering, Now Assist Topics, and AI agent skills. When a new assistant is created, all corresponding global skill types that are enabled are assigned to the assistant. By assigning a skill type to an assistant, the corresponding search sources get linked to the assistant's search profile. For example, if you want knowledge articles or external content to be enabled for an assistant, the Now Assist Q&amp;A skill must be assigned to the assistant.

    You can deselect assistant skill types at the assistant level to unassign them from an assistant.

    If Now Assist Q&amp;A isn't selected as a skill for the assistant, a check is performed to see if any portals or mobile apps have selected enhanced chat. An alert is shown if a portal or mobile app has enhanced chat. For more information about the enhanced chat experience, see [Enhanced chat](../concept/nava-enhanced-chat.md).

    **Note:** In this admin configuration, no matter which skills you choose, all responses are Synthesized Response with Multi-turn Q&amp;A for all portals, mobile applications, and Microsoft Teams.

    The Now Assist Topic skill must be turned on at the assistant level for document uploads to be active when managing your chat experience. An alert is shown if your Now Assist Topic skill is turned off.

    **Warning:** If you deactivate Now Assist topics, document uploads will also be deactivated.

2.  Select **Save and continue**.


## What to do next

[Display your assistant on a portal or channel](display-assistant-portal-channel.md).

