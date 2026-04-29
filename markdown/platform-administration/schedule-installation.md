---
title: Schedule installation
description: Schedule the installation of a plugin, application, or product at the required time from your ServiceNow instance. You can simultaneously schedule multiple installations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Schedule installation

Schedule the installation of a plugin, application, or product at the required time from your ServiceNow instance. You can simultaneously schedule multiple installations.

## Before you begin

**Note:**

Legacy Application Manager is being deprecated. Starting with Australia patch 1, Legacy Application Manager is no longer available and bookmarks will redirect to the new Application Manager experience.

A known issue affects the use of bookmarks to access the Legacy Application Manager before Australia patch 1. For details about possible issues with accessing the Legacy Application Manager, see the [Deprecated Classic App Manager URL usage causes issues on instances running ZP5 / YP10 and above \[KB2804238\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2804238) article in the Now Support knowledge base.

A new Application Manager experience is available. The new experience simplifies the process of managing your licensed applications by consolidating them in one convenient location, displaying all applications, plugins, installed applications, and available updates. For more information, see [Application Manager](../../../administer/application-manager/concept/application-manager.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the required plugin, application, or product.

3.  Click the schedule installation icon \(![Schedule installation icon.](../image/schedule-installation-icon.png) \).

    **Note:**

    -   If the app is blocked from installation, the installation and schedule installation icons are disabled.
    -   You can't schedule the installation of an in-development plugin.
4.  Specify the time at which you want to schedule the installation.

    ![Schedule the installation time.](../image/schedule-time.png)

5.  Click **Next**.

    **Note:** If another installation is scheduled at the same time, a message is displayed that the installation can't be scheduled at the mentioned time and auto-populates the next available slot.

    ![Information message about the scheduled installation.](../image/schedule-message.png)

6.  In the Schedule Activation window, choose the option to reschedule if the scheduled installation doesn't complete.

    The admin can choose to retry the installation once or exit the installation.

    ![Reschedule options.](../image/schedule-option.png)

    The installation is scheduled and a confirmation message is displayed.


## What to do next

Click the schedule summary icon \(![Schedule summary icon.](../image/schedule-summ-icon.png) \) to view the installation status and schedule calendar.

![Schedule summary.](../image/schedule-summary.png)

-   To view the status of the installation, click **View Status**.
    -   If the installation is successful, the details of the plugin, application, or product are displayed.
    -   If the installation fails, the reason for the failure is displayed along with other details.
-   To reschedule or delete the scheduled installation, click **Reschedule** or **Delete** in the app tile.

    ![Reschedule or delete the schedule installation.](../image/reschdule-delete.png)

    **Note:** If you have scheduled the installation of a product, all apps in the product will also be scheduled for installation. However, you can't modify or delete the schedule of an individual app. You can only modify or delete the schedule of the product.

-   To view the schedule of installations, click **Full schedule**. A calendar displays the details of the scheduled installations.

**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)

