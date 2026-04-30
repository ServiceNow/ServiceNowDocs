---
title: Copy an event profile for the Splunk Enterprise Security Event Ingestion integration
description: Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you may prefer to copy alarm profiles to save time.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy an event profile for the Splunk Enterprise Security Event Ingestion integration

Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you may prefer to copy alarm profiles to save time.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

If you copy a profile, the profile name is initially modified to avoid duplicate profiles. In addition, the copied profile is deactivated \(false\) so it is not activated accidentally prior to completing the configuration. Copy profiles and use existing maps for security incidents that you have already previewed and verified.

## Procedure

1.  Navigate to **All** &gt; **Splunk Integration** &gt; **Splunk Event Profile**.

2.  In the Splunk Event Profiles list that is displayed, select a profile that you want to copy, and, from the Actions on selected rows choice list, click **Copy**.

    ![Copy event profile: 1](../image/splunk_es_copy_profile1.png)

    The profile is copied and displayed on the list. The copy has all the settings of the original profile including the mapping and scheduling configuration. The name of the profile contains copy. Although the original profile is activated \(`true`\), the copy is disabled at this point \(`false`\). You may prefer to edit values of the copied profile and rename it so the configuration settings apply to the new profile as required.

    ![New profile highlighted](../image/splunk_es_copy_profile2.png)

    You have successfully copied the settings from an existing profile to a new profile.


## What to do next

You are prompted to activate \(enable\) the new profile after you complete the configuration step.

