---
title: Activate Proxy Actions for Field Service Management
description: You can activate the Proxy Actions for Field Service Management plugin \(sn\_fsm\_proxy\_actn\) if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/fsm-proxy-action.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring proxy actions, Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Activate Proxy Actions for Field Service Management

You can activate the Proxy Actions for Field Service Management plugin \(sn\_fsm\_proxy\_actn\) if you have the admin role.

## Before you begin

Role required: admin

## About this task

Proxy Actions for Field Service Management installs the proxy\_admin and proxy\_agent roles, and the tables used to configure and log proxy actions.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Proxy Actions for Field Service Management plugin \(sn\_fsm\_proxy\_actn\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/find-components.md).


