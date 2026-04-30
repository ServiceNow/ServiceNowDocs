---
title: Activate Test Management
description: To activate the Test Management \(com.snc.test\_mgmt\) plugin you must have an admin role.
locale: en-US
release: zurich
product: Test Management
classification: test-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Test Management 1.0, Test Management applications, Strategic Portfolio Management]
---

# Activate Test Management

To activate the Test Management \(com.snc.test\_mgmt\) plugin you must have an admin role.

## Before you begin

Role required: admin

## About this task

**Note:**

There are two ways to activate the Test Management plugin:

-   [As an individual application](t_ActivateTestManagement.md)
-   As part of the Project Portfolio Suite with Financials plugin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


