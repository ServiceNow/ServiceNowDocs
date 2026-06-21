---
title: Schedule installation
description: Schedule the installation of a plugin, application, or product at the required time from your ServiceNow instance. You can simultaneously schedule multiple installations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/schedule-installation.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Schedule installation

Schedule the installation of a plugin, application, or product at the required time from your ServiceNow instance. You can simultaneously schedule multiple installations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the required plugin, application, or product.

3.  Click the schedule installation icon \(\[Omitted image "schedule-installation-icon.png"\] Alt text: Schedule installation icon. \).

    **Note:**

    -   If the app is blocked from installation, the installation and schedule installation icons are disabled.
    -   You can't schedule the installation of an in-development plugin.
4.  Specify the time at which you want to schedule the installation.

    \[Omitted image "schedule-time.png"\] Alt text: Schedule the installation time.

5.  Click **Next**.

    **Note:** If another installation is scheduled at the same time, a message is displayed that the installation can't be scheduled at the mentioned time and auto-populates the next available slot.

    \[Omitted image "schedule-message.png"\] Alt text: Information message about the scheduled installation.

6.  In the Schedule Activation window, choose the option to reschedule if the scheduled installation doesn't complete.

    The admin can choose to retry the installation once or exit the installation.

    \[Omitted image "schedule-option.png"\] Alt text: Reschedule options.

    The installation is scheduled and a confirmation message is displayed.


## What to do next

Click the schedule summary icon \(\[Omitted image "schedule-summ-icon.png"\] Alt text: Schedule summary icon. \) to view the installation status and schedule calendar.

\[Omitted image "schedule-summary.png"\] Alt text: Schedule summary.

-   To view the status of the installation, click **View Status**.
    -   If the installation is successful, the details of the plugin, application, or product are displayed.
    -   If the installation fails, the reason for the failure is displayed along with other details.
-   To reschedule or delete the scheduled installation, click **Reschedule** or **Delete** in the app tile.

    \[Omitted image "reschdule-delete.png"\] Alt text: Reschedule or delete the schedule installation.

    **Note:** If you have scheduled the installation of a product, all apps in the product will also be scheduled for installation. However, you can't modify or delete the schedule of an individual app. You can only modify or delete the schedule of the product.

-   To view the schedule of installations, click **Full schedule**. A calendar displays the details of the scheduled installations.

**Parent Topic:**[Using Legacy Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/using-legacy-application-manager.md)

