---
title: Activate Lifecycle Events
description: You can activate Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Activate Lifecycle Events

You can activate Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Human Resources Scoped App: Lifecycle Events enables you to easily configure digital workflows to manage employee lifecycle events through a single service delivery platform.

It activates these related plugins if they are not already active.

<table id="table_otq_5ld_dbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Human Resources Scoped App: Core\[com.sn\_hr\_core\]

</td><td>

Provides core HR features.

</td></tr><tr><td>

Employee Center

 \[com.sn\_hr\_service\_portal\]

</td><td>

Provides Employee Center.

</td></tr></tbody>
</table>-   **Using Agent Workspace with Lifecycle Events**

    To use Agent Workspace with Lifecycle Events, you must activate:

    Human Resources Scoped App: Workspace \[com.sn\_hr\_agent\_workspace\] plugin

-   **Using Playbook with Lifecycle Events**

    To use Agent Workspace and Playbook with Lifecycle Events, you must request the Playbook plugin from the ServiceNow Store.

    **Note:** For more information on requesting a ServiceNow Store plugin, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallApplications.md).


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Lifecycle event script includes and APIs](../concept/LEScriptIncludes.md)**  
Script includes call workflows within Lifecycle Events.
-   **[Lifecycle Events workflows](../concept/LEWorkflow.md)**  
The **HR Activity Set Launcher** workflow drives the entire lifecycle event process. Associated workflows drive each of the activity sets within a lifecycle event.

**Parent Topic:**[Configuring Lifecycle Events](../concept/configuring-lifecycle-events.md)

