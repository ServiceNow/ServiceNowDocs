---
title: Create a consumer case from an anonymous chat
description: If an anonymous chat results in the need to create a consumer case, create the case directly from the conversation.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Create a consumer case from an anonymous chat

If an anonymous chat results in the need to create a consumer case, create the case directly from the conversation.

## Before you begin

Role required: sn\_customerservice.consumer\_agent, sn\_customerservice\_manager, or admin

## About this task

When you create a case from a support conversation, the system copies the conversation history to the case activity stream as comments and work notes. Future messages are tracked in the case as well.

## Procedure

1.  Respond to an anonymous chat request.

2.  Chat with the user to determine the issue.

3.  At the bottom of the conversation, click the menu icon to open the Connect actions menu.

4.  In the Connect actions menu, select **Create Case for Guest**.

    The system opens a new Case form and fills in some of the fields based on the conversation details. For a case created from a guest user chat, the **Short description** field displays the initial chat request from the user.

5.  Complete the form as necessary and click **Submit**.

    The system automatically shares the record in the conversation, copies the conversation to the record activity stream, and references the record on the Chat Queue Entry \[chat\_queue\_entry\] table.


