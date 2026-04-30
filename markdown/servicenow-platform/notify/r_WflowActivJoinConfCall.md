---
title: Join conference call workflow activity
description: The Join Conference Call activity connects an incoming or outgoing call to a Notify conference call.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Notify workflow activities, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Join conference call workflow activity

The **Join Conference Call** activity connects an incoming or outgoing call to a Notify conference call.

Notify includes the workflows Notify: \(Re\)join Conference Call and Notify: Join Conference Call Via SMS to demonstrate how to use the **join conference call** activity to connect inbound and outbound calls, and inbound SMS messages to a conference call.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|Record|Select this check box to record the conference call.|
|Advanced|Select this check box to display advanced configuration options.|
|Script|Specify advanced configuration options using JavaScript, such as if the new participant should be muted upon joining the conference call. You can access values from the workflow scratchpad.|

## Conditions

The conditions determine which transition comes after this activity. The **join conference call** activity does not specify any conditions by default.

You can add an error condition to this activity. The activity transitions through the error condition if the confernece\_call scratchpad variable is not set.

## Scratchpad entries

The activity uses the workflow scratchpad to read persistent values.

<table id="table_ld2_zsh_3gb"><thead><tr><th>

Scratchpad variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

workflow.scratchpad.conference\_call

</td><td>

A GlideRecord for a single conference call record. A call processed by this activity is added to this conference call. If this value is not specified, the **join conference call** activity will log an error.When initiating an outgoing call workflow using the Notify API call\(String notifyPhoneNumber, String toPhoneNumber, GlideRecord conferenceCall\) method, this scratchpad value is set automatically to the conference call GlideRecord. For incoming call workflows, or workflows initiated using a different mechanism, you must explicitly set this scratchpad value.

</td></tr></tbody>
</table>## Enable different attributes available with Join Conference Call activity

System administrators can enable any or all of the below attributes and use them in the Join Conference Call workflow activity.

|Attribute|Description|
|---------|-----------|
|hangupOnStar|When hangupOnStar is enabled \(set to true\), participants in a conference call can press the \* button to disconnect from the call. Control is returned to the workflow, which can be used to trigger customer-defined actions.|
|muted|When muted is enabled \(set to true\), the participant will join the conference in a muted state.|
|beepOnEnter|When beepOnEnter is enabled \(set to true\), a notification beep is played when a user joins the conference.|
|beepOnExit|When beepOnExit is enabled \(set to true\), a notification beep is played when a user leaves the conference.|
|enableImmediateInput|When enableImmediateInput is enabled \(set to true\), it allows input of a single digit immediately after the conference ends for this user and sets that in workflow.scratchpad.confDigits. This option will be ignored if hangupOnStar is false.|

To enable any of the above attributes, perform the following steps:

1.  Navigate to **Workflow** &gt; **Administration** &gt; **Workflow Versions**.
2.  Open the Notify: \(Re\)join Conference Call workflow.
3.  Click the **Show Workflow** related link.
4.  To modify the workflow, click the WorkFlow Actions icon and click **Checkout**.
5.  Open the Join Conference Call workflow activity.
6.  Enable the **Advanced** check box to display the **Script** field.
7.  Set the **hangupOnStar** attribute to true in the *config* variable in the script. The default setting is false.
8.  Click **Update**.
9.  Click the WorkFlow Actions icon and click **Publish** to save the changes.

Similarly, you can enable the other attributes.

