---
title: Activate Service Level Management - SLA Timer Config API
description: You can activate the Service Level Management - SLA Timer Config API plugin \(com.sn\_slm\_timer\) if you have the admin role.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management plugins, Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Activate Service Level Management - SLA Timer Config API

You can activate the Service Level Management - SLA Timer Config API plugin \(com.sn\_slm\_timer\) if you have the admin role.

## Before you begin

Role required: admin

## About this task

Activating this plugin provides the ability to set a preferred SLA for a given task through configuration which is dynamic, such as First SLA to breach, or declarative through a hierarchical mapping of first to match SLA definitions. This plugin includes demo data and activates related plugins if they are not already active.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Installed with Service Level Management - SLA Timer Config API](../reference/installed-with-sla-timer-config.md)**  
The Service Level Management - SLA Timer Config API \(com.sn\_slm\_timer\) plugin installs the admin role.
-   **[Script Includes installed with SLA Timer Config API](../concept/sla-timer-rest-api.md)**  
When SLA Timer Config API is activated, script includes are installed.

**Parent Topic:**[Service Level Management plugins](../concept/sla-plugins.md)

**Related topics**  


[Activate Service Level Management](activate-sla-plugin.md)

[Activate SLA Breakdown definitions](../reference/activate-sla-breakdowns-plugin.md)

[Activate SLA timeline](t_ActivateSLATimeline.md)

[List of plugins \(Australia\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

