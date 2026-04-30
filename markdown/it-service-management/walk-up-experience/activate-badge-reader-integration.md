---
title: Activate Badge Reader Integration
description: You can activate the Badge Reader Integration plugin \(com.snc.badge\_reader\) if you have the Badge sn\_badge.badge\_admin role.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Activate Badge Reader Integration

You can activate the Badge Reader Integration plugin \(com.snc.badge\_reader\) if you have the Badge sn\_badge.badge\_admin role.

## Before you begin

Role required: sn\_badge.badge\_admin

## About this task

The Badge Reader Integration application is a framework enabling other applications, such as Walk-up Experience, to integrate with badge reader hardware. Administrators configure and manage badge reader clients and integrations by linking badge scanners to walk-up locations and ensuring there is mapping between badge ID numbers and the reader.

Developers can extend the badge scanning framework to trigger actions in other applications based on a badge scan event. The Badge Reader Integration application does not require customization, but is customizable to respond to unique badge system hardware.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Installed with Badge Reader Integration](../reference/installed-with-badge-read-integ.md)**  
Several types of components are installed with activation of the Badge Reader Integration plugin, including tables and user roles.

**Parent Topic:**[Badge Reader Integration for Walk-up Experience](../concept/badge-scan-walkup-onsite.md)

