---
title: Setting up service channels and queues
description: You can set up service channels, queues, and key performance indicators \(KPIs\) to route work items automatically to agents based on an agent's availability, capacity, and skills.Add service channels and queues to automatically route incoming work items to agents.Define agent assignment rules and specify groups of agents who are eligible to receive overflow work assignments for a queue.Configure key performance indicators \(KPIs\) in service channels to your teams to track the ongoing work and real-time performance of teams.Configure key performance indicators \(KPIs\) for queues so that you can track the incoming work by category in a service channel.Configure key performance indicators \(KPIs\) in service channels for your agents so that you can track the agents' ongoing work and real-time performance.Configure supervisor lists in a service channel to view the list of active work items across service channels and queues.Use scripted extension points to configure the sort order for the columns in the All Agents and All Queues lists for Channel Management.Use scripted extension points to configure the columns in the All agents list for Channel Management.Use scripted extension points to configure the columns in the All queues list for Channel Management.Generate and distribute a daily scheduled report that summarizes the agent's work performance via email.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Configure, Workforce Optimization for Customer Service, Customer Service Management]
---

# Setting up service channels and queues

You can set up service channels, queues, and key performance indicators \(KPIs\) to route work items automatically to agents based on an agent's availability, capacity, and skills.

With Workforce Optimization for Customer Service, you, as a channel administrator, can set up service channels and work item queues so that managers can view the real-time operational metrics for the work that is being done by their teams and the specific items that their teams are working on. You can also configure real-time refresh intervals for the metrics and lists so that managers can always see the latest information about their teams.

Configure filters to refine the search and view targeted results. Filters are persisted across all channel management pages in the session. To view a list of the default interactive filters and the KPI reports for channels, queues, agents, and groups that you can map to the interactive filters, see [Interactive Filters](../reference/components-installed-configurable-wfo-cs.md) under the Channel Management section. By default, the assignment group filter is applied to all lists and groups that you manage. You can disable interactive filters by using the **sn\_channel\_mgmt.filter\_config.enable** property.

**Parent Topic:**[Configuring Workforce Optimization for Customer Service](setup-configurable-wfo-cs.md)

## Add service channels and queues

Add service channels and queues to automatically route incoming work items to agents.

### Before you begin

Role required: sn\_channel\_mgmt.admin

### About this task

A service channel is a means of assigning a specific type of work items to agents. You can modify the existing service channels or create your own custom service channel.

### Procedure

1.  To create a service channel, do the following:

    1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Service Channels**.
    2.  Click **New** and see [Create a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) to create the service channel.
    3.  Click **Submit**.
    The service channel is created.

2.  To create a queue, do the following:

    1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Queues** or select the service channel and click the **Queues** tab.
    2.  Click **New** and see [Create a work item queue](https://www.servicenow.com/docs/access?context=awa-create-queue&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) to create the queue.
    The queue is created in the service channel.


## Create assignment rules and groups

Define agent assignment rules and specify groups of agents who are eligible to receive overflow work assignments for a queue.

### Before you begin

You must first create a new assignment rule before you create a service channel. For more information, see [create a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US). Use [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) \(AWA\) to route work items automatically to agents based on an agent's availability, capacity, and skills.

Role required: sn\_channel\_mgmt.admin

### About this task

An eligible assignment group can consist of one or more groups of agents available to work on items in the queue.

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Queues**.

2.  Click the queue to which you want to define an assignment rule.

3.  In the **Assignment Eligibility** tab, click **New**.

4.  On the form, fill in the fields.

<table id="table_nln_krq_lfb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Agent assignment rule

</td><td>

Name of the rule that determines how work items are to be assigned. Select an assignment rule from the list.

</td></tr><tr><td>

Eligible at

</td><td>

Length of time in seconds before AWA considers the next set of agents for assignment.

</td></tr><tr><td>

Groups

</td><td>

Groups that are eligible for assignment. -   Click the lock \(![Lock icon.](../image/lock-new.png)\) icon to unlock it and select the agent groups in the eligible assignment pool.
-   Click the \(![Lock icon.](../image/lock-new.png)\) icon to lock it.


</td></tr></tbody>
</table>5.  Click **Submit** to create the eligible or **Update** if modifying an eligible assignment pool.

    The Queues \[awa\_queues\] table is updated with the eligible assignment group.

    **Note:** For a new service channel, you must first create a new assignment rule and then [create a service channel](https://www.servicenow.com/docs/access?context=awa-create-service-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


## Configure KPIs for service channels

Configure key performance indicators \(KPIs\) in service channels to your teams to track the ongoing work and real-time performance of teams.

### Before you begin

Role required: sn\_channel\_mgmt.admin

### About this task

Add the [channel Management reports](../reference/components-installed-configurable-wfo-cs.md) that are by default configured with Workforce Optimization for Customer Service or create a new KPI report that matters the most to you. Key performance indicators help managers perform the following actions:

-   Review real-time performance as the team is actively working on tasks across channels and queues.​
-   Track progress against KPIs and drill down into agents, team, and individual performance.​
-   Drill down into all queues and monitor ongoing cases, interactions, and tasks.
-   Jump in and support agents for help-requested work items using chat whisper or add work notes to a task.​
-   Refine data in the dashboard using the Assignment Group interactive filter without modifying the reports. For more information, see [Interactive Filters](https://www.servicenow.com/docs/access?context=c_HomepagePublishers&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

The KPI scores are automatically refreshed at an interval of five seconds. However, you can modify the refresh interval by adding the **sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds** [property](../reference/components-installed-configurable-wfo-cs.md) or choose to not automatically refresh using the **sn\_channel\_mgmt.channels\_card\_auto\_refresh.enable** [property](../reference/components-installed-configurable-wfo-cs.md). Also, the service channel cards refreshes automatically in 2 minutes as configured in the **sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds** [system property](../reference/components-installed-configurable-wfo-cs.md) or you can manually refresh by clicking the Refresh \(![Refresh overview data icon](../image/refresh-sync-new.png)\) icon.

​

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Service Channels**.

2.  Click the service channel to which you want to add KPIs.

3.  In the **Reports** tab, click **Edit**.

    **Note:** You must [add the Reports related list](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) if you do not see the **Reports** tab.

4.  Select and add the [Channel Management reports](../reference/components-installed-configurable-wfo-cs.md) that are by default configured with Workforce Optimization for Customer Service.

    **Note:** Review the report's definition and add the corresponding filters that are applicable to the service channel that matters the most to you.

5.  Click **Save**.

6.  To create a KPI report that is explicitly applicable to your teams, do the following:

    1.  Navigate to **Reports** &gt; **Create New**.

    2.  Fill in the details.

        For more information, see [Create a single score report](https://www.servicenow.com/docs/access?context=c_SingleScoreCharts&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    3.  Click **Save**.

        The KPI report is created.

    4.  Navigate to **Reports** &gt; **Administration** &gt; **Interactive Filters**.

    5.  Click **Channel Management Groups Filter**.

    6.  Select the Interactive filter references related list and click **New**.

        The Interactive Filter Reference - Channel Management Groups Filter page appears.

    7.  Select the KPI report's table name and field name.

        For more information, see [Create a reference field interactive filter](https://www.servicenow.com/docs/access?context=t_CreateAReferenceFieldPublisher&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    8.  Click **Submit**.

    9.  Repeat steps 1 to 4 for each KPI report to be added in the service channel.

    -   KPI reports are added with an **Order** being shown as 100, 200 and so on. You can also change the order of a KPI report during selection.
    -   By default, the report name is considered as the **Name**. However, you can change the display name per your business needs.

### Result

The KPIs are added to the service channel and appear in the Channels page. The first five KPIs with the lowest order number appear in the service channel cards.

## Configure KPIs for queues

Configure key performance indicators \(KPIs\) for queues so that you can track the incoming work by category in a service channel.

### Before you begin

Role required: sn\_channel\_mgmt.admin

### Procedure

1.  To add KPIs to a queue, do one of the following.

<table id="choicetable_tmd_vh5_tlb"><thead><tr><th align="left" id="d211445e842">

To

</th><th align="left" id="d211445e845">

Do This

</th></tr></thead><tbody><tr><td id="d211445e851">

**Add from a service channel**

</td><td>

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Service Channel**.
2.  Select a service channel.
3.  Click the **Queue** tab.
4.  Select a queue.


</td></tr><tr><td id="d211445e893">

**Add from a queue**

</td><td>

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Queues**.
2.  Select a queue.


</td></tr></tbody>
</table>2.  In the **Reports** tab, click **Edit**.

    **Note:** You must [add the Reports related list](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) if you do not see the **Reports** tab.

3.  Add the [Channel Management reports](../reference/components-installed-configurable-wfo-cs.md) that are by default configured with Workforce Optimization for Customer Service.

    **Note:** Review the report's definition and add the corresponding filters applicable to the service channel that matter the most to you.

4.  Click **Save**.

5.  To create a KPI report that is explicitly applicable to your teams, do the following:

    1.  Navigate to **Reports** &gt; **Create New**.

    2.  Fill in the details.

        For more information, see [Create a single score report](https://www.servicenow.com/docs/access?context=c_SingleScoreCharts&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    3.  Click **Save**.

        The KPI report is created.

    4.  Navigate to **Reports** &gt; **Administration** &gt; **Interactive Filters**.

    5.  Click **Channel Management Queues Filter**.

    6.  Select the Interactive filter references related list and click **New**.

        The Interactive Filter Reference - Channel Management Queues Filter page appears.

    7.  Select the KPI report's table name and field name.

        For more information, see [Create a reference field interactive filter](https://www.servicenow.com/docs/access?context=t_CreateAReferenceFieldPublisher&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    8.  Click **Submit**.

    9.  Repeat steps 1 to 4 for each KPI report to be added in the queue.


### Result

The key performance indicators are added to the queue and appear in the **All Queues** tab in the Channels page. By default, the KPI scores are automatically refreshed at an interval of five seconds. However, you can modify the refresh interval by adding the [sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds](../reference/components-installed-configurable-wfo-cs.md) property.

## Configure KPIs for agents

Configure key performance indicators \(KPIs\) in service channels for your agents so that you can track the agents' ongoing work and real-time performance.

### Before you begin

Role required: sn\_channel\_mgmt.admin

### About this task

Add key performance indicators to channels to help managers perform the following actions:

-   Review real-time performance of agents who are actively working on tasks across channels and queues.​
-   Track progress against KPIs and drill down into agents and individual performance.​

The KPI scores are automatically refreshed at an interval of 30 seconds. However, you can modify the refresh interval by adding the **sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds** [property](../reference/components-installed-configurable-wfo-cs.md). Also, the service channel cards refreshes automatically in 2 minutes as configured in the **sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds** [system property](../reference/components-installed-configurable-wfo-cs.md) or you can manually refresh by clicking the Refresh \(![Refresh overview data icon](../image/refresh-sync-new.png)\) icon.

​

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Service Channels**.

2.  Click the service channel that you want to add KPIs to.

3.  Click the Agents Reports related list.

4.  Add the [Reports for Agents in Channel Management](../reference/components-installed-configurable-wfo-cs.md) that are by default configured with Workforce Optimization for Customer Service.

    **Note:** Review the report's definition and add the corresponding filters that are applicable to the service channel that matters the most to you.

5.  Click **Save**.

6.  To create a KPI report that is explicitly applicable to your teams, do the following:

    1.  Navigate to **Reports** &gt; **Create New**.

    2.  Fill in the details.

        For more information, see [Create a single score report](https://www.servicenow.com/docs/access?context=c_SingleScoreCharts&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    3.  Click **Save**.

        The KPI report is created.

    4.  Navigate to **Reports** &gt; **Administration** &gt; **Interactive Filters**.

    5.  Click **Channel Management Agent Filter**.

    6.  Select the Interactive filter references related list and click **New**.

        The Interactive Filter Reference - Channel Management Agent Filter page appears.

    7.  Select the KPI report's table name and field name.

        For more information, see [Create a reference field interactive filter](https://www.servicenow.com/docs/access?context=t_CreateAReferenceFieldPublisher&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

    8.  Click **Submit**.

    9.  Repeat steps 1 to 4 for each KPI report to be added in the service channel.

    -   KPI reports are added with an **Order** being shown as 100, 200, and so on. You can also change the order of a KPI report during selection.
    -   By default, the report name is considered as the **Name**. However, you can change the display name per the business needs.

### Result

The KPIs that are configured in the service channel appear in the Current Work section of the agent's Overview page. For more information, see [Track and analyze agents' performance](use-channels-configurable-wfo-cs.md#).

## Configure supervisor lists for service channels

Configure supervisor lists in a service channel to view the list of active work items across service channels and queues.

### Before you begin

Role required: sn\_channel\_mgmt.admin

### About this task

A database view that defines table joins is used for generating reports for a supervisor list. For example, you can create a database view that can join the Case table to the Interaction and Metric tables. When you use this database view, and create a supervisor list to report on the active work items, you may include fields from any of these three tables. For more information, see [Database views](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** You can configure three supervisor lists for each service channel. The first three lists with the lowest order number appear in Channel Management.

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Service Channels**.

2.  Select the service channel to which you want to add a supervisor list.

3.  Click the **Supervisor Lists** tab.

    **Note:** You must [add the Reports related list](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) if you do not see the **Supervisor Lists** tab.

4.  Click **New**.![Service channel chat displaying supervisor lists. For information about the supervisor lists components, refer to the Supervisor Lists form table.](../image/supervisor-lists.png)

5.  On the form, fill in the fields.

<table id="table_u41_bmm_1fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List Title

</td><td>

Display name for the list.

</td></tr><tr><td>

Tab Title

</td><td>

Title for the tab that appears in the manager workspace.

</td></tr><tr><td>

Service Channel

</td><td>

Service channel in which the list appears.

</td></tr><tr><td>

View Name

</td><td>

Database view for the service channel.

</td></tr><tr><td>

Order

</td><td>

Number that displays the order.**Note:** The first three lists with the lowest order number appear in Channel Management.

</td></tr></tbody>
</table>6.  Click **Submit**.


### Result

The supervisor list is added to the service channels and appears in Channel Management. ![Active Work Items page displaying the supervisor lists in a Chat channel.](../image/lists-chat.png)

## Use extension points to configure the sort order

Use scripted extension points to configure the sort order for the columns in the All Agents and All Queues lists for Channel Management.

### Before you begin

Role required: admin

### About this task

Use the **sn\_channel\_mgmt.ChannelMgmtExtensionPoint** extension point and create an implementation to configure the sorting mechanism for the All Agents and All Queues lists in Channel Management. You can create multiple implementations; however, the implementation with the lowest order number is executed.

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_channel_mgmt.ChannelMgmtExtensionPoint`.

3.  On the form banner, click the link **here** to edit the record.

4.  Click **Create Implementation** in the related links to create your sorting mechanism extension point script.

5.  Add or modify the columns and sort directions in the `vardata` section.

    ![Scripted extension point with the vardata section empty.](../image/extension_script.jpg)

6.  Click **Update**.


### Result

The sorting mechanism is applied to the defined columns in the All Queues and All Agents lists in Channel Management.

### Example

The Presence State column with **ASC** as a sort direction in the extension script displays the Presence State records in an ascending order in the All Agents list. For more information, see [Track and analyze agents' performance](use-channels-configurable-wfo-cs.md#).

## Configure columns in the All agents list

Use scripted extension points to configure the columns in the All agents list for Channel Management.

### Before you begin

Role required: admin

### About this task

Use the **sn\_channel\_mgmt.AgentListColumns** extension point to modify the current implementation to configure the columns for the All agents list in Channel Management.

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for **sn\_channel\_mgmt.AgentListColumns**.

3.  On the form banner, click the link **here** to edit the record.

4.  Click **AgentListColumnsOOBImpl** in the related list to configure the columns for All agents.

5.  Add or modify the columns in the `getColumns` section.

    ![Scripted extension point to configure the columns in the All agents list.](../image/configure_columns_allagents.png)

6.  Click **Update**.


## Configure columns in the All queues list

Use scripted extension points to configure the columns in the All queues list for Channel Management.

### Before you begin

Role required: admin

### About this task

Use the **sn\_channel\_mgmt.QueueListColumns** extension point to modify the current implementation to configure the columns for the All queues list in Channel Management.

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for **sn\_channel\_mgmt.QueueListColumns**.

3.  On the form banner, click the link **here** to edit the record.

4.  Click **QueueListColumnsOOBImpl** in the related list to configure the columns for All agents.

5.  Add or modify the columns in the `getColumns` section.

    ![Scripted extension point to configure columns in the All queues list.](../image/configure_columns_allqueues.png)

6.  Click **Update**.


## Schedule a daily report

Generate and distribute a daily scheduled report that summarizes the agent's work performance via email.

### Before you begin

Role required: sn\_channel\_mgmt.admin

### About this task

​The scheduled job **Send Daily Agents Report** executes the event **sn\_channel\_mgmt.agents\_report**, which then triggers the **Daily Agents Report** notification. Next, the notification **Daily Agents Report** executes an email script **daily\_agents\_reports** to send an email to all managers. To change the existing report, modify the **daily\_agents\_reports** email script.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search and click **Send Daily Agents Report**.

    The scheduled script **Send Daily Agents Report** form appears.

3.  Click the link **here** to edit the record.

4.  Select the **Active** check box.

5.  In the **Run** field, ensure that the option **Daily** is selected.

    The script, by default, sends the agents' work summary report daily to the managers.

6.  Select the **Time zone**.

7.  Click **Update** to update the scheduled job or **Execute Now** to execute the scheduled script immediately.


### Result

All managers and additional managers of the teams receive an email notification that summarizes their agents' performance.

