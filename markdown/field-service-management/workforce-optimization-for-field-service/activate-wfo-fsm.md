---
title: Activate Workforce Optimization for Field Service
description: You can activate the Workforce Optimization for Field Service plugin \(com.snc.app\_fsm\_wfo\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workforce Optimization, Set up workforce, Configure, Field Service Management]
---

# Activate Workforce Optimization for Field Service

You can activate the Workforce Optimization for Field Service plugin \(com.snc.app\_fsm\_wfo\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Workforce Optimization for Field Service solution is highly modular, offering a wide range of capabilities such as Scheduling, Coaching, and Teams applications in Field Service Manager Workspace. Workforce Optimization for Field Service \(com.snc.app\_fsm\_wfo\) plugin activates all other dependent plugins to enable users to the Scheduling, Coaching, and Teams applications in Workforce Optimization for Field Service.

Workforce Optimization for Field Service requires the following ServiceNow Store applications. Ensure that these applications are installed before you install Workforce Optimization for Field Service.

-   **Required ServiceNow Store applications to use in Field Service Manager Workspace**
    -   **Shift Scheduling for Field Service \(com.snc.sn\_fsm\_shift\_schdl\)**

        Integrate the agent shift scheduling functionalities for Field Service Management Workforce Optimization. For ServiceNow Store installation steps, see Install a ServiceNow Store application.

    -   **Team Management for Field Service \(com.snc.sn\_fsm\_team\_mgmt \)**

        Implements team performance functionalities for Field Service Management Workforce Optimization. For ServiceNow Store installation steps, see Install a ServiceNow Store application.

    -   **Coaching \(com.sn\_coaching\)**

        Facilitates the coaching of employees on their work through the use of coaching opportunities that can be conditionally configured. For ServiceNow Store installation steps, see Install a ServiceNow Store application.

    -   **Coaching with Learning \(com.sn\_coach\_learning\)**

        Coach employees on their work through the use of coaching opportunities, taking advantage of critical moments in a process, that can be conditionally configured. For ServiceNow Store installation steps, see Install a ServiceNow Store application.


Role required: admin

## About this task

The following items are installed with Workforce Optimization for Field Service:

-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Workforce Optimization for Field Service components](../reference/components-wfo-fsm.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Workforce Optimization for Field Service plugin \(com.snc.app\_fsm\_wfo \) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## Result

The Workforce Optimization for Field Service plugin when activated successfully adds **Enable Shift Scheduling for FSM to Determine Availability** to the Field Service configurations inside the Assignment tab.

**Note:** You must enable the **Enable Shift Scheduling for FSM to Determine Availability** toggle switch after setting up schedules, skills, teams, and coaching for your agents to optimize your Field Service workforce accordingly.

