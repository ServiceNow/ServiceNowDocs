---
title: Copy an event profile for the Splunk Enterprise Event Ingestion integration
description: Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you might prefer to copy alarm profiles to save time.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration architecture and external systems connection, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy an event profile for the Splunk Enterprise Event Ingestion integration

Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you might prefer to copy alarm profiles to save time.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Copying an existing profile and its associated settings is optional.

If you copy a profile, the profile name is initially modified to avoid duplicate profiles. In addition, the copied profile is disabled \(false\) so it is not activated accidentally prior to completing the configuration. Copy profiles and use existing maps for security incidents that you have already previewed and verified.

## Procedure

1.  Navigate to **All** &gt; **Splunk Integration** &gt; **Splunk Event Profile**.

2.  In the Splunk Event Profiles list that is displayed, select a profile that you want to copy, and, from the Actions on selected rows choice list, click **Copy**.

    ![Event Profiles list with Actions on selected rows highlighted.](../image/splunk-copy-profile1.png)

    The profile is copied and displayed on the list. The copy has all the settings of the original profile including the mapping and scheduling configuration. The name of the profile contains copy. Although the original profile is enabled \(`true`\), the copy is disabled at this point \(`false`\). You may prefer to edit values of the copied profile and rename it so the configuration settings apply to the new profile as required.

    ![New profile highlighted.](../image/splunk-copy-profile2.png)

    You have successfully copied the settings from an existing profile to a new profile.


## What to do next

You are prompted to activate \(enable\) the new profile after you complete the configuration steps.

**Parent Topic:**[Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-integration-architecture.md)

