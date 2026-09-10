---
title: Enable ECC queue cleanup for synthetic monitoring
description: Grant the ECC Queue auto-purge job permission to remove old synthetic monitoring messages from the ECC queue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/enable-ecc-queue-cleanup.html
release: australia
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 1
breadcrumb: [Configure, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Enable ECC queue cleanup for synthetic monitoring

Grant the ECC Queue auto-purge job permission to remove old synthetic monitoring messages from the ECC queue.

## Before you begin

Role required: admin

## About this task

The [ECC Queue auto-purge job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/ecc-queue-auto-purge.md) requires **Can Delete** application access on the ECC Queue \[ecc\_queue\] table. This access is not enabled by default, so the job can evaluate messages against its purge categories but can't remove any of them until an admin grants this access.

Consider enabling this access as a performance-tuning step if you observe contention or delays in responses from synthetic monitoring checks, since an unpruned queue can contribute to that behavior.

## Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  Open the ECC Queue \[ecc\_queue\] table.

3.  In the **Application Access** related list, select **Can Delete**.

4.  Save the table record.


## Result

On its next scheduled run, the ECC Queue auto-purge job removes and flags messages according to its [purge categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/ecc-queue-auto-purge.md).

## What to do next

**Note:** Enabling this access is a manual step in this release. Automating it is planned for a future release, so this procedure may be removed once that work ships.

**Parent Topic:**[Configuring synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/configuring-synthetic-monitoring.md)

