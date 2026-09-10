---
title: Care Team Work Management data model
description: The following diagram shows the tables and their relationships within Care Team Work Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/ctwm-data-model.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Care Team Work Management data model

The following diagram shows the tables and their relationships within Care Team Work Management.

\[Omitted image "ctwm-data-model.png"\] Alt text: Data model for Care Team Work Management.

## Key relationships

The data model is anchored on three records that move together through the lifecycle of a unit-level piece of work:

-   **Care team case \[sn\_cto\_case\]** — The unit-level container generated from a task plan. A care team case represents the work that a single unit must complete.
-   **Work order \[wm\_order\]** — The fulfillment record that mirrors the care team case. Exactly one work order is created for each care team case, and the two records maintain a strict 1:1 relationship for the entire lifecycle.
-   **Care team task \[sn\_cto\_task\]** — The individual, actionable steps that agents complete. Care team tasks extend the work order task \[wm\_task\] table and are attached to the case's single work order.

The orchestration case \[sn\_hco\_orchestration\_case\] sits above this trio. A single orchestration case can fan out to multiple care team cases — one per supporting unit — but each of those care team cases still owns a single work order and its own set of care team tasks.

## State synchronization

Because the care team case and work order are 1:1, their states stay aligned:

-   When the care team case state changes — for example, from **New** to **In Progress** — the associated work order moves to the equivalent state.
-   When the work order state changes as a result of fulfillment activity, the care team case is updated to match.

## Rollup from tasks to case

Care team task completion drives the case lifecycle:

1.  Each care team task is created in a ready-for-work state under the case's single work order. No manual qualification or dispatch step is required.
2.  As agents complete tasks, the work order tracks aggregate progress.
3.  When all tasks under the work order are completed, the work order transitions to a completed state.
4.  The care team case state is updated to reflect the completed work order.

This pattern is consistent with how fulfillment runs in other healthcare domains such as Biomed, Environmental Services, and Facilities.

