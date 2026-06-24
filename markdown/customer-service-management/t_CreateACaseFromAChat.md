---
title: Create a customer service case from a chat
description: If a customer chat results in the need to open a case, create the case directly from the conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/t\_CreateACaseFromAChat.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Create a customer service case from a chat

If a customer chat results in the need to open a case, create the case directly from the conversation.

## Before you begin

Role required: sn\_customerservice\_agent or sn\_customerservice\_manager

## About this task

When you create a customer service case from a support conversation, the system copies the conversation history to the case activity stream as comments and work notes. Future messages are tracked in the case as well.

**Important:**

Starting in Utah, Connect Support has been deprecated and is no longer supported or available for new activation. For similar capabilities, please move to Advanced Work Assignment and Agent Chat. For details, see [Move from Connect Support to Advanced Work Assignment and Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/advanced-work-assignment/migrate-from-connect-support.md).

## Procedure

1.  Navigate to **All** &gt; **Connect** &gt; **Connect Support**.

    The Connect workspace opens in a new tab.

2.  Click the support tab of the Connect sidebar, indicated by a headset icon \(\[Omitted image "IconSupport.png"\] Alt text: Support icon\).

3.  Under **Cases**, open a customer service conversation.

4.  At the bottom of the conversation, click the menu icon \(\[Omitted image "IconMenu.png"\] Alt text: Menu icon\) to open the Connect actions menu.

5.  In the Connect actions menu, select **Create Case**.

    The system opens a new case form in a record tab and automatically fills in some fields based on conversation details.

6.  Complete the form as necessary and click **Submit**.

    Any comments or work notes in the record conversation appear as comments on the incident form. Work notes do not appear in the chat for the ESS user. The chat agent can select whether a message is a Comment or Work Note in the conversation.

    1.  In the record conversation, by the text entry field, click the message type icon \(\[Omitted image "IconMessageType.png"\] Alt text: Message type icon.\).

    2.  Select **Comment** or **Work Note**.

    3.  Enter a message.

    By default, record conversation messages are added as comments.

    **Note:** If you add an attachment to a record conversation, it is attached to the underlying record as well.

    The system automatically shares the record in the conversation, copies the conversation to the record activity stream, and references the record on the Chat Queue Entry \[chat\_queue\_entry\] table. Any new journal fields added to the record do not appear in the chat. The system also changes the document ID for the conversation to reference the incident number instead of the entry in the Chat Queue Entry table.


**Related topics**  


[Connect workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/connect/c_CollaborationWorkspace.md)

