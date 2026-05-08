---
title: Manage a CCaaS callback request in the Configurable Workspace
description: As a customer service agent, view the callback context information and dial the customer immediately in the CSM/FSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Customer communication, Use, Customer Service Management]
---

# Manage a CCaaS callback request in the Configurable Workspace

As a customer service agent, view the callback context information and dial the customer immediately in the CSM/FSM Configurable Workspace.

## Before you begin

Role required: sn\_customerservice\_agent

You must log in to your CCaaS account and ServiceNow Configurable Workspace to receive the callback requests on the Configurable Workspace.

## About this task

The callback interaction is either routed in the customer-first or agent-first method by CCaaS to the agent. The interaction appears like any other voice interaction in a customer-first scenario. The interaction appears with callback actions component and callback context card for an agent-first scenario. For more information on the agent-first and customer-first modes, see [Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](../concept/interaction-controls-component-icc-callback-integration-features.md). The following procedure is applicable for the agent-first scenario.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

    **Note:** The AWA inbox card displays the following information for callbacks:

    -   Name of the customer
    -   Queue to which the callback is assigned
    -   Type of callback \(ASAP and Scheduled\)
    -   Reason for callback
2.  Perform one of the following in your inbox when you receive a callback interaction request.

<table><thead><tr><th align="left" id="d257693e117">

Action

</th><th align="left" id="d257693e120">

Description

</th></tr></thead><tbody><tr><td id="d257693e126">

**Accept**

</td><td>

Select this button to accept the callback interaction request.The voice interaction page opens with the Callback Actions component on the top-left corner of the page. For more details on the callback actions component, see [Callback actions component](../concept/csm-native-voice-record-page.md#section-ccaas-callback-actions).

</td></tr><tr><td id="d257693e141">

**Reject**

</td><td>

Select this button to reject the callback interaction request.The callback interaction gets routed to the next available agent.

</td></tr></tbody>
</table>3.  View the Callback context card for the details of the callback.

    For more information on the Callback context card, see [Callback context card](../concept/csm-native-voice-record-page.md#section-callback-context).

4.  Use the callback actions card to perform the following actions.

<table id="table_ecd_ccz_1gc"><thead><tr><th>

Conversation scenarios

</th><th>

Actions

</th></tr></thead><tbody><tr><td>

Talk to the customer and try to address the customer issue

</td><td>

1.  Select the **Call number** button on the Callback actions component.

**Note:** When the timer turns down to zero on the Callback actions component, the call is automatically dialed to the number in the drop-down. The timer must be enabled by the contact center provider for auto-dialing capability.

If you get to know that the issue is resolved and the callback isn’t required, you can select **Close Callback** and wrap up the interaction. Subsequently, the callback task is closed by CCaaS.

2.  If the customer answers the call, resolve the customer's issue.


</td></tr><tr><td>

Transfer the callback before dialing the call when it falls outside the agent's scope of responsibility to ensure that it reaches the appropriate agent or queue for resolution.

</td><td>

1.  Select the **Transfer callback** button on the Callback actions component to transfer an ASAP or Scheduled callback to another queue or agent before the call to the customer begins.

When you select the Transfer callback button, the Transfer callback subcomponent appears, which includes the following options:

    -   In the search field, select from the list or to transfer the callback.
    -   In the Queues list, select the queue for transfer to which you want to transfer the callback.
    -   In the Agents list, select the agent to whom you want to transfer the callback.
2.  Select the ![Transfer callback arrow](../image/Transfer_queue_arrow.png) icon to initiate the transfer callback. When transferring a callback, the Callback actions component displays a Transferring callback, please wait... message and a 'Cancel callback transfer' button.
3.  Select the **Cancel callback transfer** button to cancel the transfer before the receiving agent accepts the request. For more details on how it’s displayed in the UI, see [CSM voice interaction record page](../concept/csm-native-voice-record-page.md).


</td></tr><tr><td>

Retry callback in case the customer doesn’t answer the call

</td><td>

1.  Select the **Retry call** button on the Callback actions component.
2.  If a customer answers the call, address the customer request.


</td></tr><tr><td id="entry-transfer-call">

Transfer the call when another agent is better equipped to assist the customer

</td><td>

1.  Select the transfer icon on the active call component. The call with the customer is placed on hold while you transfer the call to another agent.
2.  In the Agents list, select the agent to whom you want to transfer the call to.
3.  Select the three dot menu and perform one of the following:
    -   Select **Consult** to talk to the agent and provide the context of the callback request.

Once the new agent accepts the call, you can select **Merge calls** to merge your current customer call with the new agent or select **Leave &amp; transfer** to disconnect the call with the customer and transfer it to the new agent directly.

    -   Select **Blind** to transfer the call directly to the agent without any consultation. The call gets transferred to the agent directly, and you get disconnected from the call.
 Upon successful transfer of call to another agent, the callback interaction is assigned to the receiving agent. The callback task remains assigned to the original agent and can be wrapped up.

</td></tr></tbody>
</table>5.  Mute, hold, and record the calls if necessary while you are on an active call with the customer.

    ![Actions you can perform on an active conversation.](../image/ccaas-callback-call-actions.png)

    The following table provides a description for the annotations in the preceding image:

    |Annotation in the preceding image|Description|
    |---------------------------------|-----------|
    |1|Use the record icon to record the conversation. The recording is saved automatically when you end the conversation.|
    |2|Use the mute icon to mute or unmute the conversation.|
    |3|Use the hold icon to hold or resume the conversation.|
    |4|Use the dialpad to enter a phone number of your choice and press the dial button to make a call.|
    |5|To transfer the call to another agent, select the transfer icon. For more details, see [ccaas-address-callback-requests.md\#entry-transfer-call](ccaas-address-callback-requests.md#entry-transfer-call).|
    |6|Use the flag icon to escalate customer issue.|

6.  Update the **Reason** and **Notes** appropriately and select **Submit &amp; close** in the Wrap up modal after ending the call.

    After submitting wrap up, CCaas closes the interaction and callback task.

7.  Select **Close callback** on the Callback Action component to close the callback.

    In the automatic dial, the callback gets closed when the timer for closing the callback goes down to zero.

8.  Close the interaction page.


**Related topics**  


[Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](../concept/interaction-controls-component-icc-callback-integration-features.md)

[Callback interaction features](../concept/contact-center-intergration-with-icc-callback.md)

[Manage a CCaaS callback request using Global Voice Control](handle-ccaas-callback-gvc.md)

