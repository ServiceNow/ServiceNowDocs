---
title: Configure KPIs for agents
description: Configure key performance indicators \(KPIs\) in service channels for your agents so that you can track the agents' ongoing work and real-time performance.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Channels in Workforce Optimization for ITSM, Channels in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Configure KPIs for agents

Configure key performance indicators \(KPIs\) in service channels for your agents so that you can track the agents' ongoing work and real-time performance.

## Before you begin

Role required: sn\_channel\_mgmt.admin

## About this task

Add key performance indicators to channels to help managers perform the following actions:

-   Review real-time performance of agents who are actively working on tasks across channels and queues.​
-   Track progress against KPIs and drill down into agents and individual performance.​

The KPI scores are automatically refreshed at an interval of 30 seconds. However, you can modify the refresh interval by adding the **sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds** [system property](../reference/configurable-wfo-itsm-channel-management-reference.md). Also, the service channel card refreshes automatically in 2 minutes as configured in the **sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds**. You can also manually refresh by clicking the Refresh icon.

​

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Customer Service** &gt; **Channel Management** &gt; **Service Channels**.

2.  Click the service channel to which you want to add the KPIs.

3.  Click the Agents Reports related list.

4.  Add the [reports for agents in Channel Management](../reference/configurable-wfo-itsm-channel-management-reference.md) that are by default configured with Workforce Optimization for ITSM.

    **Note:** Review the report's definition and add the corresponding filters that are applicable to the service channel that matters the most to you.

5.  Click **Save**.

6.  To create a KPI report that is explicitly applicable to your teams, do the following:

    1.  Navigate to **Reports** &gt; **Create New**.

    2.  Fill in the details.

        For more information, see [Create a single score report](https://www.servicenow.com/docs/access?context=c_SingleScoreCharts&version=yokohama&pubname=yokohama-now-intelligence&section=t_CreateASingleScoreChart&ft:locale=en-US).

    3.  Click **Save**.

        The KPI report is created.

    4.  Navigate to **Reports** &gt; **Administration** &gt; **Interactive Filters**.

    5.  Click **Channel Management Agent Filter**.

    6.  Select the Interactive filter references related list and click **New**.

        The Interactive Filter Reference - Channel Management Agent Filter page appears.

    7.  Select the KPI report's table name and field name.

        For more information, see [Create a reference field interactive filter](https://www.servicenow.com/docs/access?context=t_CreateAReferenceFieldPublisher&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    8.  Click **Submit**.

    9.  Repeat steps 1 to 4 for each KPI report to be added in the service channel.

    -   KPI reports are added with an **Order** being shown as 100, 200, and so on. You can also change the order of a KPI report during selection.
    -   By default, the report name is considered as the **Name**. However, you can change the display name per the business needs.

## Result

The KPIs that are configured in the service channel appear in the Current Work section of the agent's Overview page. For more information, see [Track and analyze agent's performance](view-agents-availability-itsm-configurable-workspace.md).

**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)

