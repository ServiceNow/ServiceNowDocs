---
title: Activate Problem Management
description: You can activate the Problem Management plugin \(com.snc.problem\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Problem Management plugins, Configuring Problem Management, Problem Management, IT Service Management]
---

# Activate Problem Management

You can activate the Problem Management plugin \(com.snc.problem\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

The Problem Management plugin activates these related plugins if they are not already active.

<table id="table_ppy_4s5_glb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Problem Overview Homepage\[com.glideapp.report.itsm.problem.overview\]

</td><td>

This plugin delivers content for Problem Overview home page.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Problem Management](../reference/installed-with-pm.md)**  
Several types of components are installed with activation of the Problem Management plugin, including tables.

**Parent Topic:**[Problem Management plugins](../concept/problem-mgmt-plugins.md)

**Related topics**  


[List of plugins \(Xanadu\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

