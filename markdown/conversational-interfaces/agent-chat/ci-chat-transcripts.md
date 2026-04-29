---
title: Chat transcript downloads for requesters
description: Once a conversation between a requester and a live agent ends, the requester can download a transcript of the conversation.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Agent Chat, Conversational Interfaces]
---

# Chat transcript downloads for requesters

Once a conversation between a requester and a live agent ends, the requester can download a transcript of the conversation.

After a conversation between a requester and a live agent ends, the requester’s chat window displays a **Download** button that enables the requester to download a chat transcript. If the requester clicks the **Download** button, a .txt file is automatically downloaded from the window of the requester’s current web browser. The chat transcript contains only the written text from the conversation; attachments and images from the conversation appear as URLs. Even after the requester starts a new chat session, the **Download** button from the previous session is still available if the requester scrolls up. The chat transcript files are generated at the end of each chat session and multiple chat sessions are not combined into one file.

The requester must be configured for chat transcript downloads for the **Download** button to appear. For information about configuring the download of chat transcripts, see [Setting up Agent Chat](../task/ac-configure-agent-chat.md).

Two types of chat transcripts are generated from the conversation: internal and external.

Internal chat transcripts:

-   Are available only to the agent and chat supervisor.
-   Include any conversations between the requester and virtual agent.
-   Include any conversations between the agent and chat supervisor that occurred through Agent Whisper.
-   Include customer sentiments \(if Agent Chat is configured to display customer sentiments\).

The internal transcript field in the interaction table contains all private and public messages and is populated as soon as the chat is close completed.

External chat transcripts:

-   Are available to the requester.
-   Include only conversations between the requester and the live agent.
-   Do not include pre- or post-chat survey information.

