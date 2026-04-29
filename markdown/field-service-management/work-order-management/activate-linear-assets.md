---
title: Activate linear assets support in Field Service Management
description: You can enable the Field Service Management application to support linear assets by activating the Enterprise Asset Management plugin \(com.sn\_eam\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up work orders and tasks, Configure, Field Service Management]
---

# Activate linear assets support in Field Service Management

You can enable the Field Service Management application to support linear assets by activating the Enterprise Asset Management plugin \(com.sn\_eam\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

Linear asset support for Field Service Management requires activation of the following plugins before you install Enterprise Asset Management.

-   **Field Service Management \(com.snc.work\_management\)**

    Enables you to manage work requests that are performed on location by field service agents. For more information, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

-   **Field Service with Service Locations \(com.snc.fsm\_service\_locations\)**

    Enables you to view and select the linear assets on map.

-   **CSM and FSM Configurable Workspace Foundation \(com.snc.uib.cwf\_workspace\)**

    Enables you to create and manage work orders and work order tasks for linear assets.

-   **Dispatcher Workspace \(com.snc.uib.fsm\_dispatcher\_workspace\)**

    Enables you to access and manage work orders and work order tasks for linear assets.

-   **Field Service Mobile \(com.sn\_fsm\_mobile\)**

    Enables you to access the Agent mobile application to manage your work.

-   **Field Service Management Configurable Workspace \(com.snc.uib.fsm\_agent\_workspace\)**

    Provides the components, lists, and forms to support Field Service Management on CSM Configurable Workspace.


Role required: admin

## About this task

The following items are installed with Enterprise Asset Management:

-   Properties
-   Business rules

For more information, see [Linear Assets Support properties](../reference/linear-asset-support-properties.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Enterprise Asset Management plugin \(com.sn\_eam\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Assign work orders for linear assets in Field Service Management](../concept/managing-linear-assets-fsm.md)

