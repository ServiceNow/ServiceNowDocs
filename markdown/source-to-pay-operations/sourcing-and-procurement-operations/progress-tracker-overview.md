---
title: Progress Tracker for purchase requisitions and purchase orders
description: The Progress Tracker displays the current state of purchase requisition and purchase order records. It shows fulfillers where a request is in the PR-to-PO journey without requiring them to review related records manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-overview.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 6
keywords: [progress tracker, purchase requisition, purchase order, state progression, procurement]
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Progress Tracker for purchase requisitions and purchase orders

The Progress Tracker displays the current state of purchase requisition and purchase order records. It shows fulfillers where a request is in the PR-to-PO journey without requiring them to review related records manually.

\[Omitted image "progress-tracker-pr-happy-path.png"\] Alt text: Progress Tracker stepper on a purchase requisition record showing an expanded info card

\[Omitted image "progress-tracker-po-happy-path.png"\] Alt text: Progress Tracker stepper on a purchase order record displaying current state, completed steps, and upcoming steps

## Why the Progress Tracker exists

Before the Progress Tracker, fulfillers had no direct way to determine where a purchase requisition or purchase order was in its process. The **State** field showed only the current state. Understanding what had happened, what was blocking progress, and what needed to happen next required inspecting related approvals, tasks, and audit history manually. The Progress Tracker surfaces that information directly on the record.

## Key concepts

-   **State**

    The current lifecycle position of a PR or PO, such as **Pending Review** or **Partially Delivered**. The tracker represents every possible record state as a step.

-   **State progression \(stepper\)**

    The visual, left-to-right sequence of steps that represents the record's journey to closure. The stepper renders above the tab navigation on the record and remains visible regardless of which tab you are viewing.

-   **Happy path**

    The default, linear sequence of states a PR or PO moves through when the process follows the standard sequence. For example, on a PR: **Pending Review**, **Pending Approval**, **Awaiting Task Completion**, **Final Review**, **Pending Submission**, **Closed Complete**.

-   **Deviations**

    Non-linear branches away from the happy path, such as a revision loopback, a supplier-confirmation wait for punchout orders, or a cancellation or rejection. The tracker displays a clear path to closure when a record deviates.

-   **Info card**

    The detail panel that appears when you select a step in the stepper. The panel displays contextual information about that state: who is assigned, when the step completed, which work items are outstanding, and — for deviation states — why the record deviated and what to do next. For detailed information about info card fields, see [Progress Tracker component reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-info-card.md).


## Who uses the Progress Tracker

Procurement specialists viewing a PR or PO record in the Source-to-Pay Workspace are the primary audience. They read the tracker and info card to understand record status and next steps. Procurement administrators configure which states appear in the tracker and whether the tracker is visible. For related tasks, see [View the purchase requisition Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/view-pr-progress-tracker.md), [View the purchase order Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/view-po-progress-tracker.md), and [Configure PR and PO Progress Tracker states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.md).

## PR progress tracker and PO progress tracker

The PR progress tracker and PO progress tracker share the same underlying stepper component and info-card pattern. Each is driven by its own state model and configuration record because purchase requisitions and purchase orders progress through different states. For the state models, see [Purchase requisition state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/pr-state-model.md) and [Purchase order state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/po-state-model.md).

-   **[Progress Tracker component reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-info-card.md)**  
The Progress Tracker component displays workflow progress on purchase requisitions and purchase orders through a stepper visualization and expandable info card. The info card shows assigned users, pending work items, completion dates, and for deviation states, transition history and alert banners.
-   **[System properties for Progress Tracker visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-system-properties.md)**  
Two system properties control whether the Progress Tracker displays on purchase requisition and purchase order records. The procurement administrator role is required to read or write these properties.

**Parent Topic:**[Explore Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/exploring-spo.md)

**Related topics**  


[Shopping Hub]()

[Shopping Hub Mobile]()

[Performance Analytics for Sourcing and Procurement Operations]()

[Sourcing and Purchasing Automation]()

[Procurement Case Management]()

[Source-to-Pay Workspace]()

[Exploring the procurement case management implementation]()

[Spend and Savings Management]()

[Sourcing Pipeline Management]()

[Understanding punchout]()

[AI Search for Sourcing and Procurement Operations]()

[Universal Request in Sourcing and Procurement Operations]()

