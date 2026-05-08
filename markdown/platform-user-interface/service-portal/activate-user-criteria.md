---
title: Activate the user criteria for Service Portal plugin
description: You can activate the Service Portal User Criteria Support plugin \(com.glide.service-portal.user-criteria\) if you have the admin role.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [User criteria for Service Portal, Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate the user criteria for Service Portal plugin

You can activate the Service Portal User Criteria Support plugin \(com.glide.service-portal.user-criteria\) if you have the admin role.

## Before you begin

Activating the plugin creates user criteria records for Service Portal records already on the instance. The plugin does not create user criteria for any Service Portal records added by plugins installed after this one. For those records, you must manually create or import the user criteria.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[User criteria for Service Portal](../concept/user-criteria.md)

**Related topics**  


[List of plugins \(Australia\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

