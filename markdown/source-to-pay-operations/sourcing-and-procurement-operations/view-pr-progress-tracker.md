---
title: View the purchase requisition Progress Tracker
description: View the Progress Tracker stepper on a purchase requisition \(PR\) record to understand where the PR sits in its approval and sourcing workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/view-pr-progress-tracker.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 2
breadcrumb: [Monitor PR and PO progress, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# View the purchase requisition Progress Tracker

View the Progress Tracker stepper on a purchase requisition \(PR\) record to understand where the PR sits in its approval and sourcing workflow.

## Before you begin

This role includes **sn\_shop.shopper**, which the stepper's data broker requires. Without **sn\_shop.procurement\_specialist**, you cannot open purchase requisition records.

Role required: **sn\_shop.procurement\_specialist**

## About this task

When you open a purchase requisition record in the Source-to-Pay Workspace, the Progress Tracker appears above the tab navigation, displaying the PR's current state in the approval-to-sourcing workflow. You can understand where the PR is without inspecting individual approval records or task lists.

## Procedure

1.  Open a purchase requisition record.

    In the Source-to-Pay Workspace, search for or navigate to the PR you want to monitor.

2.  View the Progress Tracker stepper above the tab navigation.

    The stepper appears above the **Details**, **Purchase Lines**, **Related work**, **Agreements**, and **Emails** tabs.

    \[Omitted image "progress-tracker-pr-happy-path.png"\] Alt text: Progress Tracker stepper showing happy-path states for purchase requisition

    The stepper shows:

    -   Current state: Highlighted with a filled circle or colored indicator
    -   Completed states: Marked with a green checkmark
    -   Upcoming states: Shown as open circles
3.  Switch between tabs to continue working.

    The Progress Tracker remains visible at the top. Whether you are viewing the **Details** tab, **Purchase Lines**, **Related work**, or any other section of the PR, the stepper stays in place above the tabs.

4.  Click on a state in the stepper to expand the info card.

    The info card displays detailed information about that state. See [Use the Progress Tracker info card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/use-progress-tracker-info-card.md) for details on what the info card displays.


## Result

You can now see where the PR stands in its workflow and understand what has been completed and what is pending.

## Example

The Progress Tracker shows Pending Review \(green checkmark, completed\) and Pending Approval \(green checkmark, completed\). The current state is Awaiting Task Completion \(highlighted\). Upcoming steps are Final Review, Pending Submission, and Closed Complete \(shown as open circles\). Hovering over the Awaiting Task Completion step shows Days in step: 3 and a list of pending fulfiller tasks for this PR.

## What to do next

For information about the PR state model, including happy-path states and deviation branches, see [Purchase requisition state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/pr-state-model.md). For related PO Progress Tracker help, see [View the purchase order Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/view-po-progress-tracker.md).

**Parent Topic:**[Purchase requisition and purchase order progress tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/monitor-pr-po-progress.md)

**Related topics**  


[View the purchase order Progress Tracker]()

[Use the Progress Tracker info card]()

