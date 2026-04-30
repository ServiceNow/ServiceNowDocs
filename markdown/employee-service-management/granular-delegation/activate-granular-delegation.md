---
title: Activate Granular Delegation
description: You can activate the Granular Delegation plugin \(com.glide.granular\_service\_delegation\) for the ServiceNow AI Platform if you have the admin role.
locale: en-US
release: xanadu
product: Granular Delegation
classification: granular-delegation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Granular Delegation, Granular Delegation, Employee Service Management]
---

# Activate Granular Delegation

You can activate the Granular Delegation plugin \(com.glide.granular\_service\_delegation\) for the ServiceNow AI Platform if you have the admin role.

## Before you begin

Role required: admin

If the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is activated, the Employee Center is also included. On-demand delegations can be performed with the Employee Center or the ServiceNow® mobile.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Granular Delegation plugin \(com.glide.granular\_service\_delegation\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


