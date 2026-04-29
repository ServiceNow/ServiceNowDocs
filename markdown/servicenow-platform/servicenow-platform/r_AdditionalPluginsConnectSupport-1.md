---
title: Additional plugins for Connect Support
description: Additional plugins are available for Connect Support. These plugins integrate Connect Support with other features and provide capabilities to track performance metrics.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Additional plugins for Connect Support

Additional plugins are available for Connect Support. These plugins integrate Connect Support with other features and provide capabilities to track performance metrics.

You must have the admin role to activate these additional plugins. For details, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US) .

<table id="table_gzd_yj1_4v"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connect Support and Service Portal Integration\[com.glide.connect.support.service-portal\]

</td><td>

Adds Connect Support components for use in the Service Portal.

</td></tr><tr><td id="entry_PluginConnectSupportManagersDashboard">

Connect Support Manager's Dashboard\[com.glide.connect.managers\_dashboard\]

</td><td>

Provides a homepage for Connect Support, and all required configuration records. Though the plugin name contains the term dashboard, the plugin does not provide functionality related to Performance Analytics dashboards. Homepages are similar to dashboards, but do not require Performance Analytics roles to view. **Note:** The Connect Support Manager's Dashboard plugin does not activate Connect Support automatically. You must activate Connect Support to collect data for the homepage.

</td></tr><tr><td>

Human Resources Application: HR Connect\[com.snc.hr.hr\_connect\]

</td><td>

Sets up a human resources \(HR\) chat queue and makes it available on the HR Service Portal.**Note:** This plugin does not appear in the **System Definition&gt;Plugins** list. Contact ServiceNow personnel to activate it.

 If not already active, the Human Resources Application: HR Connect plugin activates the Human Resources Application: Core \[com.snc.hr.core\] plugin that provides basic HR features.

</td></tr><tr><td id="entry_PluginPerformanceAnalyticsContentPackServiceDeskChat">

Performance Analytics - Content Pack - Service Desk Chat\[com.snc.pa.chat\]

</td><td>

Provides the **Service Desk Chat Monitor** dashboard, which analyzes key Connect Support metrics and indicators. The Performance Analytics - Content Pack - Service Desk Chat plugin activates the Connect Support Manager's Dashboard \[com.glide.connect.managers\_dashboard\].

</td></tr><tr><td id="entry_PluginPerformanceAnalyticsContextSensitiveAnalyticsForChat">

Performance Analytics - Context Sensitive Analytics for Chat\[com.snc.pa.chat.context\_sensitive\_analytics\]

</td><td>

Provides in-form analytics for Connect Support. These analytics are available as a related link on the Chat Queue Entry \[chat\_queue\_entry\] form, and also as the **Context Sensitive Analytics - Chat** dashboard. The Performance Analytics - Context Sensitive Analytics for Chat plugin activates the Performance Analytics - Content Pack - Service Desk Chat \[com.snc.pa.chat\] plugin if it is not already active.

</td></tr></tbody>
</table>