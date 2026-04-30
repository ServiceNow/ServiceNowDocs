---
title: Activate Field Service Multi-Day Task Scheduling
description: Install the Field Service Multi-Day Task Scheduling application to enable scheduling of work order tasks across multiple days. You can activate the Field Service Multi-Day Task Scheduling plugin \(com.snc.fsm\_multiday\_tasks\) for Field Service if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Multi-day scheduling, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Activate Field Service Multi-Day Task Scheduling

Install the Field Service Multi-Day Task Scheduling application to enable scheduling of work order tasks across multiple days. You can activate the Field Service Multi-Day Task Scheduling plugin \(com.snc.fsm\_multiday\_tasks\) for Field Service if you have the admin role.

## Before you begin

-   Field Service Multi-Day Task Scheduling requires you to install the Field Service Management plugin. For more information about activating Field Service Management, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Multi-Day Task Scheduling plugin \(com.snc.fsm\_multiday\_tasks\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


## Result

The Field Service Multi-Day Task Scheduling plugin when activated successfully adds the following attributes:

-   The **Assign across the schedule entries** option is added to the work order task form.
-   The **sn\_fsm\_multiday.minDurationForFirstWorkSchedule** property is added to the Field Service Dynamic Scheduling Properties page. For more information about enabling a dynamic scheduling property, see [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).
-   The **sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.enableTwoAndFourWeeks** property is added to the Field Service Dispatcher Workspace set of properties. For more information about enabling a Workspace Settings property, see [Configure settings for Dispatcher Workspace](configure-workspce-settings.md).

