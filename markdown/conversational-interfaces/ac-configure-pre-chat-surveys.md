---
title: Define pre-chat survey configurations
description: Use pre-chat surveys to capture preliminary information from a customer. You can define a configuration that determines the pre-chat survey to be presented to your customers. From the responses received, Advanced Work Assignment routes chat conversations to appropriate queues and groups.
locale: en-US
release: zurich
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Define pre-chat survey configurations

Use pre-chat surveys to capture preliminary information from a customer. You can define a configuration that determines the pre-chat survey to be presented to your customers. From the responses received, Advanced Work Assignment routes chat conversations to appropriate queues and groups.

## Before you begin

[Create the chat survey](create-chat-surveys.md) to be used in this pre-chat survey configuration.

Role required: admin

## About this task

Apply the conditions that determine the pre-chat questionnaire to be presented to your requesters.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under **Pre-chat surveys** on the **General** tab, select **View all**.

3.  On the Chat Surveys page, select **New** to create a new chat survey configuration or select the configuration you want to update.

4.  Under **Details**, enter or change the settings.

<table id="table_rqd_md4_ndb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for this pre-chat survey configuration.

</td></tr><tr><td>

Active

</td><td>

Option that activates this pre-chat survey configuration.

</td></tr><tr><td>

Show Summary

</td><td>

Option that asks requesters if they want to see a summary of the survey responses they entered.

</td></tr><tr><td>

Order

</td><td>

Number that indicates the order in which survey configurations run. If there are multiple pre-chat survey configurations, the system runs the first survey configuration found, from lowest to highest order.

</td></tr><tr><td>

Condition mode

</td><td>

Type of condition to be used to control the conversational survey presented to requesters.-   **Advanced**: Specify a JavaScript scripted condition.
-   **Simple**: Specify a condition using the condition builder.


</td></tr><tr><td>

Condition

</td><td>

Condition that controls when the survey configuration is used. Select **Set Condition** to specify the conditions.

</td></tr><tr><td>

Survey

</td><td>

List of the pre-chat surveys available. Choose the survey to be presented to the requester.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

When a requester completes the pre-chat survey, the user is transferred either to a live agent if Agent Chat is set as the fulfiller interface or a virtual agent if Virtual Agent is set as the fulfiller. The user's pre-chat responses are stored as context in the chat interaction record. Before entering into a chat conversation, the assigned agent can review the context of the issue.

**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

