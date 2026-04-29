---
title: Activate Workplace Lease Administration
description: You can activate the Workplace Lease Administration plugin \(sn\_wsd\_la\) for Workplace Lease Administration if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Workplace Lease Administration
classification: workplace-lease-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Workplace Lease Administration, Workplace Lease Administration, Workplace Service Delivery, Employee Service Management]
---

# Activate Workplace Lease Administration

You can activate the Workplace Lease Administration plugin \(sn\_wsd\_la\) for Workplace Lease Administration if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Workplace Lease Administration requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

The following items are installed with Workplace Lease Administration:

-   Plugins
-   Roles
-   Tables

For more information, see [Components installed with Workplace Lease Administration](../reference/component-installed-lease-admin.md) and [Scripts installed with Workplace Lease Administration](../reference/scripts-lease-admin.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Workplace Lease Administration plugin \(sn\_wsd\_la\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configure Workplace Lease Administration](../concept/config-lease-administration.md)

