---
title: Activate Problem Management Best Practice — Madrid
description: Activate the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) plugin if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Problem Management plugins, Configuring Problem Management, Problem Management, IT Service Management]
---

# Activate Problem Management Best Practice — Madrid

Activate the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) plugin if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

The Problem Management Best Practice — Madrid plugin identifies the cause of a service interruption reported by a significant or recurring incidents. The plugin does the following activities:

-   Provides roles for problem management including a problem task analyst, a problem coordinator, a problem manager, and a problem administrator.
-   Provides fields to record the category where the issue was first reported, the workaround, the cause notes, and the fix notes.
-   Searches for and attaches knowledge articles.
-   Communicates when a workaround or fix is available.
-   Clears the **Assigned to** field when changing the **Assignment Group**.

**Note:** The plugin is activated by default for the new customers. Existing customers need to request the plugin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Problem Management](../reference/installed-with-madrid-best-prac.md)**  
Several types of components are installed with activation of the Problem Management Best Practice — Madrid plugin, including user roles.

**Parent Topic:**[Problem Management plugins](../concept/problem-mgmt-plugins.md)

**Related topics**  


[List of Australia plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

