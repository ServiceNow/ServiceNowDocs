---
title: Configure the customer service chat queue
description: Define the customer service agents, default chat messages, schedule, and escalation path for the customer service chat queue.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chat channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# Configure the customer service chat queue

Define the customer service agents, default chat messages, schedule, and escalation path for the customer service chat queue.

## Before you begin

Role required: admin

## About this task

The Customer Service Management chat communication channel uses the ServiceNow [Connect Support](https://www.servicenow.com/docs/access?context=c_ConnectSupport&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) feature.

## Procedure

1.  Navigate to **All** &gt; **Collaborate** &gt; **Administration** &gt; **Queues**.

2.  Select **Customer Service** from the Chat Queues list.

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

4.  Click **Submit**.


**Related topics**  


[Connect Support](https://www.servicenow.com/docs/access?context=c_ConnectSupport&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

