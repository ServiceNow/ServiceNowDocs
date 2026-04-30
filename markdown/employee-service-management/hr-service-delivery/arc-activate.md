---
title: Activate the Anonymous Report Center
description: You can activate the Anonymous Report Center plugin \(com.sn\_anonymous\_report\_center\) for the ServiceNow AI Platform if you have the admin role.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Anonymous Report Center \(ARC\), Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Activate the Anonymous Report Center

You can activate the Anonymous Report Center plugin \(com.sn\_anonymous\_report\_center\) for the ServiceNow AI Platform if you have the admin role.

## Before you begin

If the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is activated, the Employee Center is also included. On-demand delegations can be performed with the Employee Center or the ServiceNow® mobile.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Anonymous Report Center plugin \(com.sn\_anonymous\_report\_center\)using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


