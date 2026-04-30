---
title: Using Channel Management in Workforce Optimization for Customer Service
description: Route work items to assigned groups using channels. Use skill-based routing to ensure that the right work goes to the right agent. Review real-time performance as your team is actively working on tasks across channels. When you see escalations, you can help your agents resolve issues without the requester being aware of it.Assist agents in real time by joining their chat conversation and collaborate on any record by connecting with the right people instantly to achieve faster resolution​.Monitor your agents' workload and the status of their work items against each service channel and queue so that you can get an idea of how efficiently work is moving through the queue and to your agents.Allocate pending work items to agents to complete the work. Track your agent's performance in overview so that you can analyze and review how that agent is doing.Change the default number of work items that an agent can handle for a service channel.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Channel Management in Workforce Optimization for Customer Service, Using Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Using Channel Management in Workforce Optimization for Customer Service

Route work items to assigned groups using channels. Use skill-based routing to ensure that the right work goes to the right agent. Review real-time performance as your team is actively working on tasks across channels. When you see escalations, you can help your agents resolve issues without the requester being aware of it.

Monitor ongoing work and track your agents' performance of your direct reporting teams and teams that you manage additionally. Work items are allocated to qualified agents using work item queues, routing conditions, and assignment criteria that you define.

Review real-time performance as your team is actively working on tasks across channels in the following sections.

-   The **Overview** section displays the most important key performance indicators \(KPIs\) for each of the service channels in the form of cards. The KPIs appear as per the configuration order in the [service channels](setup-channels-queues-configurable-wfo-cs.md#). The KPI scores are real-time information and automatically refreshed at a regular interval of 5 seconds or as configured in the **sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds** [system property](../reference/components-installed-configurable-wfo-cs.md). Also, the service channel cards refreshes automatically in 2 minutes as configured in the **sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds** [system property](../reference/components-installed-configurable-wfo-cs.md) or you can manually refresh by clicking the Refresh \(![Refresh overview data icon.](../image/refresh-sync-new.png)\) icon.
-   **Assignment Group** refines reports on all pages of channels and queues as per the groups selected. Interactive filter based on the assignment group configuration, you can select the assignment group on which you want to refine the data directly from the dashboard. You can disable the **Assignment Group** interactive filter using the **sn\_channel\_mgmt.filter\_config.enable** [system property](../reference/components-installed-configurable-wfo-cs.md).
-   The **Queued Work** tab displays the active work interactions being done within each service channel and queues.
-   The **All Queues** tab displays the list of work items from queue-based routing. You can drill into specific queues and see the active interactions, work items and agents. Track real-time performance of your teams using key performance indicator reports in service channels and queues. Respond to incoming support requests by changing queues as per the priorities.
-   The **All Agents** tab displays your agents’ ongoing work, presence statuses, channels, work load, and open capacity. You can drill into specific agents to view the agent's profile, on-going tasks, presence state's history, and override channel capacity.

**Note:**

-   All lists display the real-time information and are automatically refreshed at a regular interval of 30 seconds or as set in the **sn\_channel\_mgmt.list\_auto\_refresh.interval.seconds** [system property](../reference/components-installed-configurable-wfo-cs.md). You can also refresh the service channel cards manually by clicking the Refresh \(![Refresh overview data icon.](../image/refresh-sync-new.png)\) icon.
-   The **All Queues** and **All Agents** lists offer a default sorting and filtering mechanism that lets you to view the records of the selected fields based on a default sort order. Click a column heading to toggle between ascending and descending order. The sorting order turns to the default configuration as you leave the page. Administrator can customize the default sort order by creating an implementation using the extension points. For more information, see [Use extension points to configure the sort order](setup-channels-queues-configurable-wfo-cs.md#).
-   You will also receive an email notification of your agents' work summary at the end of each day if a [scheduled report](setup-channels-queues-configurable-wfo-cs.md#) is configured.

**Parent Topic:**[Channel Management in Workforce Optimization for Customer Service](configurable-channels-wfo-cs.md)

## Assist agents by joining their chat conversations with their end users

Assist agents in real time by joining their chat conversation and collaborate on any record by connecting with the right people instantly to achieve faster resolution​.

### Before you begin

Role required: sn\_csm\_wfo\_workspa.manager

### About this task

View the work-in-progress chat interactions and​ see if any of the agents has set the **Help Requested** flag as **Yes**. You can then open the interaction record and view all messages exchanged between the end user and agent​, gain the context and choose to join the conversation by​ either sending private messages or joining the conversation in public.​​

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Do one of the following:

    -   Click the **Help Requested** indicator's score on the landing page.
    -   Click the Channels \(![Channels icon.](../image/channels-new.png)\) icon, select a queue and then click the **Active Interactions** tab.
    -   In the **Lists** page, click **Conversation Monitoring** &gt; **Help Requested**.
3.  Click the interaction record for which you want to join the conversation.

4.  Click **Join Conversation** to start an interaction with the agent or click **Send Private Message** to send a private message only to the agent.


### Result

A chat conversation is established.

## Track and analyze the queue health

Monitor your agents' workload and the status of their work items against each service channel and queue so that you can get an idea of how efficiently work is moving through the queue and to your agents.

### Before you begin

Role required: sn\_csm\_wfo\_workspa.manager

### About this task

Track the real-time performance of each queue within your service channels. You can drill into specific queues so that you can see the real-time reports, waiting work items, available agents, and status of the on-going work. This information can give you an idea of how efficiently work moves through the queue and to your agents. With this information, you can determine which queues are doing well and which queues could use a few more agents on board. For example, if you see lots of agents and not much work, you can recommend skills for your agents for other queues.

**Note:**

-   The records in the list appear based on the column's default sort order. Click a column heading to toggle between ascending and descending order. The sorting order turns to the default configuration as you leave the page. For example, the **Available agents** column is by default in descending sort order. The administrator can change it to ascending order by creating an implementation using the **sn\_channel\_mgmt.ChannelMgmtExtensionPoint** extension point. For more information, see [Use extension points to configure the sort order](setup-channels-queues-configurable-wfo-cs.md#).
-   The records in the list refresh at a regular interval of 30 seconds. The administrator can change the interval using the **sn\_channel\_mgmt.list\_auto\_refresh.interval.seconds** [property](../reference/components-installed-configurable-wfo-cs.md).

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Channels \(![Channels icon.](../image/channels-new.png)\) icon.

3.  Click the **All Queues** tab.

    |Field|Description|
    |-----|-----------|
    |Name|Queue name that was used to assign and route the work to the agent. Click to view the work items and agents that are associated with the queue.|
    |Service Channel|Service channel name to which the queue is categorized. Click to view the work items and agents that are associated with the channel.|
    |Waiting work items|Number of waiting work items in the queue.|
    |Average wait time|Average amount of time that the work items are waiting for an agent.|
    |Available agents|Number of available agents.|
    |Agents not available|Number of non-available agents.|
    |Work items assigned today|Number of work items that were assigned on a particular day.|
    |Work items canceled today|Number of work items that were canceled on a particular day.|
    |Average Agent Utilization|Agent workload/capacity in percentage. The percentage is calculated from the **Total Capacity** and **Total Capacity in Use**.|
    |Service Level|Number of work items that were accepted faster than the Queue's Target Wait Time.|


## Allocate work items manually to agents

Allocate pending work items to agents to complete the work.

### Before you begin

Role required: sn\_csm\_wfo\_workspa.manager

Ensure that the agent has the relevant skills, availability, and access to at least one queue in the service channel.

### About this task

The active work items remain in the queue and are pending manual allocation for one of the following reasons:

-   The agent has already reached the maximum capacity.
-   Available agents have not accepted the allocated work items.
-   Agents with required skills are not available.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Channels \(![Channels icon.](../image/channels-new.png)\) icon.

3.  Select the work item using one of the following actions.

<table id="choicetable_pjv_3lx_ft"><thead><tr><th align="left" id="d277071e673">

Navigate To

</th><th align="left" id="d277071e676">

Do this

</th></tr></thead><tbody><tr><td id="d277071e682">

**Queued Work tab**

</td><td>

Select the work item.

</td></tr><tr><td id="d277071e691">

**Service Channel page**

</td><td>

1.  Click a service channel. For example, Chat.
2.  Click the **Work Items** tab.
3.  Select the work item.


</td></tr><tr><td id="d277071e715">

**All Queues**

</td><td>

1.  Click a queue.
2.  Click the **Work Items** tab.
3.  Select the work item.


</td></tr></tbody>
</table>    The list of available agents appears with details such as presence state, availability, capacity, assignment groups \(common groups between manager and agents\), and matching skills.

    **Note:** The availability hours are the current shift timings of an agent, excluding the break time. However, if the shift hasn't started, then the next shift available hours are displayed.

4.  Select the agent that you want to assign the work item to.

    For example, if the capacity is 0/4, it means that the agent's maximum capacity is four work items.

    **Note:** You can allocate one work item at a time to the agent that you select. ![Agent availability.](../image/agent_availability_new.png)

5.  Click **Allocate**.

    A confirmation message appears that shows that the work item is allocated to the selected agent. You can customize the confirmation message by adding the \[glide.awa.manual\_assignment\_message\] system property to the sys\_properties.list \[sys\_properties\] table. The agent gets an alert on the assigned work item as follows:

    -   If the agent accepts the work item, the status changes from **Pending Accept** to the **Accepted** state. The ​**Assigned To** field is updated​ with the agent's name and the relevant KPI is updated.
    -   If the agent rejects the work item, the status changes to the **Queued** state.
    -   If the agent does not accept the work item for a long time, the status remains in the **Pending Accept** state. You then need to reallocate the work item.

## Track and analyze agents' performance

Track your agent's performance in overview so that you can analyze and review how that agent is doing.

### Before you begin

Role required: sn\_csm\_wfo\_workspa.manager

### About this task

View all agents and their real-time status. Drill down into a specific agent to view the following details.

-   Real-time information of KPIs such as active cases, interactions, and other rejections​.
-   Override channel capacity.
-   Agents' availability and their presence states' history.
-   Work items which are in **Pending Accept** state.
-   Interactions that are new, work in progress, and on hold states.
-   Cases that are in new, open, and awaiting info states.
-   Skill set, schedule, and profile.
-   Assigned training tasks.
-   User details and groups assigned.

**Note:**

-   The records in the list appear based on the column's default sort order. Click a column heading to toggle between ascending and descending order. The sorting order turns to the default configuration as you leave the page. For example, the agent's **Presence State** column is by default in ascending sort order. The administrator can change it to descending order by creating an implementation using the **sn\_channel\_mgmt.ChannelMgmtExtensionPoint** extension point. For more information, see [Use extension points to configure the sort order](setup-channels-queues-configurable-wfo-cs.md#).
-   The records in the list refresh at a regular interval of 30 seconds. The administrator can change the interval using the **sn\_channel\_mgmt.list\_auto\_refresh.interval.seconds** [system property](../reference/components-installed-configurable-wfo-cs.md).

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Channels \(![Channels icon.](../image/channels-new.png)\) icon.

3.  Click the **All Agents** tab.

4.  Track and analyze agents' performance.

<table id="table_dfl_xn5_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent

</td><td>

First and last name of the agent. Click the agent's name to view the agent's profile summary.

</td></tr><tr><td>

Service Channel

</td><td>

Agent’s associated service channel, so you know what type of work the available agent can handle. Click the channel to view the list of work items.

</td></tr><tr><td>

Total Capacity

</td><td>

Number of maximum work items that can be automatically assigned to agents \(pending overrides\).-   Chat: The default is 4.
-   Incident: The default is 2.


</td></tr><tr><td>

Capacity in use

</td><td>

Number of ongoing work items. Click the score to view the ongoing work of an agent.

</td></tr><tr><td>

Utilization

</td><td>

Agent workload/capacity in percentage. The percentage is calculated from the **Total Capacity** and **Capacity in Use**.

</td></tr><tr><td>

Presence State

</td><td>

Agent’s current presence status. For example, Online or Offline.

</td></tr><tr><td>

Can Take Work

</td><td>

Agent's status to accept the work item.

</td></tr><tr><td>

Time in State

</td><td>

Amount of time the agent has been in the current presence status.

</td></tr></tbody>
</table>5.  Select an agent to drill down to view the details.

    Agent profile page appears. The **Current Work** displays the data of the configured key performance indicators \(KPIs\). For more information, see [Configure KPIs for agents](setup-channels-queues-configurable-wfo-cs.md#).


## Override channel capacity for an agent

Change the default number of work items that an agent can handle for a service channel.

### Before you begin

Role required: sn\_csm\_wfo\_workspa.manager

### About this task

By default, the override capacity is valid for 12 hours. Administrator can change the duration using the**sn\_channel\_mgmt.awa\_agent\_temporary\_override\_time.minutes** [system property](../reference/components-installed-configurable-wfo-cs.md). The capacity resets to the previous value after the specified time. The scheduled job Reset Temporary Capacity Override is executed every two minutes to check the invalid or expired overridden capacity and resets to the previous value. You can override the channel capacity for a single agent at a time. Ensure that an agent to whom you want to override the channel capacity needs to be associated with Advanced Work Assignment and the required channels.

### Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Navigate to an agent's profile page.

<table id="choicetable_yv3_zcw_knb"><thead><tr><th align="left" id="d277071e1173">

To set the override capacity

</th><th align="left" id="d277071e1176">

Do this

</th></tr></thead><tbody><tr><td id="d277071e1182">

**From Channels**

</td><td>

1.  Click the Channels \(![Channels icon.](../image/channels-new.png)\) icon.
2.  Click the **All Agents** tab.
3.  Click an agent's record.


</td></tr><tr><td id="d277071e1212">

**From Teams**

</td><td>

1.  Click the Teams icon \(![Teams icon.](../image/teams-new.png)\).
2.  Click the KPI group.
3.  Select **Group Members** tab.
4.  Click an agent's record.


</td></tr></tbody>
</table>    The agent profile page appears.

3.  Click the **Overview** tab.

4.  In the **Channels** section, select the service channel for which you want to override the capacity.

5.  Click **Capacity Override**.

    The **Agent Capacity Override** page appears.

6.  In the **Override Capacity** field, enter the new capacity.

7.  Click **Apply**.


### Result

The following snapshot shows an example of an agent' capacity override. A message appears indicating the capacity update is valid for the defined duration. The capacity resets to the previous value after the specified time.![Agent Capacity Override pop-up message displaying the current capacity of the agent along with a field to update the capacity.](../image/override_channel_capacity_new.png)

