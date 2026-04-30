---
title: Using Voice
description: Agents can use ServiceNow Voice to receive inbound calls and make outbound calls with a seamless voice call experience. Managers can use this application to monitor and analyze calls.An agent can receive inbound calls using the Agent Softphone interface to handle a caller's request.Improve your productivity as an agent by initiating outbound calls to connect with customers using the click-to-call feature in the ServiceNow Voice application.When on a call with a customer, an agent can transfer the call to another agent or to a queue to get more assistance for the customer.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using Voice

Agents can use ServiceNow Voice to receive inbound calls and make outbound calls with a seamless voice call experience. Managers can use this application to monitor and analyze calls.

**Parent Topic:**[ServiceNow Voice](cloud-call-center-overview.md)

## Receiving inbound calls in ServiceNow Voice

An agent can receive inbound calls using the Agent Softphone interface to handle a caller's request.

As an agent, you should have any of the following roles to receive an inbound call:

-   sn\_openframe.user and interaction\_agent
-   If the Advanced Work Assignment plugin \(com.glide.awa\) is installed, awa\_agent &amp; awa\_integration\_user.

After a customer dials in, the corresponding contact flow is invoked in Amazon Connect. Through the configured nodes, the request is forwarded to an operation handler in the ServiceNow instance.

If an agent is available, the agent can receive the call and handle the request using Agent Softphone interface. For information about the presence states of an agent, see [Agent Inbox controls](../../../administer/advanced-work-assignment/concept/agent-experience.md).

|If|Then the interaction|
|---|--------------------|
|The interaction has just been created, is currently in a call tree being deflected by an IVR flow, or has not yet been routed and assigned to an agent|Is in **New** state.|
|The Lex Bot deflects the call or the user disconnects the call any time before the call enters the queue|Moves to **Closed Complete** state.|
|The interaction gets assigned to an agent|Moves to **Work in Progress** state.|
|The user disconnects the call while waiting in the queue|Moves to **Closed Abandoned** state.|

## Initiating outbound calls with ServiceNow Voice

Improve your productivity as an agent by initiating outbound calls to connect with customers using the click-to-call feature in the ServiceNow Voice application.

As an agent, you can initiate outbound calls using the click-to-call feature when accessing the phone number of a user. The phone number of a user, if available, is displayed on the ServiceNow application UIs. Example application UIs include the contact details on a Case form, the user record on an Incident form, the Consumer form, the Contact form, and other application UIs.

**Note:**

-   If not available, you can add the **Caller** field to an incident form.
-   The phone number of a user should be in the E.164 format. For information about configuring a phone number in this format, see [Configure the E.164 format for a consumer phone number](../task/configure-e614-consumer.md).

You should have any of the following roles to initiate an outbound call:

-   sn\_openframe.user and interaction\_agent
-   If the Advanced Work Assignment plugin \(com.glide.awa\) is installed, awa\_agent &amp; awa\_integration\_user.

You can click the link to the user's phone number displayed on the application UI. The user record must have the mobile phone, business phone, or both. The Agent Softphone pop-up window is displayed letting you know that the call will be recorded, and then the user's number is connected. An interaction record of type Phone is created for the call and is in the **Work in Progress** state.

For ServiceNow Voice Core, if the `createConversation` flag is set to true, a conversation record is created for an outgoing call.

For ServiceNow Voice with Customer Service Management, if the `sn_cti_csm_cnt.enable_ims_update` flag is set to true, a conversation record is created for an outgoing call.

The following agent presence states are configured by default for the Voice application and are displayed in your Agent Workspace Inbox.

<table id="table_iwl_fqb_ymb"><thead><tr><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CallingCustomer

</td><td>

Indicates that you are in the process of connecting with a customer. After the call is connected, the status appears as **Busy**.

</td></tr><tr><td>

Busy

</td><td>

Indicates that you are on the call.

</td></tr><tr><td>

AfterCallWork

</td><td>

Indicates that you ended the call and right now working on updating the task such as case details. The status is displayed after you click **End call** in the Agent Softphone pop-up window.

</td></tr><tr><td>

Available

</td><td>

Indicates that you are available to accept another task such as a case. The status is displayed after you click **Clear contact** in the Agent Softphone pop-up window.

</td></tr><tr><td>

FailedConnectAgent

</td><td>

Indicates that you were unable to connect with the customer. After the call doesn't go through, the status appears as **Available**.

</td></tr></tbody>
</table>**Note:** The Agent Workspace Inbox statuses are synchronized with your Advanced Work Assignment \(AWA\) activity.

The activity stream of the associated interaction record is populated with your status details, the URL to the call recording, contact trace record, and call transcript.

## Transferring a call to an agent or queue

When on a call with a customer, an agent can transfer the call to another agent or to a queue to get more assistance for the customer.

This feature is available for ServiceNow Voice for Customer Service Management. See [Integrating ServiceNow Voice with CSM](integrating-ccc-csm.md) for more information.

![Transfer a call to another agent or to a queue. The customer is Amy, the first agent is Ned, and the second agent is Beth.](../image/transfer-workflow.png "Example of a transfer flow")

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **CSM/FSM Configurable Workspace**.
2.  Ned uses the Agent Softphone to accept an incoming call from a customer.
3.  To transfer the call, Ned clicks **Quick connects** and choose either another agent or a queue \(for example "Billing queue"\). The transfer begins, and **INTERNAL-TRANSFER** displays on the softphone. The customer is placed on hold until the next agent accepts the call.
4.  Once the next agent \(Beth\) selects **Join**, and joins the call, the first agent \(Ned\) can either remain on the call or leave the call.
5.  When the Ned leaves the call, the call is reassigned to the Beth on the interaction record.

