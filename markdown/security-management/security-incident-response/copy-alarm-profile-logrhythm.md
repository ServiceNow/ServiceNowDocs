---
title: Copy an alarm profile for LogRhythm
description: Copy an existing profile and its associated settings instead of creating a new alarm profile. If you are creating multiple alarm profiles for different types of alarms and you want to reuse the settings of an existing profile, you can copy alarm profiles to save time. This process is optional.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional configurations for the LogRhythm integration, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy an alarm profile for LogRhythm

Copy an existing profile and its associated settings instead of creating a new alarm profile. If you are creating multiple alarm profiles for different types of alarms and you want to reuse the settings of an existing profile, you can copy alarm profiles to save time. This process is optional.

## Before you begin

Role required: sn\_si.admin

## About this task

If you copy a profile, the profile name is initially modified to avoid duplicate profiles. In addition, the copied profile is set to inactive so it is not activated accidentally prior to completing the configuration.

## Procedure

1.  Navigate to **All** &gt; **LogRhythm Integration** &gt; **LogRhythm Alarm Profiles**.

    In the list that is displayed, note the `Active` column indicates if the profile is active \(`true`\).

    ![Alarm profile before copying.](../image/profilecopy01__list_view.png)

2.  In the field to the left of the **Name** column, select the name of the record.

3.  From the **Actions on selected rows** choice list, select **Copy**.

    ![Task: Select copy from the choice list.](../image/profilecopy02__selected_profile_with_action_menu.png)

    In the **Alarm Profiles** list, both the copy and the original profile are displayed. Although the original record is active, the copy is inactive at this point \(`false`\). After you have configured it, you activate this copied profile.

    ![Alarm profile copy complete.](../image/6-1lr-profilecopy03__copy_complete.png)

    You can edit values of the copied profile and rename it so alarm rules you pull apply to the new profile. You are prompted to activate the new profile once the configuration steps are completed.


**Parent Topic:**[Additional configurations for the LogRhythm integration](configure-system-and-troubleshooting-properties.md)

