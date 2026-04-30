---
title: Trigger a FireEye capability profile from Related Links
description: Trigger a capability profile manually after reviewing a security incident from related links.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Trigger a FireEye capability profile from Related Links

Trigger a capability profile manually after reviewing a security incident from related links.

## Before you begin

Role required: sn\_si.admin or sn\_si.analyst

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review.

3.  Click **Run EDR Profile\(s\)**in the related links section.

    ![Run EDR Profile](../image/run-edr-profile.png)

4.  Browse and select a profile from the list of available profiles and click **Submit**.

    ![EDR Profiles](../image/run-edr-browse.png)

    ![Run EDR Profile](../image/run-edr-submit.png)

5.  The selected profile is triggered manually.

6.  Review the work notes and activities section.

7.  View the tags and check the related lists for the data.

    **Note:** In addition to running the profile for the CI or the Alternate CI of the security incident, you could also run the profile for CI values present in the Configuration Item Related list by checking the Include Related CI on the dialog box. This will fetch data for the CI values present in the related list as well. Alternatively, you could run the profile just for the CI values present in the related list.


