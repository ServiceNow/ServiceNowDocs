---
title: Activate Customer Service Management
description: You can activate the Customer Service \(com.sn\_customerservice\) plugin, if you have the admin role. This plugin includes demo data and activates related plugins if they aren’t already active.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting started with Customer Service Management, Set up your environment, Configure, Customer Service Management]
---

# Activate Customer Service Management

You can activate the Customer Service \(com.sn\_customerservice\) plugin, if you have the admin role. This plugin includes demo data and activates related plugins if they aren’t already active.

## Before you begin

Role required: admin

## About this task

If the related plugins aren’t already active, the Customer Service Management plugin activates them. For more information, see [Plugins activated with Customer Service Management](../reference/plugins-activated-with-csm.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

You can activate several related plugins after activating the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Additional plugins for Customer Service Management](../reference/r_CustServMgmtAddtlPluginsTable.md).

**Parent Topic:**[Customer Service Management](../concept/c_CustomerServiceManagement.md)

