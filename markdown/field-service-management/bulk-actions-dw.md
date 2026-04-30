---
title: Edit multiple tasks in Dispatcher Workspace
description: Select and open or bundle multiple tasks with Bulk Actions on Dispatcher Workspace.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Edit multiple tasks in Dispatcher Workspace

Select and open or bundle multiple tasks with Bulk Actions on Dispatcher Workspace.

## Select All

The **Select All** check box selects all tasks on the current panel.

**Note:** Changing the filter will unselect previously selected cards.

The checkbox has 3 states.

1.  None selected. No tasks are currently selected. This is the default state.
2.  All selected. All tasks are selected. This is the initial state upon toggling **Select All**.
3.  Indeterminate. Some tasks are selected. After toggling **Select All**, deselecting individual tasks will place the **Select All** checkbox in this state

## Bulk Open

When 1 or more tasks are selected, the **Bulk Open** action appears. Selecting **Bulk Open** will open all selected tasks as individual tabs in Dispatcher Workspace.

## Bulk Auto-assignment

When 1 or more tasks are selected, the **Auto-assignment** action is enabled. Selecting **Auto-assignment** will dynamically schedule all selected tasks. For more information, see [Dynamic scheduling](dynamic-scheduling.md).

## Bundle

When 2 or more tasks are selected, the **Bundle** action appears. Selecting **Bundle** will bundle the selected tasks. For more information, see [Bundling work order tasks](task-bundling-fsm.md)

**Note:** If the Dynamic Scheduling plugin \(com.snc.dynamic\_scheduling\) and Field Service Task Bundling plugin \(com.snc.fsm\_task\_bundle\) are both enabled, the **Auto-assignment** and **Bulk Open** actions will be consolidated into a dropdown menu.

.

