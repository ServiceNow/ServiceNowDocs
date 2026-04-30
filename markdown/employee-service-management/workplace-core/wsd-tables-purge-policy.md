---
title: Apply the archive rule
description: Apply the archival policy for Workplace Core to archive old table records.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing workplace tasks, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Apply the archive rule

Apply the archival policy for Workplace Core to archive old table records.

## Before you begin

Role required: admin

## About this task

The archival policy archives old table records to improve performance and restrict table size growth.

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Filter out the Workplace Core archive rules.

    The following Workplace Core archive rules are displayed:

    -   WSD: Archive old workplace tasks: Archives old Workplace Core workplace tasks.
    -   WSD: Archive old reservations: Archives old core reservation records.
    -   WSD: Archive blocked location records: Archives old blocked location records.
3.  Select any of the archival records listed in step 3 to edit them.

    For example: Select the **WSD: Archive old workplace tasks** to open it in edit mode.

    Primary workplace tasks table, sn\_wsd\_core\_workplace\_task in Workplace Core records that are more than one year old are archived.

4.  Select the **Active** option to activate the archival policy for a selected archival rule.

5.  Apply the required filter conditions.

6.  Select **Recalculate Estimate** to see the records eligible for archiving.

7.  Select the **Run Archive Now** related link to run the archival rule.

    **Note:** The child tables in the following applications are also archived when this archive policy is run:

    -   Workplace Case Management: [Components installed with Workplace Case Management](../../workplace-case-mgmt/reference/components-installed-with-workplace-case-mgmt.md)
    -   Workplace Reservation Management: [Components installed with Workplace Reservation Management](../../wsd-reservation-management/reference/components-installed-with-wsd-reservation-mgmt.md)
    -   Workplace Calendar Synchronization: [Components installed with Workplace Calendar Synchronization](../../workplace-calendar-synchronization/reference/components-installed-with-workplace-calendar-syncn.md)
    -   Workplace Move Management: [Components installed with Workplace Move Management](../../workplace-move-mgmt/reference/components-installed-with-workplace-move-mgmt.md)

**Parent Topic:**[Managing workplace tasks](../concept/managing-workplace-maintenance-tasks.md)

