---
title: Follow a record in Connect
description: You can follow a record in Connect Chat to track activity as it happens, in a familiar chat interface. When you follow a record, you become a member of a record conversation.
locale: en-US
release: xanadu
product: Connect
classification: connect
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Connect Chat use, Connect Chat, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Follow a record in Connect

You can follow a record in Connect Chat to track activity as it happens, in a familiar chat interface. When you follow a record, you become a member of a record conversation.

## Before you begin

**Important:**

Core UI is required to use Connect Chat. Connect Chat is not supported in Next Experience. If you turn on Next Experience, Connect Chat will no longer work. See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for more information.

Role required: whichever role is required to access the record you want to follow in Connect

## About this task

You must first activate the Connect \(com.glide.connect\) plugin to complete this task.

Any record conversation you create in Connect becomes a record feed in Live Feed, and vice versa. Unlike direct or group conversations, all messages in record conversations are comments or work notes.

**Note:** By default, record conversations are enabled for all tables that extend Task \[task\]. Administrators can enable record conversations for additional tables or disable them if desired.

## Procedure

1.  Navigate to a task record.

2.  Do one of the following actions.

<table id="choicetable_dbk_2s2_wt"><tbody><tr><td id="d401596e94">

**Follow the record**

</td><td>

In the form header, click **Follow**.

 The system adds you as a member of the record conversation, but does not open the conversation. You can open the conversation from the Connect sidebar.

</td></tr><tr><td id="d401596e112">

**Follow the record and open a chat mini window**

</td><td>

1.  In the form header, click the down arrow in the **Follow** button.
2.  Select **Open Connect Mini**.
 The system adds you as a member of the record conversation and opens it in a Connect mini window.

</td></tr><tr><td id="d401596e139">

**Follow the record and open the Connect workspace**

</td><td>

1.  In the form header, click the down arrow in the **Follow** button.
2.  Select **Open Connect Full**.
 The system adds you as a member of the record conversation and opens it in the Connect workspace, the full-screen view.

</td></tr></tbody>
</table>    The **Follow** button is relabeled **Following**.

3.  Add comments or work notes to the record directly from Connect.

    Any comments or work notes added to the record appear in the record conversation. Likewise, comments and work notes you add to the conversation appear on the record.

    1.  In the record conversation, by the text entry field, click the message type icon \(![Message type icon](../image/IconMessageType.png)\).

    2.  Select **Comment** or **Work Note**.

    3.  Enter a message.

    By default, record conversation messages are added as work notes.

    **Note:** If you add an attachment to a record conversation, it is attached to the underlying record as well.


## What to do next

[Edit your notification settings](t_EditNotifRecAConv.md) for the record conversation.

**Related topics**  


[Live Feed Core UI](../../live-feed/concept/c_GetStartedWithLiveFeed.md)

