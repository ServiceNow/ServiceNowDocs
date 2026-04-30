---
title: Activate PPM Standard \(Project Portfolio Management\)
description: Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) if you have the admin role. This plugin installs the Project Portfolio Management applications.
locale: en-US
release: zurich
product: PPM Collaboration
classification: ppm-collaboration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Project Portfolio Management, Strategic Portfolio Management]
---

# Activate PPM Standard \(Project Portfolio Management\)

Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) if you have the admin role. This plugin installs the Project Portfolio Management applications.

## Before you begin

Role required: admin

## About this task

The PPM Standard is the basic plugin for the PPM \(Project Portfolio Management\) applications.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


## Result

All PPM applications are installed in your ServiceNow instance, along with their user roles and tables. For more information, see [Components installed with Project Portfolio Management \(PPM\) Standard](../reference/r_InstalledWithProjectPortfolioSuiteWithFinancials.md).

**Parent Topic:**[Project Portfolio Management](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)

