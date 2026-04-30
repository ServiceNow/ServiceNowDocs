---
title: Copy ArcSight ESM profile for event ingestion integration
description: Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you may prefer to copy profiles to save time.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy ArcSight ESM profile for event ingestion integration

Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you may prefer to copy profiles to save time.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, if you copy a profile, the profile name is initially modified to avoid duplicate profiles. In addition, the copied profile is disabled \(false\) so it is not activated accidentally prior to completing the configuration. Copy profiles and use existing maps for security incidents that you have already previewed and verified.

## Procedure

1.  Navigate to **All** &gt; **ArcSight ESM Integration** &gt; **ArcSight ESM Event Profile**.

2.  In the ArcSight Profiles list that is displayed, select a profile that you want to copy, and, from the Actions on selected rows list, select **Copy**.

    ![ArcSight ESM: Profiles](../image/sir-arcsight-esm-copy-profile.png)

    The profile is copied and displayed on the list. The copy has all the settings of the original profile including the mapping and scheduling configuration. The name of the profile contains copy. Although the original profile is enabled \(`true`\), the copy is disabled at this point \(`false`\). You may prefer to edit values of the copied profile and rename it so the configuration settings apply to the new profile as required.

    You have successfully copied the settings from an existing profile to a new profile. Note that the **Active** column status is set to false as the profile needs to be activated.


