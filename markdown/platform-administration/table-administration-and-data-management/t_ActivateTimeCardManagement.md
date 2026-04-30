---
title: Activate Time Card Management
description: Administrators can activate the Time Card Management plugin \(com.snc.time\_card\). The plugin also activates the Performance Analytics - Content Pack - Project Portfolio Suite Dashboards plugin \(com.snc.pa.time\_card\). However, you need a Performance Analytics license to use the dashboards.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Time Card management, Working with Task table, Table admin, Tables and data, Configure core features, Administer]
---

# Activate Time Card Management

Administrators can activate the Time Card Management plugin \(com.snc.time\_card\). The plugin also activates the Performance Analytics - Content Pack - Project Portfolio Suite Dashboards plugin \(com.snc.pa.time\_card\). However, you need a Performance Analytics license to use the dashboards.

## Before you begin

Role required: admin

## About this task

**Note:** The Time Card Management plugin also gets activated as part of [PPM Standard](https://www.servicenow.com/docs/access?context=t_ActivateProjectPortfolioSuiteWithFinancials&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) plugin \(com.snc.financial\_planning\_pmo\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Time Card Management](../concept/time-card-management.md)

