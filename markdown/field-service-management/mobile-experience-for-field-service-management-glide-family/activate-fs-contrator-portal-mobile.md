---
title: Activate the Field Service Contractor for mobile feature in the Now Mobile Agent application
description: Activate the Field Service Contractor for mobile plugin \(com.snc.fsm\_ext\_mobile\) to manage work order tasks assigned to the contractor company. This plugin activates related plugins if they are not already active.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile app, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Activate the Field Service Contractor for mobile feature in the Now Mobile Agent application

Activate the Field Service Contractor for mobile plugin \(com.snc.fsm\_ext\_mobile\) to manage work order tasks assigned to the contractor company. This plugin activates related plugins if they are not already active.

## Before you begin

Field Service Contractor for mobile requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

My work, Articles, Notifications, My Incidentals and More applets, navigation tabs are activated by default for both new and upgrade customers when they activate using the Field Service Contractor for mobile plugin \(com.snc.fsm\_ext\_mobile\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Contractor for mobile plugin \(com.snc.fsm\_ext\_mobile\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


