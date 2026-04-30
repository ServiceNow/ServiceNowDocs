---
title: Small talk in conversations
description: Small talk topics and small talk utterances from the Semantic Filter Framework are recognized in Now Assist in Virtual Agent chat conversations.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-04-03"
reading_time_minutes: 1
keywords: [Now Assist, Virtual Agent, Small talk, genius results, generative AI]
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Small talk in conversations

Small talk topics and small talk utterances from the Semantic Filter Framework are recognized in Now Assist in Virtual Agent chat conversations.

Small talk is supported by your primary and fallback languages. The semantic filtering recognizes these types of small talk:

-   Greetings: For example, `Hi, how are you today?`
-   Gratitude: For example, `Thanks, this was helpful!`
-   Complaint: For example, `This answer doesn't help me.`

    Chat conversations with complaints may prompt you to request a live agent or another fallback topic, such as, a create a support request topic.

-   Closure: For example, `That's all I needed. Bye.`

    For standard chat conversations, the conversation ends when closure small talk is recognized.

    For enhanced chat conversations, conversations do not end and remain in the Active chat section. You can return to the same chat conversation as long as the conversation has not closed. You know that a message has closed when you receive the following response in the chat: `It looks like you're finished with this chat, so I'll go ahead and close it.` Chat conversations eventually close after a designated time has passed. For more information on the closed chats, see [Enhanced chat](nava-enhanced-chat.md).

    **Note:** For closure types of small talk, you may receive a confirmation message prior to exiting the conversation. The confirmation message asks, `You'd like to end this topic. Is that right?` with the **Yes** and **No** controls displayed. The confirmation message only appears if the **sn\_vad\_genai.com.glide.small\_talk.closure.prompt\_enabled** system property is switched to `False`. Closed conversations eventually move to the Closed chats.


