---
title: Copy a Microsoft Azure Sentinel profile
description: Copy an existing profile and its associated settings instead of creating a profile. When you create multiple profiles, you can reuse the settings of an existing profile by copying these profiles.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy a Microsoft Azure Sentinel profile

Copy an existing profile and its associated settings instead of creating a profile. When you create multiple profiles, you can reuse the settings of an existing profile by copying these profiles.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

When you copy a profile, the profile name is initially modified to avoid creating duplicate profiles. The copied profile is also turned off \(set to false\) to ensure that you don't accidentally activate it before you complete the configuration. You can copy the profiles and use existing maps for security incidents that you have already previewed and verified.

## Procedure

1.  Navigate to **All** &gt; **Microsoft Azure Sentinel Integration** &gt; **Azure Sentinel Profile**.

2.  In the Azure Sentinel Profiles list, select a profile that you want to copy, and then from the Actions on selected rows list, click **Copy** as shown in the following example.

    ![Copying a profile.](../image/sentinel-copying-profile.png "Copying a profile")

    The profile is copied and displayed on the list as shown in the following example. The copy has all the settings of the original profile including the mapping and scheduling configuration. The name of the profile contains the word "copy." Although the original profile is enabled \(true\), the copy is turned off at this point \(false\). You may prefer to edit values of the copied profile and rename them so that the configuration settings apply to the new profile as required.

    ![Copied profile.](../image/sentinel-copied-profile.png "Viewing the copied incident profiles")

    You have successfully copied the settings from an existing profile to a new profile. The Active column status is set to false, which means that the profile must be activated.


