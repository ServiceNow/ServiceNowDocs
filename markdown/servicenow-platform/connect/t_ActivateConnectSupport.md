---
title: Activate Connect Support
description: The Connect Support plugin \(com.glide.connect.support\) is no longer available.Properties are added with activation of Connect Support.Additional plugins are available for Connect Support. These plugins integrate Connect Support with other features and provide capabilities to track performance metrics.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate Connect Support

The Connect Support plugin \(com.glide.connect.support\) is no longer available.

## Before you begin

**Important:**

This plugin is no longer available. In Paris and future releases, Connect Support no longer receives enhancements or non-priority bug fixes. Consider migrating to ServiceNow® Advanced Work Assignment and Agent Chat in workspace to automatically assign chat requests and other work items to agents. For details, see [Migrate from Connect Support to Advanced Work Assignment and Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/migrate-from-connect-support.md).

If you are currently using the legacy chat feature to provide help desk support, close any open help desk chats before activating Connect Support. Legacy chat and Connect Support should not be used concurrently. When you activate Connect Support, the system automatically sets the state of all Chat Queue Entry \[chat\_queue\_entry\] records to **Closed Complete**. This ends any open help desk chats. For more information, see [Migrate from legacy chat to Connect Support](t_ConnectSupportMigration.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## Properties installed with Connect Support

Properties are added with activation of Connect Support.

<table id="table_vmr_bbd_br1"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

connect.support.conversation\_limit

</td><td id="Entry_ConnectSupportConversationLimitDescription">

Determines how many support conversations an individual agent can have at one time. When the value is set to **-1**, an agent can participate in an unlimited number of conversations.-   **Type**: integer
-   Default value: -1
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.idle.delay

</td><td id="entry_ConnectSupportIdleDelayDescription">

Determines how many seconds a user must be inactive in a support conversation before an idle countdown timer appears.-   **Type**: integer
-   Default value: 120
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.idle.count\_down

</td><td id="entry_ConnectSupportIdleCountDownDescription">

Determines how many seconds the idle countdown timer remains open after it appears. If the idle user does not dismiss the timer before the countdown completes, the system closes the support session.-   **Type**: integer
-   Default value: 60
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.show\_agent\_avatar

</td><td id="entry_ConnectSupportShowAgentAvatarDescription">

Determines whether an agent's avatar is shown in a support conversation \(enabled\). When the property is disabled, users see the agent's name only.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.user.closed.conversation\_limit

</td><td id="entry_ConnectSupportUserClosedConversationLimitDescription">

Determines how many closed conversations appear in a user's support conversation history. When the value is set to **0**, all previous conversations appear in the history.-   **Type**: integer
-   Default value: 0
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

glide.connect.support.enabled

</td><td id="entry_GlideConnectSupportEnabledDescription">

Disables or enables Connect Support. When the property is enabled, the **Service Desk Chat** button in the Employee Self-Service portal opens the conversation in Connect Support, rather than legacy chat. Additionally, the Support tab appears in the Connect sidebar.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

glide.connect.support.reflect\_system\_messages

</td><td>

Controls whether Connect Support reflects system messages in records created from a support chat, for example, transfer notices, automated queue messages, etc.-   **Type**: true \| false
-   **Default value**: false
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Additional plugins for Connect Support

Additional plugins are available for Connect Support. These plugins integrate Connect Support with other features and provide capabilities to track performance metrics.

You must have the admin role to activate these additional plugins. For details, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md) .

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