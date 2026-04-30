---
title: Trigger the Microsoft Defender for Endpoint capabilities from Related Links
description: Trigger a capability profile manually after reviewing a security incident from related links.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Trigger the Microsoft Defender for Endpoint capabilities from Related Links

Trigger a capability profile manually after reviewing a security incident from related links.

## Before you begin

Role required: sn\_si.admin or sn\_si.analyst

## About this task

In addition to running the profile for the CI or the Alternate CI of the security incident, you can also run the profile for CI values present in the Configuration Item related list by selecting **Include Related CI** in the dialog box. This retrieves the data for the CI values present in the related list as well. Alternatively, you could run the profile just for the CI values present in the related list.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the Microsoft Defender for Endpoint information.

3.  In the Related Links section, click **Run EDR Profile\(s\)**.

4.  Browse and select a profile from the list of available profiles, and click **Submit**.

    ![Trigger a Microsoft Defender for Endpoint capability profile from Related Links](../image/select_profile.png "Select a profile")

    The selected profile is triggered manually.

5.  Validate the work notes and activities section.

6.  View the tags, and validate the data in the related lists.


