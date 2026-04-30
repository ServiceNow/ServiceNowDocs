---
title: Activate Universal Request
description: You can activate the Universal Request plugin \(com.snc.universal\_request\) if you have the admin role. This plugin is not active by default, and you must install it to use the Universal Request application. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Universal Request plugins, Configure, Universal Request, Employee Service Management]
---

# Activate Universal Request

You can activate the Universal Request plugin \(com.snc.universal\_request\) if you have the admin role. This plugin is not active by default, and you must install it to use the Universal Request application. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

The Universal Request plugin activates these related plugins if they are not already active.

<table id="table_fdv_mjv_llb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Universal Request: Reporting\[com.snc.universal\_request.reporting\]

</td><td>

To create and view various Universal Request reports.

</td></tr><tr><td>

Agent Workspace \[com.agent\_workspace\]

</td><td>

To create, view, and resolve universal requests from the Agent Workspace.

</td></tr><tr><td>

Agent Assist Recommendation\[com.snc.agent\_recommend\]

</td><td>

To use Agent Assist recommendation in Agent Workspace.

</td></tr><tr><td>

Universal Request Core\[com.snc.universal\_request\_core\]

</td><td>

Contains the data model changes on the Task table to support the Universal Request application.

</td></tr><tr><td>

Service Catalog - Workspace\[com.glideapp.servicecatalog.workspace\]

</td><td>

To use Service Catalog in Agent Workspace.

</td></tr><tr><td>

Service Portal - Standard Ticket\[com.glideapp.servicecatalog.standard\_ticket\]

</td><td>

To enable the Standard Ticket page for your Service Portal.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Universal Request](../reference/installed-with-ur.md)**  
Several types of components are installed with activation of the Universal Request plugin, including tables, user roles, and scheduled jobs.

**Parent Topic:**[Universal Request plugins](../concept/ur-plugins.md)

**Related topics**  


[List of plugins \(Zurich\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

