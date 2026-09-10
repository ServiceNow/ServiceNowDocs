---
title: Progress Tracker component reference
description: The Progress Tracker component displays workflow progress on purchase requisitions and purchase orders through a stepper visualization and expandable info card. The info card shows assigned users, pending work items, completion dates, and for deviation states, transition history and alert banners.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-info-card.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 4
breadcrumb: [Progress Tracker overview, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Progress Tracker component reference

The Progress Tracker component displays workflow progress on purchase requisitions and purchase orders through a stepper visualization and expandable info card. The info card shows assigned users, pending work items, completion dates, and for deviation states, transition history and alert banners.

## Component overview

The Progress Tracker is a two-part component: a stepper \(the workflow visualization at the top\) and an expandable info card \(details view when a step is selected\). The stepper displays workflow states in sequence and highlights the current step. The info card provides contextual details including assigned users, pending work items, and completion dates. For deviation states, the info card also displays a transition history and alert banner explaining why the record deviated.

## Stepper placement and persistence

The Progress Tracker stepper renders above the tab navigation on PR and PO records in the Source-to-Pay Workspace details tab. It remains visible across all tabs, providing persistent access to progress information.

## Stepper indicators and tooltips

|Indicator|Description|
|---------|-----------|
|Per-state duration tooltip|Hovering over a step displays how long the record spent in that state, computed from the record state history.|
|Pending cases/tasks tooltip|Hovering over a step displays the cases or tasks still pending for that step.|
|SLA indicator|Displays the time remaining on the record SLA \(record-level, not per-step\). Distinct from the per-state duration tooltip, which is scoped to a single step.|
|State text labels|Labels in the stepper reflect the record actual state names and are not paraphrased.|
|Step completion icons|Completed happy-path steps display a green checkmark. Closed Rejected and Closed Canceled display a red X icon on the terminal step.|

The stepper itself does not display avatar bubbles; avatars appear only in the expandable info card.

## Info card fields

Select a step in the stepper to expand an info card with the following fields:

-   **State badge and avatars**

    Displays the current state label as a badge with assigned user avatars. Up to 8 avatars display inline \(1 primary plus 7 in the overflow row\). An ellipsis trigger appears only when you select the "+N" badge, never on initial load, and only when more than 8 assignees exist.

-   **Date Completed**

    Displays the date the step finished, or "---" if the step is still in progress.

-   **Work Items**

    Links to related work items for the step \(for example, task or approval records\). When no linked records exist, this field displays contextual guidance describing the next action instead of a list of links.

-   **Transition history**

    Displays only for deviation states. A chronological log of state changes with timestamp, actor, and a short description for each entry. Each entry is selectable and surfaces further context.

-   **Alert banner**

    Displays only for deviation states. Appears at the top of the State section and explains why the record deviated and, where applicable, what action is needed.


## Info card content by state category

|State category|Badge|Date Completed|Work Items|Transition history / Alert banner|
|--------------|-----|--------------|----------|---------------------------------|
|Happy path \(in progress\)|Current state|"---"|Links to related work items|Not displayed|
|Happy path \(completed step\)|Step state|Actual date|Contextual guidance message|Not displayed|
|Pending Revision|"Pending Revision"|Not displayed|Guidance to resubmit|Displayed \(chronological log\); displayed \(revision trigger and date\)|
|Closed Rejected|"Closed Rejected"|Actual date|Empty or not applicable|Optional; displayed \(rejection cascade and date\)|
|Closed Canceled|"Closed Canceled"|Actual date|Empty or not applicable|Optional; displayed \(cancellation reason and date\)|

\[Omitted image "progress-tracker-pr-happy-path.png"\] Alt text: Info card showing in-progress step with state badge, avatars, and pending work items.

\[Omitted image "progress-tracker-pr-pending-revision.png"\] Alt text: Info card showing Pending Revision state with alert banner and transition history.

## Click behavior

Work item links navigate to the linked record within the same workspace tab; no new browser tab opens. Transition history entries are selectable and surface a contextual popover or navigate to the related approval or activity record. For step-by-step instructions on using the info card, see [Use the Progress Tracker info card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/use-progress-tracker-info-card.md).

## PO-specific info card content

On PO records, the **Work Items** field is populated from receipt task, invoice task, service acknowledgment task, spend task, milestone, and procurement case records depending on the current state. This differs from PR records, which use approval or fulfillment tasks. When no task-based assignee exists for a state, the info card falls back to a configured header field \(for example, the PO business owner\) for selected states only.

## Permanently locked fields

The **Submitted by** field is permanently read-only \(**strict\_read\_only**\) on both the Sourcing Activity \(SRC\) record and the Purchase Requisition \(PR\) record. This lock applies regardless of the record current Progress Tracker state, and it is not exposed as an administrator-configurable option. The state-configuration task does not control field-level locking.

**Parent Topic:**[Progress Tracker for purchase requisitions and purchase orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-overview.md)

**Related topics**  


[System properties for Progress Tracker visibility]()

