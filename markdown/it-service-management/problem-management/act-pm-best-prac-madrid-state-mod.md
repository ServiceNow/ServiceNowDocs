---
title: Activate Problem Management Best Practice — Madrid — State Model
description: The Problem Management Best Practice — Madrid — State Model plugin \(com.snc.best\_practice.problem.madrid.state\_model\) introduces new best practice states and guided actions to navigate the life cycle of a problem.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Problem Management plugins, Configuring Problem Management, Problem Management, IT Service Management]
---

# Activate Problem Management Best Practice — Madrid — State Model

The Problem Management Best Practice — Madrid — State Model plugin \(com.snc.best\_practice.problem.madrid.state\_model\) introduces new best practice states and guided actions to navigate the life cycle of a problem.

## Before you begin

Role required: admin

## About this task

The new best practice states are not compatible with the previous version of Problem Management and require verification before this plugin can be activated. The plugin is activated by default for the new customers.

Existing customers should use the [Migration Utility](../concept/migration-utility.md) to verify and migrate to this plugin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Problem Management plugins](../concept/problem-mgmt-plugins.md)

**Related topics**  


[List of Australia plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

