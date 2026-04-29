---
title: Create a consumer case from a chat
description: If a consumer chat results in the need to open a case, create the case directly from the conversation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Create a consumer case from a chat

If a consumer chat results in the need to open a case, create the case directly from the conversation.

## Before you begin

Role required: sn\_customerservice.consumer\_agent, sn\_customerservice\_manager, or admin

## About this task

When you create a case from a support conversation, the system copies the conversation history to the case activity stream as comments and work notes. Future messages are tracked in the case as well.

## Procedure

1.  Navigate to **All** &gt; **Collaborate** &gt; **Connect Support**.

    The Connect workspace opens in a new tab.

2.  Click the support tab of the Connect sidebar, indicated by a headset icon.

    The support tab displays **Queues** to which you belong. It also displays your open support conversations under **Cases**. When a consumer starts a support conversation or an agent transfers a conversation to a queue, any agent who belongs to the associated queue has the option to accept the conversation. An agent can also request to transfer a conversation directly to you.

3.  Under **Cases**, open a consumer conversation.

4.  At the bottom of the conversation, click the menu icon to open the Connect actions menu.

5.  In the Connect actions menu, select Create Case.

    The system opens a new Case form and fills in some of the fields based on the conversation details. \(For a case created from a consumer chat, the **Consumer** field is filled in and the **Short description** field displays the initial chat request from the consumer.\)

6.  Complete the form as necessary and click **Submit**.

    The system shares the record in the conversation, copies the conversation to the record activity stream, and references the record on the Chat Queue Entry \[chat\_queue\_entry\] table.


