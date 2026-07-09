---
title: Change the sync schedule
description: Adjust how often the EMR Provider Directory Sync imports data by editing the FHIR Sync — Daily scheduled job directly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-configure-schedule.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [schedule, scheduled job, sync cadence]
breadcrumb: [Prerequisites for the FHIR integration, EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Change the sync schedule

Adjust how often the EMR Provider Directory Sync imports data by editing the **FHIR Sync — Daily** scheduled job directly.

## Before you begin

Role required: `sn_hco_intg_fhir.admin`.

## About this task

The sync cadence is controlled entirely by the scheduled job record — the application defines no separate system property for it. Edit the job's run frequency and time to change when the sync runs.

**Important:** The **FHIR Sync — Daily** job is installed inactive. Set the **Active** field to true on the job record before the sync will run on its configured schedule.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and open the **FHIR Sync — Daily** record.

2.  Set the **Run** frequency and the run time to your preferred cadence.

    The default is daily at 03:00 instance time. Choose a window when load on both your instance and the FHIR server is low.

3.  Save the record.


## Result

The change takes effect on the next scheduled run. No restart is required.

