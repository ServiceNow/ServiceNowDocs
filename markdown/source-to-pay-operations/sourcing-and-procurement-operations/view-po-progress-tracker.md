---
title: View the purchase order Progress Tracker
description: View the Progress Tracker stepper on a purchase order record to understand where the PO is in its fulfillment workflow \(receipt and invoicing\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/view-po-progress-tracker.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 3
breadcrumb: [Monitor PR and PO progress, Use Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# View the purchase order Progress Tracker

View the Progress Tracker stepper on a purchase order record to understand where the PO is in its fulfillment workflow \(receipt and invoicing\).

## Before you begin

Without the sn\_shop.procurement\_specialist role, you cannot open the purchase order record. The stepper's data broker additionally requires the sn\_shop.shopper role, which is already included by sn\_shop.procurement\_specialist.

Role required: sn\_shop.procurement\_specialist

## About this task

Whenever you open a purchase order record in the Source-to-Pay Workspace, the Progress Tracker appears above the tab navigation. It displays the PO's current state in the receipt and invoicing workflow. This gives you a quick visual reference for understanding where the PO is in fulfillment, without having to inspect individual receipt or invoice records.

## Procedure

1.  In the Source-to-Pay Workspace, open a purchase order record.

    Search for or navigate to the PO you want to monitor.

2.  View the Progress Tracker stepper above the tab navigation \(Details, Purchase Lines, Related work, Agreements, Emails, Receipts, Invoices\).

    \[Omitted image "progress-tracker-po-happy-path.png"\] Alt text: Progress Tracker displaying completed, current, and upcoming purchase order states

    The stepper shows:

    -   Current state: highlighted with a filled circle or colored indicator
    -   Completed states: display a checkmark icon
    -   Upcoming states: shown as open circles
3.  Switch between tabs to continue working.

    Whether you are viewing the Details tab, Purchase Lines, Related work, Receipts, Invoices, or any other section of the PO, the stepper stays in place above the tabs.

    The Progress Tracker remains visible at the top.

4.  To see detailed information about any state, select that state in the stepper.

    See [Use the Progress Tracker info card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/use-progress-tracker-info-card.md) for details on what the info card displays.

    The info card expands.


## Result

You can see where the PO stands in its receipt and invoicing workflow and understand what has been completed and what is pending.

## Example

A procurement specialist opens purchase order PO0001008 and sees the Progress Tracker showing six states. **Pending Submission** displays a checkmark icon \(completed, less than 1 minute in state\). **Ordered** is highlighted with a green border as the current state \(35 minutes in state\). Four upcoming states appear as numbered circles: **Partially Delivered**, **Delivered**, **Payment Pending**, and **Closed Paid**. Selecting the current **Ordered** state expands the info card showing the work item RTSK0001008.

## What to do next

For information about the PO state model, including happy-path states and deviation branches, see [Purchase order state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md). For comparison with the PR Progress Tracker, see [View the purchase requisition Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/view-pr-progress-tracker.md). For related configuration tasks, see [Configure PR and PO Progress Tracker states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.md).

**Parent Topic:**[Purchase requisition and purchase order progress tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/monitor-pr-po-progress.md)

**Related topics**  


[View the purchase requisition Progress Tracker]()

[Use the Progress Tracker info card]()

