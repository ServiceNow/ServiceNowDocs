---
title: Verify the Trigger Condition Filters
description: Validate the profile, and verify that the trigger condition filters that you have configured are working as expected.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure profiles and security incidents for the Microsoft Defender for Endpoint integration, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify the Trigger Condition Filters

Validate the profile, and verify that the trigger condition filters that you have configured are working as expected.

## Before you begin

Role required: sn\_si.admin or sn\_si.analyst

## About this task

After you activate the profile, based on the configured trigger conditions you can view the query results in the ServiceNow AI Platform® security incidents.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  To create a new security incident, select **New**.

3.  To trigger the respective profile, provide the filter conditions as given in the capability profile.

4.  Click **Save**.

5.  To validate the work notes and activities section, view and check the records that are tagged with the profile initiated, profile completed, or profile failed tags.

    ![Validate the work notes and activities](../image/review_activities.png "Work notes and activities")

6.  To validate all the data in the related lists, click **Show All Related Lists**.

7.  Click any **Related List** tab to validate the details.

    For example, Host Details.


