---
title: Activate Agile Development 2.0
description: Activate the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) if you have the admin role.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Activate Agile Development 2.0

Activate the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) if you have the admin role.

## Before you begin

Role required: admin

## About this task

-   If you are upgrading from an earlier ServiceNow release version of Agile Development to Agile Development 2.0, read upgrade information before activating the plugin.
-   The dashboards for Agile Development 2.0, if required, must be activated separately using the Performance Analytics – Content Pack – Project Portfolio Suite Dashboards plugin \(com.snc.pps\_dashboards\). The Performance Analytics license is required to use the dashboards.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring Agile Development 2.0](../concept/setting-up-agile-development-2.md)

