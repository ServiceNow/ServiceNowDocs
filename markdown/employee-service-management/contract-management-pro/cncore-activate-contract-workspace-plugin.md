---
title: Activate Contract Workspace
description: You can activate the Contract Workspace plugin \(sn\_cm\_workspace\) for Contract Management Pro if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Contract Workspace with UI Builder components, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Activate Contract Workspace

You can activate the Contract Workspace plugin \(sn\_cm\_workspace\) for Contract Management Pro if you have the admin role.

## Before you begin

Review the [Contract Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/1803d03a37023110da6cdf3c24924bab) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

Two roles are installed with the Contract Workspace plugin.

For more information, see [Components installed with Contract Workspace](../reference/cncore-comp-contract-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Contract Workspace plugin \(sn\_cm\_workspace\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


