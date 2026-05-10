---
title: Controlling idle live chat sessions
description: Configure how active chat sessions are handled by the system when live chats become idle.
locale: en-US
release: australia
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Agent Chat, Conversational Interfaces]
---

# Controlling idle live chat sessions

Configure how active chat sessions are handled by the system when live chats become idle.

By default, the system automatically checks live chat sessions every two minutes through the Idle Chat Timer Task scheduled job to ensure that chat sessions are still active. If the requester does not respond within 180 seconds \(three minutes\) during an active chat session, the session becomes idle. The user receives a reminder message that the conversation is timing out and asks if they are still there. If they don't respond, the system automatically cancels \(times out\) the chat session 360 seconds \(six minutes\) after the requester's last response.

You can change the idle chat reminder message and the default time after which the system displays the reminder message and closes an idle chat.

**Important:**

Idle live chats are not available for Connect Support. Starting with the Paris release, Connect Support no longer receives enhancements or non-priority bug fixes. Consider moving to ServiceNow® Advanced Work Assignment and Agent Chat in workspace to automatically assign chat requests and other work items to agents. For details, see [Move from Connect Support to Advanced Work Assignment and Agent Chat](../../advanced-work-assignment/task/migrate-from-connect-support.md).

## Change the idle chat reminder message

The default idle chat reminder message displayed to requesters is: `The conversation is timing out, are you still there?` Agents receive the message: `User response will indicate if they want to continue the chat.`

You can modify the default message sent to requesters by updating the **com.glide.cs.idle\_chat\_reminder\_message** property.

1.  As admin, navigate to **All**, and then enter `sys_properties.list` in the filter.
2.  Open the **com.glide.cs.idle\_chat\_reminder\_message** property.
3.  In the **Value** field, enter the new reminder message to be displayed.
4.  Select **Update**.

## Change the idle chat timeout values

Add the **com.glide.cs.idle\_chat\_reminder\_timeout** and the **com.glide.cs.idle\_chat\_cancel\_timeout** properties to the System Property \[sys\_properties\] table to set the chat reminder message timeout and the idle chat cancel timeout values. Create both properties at the same time.

1.  As admin, navigate to **All**, and then enter `sys_properties.list` in the filter.
2.  Select **New** to add the **com.glide.cs.idle\_chat\_reminder\_timeout** property.
    1.  On the form, fill in the fields.

<table id="table_k4d_c1t_wlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

System property name. Enter: `com.glide.cs.idle_chat_reminder_timeout`

</td></tr><tr><td>

Description

</td><td>

Explanation for this property. For example: `Idle chat reminder timeout (in seconds)`

</td></tr><tr><td>

Type

</td><td>

Data type. Select `integer`.

</td></tr><tr><td>

Value

</td><td>

Enter the number of seconds before the idle chat reminder message is displayed, after the requester's last response. This value must be equal to or greater than 120 seconds, since the Idle Chat Timer Task job runs every 120 seconds to check active chat sessions.For example, if the idle chat reminder message is to be displayed 5 minutes after the requester's last response, enter 300 seconds.

 **Note:** If you want to set an idle chat message reminder timeout that is under 120 seconds, you must also change the time at which the Idle Chat Timer Task job runs. The job must check for idle chats within a shorter time frame. For example, if the reminder message timeout is 60 seconds after the requester's last response, set the Idle Chat Timer Task job to run every 60 seconds. For more information on base system scheduled jobs, see [System scheduler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_SystemScheduler.md).

</td></tr></tbody>
</table>    2.  Select **Submit**.
3.  In the System Properties table, select **New** to add the **com.glide.cs.idle\_chat\_cancel\_timeout** property.
    1.  On the form, fill in the fields.

<table id="table_zjc_tg5_wlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

System property name. Enter: `com.glide.cs.idle_chat_cancel_timeout`

</td></tr><tr><td>

Description

</td><td>

Explanation for this property. For example: `Idle chat cancel timeout (in seconds)`

</td></tr><tr><td>

Type

</td><td>

Data type. Select `integer`.

</td></tr><tr><td>

Value

</td><td>

Number of seconds before an idle chat is canceled \(times out\). This value must be larger than **com.glide.cs.idle\_chat\_reminder\_timeout**, where the difference between this value and **com.glide.cs.idle\_chat\_reminder\_timeout** is larger than or equal to 120 seconds \(2 minutes, which is when the Idle Chat Timer Task job runs\). For example, if the reminder message timeout value is 300 seconds \(5 minutes\), the idle chat cancel timeout value must be 420 seconds or greater.

 **Note:** If you changed the Idle Chat Timer Task job, the difference between the chat cancel timeout value and the idle chat reminder timeout must be larger or equal to the Idle Chat Timer Task job time. For example, if the reminder timeout is 60 seconds and the Idle Chat Timer Task job is also 60 seconds, the idle chat cancel timeout value must be 120 seconds or greater.

</td></tr></tbody>
</table>    2.  Select **Submit**.

## Set the inactivity timeout behavior

The **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** property determines the timeout behavior when inactivity is triggered. When this property is `true`, the inactivity timer does not start until the agent sends a non-automated response to the requester.

1.  As admin, navigate to **All**, and then enter `sys_properties.list` in the filter.
2.  Select **New** to add the **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** property.
    1.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|System property name. Enter: `com.glide.cs.start_idle_timeout_after_agent_response`|
        |Description|Explanation for this property. For example: `Timeout behavior when inactivity should be triggered.`|
        |Type|Data type. Select `true/false`.|
        |Value|Either `true` or `false`.|

    2.  Select **Submit**.

## Set the server disconnect timeout for guest conversations

The **com.glide.cs.chat\_disconnect\_timeout** property determines how long the system will wait to reconnect a disconnected conversation before it ends the chat. If communication is reestablished during that timeframe, the conversation resumes.

1.  As admin, navigate to **All**, and then enter `sys_properties.list` in the filter.
2.  Select **New** to add the **com.glide.cs.chat\_disconnect\_timeout** property.
    1.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|System property name. Enter: `com.glide.cs.chat_disconnect_timeout`|
        |Description|Explanation for this property. For example: `Timeout behavior for disconnected guest conversations.`|
        |Type|Data type. Select `integer`.|
        |Value|Number of seconds before a disconnected guest chat is canceled \(times out\). The client will try to reconnect during that time.|

    2.  Select **Submit**.

## Examples

These examples show how the **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** system setting may affect how the system handles idle chats. In the following examples, the inactivity timeout is set to 60 seconds and the inactivity reminder is set to 30 seconds.

Example 1: In this example, **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** does not affect how the system handles an idle chat.

1.  Agent enters the chat.
2.  System sends automated message `Thank you for contacting support. I am looking into your question now and will be with you shortly.`
3.  Agent sends the message `What can I help you with today?`
4.  If the requester does not respond after 30 seconds, then the system sends the message `The conversation is timing out, are you still there?`
5.  If the requester does not respond within 60 seconds after the agent's message, then the system sends the message `It seems you have left the conversation` and ends the chat.

Example 2: In this example, **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** affects how the system handles an idle chat.

1.  Agent enters the chat.
2.  System sends automated message `Thank you for contacting support. I am looking into your question now and will be with you shortly.`
3.  If the agent does NOT send a message, one of the following occurs:
    -   If **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** is not set or is set to false, then
        1.  The system starts the inactivity timer.
        2.  If the requester does not respond after 30 seconds, then the system sends the message `The conversation is timing out, are you still there?`
        3.  If the requester does not respond within 60 seconds after the automated message, then the system sends the message `It seems you have left the conversation` and ends the chat.
    -   If **com.glide.cs.start\_idle\_timeout\_after\_agent\_response** is set to true, the system does not start the inactivity timer and the chat will not time out.

**Parent Topic:**[Configuring Agent Chat](ci-agent-chat-configuring.md)

