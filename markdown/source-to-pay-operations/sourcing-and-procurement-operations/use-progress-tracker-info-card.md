---
title: Use the Progress Tracker info card
description: View detailed information about a step in the Progress Tracker by selecting the step to expand the info card.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/use-progress-tracker-info-card.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 3
breadcrumb: [Monitor PR and PO progress, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Use the Progress Tracker info card

View detailed information about a step in the Progress Tracker by selecting the step to expand the info card.

## Before you begin

Role required: sn\_shop.procurement\_specialist

## About this task

The Progress Tracker info card provides step-by-step detail about the PR or PO journey. It shows current and completed work items, who is assigned, and when steps completed. For deviation states, it shows why the record deviated and what to do next.

## Procedure

1.  On a purchase requisition or purchase order record, select a step in the Progress Tracker stepper.

    Select any state label or circle in the stepper.

2.  Review the info card details that appear below the stepper.

    \[Omitted image "progress-tracker-pr-pending-revision.png"\] Alt text: Info card showing Pending Revision state with assigned users, alert banner, and transition history.

    The info card displays the following information depending on the current state:

    -   State badge and avatars—The step state and assigned users. Select the "+N" badge to view additional assignees when more than 8 exist.
    -   Date Completed—The date the step finished, or three dashes if still in progress.
    -   Work Items—Links to related tasks, approvals, or cases for that step.
    -   Transition history—\(Shown only for deviation states\) A chronological log of state changes.
    -   Alert banner—\(Shown only for deviation states\) An explanation of why the record deviated.
3.  To view a specific work item, select its link in the Work Items field.

    The linked record \(for example, an approval or task\) opens in the same workspace tab or modal. You can navigate back to the PR or PO record to continue reviewing the Progress Tracker.

4.  For deviation states, select a transition history entry to see more detail about that state change.

    A popover or detail panel appears showing the actor, timestamp, and reason for the state change. Close the detail to return to the info card.


## Result

You can now see the contextual information about each step in the PR or PO progress, including assigned work, completion dates, and any deviations from the expected path.

## Example

When a PR enters the Pending Revision state, the info card displays an alert banner with the approver name, rejection date, and reason for rejection. The transition history log shows when the PR moved from Pending Approval to Pending Revision. Select the transition entry to view the approver feedback or comments on the rejection.

## What to do next

For complete information about info card fields and content model, see [Progress Tracker component reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-info-card.md). For task help on viewing the full tracker, see [View the purchase requisition Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/view-pr-progress-tracker.md) or [View the purchase order Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/view-po-progress-tracker.md).

**Parent Topic:**[Purchase requisition and purchase order progress tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/monitor-pr-po-progress.md)

**Related topics**  


[View the purchase requisition Progress Tracker]()

[View the purchase order Progress Tracker]()

