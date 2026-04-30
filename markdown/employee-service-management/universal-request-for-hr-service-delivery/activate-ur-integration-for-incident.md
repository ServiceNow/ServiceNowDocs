---
title: Activate Universal Request Integration for Incident management
description: You can activate the Universal Request: Integration for Incident management plugin \(com.snc.incident.universal\_request\) if you have the admin role. Activating this plugin enables ServiceNow Incident Management application integration with Universal Request. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Universal Request plugins, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Activate Universal Request Integration for Incident management

You can activate the Universal Request: Integration for Incident management plugin \(com.snc.incident.universal\_request\) if you have the admin role. Activating this plugin enables ServiceNow Incident Management application integration with Universal Request. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Before installing the Universal Request Integration for Incident management \(com.snc.incident.universal\_request\) plugin, install the Universal Request plugin.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Universal Request plugins](../concept/ur-plugins.md)

**Related topics**  


[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

