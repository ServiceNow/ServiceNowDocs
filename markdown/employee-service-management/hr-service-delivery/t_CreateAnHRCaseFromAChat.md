---
title: Create an HR case from a chat
description: If an HR chat results in the need to open a case, create the case directly from the conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/t\_CreateAnHRCaseFromAChat.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [HR chat from lists and forms, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an HR case from a chat

If an HR chat results in the need to open a case, create the case directly from the conversation.

## Before you begin

Role required: sn\_hr\_core.basic or sn\_hr\_core.case\_writer.

**Note:** Connect Support has been deprecated and is no longer supported or available for new activation. For similar capabilities, please move to Advanced Work Assignment and Agent Chat. For details, see Move from Connect Support to Advanced Work Assignment and Agent Chat.

## About this task

When you create an HR case from a support conversation, the system copies the conversation history to the case activity stream as comments and work notes. Future messages are tracked in the case as well.

## Procedure

1.  Navigate to **All** &gt; **Connect** &gt; **Connect Support**.

    The Connect workspace opens in a new tab.

2.  Click the support tab of the Connect sidebar, indicated by a headset icon \(\[Omitted image "IconSupport.png"\] Alt text: Support icon\).

3.  Under **Cases**, open an HR conversation.

4.  At the bottom of the conversation, click the menu icon \(\[Omitted image "IconMenu.png"\] Alt text: Menu icon\) to open the Connect actions menu.

5.  In the Connect actions menu, select **Create HR Case**.

    A new case form opens in a record tab. The system automatically sets certain fields based on conversation details.

6.  Complete the form as necessary and click **Submit**.

    Any comments or work notes in the record conversation appear as comments on the incident form. Work notes do not appear in the chat for the ESS user. The chat agent can select whether a message is a Comment or Work Note in the conversation.

    1.  In the record conversation, by the text entry field, click the message type icon \(\[Omitted image "IconMessageType.png"\] Alt text: Message type icon.\).

    2.  Select **Comment** or **Work Note**.

    3.  Enter a message.

    By default, record conversation messages are added as comments.

    **Note:** If you add an attachment to a record conversation, it is attached to the underlying record as well.

    The system automatically shares the record in the conversation, copies the conversation to the record activity stream, and references the record on the Chat Queue Entry \[chat\_queue\_entry\] table. Any new journal fields added to the record do not appear in the chat. The system also changes the document ID for the conversation to reference the incident number instead of the entry in the Chat Queue Entry table.


**Parent Topic:**[HR chat from lists and forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/chat-with-scoped-hr.md)

