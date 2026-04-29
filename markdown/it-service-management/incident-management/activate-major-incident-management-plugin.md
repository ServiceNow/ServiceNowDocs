---
title: Activate Incident Management - Major Incident Management
description: You can activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Major Incident Management plugins, Managing major incidents, Incident Management, IT Service Management]
---

# Activate Incident Management - Major Incident Management

You can activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) must be manually activated for new and existing customers.

Incident Management - Major Incident Management plugin activates these related plugins if they are not already active:

-   Incident Communications Management \(com.snc.iam\)
-   Incident Updates \(com.snc.incident.updates\)
-   Task-Outage Relationship \(com.snc.task\_outage\)

<table id="table_fd2_xjb_rbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notify\[com.snc.notify\]

</td><td>

Provides platform features for workflow-driven voice calls, conference calls, and SMS messages. Requires the Twilio Direct Driver and a separate contract with Twilio for SMS and Voice capabilities.**Note:** Existing users already using Twilio Driver need to [migrate](https://www.servicenow.com/docs/access?context=t_MigrateToTwilioDirectDriver&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) to Twilio Direct Driver.

</td></tr><tr><td>

On-Call Scheduling\[com.snc.on\_call\_rotation\]

</td><td>

Provides the ability to create on-call schedules and escalation trees. When an incident is created, dynamically route the escalation to an on-call resource. On-Call Scheduling enables you to configure and build different on-call schedules per process and assignment group.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Incident Management - Major Incident Management](installed-with-mim.md)**  
Several types of components are installed with activation of the Incident Management - Major Incident Management plugin, including tables and user roles.
-   **[Slack notification installed with Major Incident Management](../reference/slack-notification-installed-with-MIM.md)**  
Slack notifications are added with activation of Incident Management – Major Incident Management.

**Parent Topic:**[Major Incident Management plugins](../concept/mim-plugins.md)

**Related topics**  


[Managing major incidents](../concept/major-incident-management.md)

[Legacy: Major incident overview dashboard](../concept/major-incident-overview.md)

[Major incident workbench](../concept/major-incident-workbench.md)

[List of Australia plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

