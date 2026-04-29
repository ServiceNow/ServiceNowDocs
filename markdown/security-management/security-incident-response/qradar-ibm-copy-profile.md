---
title: Optional: Copy a IBM QRadar profile
description: Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you may prefer to copy profiles to save time.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Optional: Copy a IBM QRadar profile

Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you may prefer to copy profiles to save time.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, if you copy a profile, the profile name is initially modified to avoid duplicate profiles. In addition, the copied profile is disabled \(false\) so it is not activated accidentally prior to completing the configuration. Copy profiles and use existing maps for security incidents that you have already previewed and verified.

## Procedure

1.  Navigate to **All** &gt; **IBM QRadar Integration** &gt; **IBM QRadar Profile**.

2.  In the IBM QRadar Profiles list that is displayed, select a profile that you want to copy, and, from the Actions on selected rows choice list, select **Copy**.

    ![IBM QRadar: copy profile](../image/ibm-qradar-profile-copy.png)

    The profile is copied and displayed on the list. The copy has all the settings of the original profile including the mapping and scheduling configuration. The name of the profile contains copy. Although the original profile is enabled \(`true`\), the copy is disabled at this point \(`false`\). You may prefer to edit values of the copied profile and rename it so the configuration settings apply to the new profile as required.

    **Note:** If you select a different source for the profile, you must select new rules \([Select IBM QRadar rules](qradar-ibm-create-profile-eventsearch.md)\) for the profile. But if you use the same source and select new rules, the sample offenses will be cleared.

    You have successfully copied the settings from an existing profile to a new profile. Note that the **Active** column status is set to false as the profile needs to be activated.


## What to do next

You are prompted to activate \(enable\) the new profile after you complete the configuration steps.

