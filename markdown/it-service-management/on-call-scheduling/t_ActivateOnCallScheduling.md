---
title: Activate On-Call Scheduling
description: You can activate the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin if you have the admin role.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, On-Call Scheduling, IT Service Management]
---

# Activate On-Call Scheduling

You can activate the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin if you have the admin role.

## Before you begin

Role required: admin

## About this task

Activating the On-Call Scheduling plugin activates the following third-party libraries:

-   Subscription-based notifications
-   Advanced Schedules support
-   NG shared components
-   ServiceNow common calendar
-   Fullcalendar library

**Note:** The On-Call Scheduling plugin \(com.snc.on\_call\_rotation\) is active by default for zBoot customers.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configuring On-Call Scheduling](../concept/configuration.md)

**Related topics**  


[On-Call Scheduling](../../on-call-scheduling/concept/c_OnCallScheduling.md)

