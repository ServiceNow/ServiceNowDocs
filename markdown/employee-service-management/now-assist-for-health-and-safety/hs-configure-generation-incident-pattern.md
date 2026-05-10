---
title: Configure the generation of incident patterns
description: Configure the scheduled jobs that generate the incident patterns from the safety incident records to run at a particular interval or time.
locale: en-US
release: australia
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure incident patterns, Configure, Now Assist for Health and Safety, Health and Safety, Employee Service Management]
---

# Configure the generation of incident patterns

Configure the scheduled jobs that generate the incident patterns from the safety incident records to run at a particular interval or time.

## Before you begin

Verify that the application scope is selected as Health and Safety Core. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: sn\_ohs\_im.admin

## About this task

The scheduled jobs to generate the incident patterns run by default when you have the Health and Safety Incident Management application and the generative AI \[com.snc.sn\_hs\_gen\_ai\] plugin installed. These jobs can be configured to start or end on a particular date or time as required.

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Scheduled jobs**.

2.  Search and open the jobs:

    -   HS pattern detection: data cleaning
    -   HS pattern detection: incident data preprocessing
    -   HS pattern detection: pattern generation
3.  Define how the schedule job should repeat from the **Run**, **Time zone**, and **Time** fields.

    For more information, see [Advanced options for scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/advanced-options-for-scheduled-jobs.md).

4.  Select **Update**.

    **Note:** To run the job and update metrics on demand, select **Execute Now**.


**Parent Topic:**[Configure incident patterns](../concept/hs-configure-incident-patterns.md)

