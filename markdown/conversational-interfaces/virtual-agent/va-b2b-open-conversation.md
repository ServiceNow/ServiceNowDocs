---
title: Closing idle bot-to-bot conversations
description: In bot-to-bot integrations \(Virtual Agent API\), abandoned conversations that are "idle" for more than an hour are automatically closed by the scheduled job, Time Out Abandoned B2B Conversations. This job runs hourly each day.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Closing idle bot-to-bot conversations

In bot-to-bot integrations \(Virtual Agent API\), abandoned conversations that are "idle" for more than an hour are automatically closed by the scheduled job, **Time Out Abandoned B2B Conversations**. This job runs hourly each day.

The default timeout period for abandoned bot-to-bot conversations is one hour \(3600 seconds\). The **Time Out Abandoned B2B Conversations** job closes any bot-to-bot conversations that have been open longer than one hour \(3600 seconds\). You \(admins\) can change the default timeout period for idle bot-to-bot conversations by [adding the system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) **com.glide.cs.b2b\_conversation\_idle\_timeout**.

The timeout value that you specify in this property applies to all bot-to-bot conversations involving the Virtual Agent.

## Change the timeout period for idle bot-to-bot conversations

Add the **com.glide.cs.b2b\_conversation\_idle\_timeout** property to the System Property \[sys\_properties\] table to specify the length of time that an abandoned bot-to-bot conversation remains open \(idle\). When the **Time Out Abandoned B2B Conversations** job runs hourly, it closes any bot-to-bot conversations that have been idle longer than the specified time.

1.  Navigate to **All**, and then enter `sys_properties.list` in the navigation filter.
2.  Click **New**.
3.  On the form, fill in the fields.

<table id="table_ojt_jwz_n4b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the system property name:**com.glide.cs.b2b\_conversation\_idle\_timeout**

</td></tr><tr><td>

Description

</td><td>

Enter an explanation for this property: `Idle timeout period (in seconds) for all bot-to-bot conversations`

</td></tr><tr><td>

Type

</td><td>

Select `integer`.

</td></tr><tr><td>

Value

</td><td>

Enter the number of seconds that the abandoned bot-to-bot conversations remain open, after the requester's last response. For example, a value of 1800 seconds \(30 minutes\) means that an abandoned bot-to-bot conversation remains open for 1800 seconds \(30 minutes\). When the **Time Out Abandoned B2B Conversations** job runs, it closes any conversations that have been idle longer than 1800 seconds.

</td></tr></tbody>
</table>4.  Click **Submit**.

## Change the Time Out Abandoned B2B Conversations scheduled job

To change the time that this hourly scheduled job runs or to make other adjustments to the scheduled job:

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and open the Time Out Abandoned B2B Conversations record.
2.  In the Scheduled Script Execution form, change the Time at which the scheduled job runs. Or, depending on how you want to adjust the timing, change other fields in the form as needed.

    For example, to change the interval at which the job runs, in the **Run** field, select **Periodically**. You then specify the **Repeat Interval** \(**Days** and **Hours**\) that the job runs and the **Starting** date for the interval. For a description of the other fields that you can change in this form, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  Click **Update**.

    The job runs at the specified time and frequency.


**Parent Topic:**[Using Virtual Agent API](virtual-agent-api.md)

