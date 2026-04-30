---
title: Connect Support metrics
description: Optional plugins provide a homepage and Performance Analytics dashboards, which contain helpful Connect Support metrics.Use the Connect Support homepage to view key indicators and metrics related to support conversations, queues, and agents.Use the Connect Support dashboards in Performance Analytics to understand trends in your support organization's performance over time.
locale: en-US
release: yokohama
product: Connect
classification: connect
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Connect Support administration, Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Connect Support metrics

Optional plugins provide a homepage and Performance Analytics dashboards, which contain helpful Connect Support metrics.

The reporting homepage is ideal for support managers who want a simple solution to track the recent performance of the support organization. The Performance Analytics dashboards provide a more full-featured solution for support managers who want to analyze trends over time.

Users with the admin role can activate the following plugins to use these features.

<table id="table_ihk_rnc_4v"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connect Support Manager's Dashboard\[com.glide.connect.managers\_dashboard\]

</td><td>

Provides a homepage for Connect Support, and all required configuration records. Though the plugin name contains the term dashboard, the plugin does not provide functionality related to Performance Analytics dashboards. Homepages are similar to dashboards, but do not require Performance Analytics roles to view.

</td></tr><tr><td>

Performance Analytics - Content Pack - Service Desk Chat\[com.snc.pa.chat\]

</td><td>

Provides the **Service Desk Chat Monitor** dashboard, which analyzes key Connect Support metrics and indicators.

</td></tr><tr><td>

Performance Analytics - Context Sensitive Analytics for Chat\[com.snc.pa.chat.context\_sensitive\_analytics\]

</td><td>

Provides in-form analytics for Connect Support. These analytics are available as a related link on the Chat Queue Entry \[chat\_queue\_entry\] form, and also as the **Context Sensitive Analytics - Chat** dashboard.

</td></tr></tbody>
</table>**Note:** For more information about these plugins, including which other plugins they activate, see [Additional plugins for Connect Support](../task/t_ActivateConnectSupport.md#).

**Related topics**  


[Performance Analytics concepts](https://www.servicenow.com/docs/access?context=c_PerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

## Use the Connect Support homepage

Use the Connect Support homepage to view key indicators and metrics related to support conversations, queues, and agents.

### Before you begin

Activate the Connect Support Manager's Dashboard plugin \(com.glide.connect.managers\_dashboard\) to view this homepage.

Role required: chat\_admin

### About this task

The homepage is called **Service Desk - Chat**.

### Procedure

1.  Navigate to **All** &gt; **Connect** &gt; **Support Administration** &gt; **Reporting Dashboard**.

    **Note:** Though the module name contains the term dashboard, the module does not provide functionality related to Performance Analytics dashboards. Homepages are similar to dashboards, but do not require Performance Analytics roles to view.

    The Connect Support homepage, which is called **Service Desk - Chat**, opens.

2.  Click a widget to drill down into its data.


## Use the Connect Support dashboards

Use the Connect Support dashboards in Performance Analytics to understand trends in your support organization's performance over time.

### Before you begin

Activate one or both of the following plugins, according to your analytics needs:

-   Performance Analytics - Content Pack - Service Desk Chat \(com.snc.pa.chat\)
-   Performance Analytics - Context Sensitive Analytics for Chat \(com.snc.pa.chat.context\_sensitive\_analytics\)

Role required: both chat\_admin and pa\_viewer

### About this task

The Performance Analytics - Content Pack - Service Desk Chat plugin \(com.snc.pa.chat\) includes the **Service Desk Chat Monitor** dashboard, which contains the following tabs:

-   **Chat Monitor By State**: Contains metrics related to closed support conversations.
-   **Overview**: Contains several metrics related to support conversations, queues, and agents.
-   **KPI Process**: Contains metrics that are key performance indicators \(KPIs\) of the Connect Support process, including the average queue response time, the average duration of support conversations, and the number of new support conversations per day.

The Performance Analytics - Context Sensitive Analytics for Chat plugin \(com.snc.pa.chat.context\_sensitive\_analytics\) includes the **Context Sensitive Analytics - Chat** dashboard. The dashboard contains additional metrics related to support queues, including the number of support conversations closed.

**Note:** You must license Performance Analytics to collect scores for the indicators on the dashboards. Without Performance Analytics premium, the dashboards display the indicators with no data.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Dashboards**.

    The last dashboard you viewed opens.

2.  In the dashboard picker, under the **Connect Chat** group, select the dashboard you want to view.

3.  View the indicators.


**Related topics**  


[Performance Analytics concepts](https://www.servicenow.com/docs/access?context=c_PerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

