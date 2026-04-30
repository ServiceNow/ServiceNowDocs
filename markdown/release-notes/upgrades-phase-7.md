---
title: Phase 7 - Upgrade the production instance
description: After you have upgraded your development, non-production, and test instances, upgrade your production instance last. Then validate that the upgrade was complete, apply update sets and fix scripts, and perform post-upgrade user acceptance testing \(UAT\).
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Upgrade to the Zurich release, Zurich release notes]
---

# Phase 7 - Upgrade the production instance

After you have upgraded your development, non-production, and test instances, upgrade your production instance last. Then validate that the upgrade was complete, apply update sets and fix scripts, and perform post-upgrade user acceptance testing \(UAT\).

## Before you begin

Role required: admin.

## About this task

![Upgrade progress bar](../image/progress-bar-phase-7.png)

## Procedure

1.  Schedule the upgrade in Now Support.

    1.  Log in to Now Support.

    2.  Click **Instances** in the left navigation menu.

    3.  Select **Manage Instances**.

    4.  Partners only: From the user menu, use the **Switch Company** feature to select a company.

    5.  Select the instance that you want to upgrade or patch.

    6.  In the **Actions** menu, click **Upgrade Instance**.

        The **Upgrade an Instance** Service Catalog item opens up. It is prepopulated with the instance name and available versions to which you can upgrade or patch the instance.![Upgrade an instance dialog](../image/upgrades-dashboard.png)

    7.  To specify a date and time for the upgrade or patch, click the calendar icon next to the **Start Date and Time** field.

    8.  Click the clock icon to select the time for the upgrade or patch.

        **Note:** Setting the time for an upgrade or patch is important. Set the upgrade or patch to start 10–15 minutes before the **Check distribution for possible upgrade** scheduled job runs. This setting allows enough time for the upgrade or patch request to update Now Support 's records about which release version your instance should be on before the **Check distribution for possible upgrade** scheduled job runs.

    9.  Click **Submit**.

        A confirmation message appears. If you do not need an entitlement, a change request is created.

2.  If applicable, request a version entitlement.

    1.  In the **Actions** column, click **Schedule**.

        If the version does require an entitlement, this screen appears:

        ![Requires entitlement approval message](../image/upgrades-schedule-with-ent.png)

    2.  Click the calendar icon and specify a date and time at least three days in the future.

        ServiceNow entitlement managers respond to your entitlement request within three days.

        **Note:** Setting the time for an upgrade or patch is important. Set the upgrade or patch to start 10–15 minutes before the **Check distribution for possible upgrade** scheduled job runs. This setting allows enough time for the upgrade or patch request to update Now Support 's records about which release version your instance should be on before the **Check distribution for possible upgrade** scheduled job runs.

    3.  Click **Schedule**.

        A confirmation message appears. If you need an entitlement, the entitlement request number is included. Click the entitlement request number to view the request.

    4.  If you have any questions about your entitlement, comment on your entitlement request after you have submitted it.

3.  Monitor the upgrade to your instance and validate that the upgrade to your production instance is complete.

    There are several methods of verifying that your upgrade is complete:

    -   Navigate to the **System Diagnostics** &gt; **Upgrade Monitor**.
    -   Navigate to **System Diagnostics** &gt; **Upgrade Log** and locate the `Notifying HI that upgrade has been completed` message.
    -   Navigate to **System Definition** &gt; **System Upgrades**. Information about all system upgrades is listed.
    -   Navigate to **System Diagnostics** &gt; **Upgrade History** and search for the most recent upgrade.
4.  Apply any update sets and post-upgrade fix scripts that you have.

5.  Validate and test your instance by conducting user acceptance testing \(UAT\).

    Performance and operating information is available in the system logs, which offer an excellent source of information for evaluating the inner workings of a ServiceNow instance. Use this information to help resolve as many errors as possible. To access the log data, navigate to **System Logs** &gt; **System Log** &gt; **Errors**.

    **Note:** Not all errors in the error log are results of your upgrade. Error messages are often present in pre-upgrade instances, and many of these messages do not affect users or performance.


