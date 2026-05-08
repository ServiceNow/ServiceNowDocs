---
title: Working with the CTI using the OpenFrame window
description: Use the OpenFrame window to make a call, answer a call, transfer a call, or set status.Use the OpenFrame window to answer an incoming call.Use the OpenFrame window to make an outgoing call.After accepting an incoming call, a customer service agent can transfer a call to another agent.Customer service agents can set their current call status.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CTI demo implementation, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Working with the CTI using the OpenFrame window

Use the OpenFrame window to make a call, answer a call, transfer a call, or set status.

## Answer an incoming call

Use the OpenFrame window to answer an incoming call.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_open\_frame, or admin

### About this task

The OpenFrame window displays the incoming call, including the phone number and the customer contact or consumer information.

### Procedure

1.  Click **Accept**.

2.  When the call is finished, click **End**.


## Make an outgoing call

Use the OpenFrame window to make an outgoing call.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_open\_frame, or admin

### Procedure

1.  Select one of the following options.

<table id="choicetable_jqk_nzc_bx"><tbody><tr><td id="d161294e169">

**Click the phone icon in the banner frame.**

</td><td>

Enter the phone number in the **Number** field and click **Call**.

</td></tr><tr><td id="d161294e184">

**Click the phone icon next to the __Contact__ or __Consumer__ fields on the Case form.**

</td><td>

Customer contacts and consumers can have multiple phone numbers. -   If only one phone field is populated, a call is placed to that number.
-   If more than one phone field is populated, a dialog box displays the available numbers. Click the desired number to place the call and close the dialog box.


</td></tr></tbody>
</table>2.  When finished with the call, click **End**.


## Transfer a call

After accepting an incoming call, a customer service agent can transfer a call to another agent.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_open\_frame, or admin

### Procedure

1.  Answer an incoming call.

2.  Click **Transfer**.

3.  Select an agent from the drop-down list.

4.  Click **Call**.


## Set agent call status

Customer service agents can set their current call status.

### Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_open\_frame, or admin

### Procedure

1.  Click the phone icon in the banner frame.

2.  Select your availability.

<table id="choicetable_dsw_qcw_ht"><tbody><tr><td id="d161294e363">

**Available**

</td><td>

The agent is available to take a call.

</td></tr><tr><td id="d161294e372">

**Not Available**

</td><td>

The agent is not available to take a call.

</td></tr><tr><td id="d161294e381">

**Busy**

</td><td>

The agent is currently on a call with a customer.

</td></tr><tr><td id="d161294e390">

**Wrap Up**

</td><td>

The agent is updating case information after completing a call. After completing a call and the subsequent wrap up, an agent must manually change the status from **Wrap Up** to **Available**.

</td></tr></tbody>
</table>    The **Presence** field in the **OpenFrame** &gt; **OpenFrame Agent Presence** record is updated with the availability status set for the agent.


