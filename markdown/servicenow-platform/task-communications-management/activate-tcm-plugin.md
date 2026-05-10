---
title: Activate Task Communications Management
description: The Task Communications Management plugin \(com.snc.task\_communication\_management\) is activated when you activate the Incident Communications Management plugin \(com.snc.iam\) or the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Task Communications Management
classification: task-communications-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Communications Management plugins, Task Communications Management, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate Task Communications Management

The Task Communications Management plugin \(com.snc.task\_communication\_management\) is activated when you activate the Incident Communications Management plugin \(com.snc.iam\) or the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Task Communications Management activates these related plugins if they are not already active.

<table id="table_gy1_jjl_2db"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contact Management \[com.snc.contact\_management\]

</td><td>

The Contact Management plugin manages the connections between users or groups and other resources in the system.

</td></tr><tr><td>

Targeted Communications \[com.sn\_publications\]

</td><td>

The Targeted Communications plugin provides a way to publish and send out newsletter like articles to targeted internal or external customers.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Task Communications Management](../reference/components-installed-with-tcm.md)**  
Several types of components are installed with the Task Communications Management plugin, including tables and user roles.

**Parent Topic:**[Task Communications Management plugins](../concept/tcm-plugins.md)

**Related topics**  


[Install Collaboration Services for Task Communications Management](install-collab-services-for-tcm.md)

[List of plugins \(Australia\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

