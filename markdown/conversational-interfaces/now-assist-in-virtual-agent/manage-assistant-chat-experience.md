---
title: Manage an assistant chat experience
description: Manage the chat experience of your Now Assist in Virtual Agent assistant. Define your greeting, closing, fallback messages, and streaming responses.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 4
breadcrumb: [Configuring Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Manage an assistant chat experience

Manage the chat experience of your Now Assist in Virtual Agent assistant. Define your greeting, closing, fallback messages, and streaming responses.

## Before you begin

[Brand an assistant](brand-assistant.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Manage your assistant's greeting, closing, fallback messages, streaming responses, and document uploads.

    **Note:** For Now Assist panel assistant \(Platform\), closing message, fallback options, and document uploads aren't supported. For Now Assist panel assistant \(Developer\), closing message, fallback options, document uploads, and response streaming aren't supported.

    ![Greeting, closing,fallback options, streaming responses, and document uploads for your Virtual Agent in the Define your chat experience page.](../image/NAinVA-chat-exp1-052025.png "Greeting, closing, and fallback options for your assistant")

    Use the simple settings type to define the default chat experience.

    For fallback options:

    1.  Live Agent support routes you to an available agent when configured.
    2.  Reset conversation restarts the conversation to the beginning to ask another question.
    3.  A record producer directs the user to a catalog record producer to create an incident or a case.

        **Note:** For this fallback option to work for guest users, create a public record producer. For more information, see [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). If the public record producer is set to active, it automatically appears in the Now Assist in Virtual Agent Fallback options &gt; Record producer drop-down menu.

    ![Response streaming and document uploads screen.](../image/NAinVA-chat-exp2-052025.png "Response streaming and document uploads for your assistant")

    In the **Response streaming** section, if **Allow response streaming** is active, LLM messages appear as each word is generated as opposed to showing the entire message at once. If **Allow response streaming** is grayed out, it's because it's not supported when using Dynamic Translation. Channels that support synthesized response also support streaming when streaming is turned on.

    If Dynamic Translation is turned on, the **Allow response streaming** check box is grayed out. To turn off Dynamic Translation, go to the Now Assist Admin console. Turning off Dynamic Translation impacts the entire instance.

    In the **Document uploads** section, **Allow document uploads** is turned off by default. If you select the check box, users can upload documents in the chat and ask questions about the content or get a summary. For more information on file formats for uploading files to an assistant, see [Upload documents in Now Assist in Virtual Agent](upload-documents-na-va.md).

    **Note:** The Now Assist Topic skill must be turned on at the assistant level for document uploads to be active when managing your chat experience. The following alert is shown if your Now Assist Topic skill is turned off.

    **Warning:** If you deactivate Now Assist topics, document uploads will also be deactivated.

    More configurations are available in Advanced settings, replacing the default. Select from a prefiltered list to override setup topics defined in Virtual Agent Designer. If you change one of your setup topics, and you return to the simple setting, that topic is unavailable.

    **Note:** For Now Assist panel assistants \(Platform and Developer\), the available setup topic types are Greeting, Fallback, Error, and Explore help.

    ![Advanced chat settings in the Define your chat experience page.](../image/NAinVA-chat-exp-adv-052025.png "Chat experience advanced settings")

    You can create your own custom topics and use them to replace the greeting and closing messages, and the default fallback and Live Agent topics.

    In the **Promoted assets** tab, navigate to Virtual Agent Designer to define promoted assets for this assistant. Promoted assets appear as suggested assets for users to launch after they receive the assistant's greeting. For more information on promoting assets in Virtual Agent Designer, see [Promote or demote LLM topics in Virtual Agent Designer](../../virtual-agent/task/promote-demote-va-topics.md)

    ![Link to Virtual Agent Designer to define promoted assets.](../image/NAinVA-promoted-assets-052025.png "Define promoted assets")

    After promoting the assets in Virtual Agent Designer, you can then use the up or down arrows to reorder the assets. A maximum of six assets are shown to the user. On each asset, a tag shows whether it's a topic, subflow, action, custom skill, or AI agent.

    ![List of promoted topics that can be reordered.](../image/NAinVA-chat-promo-reorder2-052025.png "Promoted assets list")

    The **Closed chats** tab is available if the enhanced chat experience is active. If **Show closed chats** is turned on, users can access the chat history in the enhanced chat experience.

    ![Check box to allow users to view past chat history.](../image/NAinVA-closed-chats-052025.png "View past chat history")

2.  Select **Save and continue**.


## What to do next

[Review assistant settings](review-assistant-settings.md).

