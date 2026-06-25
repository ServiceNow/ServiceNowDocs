---
title: Activate KCS Integration for Incident Management
description: Activate the KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) if you have the admin role. This plugin provides integration of Incident Management with the Advanced Knowledge Management features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/activate-kcs-integration-for-im.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Incident Management plugins, Reference, Incident Management, IT Service Management]
---

# Activate KCS Integration for Incident Management

Activate the KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) if you have the admin role. This plugin provides integration of Incident Management with the Advanced Knowledge Management features.

## Before you begin

Role required: admin

## About this task

The KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\) activates the Knowledge Management Advanced Installer plugin.

<table id="table_cgl_kgd_tgb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Management Advanced Installer\[com.snc.knowledge\_advanced.installer\]

</td><td>

Use this plugin to install the Knowledge Management Advanced plugin. Activating or upgrading this plugin validates knowledge articles and knowledge bases to ensure that the Knowledge Management Advanced plugin can be successfully installed.

</td></tr></tbody>
</table>After activating this plugin, agents can create knowledge articles directly from resolved incidents by using the **Create Knowledge** option available for the Incident Form. For more information, see [Create a knowledge article from an incident using an article template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/create-a-knowledge-article.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


-   **[Component installed with KCS Integration for Incident Management plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/installed-with-incident-mgmt.md)**  
The Incident KCS Article table is installed with the activation of the KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\).

**Parent Topic:**[Incident Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/incident-mgmt-plugins.md)

**Related topics**  


[List of Australia plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

[Create a knowledge article from an incident using an article template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/create-a-knowledge-article.md)

[Create a knowledge article from an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/create-knowledge-incident.md)

