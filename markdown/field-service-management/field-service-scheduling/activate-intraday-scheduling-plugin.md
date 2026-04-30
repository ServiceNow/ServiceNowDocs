---
title: Activate intra-day schedule automation
description: You can activate the Field Service Management Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) for Field Service Management if you have the admin role. After the plugin is installed, three flow designer flows and nine subflows are added to your instance.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Intraday schedule automation, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Activate intra-day schedule automation

You can activate the Field Service Management Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) for Field Service Management if you have the admin role. After the plugin is installed, three flow designer flows and nine subflows are added to your instance.

## Before you begin

Role required: admin

## About this task

For more information, see [Intra-day schedule automation flows and subflows](../reference/intraday-scheduling-flows.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Management Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


