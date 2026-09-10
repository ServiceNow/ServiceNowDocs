---
title: Troubleshoot ECC queue growth
description: If the ECC queue keeps growing or contains large numbers of stale synthetic monitoring messages, use this information to identify why the auto-purge job isn't clearing them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/troubleshoot-ecc-queue-growth.html
release: zurich
topic_type: reference
last_updated: "2026-08-20"
reading_time_minutes: 1
breadcrumb: [Troubleshoot, Reference, Landing page, ITOM AIOps, IT Operations Management]
---

# Troubleshoot ECC queue growth

If the ECC queue keeps growing or contains large numbers of stale synthetic monitoring messages, use this information to identify why the auto-purge job isn't clearing them.

## The job reports success but the queue doesn't shrink

The most common cause of this condition is that the ECC Queue \[ecc\_queue\] table doesn't have **Can Delete** application access enabled. This access isn't enabled by default, so until an admin grants it, the job can evaluate messages against the purge categories but can't actually remove any of them.

Review the job's log output for warnings from the most recent run. If a warning indicates that records couldn't be removed, confirm that the job has delete access to the ECC Queue \[ecc\_queue\] table. To grant that access, see [Enable ECC queue cleanup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/enable-ecc-queue-cleanup.md).

## Messages remain for monitors that are disabled

When a monitor is disabled, messages that it already placed in the queue can remain there. On its next run, the auto-purge job flags queued messages in the **Ready** or **Processing** state as errored when the monitor they belong to is disabled. Because the job runs once daily, these messages can persist until the next run.

## Stale entries appear to be pending work

Messages left in the **Ready** state that were never picked up, and messages stuck in the **Processing** state, can look like pending work when they are reviewed in the queue. The auto-purge job flags both as errored so that they are distinguishable from messages that are genuinely waiting to be processed. For the age thresholds that apply to each state, see [ECC queue auto-purge for synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/ecc-queue-auto-purge.md).

**Parent Topic:**[Troubleshoot synthetic monitors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/troubleshoot-synthetic-monitors.md)

