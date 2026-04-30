---
title: Activate Localization Framework
description: You can activate the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) for Localization Framework if you have the admin role. The application installs related plugins if they are not already installed. Optionally, you can activate plugins for the Localization Framework Hub and Spoke architecture on a set of instances.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2024-11-20"
reading_time_minutes: 2
breadcrumb: [Activating the Localization Framework, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate Localization Framework

You can activate the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) for Localization Framework if you have the admin role. The application installs related plugins if they are not already installed. Optionally, you can activate plugins for the Localization Framework Hub and Spoke architecture on a set of instances.

## Before you begin

Role required: admin

## About this task

The Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) can be activated in two ways:

-   Manual installation of the plugin.
-   Auto-installation of the plugin.

    When a language plugin is installed, the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) is automatically installed with the language plugin. For more information, see [language plugins](../../localization/task/t_ActivateALanguage.md).


The following items are installed with Localization Framework:

-   Plugins
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Localization Framework](../reference/components-installed-with-lf.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Optionally, next you can install plugins for the [Localization Framework Hub and Spoke architecture](../concept/localization-framework-hub-spoke-architecture.md). This enables you to designate one instance as a hub to fulfill localization requests, and one or more instances as spokes that submit requests to the hub.

Decide which instance should function as the hub. On that instance, follow the above procedure to search for and install the Localization Framework Hub plugin \[com.sn.localization\_framework.hub\].

Decide which instance\(s\) should function as spokes. On each of those instances, follow the above procedure to search for and install the Localization Framework Spoke plugin \[com.sn.localization\_framework.spoke\].

**Parent Topic:**[Activating the Localization Framework](../concept/activation-localization-framework.md)

