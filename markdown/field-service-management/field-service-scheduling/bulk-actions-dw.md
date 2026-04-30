---
title: Edit multiple tasks in Dispatcher Workspace
description: Select and open or bundle multiple tasks with Bulk Actions on Dispatcher Workspace.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Dispatcher Workspace, Assigning WOTs from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Edit multiple tasks in Dispatcher Workspace

Select and open or bundle multiple tasks with Bulk Actions on Dispatcher Workspace.

## Select All

The **Select All** check box selects all tasks on the current panel.

**Note:** Changing the filter unselects previously selected cards.

The check box has three states.

1.  None selected. No tasks are currently selected. This option is the default state.
2.  All selected. All tasks are selected. This option is the initial state upon toggling **Select All**.
3.  Indeterminate. Some tasks are selected. After toggling **Select All**, deselecting individual tasks will place the **Select All** check box in this state

## Bulk Open

When one or more tasks are selected, the **Bulk Open** action appears. Selecting **Bulk Open** opens all selected tasks as individual tabs in Dispatcher Workspace.

## Bulk Auto-assignment

When one or more tasks are selected, the **Auto-assignment** action is enabled. Selecting **Auto-assignment** will dynamically schedule all selected tasks. For more information, see [Dynamic scheduling](dynamic-scheduling.md).

## Bundle

When two or more tasks are selected, the **Bundle** action appears. Selecting **Bundle** creates a bundle of the selected tasks. For more information, see [Bundling work order tasks](task-bundling-fsm.md)

**Note:** If the Dynamic Scheduling plugin \(com.snc.dynamic\_scheduling\) and Field Service Task Bundling plugin \(com.snc.fsm\_task\_bundle\) are both enabled, the **Auto-assignment** and **Bulk Open** actions are consolidated into a drop-down menu.

.

