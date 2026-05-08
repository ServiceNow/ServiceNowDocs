---
title: Activate SLA timeline
description: You can activate the SLA timeline plugin \(com.snc.sla.timeline\) if you have the admin role. This plugin activates related plugins if they are not already active.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management plugins, Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Activate SLA timeline

You can activate the SLA timeline plugin \(com.snc.sla.timeline\) if you have the admin role. This plugin activates related plugins if they are not already active.

## Before you begin

Role required: sla\_admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Script includes installed with SLA timeline](../reference/r_ScriptIncludesIWithSLATimeline.md)**  
When SLA timeline is activated, script includes are installed.

**Parent Topic:**[Service Level Management plugins](../concept/sla-plugins.md)

**Related topics**  


[Activate Service Level Management](activate-sla-plugin.md)

[Activate SLA Breakdown definitions](../reference/activate-sla-breakdowns-plugin.md)

[Activate Service Level Management - SLA Timer Config API](activate-sla-timer-config-api.md)

[bundle-platadm.list-of-plugins]

