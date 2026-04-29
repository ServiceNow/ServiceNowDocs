---
title: Configure KPIs for service channels
description: Configure key performance indicators in service channels to track the ongoing work and real-time performance of your teams.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up Channels, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Configure KPIs for service channels

Configure key performance indicators in service channels to track the ongoing work and real-time performance of your teams.

## Before you begin

Role required: sn\_channel\_mgmt.admin

## About this task

Add the [Channel Management reports](../reference/configurable-wfo-itsm-channel-management-reference.md) that are by default configured with Workforce Optimization for ITSM or create a new KPI report that matters the most to you. Key performance indicators help managers perform the following actions:

-   Review real-time performance as the team is actively working on tasks across channels and queues.​
-   Track progress against KPIs and drill down into agents, team, and individual performance.​
-   Drill down into all queues and monitor ongoing incidents, interactions, and tasks.
-   Jump in and support agents for help-requested work items using chat whisper or add work notes to a task.​
-   Refine data in the dashboard using the Assignment Group interactive filter without modifying the reports. For more information, see [Interactive Filters](https://www.servicenow.com/docs/access?context=c_HomepagePublishers&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Enable or disable KPI score auto-refresh**

-   By default, the KPI scores are set for auto-refresh every five seconds. You can change the interval using the **sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds** system property.
-   To disable auto-refresh, set the **sn\_channel\_mgmt.channels\_card\_auto\_refresh.enable** property to **false**.

**Refresh the service channel cards automatically or manually**

-   By default, the service channel cards are set for auto-refresh every two minutes. You can change the interval using the **sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds** syetem property.
-   To manually refresh the service channel cards, select the refresh icon.

For more information on the properties, see [Channel Management components in Workforce Optimization for ITSM](../reference/configurable-wfo-itsm-channel-management-reference.md).

​

## Procedure

1.  Navigate to **Workforce Optimization for ITSM** &gt; **Channel Management** &gt; **Service Channels**.

2.  Click the service channel to which you want to add KPIs.

3.  In the **Reports** tab, click **Edit**.

    **Note:** You must [add the Reports related list](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) if you do not see the **Reports** tab.

4.  Add reports that are configured by default in Workforce Optimization for ITSM.

    For information on Channel Management reports, see [Channel Management components in Workforce Optimization for ITSM](../reference/configurable-wfo-itsm-channel-management-reference.md).

    **Note:** Review the report's definition and add the corresponding filters that are applicable to the service channel that matters the most to you.

5.  Add Workforce Optimization for ITSM KPIs filtered based on **My Managed Groups**.

6.  Select **Save**.

7.  To create a KPI report that explicitly apply to your teams, do the following:

    1.  Navigate to **Reports** &gt; **Create New** &gt; **.**
    2.  Fill in the details on the form. For more information, see [Single score report](https://www.servicenow.com/docs/access?context=c_SingleScoreCharts&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).
    3.  Select **Save**.

        The KPI report is created.

    4.  Navigate to **Reports** &gt; **Administration** &gt; **Interactive Filters**.
    5.  Select **Channel Management Groups Filter**.
    6.  Select the Interactive filter references related list and select **New**.

        The Interactive Filter Reference - Channel Management Groups Filter page appears.

    7.  Select the KPI report's table name and field name. For more information, see [Create a reference field interactive filter](https://www.servicenow.com/docs/access?context=t_CreateAReferenceFieldPublisher&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).
    8.  Select **Submit**.

        Repeat the steps above to add more reports.

        -   KPI reports are added with an **Order** being shown as 100, 200 and so on. You can also change the order of a KPI report during selection.
        -   By default, the report name is considered as the **Name**. However, you can change the display name per your business needs.
    The KPIs are added to the service channel and appear in the Channels page. The first five KPIs with the lowest order number appear in the service channel cards.


**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)

