---
title: Activate Walk-up Experience
description: You can activate the Walk-up Experience plugin \(com.snc.walkup\) if you have the admin role. This plugin includes demo data.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administration, Configure, Walk-up Experience, IT Service Management]
---

# Activate Walk-up Experience

You can activate the Walk-up Experience plugin \(com.snc.walkup\) if you have the admin role. This plugin includes demo data.

## Before you begin

Role required: admin

## About this task

The Walk-up Experience application is for pre-built support lounges. The application enables your organization to set up a walk-up contact channel to support online and on-site queue check-in.

The Interaction Logging, Routing, and Queuing \(com.glide.interaction\) plugin are activated with the Walk-up Experience plugin \(com.snc.walkup\). The following plugins must also be activated in order to use the Walk-up Experience application:

-   Asset Management \(com.snc.asset\_management\)
-   Service Portal \(com.glide.service-portal\)

To activate Walk-up Experience Badge Reader Integration and for more information about this feature, refer to [Badge Reader Integration for Walk-up Experience](../concept/badge-scan-walkup-onsite.md).

For enhanced security, activate the Explicit Role \(com.glide.explicit\_roles\) plugin. The walk-up user is assigned snc\_external automatically. This plugin was introduced in the ServiceNow AI Platform Paris release.

**Note:** Refer to  for details about the plugin and [Explicit Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/explicit-roles.md) for more information about this upgrade process.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Walk-up Experience administration](../concept/walkup-experience-administration.md)

**Related topics**  


[List of plugins \(Australia\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

