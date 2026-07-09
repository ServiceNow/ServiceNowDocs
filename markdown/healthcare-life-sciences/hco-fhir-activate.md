---
title: Activate the FHIR sync schedule
description: Activate the FHIR Sync — Daily scheduled job so that the EMR Provider Directory Sync imports FHIR provider-directory data on a recurring schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-activate.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [activate, scheduled job, FHIR sync]
breadcrumb: [Prerequisites for the FHIR integration, EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# Activate the FHIR sync schedule

Activate the **FHIR Sync — Daily** scheduled job so that the EMR Provider Directory Sync imports FHIR provider-directory data on a recurring schedule.

## Before you begin

Role required: `sn_hco_intg_fhir.admin` \(granted through `sn_hco.admin`\).

Complete the steps in [Prerequisites for the FHIR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-prerequisites.md) first.

## About this task

The application ships a scheduled job named **FHIR Sync — Daily** that starts the import orchestration subflow. Activate the job to begin scheduled syncs.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **FHIR Sync — Daily** scheduled job record.

3.  Set **Active** to true and save the record.

    By default the job runs daily at 03:00 instance time. To change the cadence, see [Change the sync schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-configure-schedule.md).


## Result

The scheduled job is active and will run the FHIR import on its schedule. To run the first full load immediately, see [Run the initial load](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hco-fhir-run-initial-load.md).

