---
title: Create exclusion table for audit date
description: Create exclusion lists for the various policy types used in Audit Management.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Create audit engagement, Manage engagements, Use, Audit Management, Governance, Risk, and Compliance]
---

# Create exclusion table for audit date

Create exclusion lists for the various policy types used in Audit Management.

## Before you begin

**Note:** Perform the steps in this topics if your version is below Yokohama patch 10 and Zurich patch 4 release.

Role required: sn\_audit.admin

## Procedure

1.  Navigate to **All** &gt; **planned\_task\_recalculation\_exclusions.list**.

2.  Select **New** to add new records to the exclusion list.

3.  Select a record in the **Exclude Table** drop-down list.

    The required records are:

    -   Engagement \(sn\_audit\_engagement\)
    -   Audit Task \(sn\_audit\_task\)
    -   Control Test \(sn\_audit\_control\_test\)
    -   Walkthrough \(sn\_audit\_walkthrough\)
    -   Interview \(sn\_audit\_interview\)
    -   Activity \(sn\_audit\_activity\)

        **Note:** You can add only one record to the exclusion list at a time.

4.  Select **Submit** to add the record to the exclusion list.


**Parent Topic:**[Create an engagement](t_CreateEngagement.md)

