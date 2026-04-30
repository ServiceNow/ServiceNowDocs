---
title: Conversational SMS service channel
description: Using the Conversational SMS service channel app on the ServiceNow Store, workspace agents can provide support for long-running SMS conversations and conversations that use multiple service channels.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Conversational SMS service channel

Using the Conversational SMS service channel app on the ServiceNow Store, workspace agents can provide support for long-running SMS conversations and conversations that use multiple service channels.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview

Requesters can initiate support conversations through SMS. Since these support conversations can be long-running, workspace agents need the ability to track ongoing conversations while also addressing requesters on other service channels. With the Conversational SMS service channel store app, workspace agents can initiate or continue SMS conversations and also accept SMS work items from the Workspace Inbox. Requesters in SMS conversations see a limited subset of system messages. This minimizes the number of system messages in case the conversation is long-running.

## Messaging profiles

Messaging profiles provide a way to match an incoming phone number to a requester:

<table id="table_fg5_gck_gmb"><thead><tr><th>

If

</th><th>

Then

</th></tr></thead><tbody><tr><td>

New SMS is received from a requester who is associated to a phone number on the User \[sys\_user\] table but has no messaging profile match

</td><td>

-   A messaging profile record is generated to match the number to the User table.
-   An interaction record is associated to the matching User table​.

</td></tr><tr><td>

New message received from a requester who does not have a phone number match in the User table but does have messaging profile match​

</td><td>

-   An interaction record is associated to the matching messaging profile user​.
-   The User table record is not associated to the phone number. The agent can manually verify.

</td></tr><tr><td>

New message received from a requester who does not have a phone number match in the User table or messaging profiles​

</td><td>

-   An interaction record is associated to the guest user \(Virtual agent or live agent can manually verify\)​.
-   A messaging profile record is generated for the phone number but not associated to a user​.

</td></tr><tr><td>

New SMS from a requester that conflicts with an existing User table or messaging profile​

</td><td>

-   An interaction is associated with the messaging profile/user currently associated with the number​.
-   Virtual agent or live agent can verify the user and reassociate the interaction/profile with the correct user​.

</td></tr></tbody>
</table>## Messaging actions

Messaging actions provide a way to trigger actions based on messaging activity on a conversation.

<table id="table_bkl_4ck_gmb"><thead><tr><th>

Messaging action parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event​ 1.  Requester message without agent response​
2.  Agent message without requester response

</td><td>

Sending of a message from a requester or agent starts a timer that can trigger an action

</td></tr><tr><td>

Duration

</td><td>

Time set to trigger an action based on the Event parameter being set​

</td></tr><tr><td>

Filter conditions

</td><td>

Condition needed on the Interaction record for a messaging action to be triggered \(for example, State is "On Hold"\)​

</td></tr><tr><td>

Action

</td><td>

Possible actions include:-   Prompt agent – Sent Workspace notification to agent​
-   Prompt requester – Sent system message in messaging conversation to requester​
-   Reassign – Remove assigned agent from interaction​
-   Set state – Set Interaction state to desired state​

</td></tr></tbody>
</table>## Ongoing conversations

The Agent Inbox displays new SMS messages and agents can locate currently assigned SMS conversations in the **Ongoing** tab. The tab indicator and record highlight indicate when an SMS conversation has a new message​. Unlike chat conversations, SMS conversations can be long-running. Completed SMS conversations do not display in the **Ongoing** tab.

![Active conversation in the Ongoing tab.](../image/ongoing-conversations-example.png)

## Requester initiated SMS conversations

When a requester initiates a support conversation, a virtual agent or a live agent addresses the conversation. Like other service channels, Advanced Work Assignment handles the routing of SMS conversations to live agents. This is how requester-initiated SMS conversations are handled:

<table id="table_mfj_b1k_gmb"><thead><tr><th>

If

</th><th>

Then

</th></tr></thead><tbody><tr><td>

There is no active SMS interaction

</td><td>

-   Create a new SMS interaction
-   Assign the interaction to a virtual agent or a live agent

</td></tr><tr><td>

There is an active interaction involving a live agent

</td><td>

-   Inject the message into an existing conversation
-   Continue with agent in current conversation
-   Track using the same interaction record

</td></tr><tr><td>

There is an active interaction involving a virtual agent

</td><td>

-   Inject the message into existing conversation
-   Continue with existing virtual agent topic
-   Track using the same interaction record

</td></tr></tbody>
</table>An active SMS interaction represents an ongoing conversation between a requester's phone number and a company's phone number.

## Agent initiated SMS conversations

To initiate an SMS conversation with a requester, agents can select a provider number for an outbound service or manually enter a provider number. If there is a current ongoing SMS conversation, it automatically appears. When an agent initiates an SMS conversation:

<table id="table_vp2_ykk_gmb"><thead><tr><th>

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
</table>An active SMS interaction represents an ongoing conversation between a requester’s phone number and a company’s phone number​.

**Parent Topic:**[Exploring Advanced Work Assignment](awa-overview.md)

