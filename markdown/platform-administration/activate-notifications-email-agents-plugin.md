---
title: Activate Notifications Email Agents plugin
description: You can activate the Notifications Email Agents plugin \(sn\_notif\_agents\) for Notifications if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure email agentic workflows, Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate Notifications Email Agents plugin

You can activate the Notifications Email Agents plugin \(sn\_notif\_agents\) for Notifications if you have the admin role.

## Before you begin

Now Assist for Notifications requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: sn\_notif\_agents.notification\_ai\_admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Notifications Email Agents plugin \(sn\_notif\_agents\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Enable intent to action from [Inbound email actions](enable-intent-to-action.md) or [Inbound email triggers in Workflow Studio](trigger-intent-to-action.md).

