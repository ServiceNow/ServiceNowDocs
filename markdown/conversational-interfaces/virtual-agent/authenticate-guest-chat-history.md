---
title: Login to transfer guest chat history to an authenticated Virtual Agent session
description: Elevate guest users to an authenticated session by logging in, and without losing chat context or history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/authenticate-guest-chat-history.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Virtual Agent, Guest, Authenticated, Chat history, Elevate, User]
breadcrumb: [Other Virtual Agent features, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Login to transfer guest chat history to an authenticated Virtual Agent session

Elevate guest users to an authenticated session by logging in, and without losing chat context or history.

## Before you begin

Role required: virtual\_agent\_admin or admin

Ensure you've installed the Glide conversation server \(**com.glide.cs**\) plugin.

## About this task

If you change your chat to another portal without logging in, your conversation is reset in the new context. By logging in, you can elevate chat sessions and preserve history and context. The login option is available in Australia, Patch 4, but you must activate the com.glide.cs plugin, and place the login topic block in your topic, to use it in your Virtual Agent chat. You can then use the login feature in Virtual Agent and Live Agent chat sessions, and in Virtual Agent API

The login feature is wrapped in the **Glide Authentication** block, which you must place in a topic. The topic block is then called when an action requires authentication, when you enter an utterance such as **I want to sign in**, or when a live agent sends you a login link.

This topic block is automatically added to your instance as part of the **com.glide.cs** plugin.

When you login during a guest chat, you sign on using your own user credentials. The guest user elevation feature then retrieves all the records from your active guest chats, and updates them to be associated with your logged in user.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  In the Asset library, select **+Create** to create a new topic, or open a topic you've created, where you want to put the login option.

4.  Add the **glide\_authentication** topic block to your topic.

5.  Select **Save**.


## Result

The login control is added to your chat, and a guest user can sign in as an authenticated customer.

## What to do next

When you start a Virtual Agent session, use the login link that appears in the chat window to sign in with your account info, or a single sign-in via OAuth.

\[Omitted image "auth-guest-login-00.png"\] Alt text: Now Assist in Virtual Agent chat windows. The user selects "login to glide" and the Virtual Agent provides a Log in link.

\[Omitted image "auth-guest-login-01.png"\] Alt text: The user enters their login information and any authentication needed.

\[Omitted image "auth-guest-login-02.png"\] Alt text: The user is logged in, and the Virtual Agent chat window transfers the same conversation.

**Note:** Depending on the instance, the buttons may have a different name such as **Sign in**.

**Parent Topic:**[Other Virtual Agent features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/exploring-other-vad-features.md)

