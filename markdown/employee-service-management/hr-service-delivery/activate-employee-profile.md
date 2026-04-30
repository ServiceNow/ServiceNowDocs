---
title: Activate Employee Profile
description: You can activate the Employee Profile plugin \[sn\_employee\] if you have the admin role.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Employee Profile table, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Activate Employee Profile

You can activate the Employee Profile plugin \[sn\_employee\] if you have the admin role.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Employee Profile](../reference/installed-with-employee-profile.md)**  
Several types of components are installed with activation of the Employee Profile \[sn\_employee\_profile\] plugin, including tables, user roles, and scheduled jobs.

**Parent Topic:**[Employee Profile table](../concept/employee-profile.md)

