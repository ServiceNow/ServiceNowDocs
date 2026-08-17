---
title: Populate planning items on RIDAC records
description: Run the scheduled job to populate the planning item field on RIDAC records that were created before the Strategic Planning was installed. This job ensures legacy RIDAC records appear correctly in related lists and reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/update-ridac-planning-items-spw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 1
keywords: [backfill, planning item, scheduled job, RIDAC, migration]
breadcrumb: [Configure, RIDAC, Strategic Planning, Strategic Portfolio Management]
---

# Populate planning items on RIDAC records

Run the scheduled job to populate the planning item field on RIDAC records that were created before the Strategic Planning was installed. This job ensures legacy RIDAC records appear correctly in related lists and reports.

## Before you begin

Role required: admin

**Important:** This is a one-time job and is not meant to be run on a recurring schedule.

## About this task

RIDAC records created before the Strategic Planning installation have an empty planning item field. These records don't appear in core project related lists until the planning item is populated. The **Update planning item on RIDAC tables** scheduled job automatically updates the planning item field on the existing RIDAC records based on a configurable time window.

## Procedure

1.  Navigate to **System Administration** &gt; **Scheduled Jobs**.

2.  Search and select the **Update planning item on RIDAC tables** scheduled job.

3.  On the Scheduled Script Execution form, ensure that the **Run** field is set to **On Demand**.

4.  Set the time window variable to control which RIDAC records are included in the backfill:

    1.  **3M** — Update RIDAC records created in the last 6 months

    2.  **6M** — Update RIDAC records created in the last 6 months

    3.  **1 year** — Update RIDAC records created in the last 12 months

    4.  **Custom** — Specify a custom start date and time

    The time window filter helps optimize performance by limiting the backfill to recent records. If your organization has a large number of RIDAC records \(for example, 700,000+\), older records \(&gt;1 year old\) may be stale. These older records may no longer require updating. Select the time window that best matches your organizational needs. When you select **CUSTOM**, you must also set the **CUSTOM\_DATE** variable in the script to specify the start date in `YYYY-MM-DD` format. This variable is ignored for all other window options. \[Omitted image "update-planning-item-on-RIDAC-tables.png"\] Alt text: Update planning item on the existing RIDAC records

5.  Select **Execute Now**.


## Result

The scheduled job runs and stamps the planning item details on all existing RIDAC records that are part of the time periods selected in the time window variable.

