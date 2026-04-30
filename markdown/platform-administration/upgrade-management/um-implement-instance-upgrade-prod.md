---
title: Implement instance upgrade activities on a prod instance
description: Implement the instance upgrade tasks for a successful upgrade on your prod instance.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access guided upgrade on a production instance, Configure, Upgrade Console, Upgrade, Administer]
---

# Implement instance upgrade activities on a prod instance

Implement the instance upgrade tasks for a successful upgrade on your prod instance.

## Before you begin

**Note:** You will be able to perform the Instance upgrade tasks only after completing the pre-upgrade tasks.

Role required: admin

## Procedure

1.  Upgrade your instance.

    In this section you will see the following information:

    -   Scheduled Upgrade: It shows the current status of the upgrade on the instance. You can see the following stages in this section.

        -   Not scheduled
        -   Scheduled
        -   Running or in progress
        -   Complete
        Select **Reschedule upgrade** if you want to reschedule the upgrade. If there is no upgrade scheduled, select **Schedule upgrade** to schedule an upgrade. You are now redirected to ServiceNow Support to schedule an upgrade for your instance. You can then select one of the available versions and **Submit**. This automatically creates the upgrade request for your instance.

        When the status is Complete, you can view when the upgrade started and completed, as well as the total duration. By default, you are in the America/Los Angeles timezone. You can modify the timezone preference by navigating to **User Menu** &gt; **Preferences** &gt; **Language &amp; Region**. You can then select the required timezone from the drop down menu.

    -   Pre-stage your Schema Alters: This section notes the changes in the database during the upgrade process on your instance. It is to be noted that these database modifications are necessary for new platform features. You can now pre-stage the schema alters so that the actual upgrade process is expedited.

        **Note:** It is recommended to pre-stage your schema changes which accelerates the actual upgrade process. By default, it is scheduled one week prior to the upgrade. During this time, no scheduled upgrade can process. The schema alter process can't start after the scheduled upgrade.

        You can see the start time of the scheduled schema alters. Select **Reschedule Schema Alters** to update the scheduled time for schema alters.

        **Note:** The option of seeing the schema alters and updating the starting time is applicable only if the glide.staged\_upgrade.enabled property is enabled or set to true. By default, the glide.staged\_upgrade.enabled property is set to false.

2.  Select **Mark as complete** when the upgrade process completes.


**Parent Topic:**[Access guided upgrade on a production instance](um-guided-tour-implement-prod.md)

