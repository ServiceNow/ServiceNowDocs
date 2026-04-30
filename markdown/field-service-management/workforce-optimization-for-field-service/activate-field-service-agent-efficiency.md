---
title: Activate Field Service Agent Efficiency
description: You can activate the Field Service Agent Efficiency plugin \(com.snc.fsm\_agent\_efficiency\) if you have the admin role. The application includes demo data and installs related plugins if they are not already installed.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Efficiency, Set up workforce, Configure, Field Service Management]
---

# Activate Field Service Agent Efficiency

You can activate the Field Service Agent Efficiency plugin \(com.snc.fsm\_agent\_efficiency\) if you have the admin role. The application includes demo data and installs related plugins if they are not already installed.

## Before you begin

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate this feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

The following items are installed with Field Service Agent Efficiency:

-   Plugins
-   Tables

For more information, see [Field Service Agent Efficiency components](../reference/field-service-agent-efficiency-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Agent Efficiency plugin \(com.snc.fsm\_agent\_efficiency\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


