---
title: Phase 3 - Verify your upgrade configurations and schedule the development instance upgrade in Now Support
description: Check the configuration of the Check distribution for possible upgrade scheduled job to view how often and when it runs. Review information about timing your upgrade in coordination with the Check distribution for possible upgrade scheduled job. Then, schedule your upgrade in Now Support.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Upgrade to the Zurich release, Zurich release notes]
---

# Phase 3 - Verify your upgrade configurations and schedule the development instance upgrade in Now Support

Check the configuration of the **Check distribution for possible upgrade** scheduled job to view how often and when it runs. Review information about timing your upgrade in coordination with the **Check distribution for possible upgrade** scheduled job. Then, schedule your upgrade in Now Support.

## Before you begin

Role required: admin.

You must check the configuration of the **Check distribution for possible upgrade** and **Check database for possible upgrade** sys\_triggers, which are essential to making sure your instance upgrades to the correct target version.

**Note:** Starting in the Paris release, 'Upgrade' job has been renamed to 'Check distribution for possible upgrade'. In addition, the 'Check Upgrade Script' job has been renamed to 'Check database for possible upgrade'.

<table id="table_xt2_ywq_rx"><thead><tr><th>

sys\_trigger

</th><th>

Function

</th></tr></thead><tbody><tr><td>

Check distribution for possible upgrade

</td><td>

-   Queries Now Support to ask whether an upgrade is going to happen in a given time interval, which is determined by the configuration for the **Check distribution for possible upgrade** scheduled job.
-   Asks whether the instance should be running a different version. If so, the distribution for that version is downloaded, and your instance upgrades to the target version.

</td></tr><tr><td>

Check database for possible upgrade

</td><td>

-   Runs after the distribution has been upgraded.
-   Performs the database upgrade.

</td></tr></tbody>
</table>## About this task

![Upgrade progress bar](../image/progress-bar-phase-3.png)

**Important:** Your upgrades are orchestrated out of your instance, not Now Support.

Now Support keeps records of what version you should be running, and your instance periodically queries Now Support to check its assigned version. When you designate a time for your upgrade, your instance begins the upgrade at that time. For example:

|Action|Result|
|------|------|
|You schedule an upgrade to Zurich Patch 8 to take place on June 10 at 3:00pm.|Now Support changes its records to reflect that you should be on Zurich Patch 8 on June 10 at 3:00pm.|
|Now Support waits to get pinged by your instance after the scheduled time on June 10.|Your instance continues to operate on its current release version, and it periodically pings Now Support.|
|After the scheduled time on June 10, Now Support receives a ping from your instance.|Now Support tells your instance that it should be on Zurich Patch 8.|
|Your instance receives a Now Support notification that it should be running a different version.|Your instance starts the upgrade.|

How to schedule and manage instance upgrades on Now Support

You can browse the Now Support service catalog to request and self-service tasks such as scheduling an upgrade.

Request plugins and self-service tasks using service catalog on Now Support

## Procedure

1.  Check the configuration of the **Check distribution for possible upgrade** scheduled job to view how often and when it runs.

    1.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

    2.  In the list, find the **Check distribution for possible upgrade** scheduled job.

    3.  View the **Next action** column to determine when the job next runs.

2.  Verify that the **Check distribution for possible upgrade** sys\_trigger is set properly for upgrading.

    1.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

    2.  Find and click the **Check distribution for possible upgrade** scheduled job.

    3.  Make sure that the **Trigger type** is set to **Interval**.

    4.  Make sure that the **System ID** is set to **None**.

3.  Verify that the **Check database for possible upgrade** sys\_trigger is set properly for upgrading.

    1.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

    2.  Find and click the **Check database for possible upgrade** scheduled job.

    3.  Make sure that the **Trigger type** is set to **Run at System Startup**.

4.  Schedule the upgrade in Now Support.

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

5.  If applicable, request a version entitlement.

    1.  In the **Actions** column, click **Schedule**.

        If the version does require an entitlement, this screen appears:

        ![Requires entitlement approval message](../image/upgrades-schedule-with-ent.png)

    2.  Click the calendar icon and specify a date and time at least three days in the future.

        ServiceNow entitlement managers respond to your entitlement request within three days.

        **Note:** Setting the time for an upgrade or patch is important. Set the upgrade or patch to start 10–15 minutes before the **Check distribution for possible upgrade** scheduled job runs. This setting allows enough time for the upgrade or patch request to update Now Support 's records about which release version your instance should be on before the **Check distribution for possible upgrade** scheduled job runs.

    3.  Click **Schedule**.

        A confirmation message appears. If you need an entitlement, the entitlement request number is included. Click the entitlement request number to view the request.

    4.  If you have any questions about your entitlement, comment on your entitlement request after you have submitted it.


