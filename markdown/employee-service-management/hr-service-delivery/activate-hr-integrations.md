---
title: Activate HR Integrations
description: You can activate Human Resources Scoped App: Integrations \[com.sn\_hr\_integrations\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Activate HR Integrations

You can activate Human Resources Scoped App: Integrations \[com.sn\_hr\_integrations\] if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Human Resources Scoped App: Integrations allows you to integrate HR Service Delivery with third-party systems.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with HR Integrations](../reference/components-installed-with-hr-integrations.md)**  
Several types of components install with the activation of the HR Integrations plugin, including tables, user roles, and scheduled jobs.

**Parent Topic:**[HR Integrations](../concept/scoped-hr-third-party-integrations.md)

