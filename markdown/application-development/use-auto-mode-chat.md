---
title: Use auto mode in an Arc chat
description: Switch a chat to auto mode so a safety check approves lower risk actions for you, and set the mode that new chats start in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/use-auto-mode-chat.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [auto mode, approval mode, Standard, Auto, safety check]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Use auto mode in an Arc chat

Switch a chat to auto mode so a safety check approves lower risk actions for you, and set the mode that new chats start in.

## Before you begin

Your administrator has made auto mode available. For more information, see [Make auto mode available to Arc users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/make-auto-mode-available.md).

Role required: sn\_app\_arc.user

## About this task

In **Standard** mode, Arc asks you before actions that need approval. In **Auto** mode, a safety check decides these actions for you, and anything it blocks or can't check comes to you as an approval card. Actions that a policy denies or places under a hard gate, connector capabilities set to **Ask me first**, and sandbox rules work the same in both modes. If the safety check isn't available, Arc shows the approval card.

The safety check is an AI model, and its decisions may be inaccurate or inappropriate.

When your organization first makes auto mode available, a notice above the message box says **Your organization turned on auto mode**. Select **Try Auto** to switch the current chat, or **Not now** to close the notice.

## Procedure

1.  In the message box, select the approval mode picker next to the model picker, which shows the current mode, such as **Standard**, and then select **Auto**.

    If **Auto** isn't available, your organization hasn't turned on auto mode for you. The menu shows **Auto mode isn't enabled by your organization**.

    The picker changes only the current chat, and the chat keeps its mode when you return to it.

2.  Describe what you need, and then select the send icon.

    Steps that the safety check approves show **Auto-mode allowed this**.

3.  To set the mode that new chats start in, navigate to **Settings** &gt; **Approvals**, and select a **Default approval mode**.

    The default is **Standard**. Background runs, such as scheduled tasks, also start in the default mode.

    When auto mode is available, you can also open this setting from the approval mode picker by selecting **Change default**.


## Result

The chat runs in the mode you selected. Your choice applies wherever you use Arc. If your organization turns off auto mode, your chats return to **Standard**.

**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

