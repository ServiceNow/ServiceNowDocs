---
title: Activate Dispatcher Workspace
description: You can activate the Dispatcher Workspace plugin \(sn\_fsm\_disp\_wrkspc\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related plugins if they are not already installed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Activate Dispatcher Workspace

You can activate the Dispatcher Workspace plugin \(sn\_fsm\_disp\_wrkspc\) for Field Service Management if you have the admin role. The application includes demo data and installs related plugins if they are not already installed.

## Before you begin

Role required: admin.

## About this task

Activation of Field Service Management Dispatcher Workspace \[sn\_fsm\_disp\_wrkspc\] plugin activates the following plugins.

<table id="table_fmk_ryw_jyb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Service Management Configurable Workspace\[com.snc.uib.fsm\_agent\_workspace\].

</td><td>

Provides the components, lists, and forms to support Field Service Management on CSM Configurable Workspace.

</td></tr><tr><td>

sn-fsm-components\[com.sn\_fsm\_components\].

</td><td>

Provides the repository in which to store Field Service Management custom components to be used in the UI Builder.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the **FSM Configurable Dispatcher Workspace** plugin \(sn\_fsm\_disp\_wrkspc\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


