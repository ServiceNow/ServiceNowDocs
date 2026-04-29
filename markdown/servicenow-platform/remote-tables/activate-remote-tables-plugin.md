---
title: Activate the remote tables plugin
description: If you have the admin role, you can activate the Remote Tables plugin \(com.glide.script.vtable\). This plugin includes demo data and activates related plugins if they aren’t already active.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Activate the remote tables plugin

If you have the admin role, you can activate the Remote Tables plugin \(com.glide.script.vtable\). This plugin includes demo data and activates related plugins if they aren’t already active.

## Before you begin

Role required: admin

## About this task

Remote Tables activates these related plugins if they are not already active.

<table id="table_afh_nxh_5gb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Remote Tables\[com.glide.script.vtable\]

</td><td>

Supports remote tables and associated script definitions that can be used to retrieve and optionally cache data from external sources.

</td></tr><tr><td>

Transformation Service\[com.glide.transform\]

</td><td>

Supports use of Transform APIs that are associated with the remote tables.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Remote tables](../concept/remote-tables.md)

**Related topics**  


[List of plugins \(Australia\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

