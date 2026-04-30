---
title: Activate Release Management
description: Activate the Release Management plugin \(com.snc.release\_management\_v2\) with the admin role.
locale: en-US
release: yokohama
product: Release Management
classification: release-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Release Management, IT Service Management]
---

# Activate Release Management

Activate the Release Management plugin \(com.snc.release\_management\_v2\) with the admin role.

## Before you begin

Role required: admin

## About this task

For more information, see [Components installed with Release Management](../reference/components-installed-with-release-management-v2.md) v2.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Release Management v2](../concept/configuring-release-management.md)

