---
title: Components installed with ServiceNow Voice Core
description: Several types of components are installed with activation of the ServiceNow Voice Core application \(sn\_cti\_core\), including user roles, plugins, and operation handlers.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Voice reference, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with ServiceNow Voice Core

Several types of components are installed with activation of the ServiceNow Voice Core application \(sn\_cti\_core\), including user roles, plugins, and operation handlers.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

CTI service account\[sn\_cti\_core.service\]

</td><td>

Allows communication between the third-party phone system instance and the ServiceNow instance.

</td><td>

sn\_openframe\_api\_user

</td></tr><tr><td>

CTI admin\[sn\_cti\_core.admin\]

</td><td>

Creates the framework for integration with a third-party phone system.

</td><td>

None

</td></tr><tr><td>

CTI user manager\[sn\_cti\_core.user\_manager\]

</td><td>

-   Can access the Call Analysis tab and interaction to analyze transcripts, recordings, and sentiments.
-   Can manage the CTI-enabled user PIN.

</td><td>

None

</td></tr></tbody>
</table>## Plugins installed

|Plugin|Description|
|------|-----------|
|Interaction Management \(com.glide.interaction\)|Enables interaction logging, routing, and queueing|
|Openframe \(com.sn\_openframe\)|Provides an interface to integrate a communication frame to place and receive calls.|

## Operation handlers installed

Operation handlers are defined in the ServiceNow instance to run a script based on the intent of the caller and provide response to the caller.

<table id="table_zb5_ldr_2nb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$transcript

</td><td>

Saves the call transcript

</td></tr><tr><td>

$query2ssml

</td><td>

Securely queries tables and returns the response as ssml

</td></tr><tr><td>

workItemEvent

</td><td>

If the Advanced Work Assignment plugin \(com.glide.awa\) is installed, creates a work item on Advanced Work Assignment table before routing the call to agent, and associates an interaction with the work item.**Note:** In a contact flow, invoke this operation handler in the Invoke AWS Lambda Function node just before transferring the flow to a queue

</td></tr><tr><td>

interactionEvent

</td><td>

Defines the life cycle of the an Amazon Web Services \(AWS\) interaction event, such as initiating an interaction and associating an agent and caller to the interaction

</td></tr><tr><td>

authenticate

</td><td>

Authenticates a user based on the PIN. For information on PIN configuration, see [Configuring a phone PIN](../concept/set-pin-ccc.md#).

</td></tr><tr><td>

fetchVoiceInteraction

</td><td>

Fetches interaction and processes createConversation flag for creating conversation.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Voice reference](ccc-reference.md)

