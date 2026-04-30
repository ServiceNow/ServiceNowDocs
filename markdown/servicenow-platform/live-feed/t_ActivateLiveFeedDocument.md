---
title: Activate the Live Feed Document plugin
description: The Live Feed Document plugin is active by default.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Record feeds, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate the Live Feed Document plugin

The Live Feed Document plugin is active by default.

## Before you begin

Role required: admin

## About this task

Administrators can enable record feeds in an instance by activating the Live Feed Document plugin, which activates the Live Feed plugin if it is not active. For upgrades, administrators must activate the plugin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Record feeds](../concept/c_RecordFeeds.md)

