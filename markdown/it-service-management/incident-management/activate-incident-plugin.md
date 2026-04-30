---
title: Activate Incident
description: You can activate the Incident plugin \(com.snc.incident\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Incident Management plugins, Reference, Incident Management, IT Service Management]
---

# Activate Incident

You can activate the Incident plugin \(com.snc.incident\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Incident plugin activates these related plugins if they are not already active.

<table id="table_m4z_wfs_wfb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Management Basics\[com.snc.service\]

</td><td>

Provides the baseline for Service Management functionality.

</td></tr><tr><td>

Incident Management Notification\[com.snc.incident\_notification\]

</td><td>

Provides notification functionality for Incident Management.

</td></tr><tr><td>

Incident Overview Homepage\[com.glideapp.report.itsm.incident.overview\]

</td><td>

Incident Overview Homepage

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with the Incident plugin](../reference/installed-with-incident.md)**  
Several types of components are installed with activation of the Incident plugin in Incident Management.

**Parent Topic:**[Incident Management plugins](../concept/incident-mgmt-plugins.md)

**Related topics**  


[List of Zurich plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

