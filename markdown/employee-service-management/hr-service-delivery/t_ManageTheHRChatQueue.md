---
title: Manage the HR chat queue
description: You can configure the HR department chat queue and review the chat records to measure how well employees are being assisted when they initiate a conversation.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [HR chat from lists and forms, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Manage the HR chat queue

You can configure the HR department chat queue and review the chat records to measure how well employees are being assisted when they initiate a conversation.

## Before you begin

To use the HR chat queue, the administrator must activate the Advanced Work Assignment \[com.glide.awa\] and Agent Chat \[com.glide.interaction.awa\] plugins.

Role required: admin or hr\_admin

## About this task

You can configure the assignment group for monitoring the chat queue and the messages that employees see when they initiate a conversation and while they are waiting.

You can review the chat records to see how long employees waited for a response and who is accepting the chat requests.

## Procedure

1.  Navigate to **All** &gt; **Collaborate** &gt; **Connect Support** &gt; **Support Administration** &gt; **Queues**.

2.  Select **HR Department Chat Queue** from the Chat Queues list.

3.  Fill in the fields, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the queue.|
    |Active|Not used in Connect.|
    |Assignment group|User group that contains the support staff for the queue. Any user in the group can view the queue in the Connect sidebar and accept chats. No other users can access the queue. This field must be populated.|
    |Average wait time|Average time it takes for an agent to accept a chat in the queue. This value is automatically calculated. Do not manually edit.|
    |Confirm problem|Not used in Connect.|
    |Escalate to|Different queue to which an agent can escalate a chat. For example, there is a queue for high priority support chats. When a queue is defined in this field, agents can access the **Escalate** option in conversations.|
    |Initial agent response|Message that users see when an agent accepts their chat. For example, **Thank you for contacting support. We are looking into your question now and will be with you shortly.**|
    |Not available|Message that users see when they attempt to start a chat outside the defined queue **Schedule**. You can use HTML to format the message and include links or media.|
    |Question|Initial phrase that users see when they start a new chat in the queue. For example, **How can I help you?**|
    |Schedule|Schedule that defines when the queue is available. Leave the field blank to make the queue available all the time. Users cannot start a new conversation in the queue outside the schedule hours.|

4.  To review conversations associated with the queue, add the **Chat Queue Entries** related list and review the records for the following information.

    |Type of data|Description|
    |------------|-----------|
    |**How long the user waited and the result**|Review information in the **State** and **Wait time** columns.|
    |**Who is actively helping employees in the queue**|Review the names of agents in the **Assigned to** column.|


**Parent Topic:**[HR chat from lists and forms](../concept/chat-with-scoped-hr.md)

