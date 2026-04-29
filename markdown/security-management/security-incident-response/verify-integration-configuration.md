---
title: Verify CrowdStrike Falcon Insight profile trigger conditions
description: Test the profile and verify that the trigger condition filters that you have configured work as expected.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify CrowdStrike Falcon Insight profile trigger conditions

Test the profile and verify that the trigger condition filters that you have configured work as expected.

## Before you begin

Role required: sn\_si.admin

## About this task

Activate the profile that is based on the configured trigger conditions you specified so that you can view the query results in the ServiceNow AI Platform security incidents.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Select **New** to create a security incident.

3.  To create a security incident, fill in the required information and click **Save**.

4.  Review the work notes and activities section to view the profile-initiated and profile-completed tags.![Reviewing work notes for automation activity.](../image/falcon-insight-test-work-notes.png)

5.  Review the details in the CrowdStrike Falcon Insight Details related lists such as Get File, Host Details, Logged on Users, Running Processes, Running Services, Network Statistics, and so on.

    ![Review therelated lists for details.](../image/falcon-insight-test-related-lists.png)


