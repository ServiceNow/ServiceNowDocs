---
title: Agent initiated SMS conversation
description: Customer Service Management supports additional messaging channel such as SMS which tracks interactions between the agent and customer.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Agent initiated SMS conversation

Customer Service Management supports additional messaging channel such as SMS which tracks interactions between the agent and customer.

## Requirements

At least one provider configuration for messaging type channel must be available to view the **Compose SMS** option in the agent interaction screen. For more information about provider sys\_cs\_provider\_application.list, see [Create a channel identifier](https://www.servicenow.com/docs/access?context=create-adapter-for-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

## Phone number validation

REST endpoint `/api/now/initiate_message/validate_phone_number` is used to validate if the phone number is in the E.164 format. If the number of a known consumer is not in the E.164 format, the system converts it to the E.164 format based on for example, the location of the consumer. If the location is not found, it will by default convert the number to an E.164 format. For more information about E.164 formats and validation, see [Phone number field type](https://www.servicenow.com/docs/access?context=c_UsePhoneNumberFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Customer profile validation

REST endpoint `/api/now/initiate_message/validate_profile` is used to validate the channel user profile. When you send an SMS in reply to an interaction of type phone, the message is sent to a consumer originally associated with the interaction. If the same phone number is associated to a different consumer, and you send an SMS, you will get a message that the phone number is currently associated to another consumer and sending the new message will associate the phone number to the current user.

A phone number is associated to consumer A and an interaction has occurred after which the phone number was disconnected for consumer A. There is a new interaction with consumer B and you select the same phone number that was associated with consumer A. A message appears that the phone number is currently associated to consumer A, and sending a new message will associate consumer A's phone number to consumer B who is the current user.

## Agent initiated SMS conversations

To initiate an SMS conversation with a requester, agents can select a provider number for an outbound service or manually enter a provider number. If there is a current ongoing SMS conversation, it automatically appears. When an agent initiates an SMS conversation:

<table id="table_agent_intiated_sms"><thead><tr><th>

If

</th><th>

Then

</th></tr></thead><tbody><tr><td>

There is no active SMS interaction​

</td><td>

-   Create a new SMS interaction​
-   Assign interaction to agent​

</td></tr><tr><td>

There is an active interaction involving an agent​

</td><td>

-   Inject the message into existing conversation​
-   Add agent to live group profile​
-   No reassignment​

</td></tr><tr><td>

There is an active interaction involving VA​

</td><td>

-   Close existing interaction​
-   Create a new interaction and assign to agent​

</td></tr><tr><td>

There is an active interaction involving a different contact/consumer/user​

</td><td>

-   Close existing interaction​
-   Create a new channel user profile and deactivate the existing channel user profile​
-   Create a new interaction and assign to agent​

</td></tr></tbody>
</table>## Customize the behaviour of send from and to numbers

The AgentInitiatedConversationUtil extension point is added to implement a customers' logic to change the default behaviour of the **Send from** and **Send to** fields. For more information, see [Associating user profiles on messaging interactions](https://www.servicenow.com/docs/access?context=associate-user-profiles-messaging-interactions&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US). For this store application, AgentInitiatedMessagingUtilExtPointImpl extension point is configured for fetching the from and to numbers.

**Parent Topic:**[Using Advanced Work Assignment](using-awa.md)

**Related topics**  


[Check for an agent's presence and capacity](../task/awa-agent-presence.md)

[Check unassigned interactions](../task/awa-unassigned-interactions.md)

[Check unassigned task work items](../task/awa-unassigned-task-work-items.md)

[Check work items and AWA events](../task/awa-work-items-all.md)

[Compose an SMS conversation](../task/compose-sms-store-app.md)

