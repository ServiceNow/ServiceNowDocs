---
title: Add a scripted extension point for Connect Support chats
description: Implement the ConversationServerInteractionService extension point, which enables you to create custom scripts that use context variables from pre-chat surveys presented to requesters in the Agent Chat client.
locale: en-US
release: xanadu
product: Connect
classification: connect
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Connect Support administration, Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add a scripted extension point for Connect Support chats

Implement the ConversationServerInteractionService extension point, which enables you to create custom scripts that use context variables from pre-chat surveys presented to requesters in the Agent Chat client.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points** and select the ConversationServerInteractionService scripted extension point.

2.  Click the **Create implementation** related link to create a new custom script include.

3.  In the Script Include form, create the code that uses the pre-chat context variables to route chats to the appropriate Connect Support queue.

4.  Click **Update**.


## Result

The custom script is created and registered against the ConversationServerInteractionService scripted extension point.

