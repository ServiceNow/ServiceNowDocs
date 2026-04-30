---
title: Activate Service Level Management
description: You can activate the Service Level Management plugin \(com.snc.sla\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: yokohama
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Level Management plugins, Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Activate Service Level Management

You can activate the Service Level Management plugin \(com.snc.sla\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Activating this plugin, provides the core SLA functional.ities.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Installed with Service Level Management](../reference/r_InstalledWithServiceLevelMgmt.md#)**  
Activating the Service Level Management plugin adds or modifies these components: tables, properties, UI actions, UI policies, script includes, client scripts, business rules, email notifications, scheduled jobs, and workflows.

**Parent Topic:**[Service Level Management plugins](../concept/sla-plugins.md)

**Related topics**  


[Activate SLA Breakdown definitions](../reference/activate-sla-breakdowns-plugin.md)

[Activate SLA timeline](t_ActivateSLATimeline.md)

[Activate Service Level Management - SLA Timer Config API](activate-sla-timer-config-api.md)

[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

