---
title: Make an activity unavailable in playbooks
description: Deactivate an activity to stop users from adding it to playbooks in Creator Studio.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [About custom activities, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Make an activity unavailable in playbooks

Deactivate an activity to stop users from adding it to playbooks in Creator Studio.

## Before you begin

For example, you could hide an base system activity, like sending an email, if it's not relevant to your workflow.

**Note:** Hiding an activity doesn't change anything about the processes using that activity. Hiding an activity only makes it unavailable in Creator Studio.

Role required: admin or app\_engine\_admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Request App Administration** &gt; **Creator Studio Activities**.

    All of the standard Creator Studio activities appear in the list, not just custom activities.

    ![Creator Studio Activities table showing available activities with their descriptions and order values.](../image/crs-activities-table.png "Activities table")

    The Creator Studio Activities table appears.

2.  Open the Creator Studio Activity record for the activity that you want to hide by selecting is **Short Description** field.

3.  Hide the activity by clearing the **Active** check box.

    ![Creator Studio Activity form with the Active check box selected](../image/crs-activity-active-box.png "Active box for activity")

4.  Select **Update** to save the record.


**Parent Topic:**[Administering activities in Creator Studio](../concept/creator-studio-administering-activities.md)

