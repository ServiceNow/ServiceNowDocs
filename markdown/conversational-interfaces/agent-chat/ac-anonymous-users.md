---
title: Controlling the browser experience for chat guest sessions
description: Anonymous users \(unauthenticated guests\) can chat with support agents in the web chat client, without logging in to a service portal. Admins can control certain aspects of the conversational experience for unauthenticated guest users, such as enabling resumable chat sessions after a browser refresh.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Agent Chat, Conversational Interfaces]
---

# Controlling the browser experience for chat guest sessions

Anonymous users \(unauthenticated guests\) can chat with support agents in the web chat client, without logging in to a service portal. Admins can control certain aspects of the conversational experience for unauthenticated guest users, such as enabling resumable chat sessions after a browser refresh.

When guest users refresh the browser window while chatting with an agent, the refresh automatically starts a new conversation and chat session. By default, the ongoing conversation and chat session history are not retained.

You can change the default guest session behavior to let your guest users resume an ongoing conversation and see the chat session history after a browser refresh. You can also set the duration of the guest chat session user cookie, to let guest users resume chat sessions after they close and reopen their browser.

## Enable resumable guest sessions

As admin, use the **com.glide.cs.guest\_session\_resumable** system property to the change the default chat guest session behavior for guest users.

1.  Navigate to **All**, and in the Filter enter `sys_properties.list`.
2.  Open the **com.glide.cs.guest\_session\_resumable** property.
3.  In the **Value** field, enter `true` to enable resumable guest chat sessions and retain the chat session history.
4.  Select **Update**.

After a browser refresh, your guest users can continue their conversations with agents and see the chat session history in the chat panel.

## Change the guest chat session cookie time

The guest chat session cookie time is the length of time \(duration\), in seconds, of the guest session user cookie. Use the **com.glide.cs.guest\_session\_cookie\_max\_age** property to change the guest session cookie time, in case your guest users want to resume a chat after closing and reopening their browser.

For security reasons, the default property value is -1, which means the guest session cookie is immediately deleted when the browser is closed. But you can specify a maximum time length that sets the duration of the guest session cookie, for example 900 seconds \(15 minutes\).

1.  As admin, navigate to **All**, and in the Filter enter `sys_properties.list`.
2.  Open the **com.glide.cs.guest\_session\_cookie\_max\_age** property.
3.  In the **Value** field, enter the maximum length of time \(seconds\) for the guest session cookie.

    For example, the value `900` is the duration of the guest session cookie in seconds \(15 minutes\), to give your guest users time to resume a chat session after closing and reopening the browser.

4.  Select **Update**.

**Parent Topic:**[Configuring Agent Chat](ci-agent-chat-configuring.md)

