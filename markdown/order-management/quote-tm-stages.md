---
title: Quote transaction stages
description: Stages represent phases in the quoting process. Each stage can have entry criteria, rule group associations, and stage-specific layout behavior in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-stages.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction stages

Stages represent phases in the quoting process. Each stage can have entry criteria, rule group associations, and stage-specific layout behavior in ServiceNow CPQ.

Stages structure the quoting process into discrete phases. A typical implementation uses stages such as Draft, Pending Approval, Approved, Contracted, and Ordered, but administrators can add or remove stages to match their organization's selling process. A transaction is in one stage at a time.

## Stage ordering

Administrators can change the order in which stages are evaluated. In the stages list, select a stage and select the chevron icon to access reordering controls. Use the **&lt;** and **&gt;** buttons to move the stage in the sequence. The **+** button creates a new stage at the selected position in the sequence.

## Transitions between stages

Transitions represent structured movement from one stage to the next. A transaction cannot automatically transition between stages without an event — such as a **Submit for Approval** or **Revise** button — that explicitly triggers the transition. Stage transitions can also be defined for when a new transaction is created or edited.

## Entry criteria

Entry criteria are conditions that must be met before a transaction can advance to a stage. When an event transition is set to **forward**, ServiceNow CPQ evaluates the entry criteria of each succeeding stage until a stage's criteria are met. If no stage meets the criteria, no transition occurs. When an event transition is set to **backward**, the transaction moves to the stage defined by the administrator without checking entry criteria. The first stage in a process has no entry criteria.

For example, a transaction might transition to the **pending approval** stage, or, if approval is not required, it might bypass **pending approval** and move directly to the **approved** stage. This is configured using entry criteria on the **pending approval** stage.

## Stages and rule groupings

Rule groupings are associated with stages. They execute when the stage is transitioned to and when users update fields or run events while in the stage. For more information about rule groupings, see [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md).

## Stages and views

Stages enable administrators to assign distinct permissions to determine how personas view and interact with field data at each stage. For more information about defining views for stages, see [Quote transaction views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-views.md).

## Behavior on open transaction

The **Behavior on Open Transaction** stage setting determines which rule groupings and integrations run when a user opens a transaction in that stage. Administrators can configure the **Refresh Product Data** toggle to refresh product data when the transaction opens, and can add one or more rule groupings or integrations to run on open.

## Behavior on idle timeout

The **Behavior on Idle Timeout** stage setting defines an event that triggers after a user remains inactive for a specified period. Administrators can define one such event per stage. If the event fails on its first execution, it is not retried or requeued. Supported action types are rule groups and integrations.

Note the following guidelines when configuring idle timeout behavior:

-   Set the idle time carefully to balance user convenience with session management and system efficiency.
-   Test all configured rule groups and integrations in a nonproduction environment before enabling them in live stages.

## Deleting a stage

Deleting a stage is restricted because deleting a stage that is in use by transactions can cause data issues. Contact [ServiceNow Support](https://support.servicenow.com) if a stage deletion is required.

