---
title: Demand tasks
description: A demand task is a unit of work created within a demand to break down initial planning activities before converting the demand into an entity.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Demand tasks

A demand task is a unit of work created within a demand to break down initial planning activities before converting the demand into an entity.

## Demand tasks overview

You can create a demand task from the **Demand Tasks** related list to delegate activities that help assess demand feasibility.

Demand tasks differ from project tasks in the following ways:

-   Planned dates, actual dates, and original dates aren’t supported in demand tasks.
-   The due date indicates when the task is targeted for completion and doesn’t affect the demand workflow. Project tasks affect project completion dates when planned dates and actual dates are changed.
-   Nested demand tasks aren’t supported.
-   Task constraints such as Start ASAP and Start on a specific date aren’t supported.
-   Execution types such as Agile, Waterfall, or Hybrid aren’t supported.

## Resource assignment

Resources for a demand task can be assigned using the **Assigned to**, **Additional Assignee list**, and **Assignment Group** fields. Don’t create resource assignments to allocate resources or groups to a demand task or submit time spent on the demand. If you associate a resource assignment with a demand task, the associated resource plan isn’t transferred to the work entity created from that demand.

Resource assignments aren’t associated with the demand by default. Don’t use the resource assignments you created for the future work entity to submit time spent on a demand. When you submit a time card for a demand, the time and cost incurred aren’t transferred to the work entity created from the demand. The time and cost remain within the demand as the demand cost and effort. Resources assigned to a demand task can submit the time spent on it using a time card.

## Actual cost and effort

The actual effort for work performed on the demand task is derived from the time card. The actual cost is derived from the hourly resource rate defined in the rate model, default labor rate, or default system property. The actual cost and effort for a demand task roll up to derive the actual cost and effort for the associated demand. For more information, see [Actual cost and effort calculation for a demand and demand task](actual-cost-and-effort-calculation-ppw.md).

