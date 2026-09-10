---
title: Schedule a CSV download report for historic snapshots
description: Schedule a recurring job to generate CSV download reports of historic snapshots from the Digital resilience third-party registers. The job reuses the configuration of an existing Excel download/upload request record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/schedule-csv-report-historic-snapshots.html
release: australia
topic_type: task
last_updated: "2026-08-09"
reading_time_minutes: 1
breadcrumb: [Configuring Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Schedule a CSV download report for historic snapshots

Schedule a recurring job to generate CSV download reports of historic snapshots from the Digital resilience third-party registers. The job reuses the configuration of an existing Excel download/upload request record.

## Before you begin

An existing Excel download/upload request record with Type set to **Plain-csv reporting package**, Request type set to **Download**, and valid Entity, Competent authority, and Base currency values. The record can be in Draft state.

Role required: sn\_oper\_res.admin

## About this task

The scheduled job generates a CSV download report of historic snapshots on a recurring basis. It copies the entity, competent authority, and base currency from the template record.

The job is inactive by default, and an administrator must activate it to run on schedule.

No email notification is sent for these runs because the job runs as the system user, not a real requester.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**, then open the historic snapshot CSV download report job.

2.  Select the **Active** check box.

    **Note:** The job does not run until you select this check box.

3.  In the **Run** field, select a different frequency than the default **Quarterly** value.

    The default frequency aligns with quarterly DORA reporting cycles.

4.  Select **Save**.


## Result

The job runs on the configured schedule and generates a CSV download report of historic snapshots using the template record's configuration.

**Parent Topic:**[Configuring Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-dg-resi-party-regi.md)

