---
title: Trigger a CrowdStrike Falcon Insight profile manually from a security incident
description: Trigger a profile manually after you review a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Trigger a CrowdStrike Falcon Insight profile manually from a security incident

Trigger a profile manually after you review a security incident.

## Before you begin

Role required: admin

## About this task

Once you activate the profile, based on the configured trigger conditions, you can view the query results in the ServiceNow AI Platform security incidents. CrowdStrike Falcon Insight also enables you to run individual capabilities on Configuration Items \(CIs\) without using a profile.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review with the CrowdStrike Falcon Insight information.

3.  In the related lists section, select **Run EDR Profile\(s\)**.

4.  Browse and select a profile from the list of available profiles.

5.  Select **Include Related CI** to run this profile on all the related CIs of the profile.

    For example, if there are five CIs associated with the security incident, then the selected profile runs on all the five CIs.

6.  Select **Submit**.

    The selected profile is triggered manually. You can review the work notes and activities section and the profile-initiated and profile-completed tags in the work notes section. ![Reviewing work notes for automation activity.](../image/falcon-insight-test-work-notes.png)

7.  The results appear in the form of related lists such as Get File, Host Details, Logged on Users, Running Processes, Running Services, Network Statistics, and so on.

8.  To run individual capabilities on a CI, perform the following steps:

    1.  In the Configuration Items related list, select the required CI.

    2.  Select the **Actions on selected rows...** drop down list, and select the required capability that you want to run for the selected CI.

        For example, Isolate Host.

    3.  Look up the required capability implementation for the CI using the search option, and select **CrowdStrike Falcon Insight Isolate Host**.

    4.  Select **Isolate Host** to run it on the selected CI.


