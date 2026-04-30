---
title: Activate Field Service Task Bundling
description: Activate the Task Bundling plugin \(com.snc.fsm\_task\_bundle\) for Field Service Management if you have the admin role.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Task Bundling, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Activate Field Service Task Bundling

Activate the Task Bundling plugin \(com.snc.fsm\_task\_bundle\) for Field Service Management if you have the admin role.

## Before you begin

Role required: admin

## About this task

The ability to bundle work order tasks in Dispatcher Workspace is installed with Field Service Task Bundling.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Task Bundling plugin \(com.snc.fsm\_task\_bundle\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


