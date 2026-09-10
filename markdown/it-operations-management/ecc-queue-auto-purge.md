---
title: ECC queue auto-purge for synthetic monitoring
description: A scheduled job removes old Synthetic monitoring messages from the ECC queue. The job also flags stuck or orphaned messages with status as error, so that the queue doesn't grow indefinitely and stale entries aren't mistaken for pending work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/ecc-queue-auto-purge.html
release: zurich
topic_type: reference
last_updated: "2026-08-20"
reading_time_minutes: 2
breadcrumb: [Reference, Landing page, ITOM AIOps, IT Operations Management]
---

# ECC queue auto-purge for synthetic monitoring

A scheduled job removes old Synthetic monitoring messages from the ECC queue. The job also flags stuck or orphaned messages with status as error, so that the queue doesn't grow indefinitely and stale entries aren't mistaken for pending work.

## Enable the cleanup job

The ECC Queue auto-purge job requires **Can Delete** application access on the ECC Queue \[ecc\_queue\] table. This access is not enabled by default, so the job can't remove any records until an admin grants it.

For information about enabling this access, see [Enable ECC queue cleanup for synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/enable-ecc-queue-cleanup.md).

## How the job runs

The ECC Queue auto-purge job runs once daily, overnight. On each run, the job evaluates synthetic monitoring messages in the ECC Queue \[ecc\_queue\] table against the categories in the following table. The job then either removes each matching message or flags it as error.

**Important:** Only messages that belong to synthetic monitoring are evaluated. Messages that other applications place in the same queue table are never removed or modified, regardless of their state or age.

## Purge categories

|Category|Applies to|Condition|Result|
|--------|----------|---------|------|
|Completed requests|Output-queue messages|State is **Processed** and the message was created more than 30 days ago.|Removed from the queue|
|Completed responses|Input-queue messages|State is **Processed** and the message was created more than 30 days ago.|Removed from the queue|
|Failed executions|Messages in either queue|State is **Error** and the message was created more than 30 days ago.|Removed from the queue|
|Orphaned ready|Messages in either queue|State is **Ready** and the message was created more than 1 day ago, meaning it was never picked up.|Flagged as error|
|Orphaned processing|Messages in either queue|State is **Processing** and the message was last updated more than 7 days ago, meaning it is stuck in progress.|Flagged as error|
|Disabled monitor|Messages in either queue|State is **Ready** or **Processing** and the monitor that the message belongs to has been disabled. Age isn't considered.|Flagged as error|

Messages that are flagged as errored remain in the queue with a state of **Error**. They are then eligible for removal under the failed executions category once they are more than 30 days old.

## When cleanup can't be completed

If the job can't remove records for reasons such as a table permission restriction, then the job writes a warning to its log instead of reporting success. Review the job's log output to confirm that each run completed the cleanup it reported.

For more information, see [Troubleshoot ECC queue growth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/troubleshoot-ecc-queue-growth.md).

**Parent Topic:**[Synthetic monitoring reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/synthetic-monitoring-reference.md)

