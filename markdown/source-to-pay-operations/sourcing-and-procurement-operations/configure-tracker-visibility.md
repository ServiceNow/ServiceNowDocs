---
title: Configure Progress Tracker visibility
description: Enable or disable whether the Progress Tracker displays on purchase requisition and purchase order records system-wide.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-tracker-visibility.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [Progress Tracker, purchase requisition, purchase order, system property, visibility]
breadcrumb: [Configure the Progress Tracker, Use Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure Progress Tracker visibility

Enable or disable whether the Progress Tracker displays on purchase requisition and purchase order records system-wide.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

By default, the Progress Tracker displays on all purchase requisition \(PR\) and purchase order \(PO\) records in Source-to-Pay Workspace. You can disable the Progress Tracker system-wide for PR records, PO records, or both using system properties.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

    Filter for `progress_tracker` to show the PR and PO Progress Tracker system properties.

2.  Open the system property for PR or PO.

    Select **sn\_spend\_workspace.pr.progress\_tracker\_UI.enabled** to control the PR Progress Tracker, or **sn\_spend\_workspace.po.progress\_tracker\_UI.enabled** to control the PO Progress Tracker.

3.  In the **Value** field, enter `true` or `false`.

    \[Omitted image "progress-tracker-sys-property.png"\] Alt text: System property form with Value field set to true to enable Progress Tracker visibility

    -   `true`—The Progress Tracker is visible on all PR or PO records.
    -   `false`—The Progress Tracker is hidden on all PR or PO records.
4.  Select **Update**.

    The visibility change takes effect immediately for all records.


## Result

The Progress Tracker is now enabled or disabled on PR and PO records according to your system property setting.

## What to do next

To customize which states display in the Progress Tracker stepper or the order in which they appear, see [Configure PR and PO Progress Tracker states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.md). For system property reference, see [System properties for Progress Tracker visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-system-properties.md).

**Parent Topic:**[Configure the Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-progress-tracker.md)

**Related topics**  


[Configure PR and PO Progress Tracker states]()

