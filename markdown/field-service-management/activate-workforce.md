---
title: Activate Field Service Manager Workforce
description: Activate the Workforce plugin to start using Workforce for Field Service Management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Activate Field Service Manager Workforce

Activate the Workforce plugin to start using Workforce for Field Service Management.

## Before you begin

Field Service Manager Workforce requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

Installing Field Service Manager Workforce also installs Dispatcher Workspace \(sn\_fsm\_disp\_wrkspc\).

For more information, see [Configuring Workforce](../concept/configuring-workforce.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Manager Workforce plugin \(com.snc.fsm\_manager\_workforce\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


