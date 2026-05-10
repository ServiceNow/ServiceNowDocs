---
title: Configure KPIs for queues
description: Configure key performance indicators in queues to track the incoming work for specific categories of work in a service channel.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Channels, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Configure KPIs for queues

Configure key performance indicators in queues to track the incoming work for specific categories of work in a service channel.

## Before you begin

Role required: sn\_channel\_mgmt.admin

## Procedure

1.  Add KPIs to a queue.

<table id="choicetable_tmd_vh5_tlb"><thead><tr><th align="left" id="d116850e57">

To

</th><th align="left" id="d116850e60">

Do This

</th></tr></thead><tbody><tr><td id="d116850e66">

**Add from a service channel**

</td><td>

1.  Navigate to **Workforce Optimization for ITSM** &gt; **Channel Management** &gt; **Service Channel**
2.  Select a service channel.
3.  Select the **Queue** tab.
4.  Select a queue.


</td></tr><tr><td id="d116850e104">

**Add from a queue**

</td><td>

1.  Navigate to **Workforce Optimization for ITSM** &gt; **Channel Management** &gt; **Queues**
2.  Select a queue.


</td></tr></tbody>
</table>2.  Click the **Reports** tab.

    **Note:** You may have to configure the related list to display the **Reports** tab.

3.  Click **Edit**.

4.  Add Workforce Optimization for ITSM KPIs \(reports\) that are filtered based on **My Managed Groups**.

    To create reports that explicitly apply to your managed teams, refer to [Create a report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/c_SingleScoreCharts.md).

5.  Click **Submit**.

    The key performance indicators are added to the queue and appear in the **All Queues** tab in Manager Workspace. By default, the indicators get automatically refreshed at an interval of five seconds. You can add the **sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds** property to the system properties to modify the interval time.


**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)

