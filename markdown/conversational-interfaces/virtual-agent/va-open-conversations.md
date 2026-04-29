---
title: Closing Virtual Agent and Agent Chat conversations
description: Virtual Agent and Agent Chat conversations that are abandoned by requesters remain open until they are automatically closed by the scheduled job, Time Out Abandoned VA Conversations. This job runs hourly each day.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Virtual Agent with a live agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Closing Virtual Agent and Agent Chat conversations

Virtual Agent and Agent Chat conversations that are abandoned by requesters remain open until they are automatically closed by the scheduled job, **Time Out Abandoned VA Conversations**. This job runs hourly each day.

The default timeout period for abandoned Virtual Agent and live agent conversations is two hours \(7200 seconds\). The **Time Out Abandoned VA Conversations** job runs hourly to find and close any conversations that have been open longer than the default \(or configured\) timeout period.

As admins, you can change the default timeout period for closing Virtual Agent and live agent conversations by [adding the system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) **com.glide.cs.conversation\_idle\_timeout**. The timeout value that you specify in this property applies to all conversations in supported Virtual Agent and live agent channels, including chat channels \(such as Microsoft Teams, Slack, and Workplace from Facebook\) and messaging channels \(such as SMS\). For details, see [Change the timeout period for Virtual Agent and live agent conversations](va-open-conversations.md#section_sjj_wy2_cmb).

If you're using Virtual Agent and Agent Chat on multiple chat channels, you can add a channel-level idle timeout value that overrides the timeout value set in the **com.glide.cs.conversation\_idle\_timeout** property for chat channels. For details, see [Override the conversation timeout period by channel](va-open-conversations.md#section_yd3_fgp_14b).

If needed, you can also change the time at which the Time Out Abandoned VA Conversations job runs.

**Note:** If you're using NLU/keyword, you can initiate the Closing Conversation topic with phrases tied to the intent \(End Conversations\) such as `Bye` or `Exit`. If the chat isn't closing when you enter an appropriate phrase, the NLU model for the setup topics might not be published or assigned.

Closing the conversation in an LLM chat works similarly to NLU/keyword chat. You enter a phrase such as `Bye` or `Exit`, the LLM recognizes the statement, and closes the conversation.

## Change the timeout period for Virtual Agent and live agent conversations

Add the **com.glide.cs.conversation\_idle\_timeout** property to the System Property \[sys\_properties\] table to specify the length of time that an abandoned Virtual Agent or Live Agent conversation remains open \(idle\). When the **Time Out Abandoned VA Conversations** job runs hourly, it closes any Virtual Agent and Live Agent conversations that have been open longer than the specified time.

1.  In the navigation filter, enter `sys_properties.list`.
2.  Click **New**.
    1.  Complete these fields:

<table id="table_k4d_c1t_wlb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the system property name: `com.glide.cs.conversation_idle_timeout`

</td></tr><tr><td>

Description

</td><td>

Enter an explanation for this property: `Idle timeout period (in seconds) for all conversations`

</td></tr><tr><td>

Type

</td><td>

Select `integer`.

</td></tr><tr><td>

Value

</td><td>

Enter the number of seconds that abandoned Virtual Agent or Live Agent conversations remain open, after the requester's last response. This value must be less than 7200 seconds, since the **Time Out Abandoned VA Conversations** job runs every 3600 seconds \(hourly\) to close idle conversations.

 For example, a value of 1800 seconds \(30 minutes\) means that an abandoned conversation remains open for 1800 seconds \(30 minutes\). When the **Time Out Abandoned VA Conversations** job runs, it closes any conversations that have been idle longer than 1800 seconds.

</td></tr></tbody>
</table>    2.  Click **Submit**.

## Override the conversation timeout period by channel

You can set the conversation timeout value for a channel by adding a channel-specific conversation timeout value that overrides the **com.glide.cs.conversation\_idle\_timeout** property. When the **Time Out Abandoned VA Conversations** job runs hourly, it closes any Virtual Agent or Live Agent conversations in the channel that have been open longer than the specified time.

1.  In the navigation filter, enter `sys_cs_channel.list`.
2.  In the Messaging Channels table, locate the channel record to be changed and double click the **Conversation Idle Timeout** field.
3.  Enter the number of seconds that abandoned Virtual Agent or Live Agent conversations remain open in the channel, after the requester's last response.

    For example, a value of 1800 seconds \(30 minutes\) means that an abandoned conversation in the channel remains open for 1800 seconds \(30 minutes\). When the **Time Out Abandoned VA Conversations** job runs, it closes any conversations that have been idle longer than 1800 seconds.

4.  Save the value.

## Change the Time Out Abandoned VA Conversations scheduled job

To change the time that this hourly scheduled job runs or to make other adjustments to the scheduled job:

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and open the Time Out Abandoned VA Conversations record.
2.  In the Scheduled Script Execution form, change the **Time** at which the scheduled job runs. Or, depending on how you want to adjust the timing, change other fields in the form as needed.

    For example, to change the interval at which the job runs, in the **Run** field, select **Periodically**. You then specify the **Repeat Interval** \(**Days** and **Hours**\) that the job runs and the **Starting** date for the interval. For a description of the other fields that you can change in this form, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Click **Update**.

    The job runs at the specified time and frequency.


**Parent Topic:**[Using Virtual Agent with a live agent](using-va-agent-chat.md)

