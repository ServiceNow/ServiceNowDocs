---
title: Manage a CCaaS callback request using Global Voice Control
description: As a customer service agent, when you leave the callback interaction page on the CSM/FSM Configurable Workspace during a call, you can use Global Voice Control \(GVC\) to continue with callback actions. You can return to the interaction page by selecting the Open interaction link.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CCaaS callback requests in the Configurable Workspace, Customer communication, Use, Customer Service Management]
---

# Manage a CCaaS callback request using Global Voice Control

As a customer service agent, when you leave the callback interaction page on the CSM/FSM Configurable Workspace during a call, you can use Global Voice Control \(GVC\) to continue with callback actions. You can return to the interaction page by selecting the **Open interaction** link.

## Before you begin

Role required: sn\_customerservice\_agent

You must log in to your CCaaS account and CSM/FSM Configurable Workspace to receive the callback requests on the CSM Configurable Workspace.

## About this task

The callback interaction is either routed in the customer-first or agent-first method by contact center providers to the agent. In the customer-first scenario, the interaction appears like any other voice interaction. In the agent-first scenario, the interaction appears with a callback actions component and callback context card. For more information on the agent-first and customer-first modes, see [Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](../concept/interaction-controls-component-icc-callback-integration-features.md). The following procedure is applicable for the agent-first scenario.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

    **Note:** The AWA inbox card displays the following information for callbacks:

    -   Name of the customer
    -   Queue to which the callback is assigned
    -   Type of callback \(ASAP or Scheduled\)
    -   Reason for callback
2.  Perform one of the following in your inbox when you receive a callback interaction request.

<table id="choicetable_xrb_1lf_cgc"><thead><tr><th align="left" id="d158711e120">

Action

</th><th align="left" id="d158711e123">

Description

</th></tr></thead><tbody><tr><td id="d158711e129">

**Accept**

</td><td>

Select this button to accept the callback interaction request.The voice interaction page opens with the Callback Actions component on the top-left corner of the page. For more details on the callback actions component, see [Callback actions component](../concept/csm-native-voice-record-page.md#section-ccaas-callback-actions).

</td></tr><tr><td id="d158711e144">

**Reject**

</td><td>

Select this button to reject the callback interaction request.The callback interaction gets routed to the next available agent.

</td></tr></tbody>
</table>3.  View the Callback context card for the details of the callback who requested a callback.

    For more information on the Callback context card, see [Callback context card](../concept/csm-native-voice-record-page.md#section-callback-context).

4.  Select the GVC icon on the unified navigation bar to perform call-related actions when you are on other pages.

    You might have to open a knowledge article or case to address a customer request. While on a different page, you need not come back to the interaction page to control the call. Instead, you can use the GVC to control the call.

    You can use the callback actions such as Call number, Close Callback, Retry call, and so on, on the GVC in the same way as you use them on the Callback Actions component. For more information on how to use the callback actions component for callback interactions, see [Manage a CCaaS callback request in the Configurable Workspace](ccaas-address-callback-requests.md).

    **Note:** The Transfer function isn't supported in GVC.

5.  Select the **Open interaction** link on GVC to open the callback interaction record.

6.  Update the **Reason** and **Notes** appropriately and select **Submit &amp; close** in the Wrap up modal after ending the call.

    After submitting wrap up, CCaas closes the interaction and callback task.

7.  Select **Close callback** on the Callback Action component to close the callback.

    In the automatic dial, the callback gets closed when the timer for closing the callback reaches zero.

8.  Close the callback interaction page.


