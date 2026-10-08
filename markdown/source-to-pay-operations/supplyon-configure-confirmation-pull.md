---
title: Configure and run the confirmation pull
description: Set the schedule and look-back window for the confirmation pull, and run it on demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-configure-confirmation-pull.html
release: zurich
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure and run the confirmation pull

Set the schedule and look-back window for the confirmation pull, and run it on demand.

## Before you begin

Role required: admin

## About this task

The confirmation pull subflow is registered against the SupplyOn ERP source configuration.

## Procedure

1.  Set the **Look-back window** on the source configuration.

    The default equals the schedule interval, and SupplyOn limits the range to 100 days or less.

2.  Set the **Schedule**.

3.  Select **Run job** on the ERP source configuration.


## What to do next

**Note:** The pull uses the date of the last successful run as the window start. On the first run it falls back to the last 24 hours, and if the job has not run for some time it pulls the full elapsed window \(for example, 15 days if it has not run for 15 days\). When a run completes, the processing message summarizes the date range used and the number of confirmations pulled. The pull maintains a high-water mark \(`lastResponseDate`\) so that re-runs help avoid missing or double-counting confirmations. Empty windows complete successfully with no records processed.

