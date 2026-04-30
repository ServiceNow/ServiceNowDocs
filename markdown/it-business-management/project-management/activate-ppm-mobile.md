---
title: Activate Mobile Project Status
description: Activate the MobilenProject Status application from ServiceNow Store, earlier known as PPM Mobile \(com.sn\_ppm\_mobile\), if you have an admin role. Installing this application also activates related plugins if they are not already active.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage status of your projects using Project Status application, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Activate Mobile Project Status

Activate the MobilenProject Status application from ServiceNow Store, earlier known as PPM Mobile \(com.sn\_ppm\_mobile\), if you have an admin role. Installing this application also activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Mobile: Project Status activates the following related plugin if it is not already active.

<table id="table_njl_r1x_c3b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project Portfolio Suite with Financials\[com.snc.financial\_planning\_pmo\]

</td><td>

Enables you to manage your demands, resources, portfolios and projects. It also helps you plan, track, and manage the cost and budget of projects and demands in a portfolio to strike a balance between investment and returns.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

