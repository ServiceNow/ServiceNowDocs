---
title: Enhancing event task management with Hierarchical view
description: The Hierarchical view for event tasks has been enhanced with several key features. It now displays dependencies between tasks, and shows color-coded states with planned start and end dates. Dependencies can be updated directly through the Hierarchical view \(Gantt chart\), streamlining event task management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Enhancing event task management with Hierarchical view

The Hierarchical view for event tasks has been enhanced with several key features. It now displays dependencies between tasks, and shows color-coded states with planned start and end dates. Dependencies can be updated directly through the Hierarchical view \(Gantt chart\), streamlining event task management.

## Sorting plans

In the Hierarchical view, activated plans are now sorted by their start date. The example shows an event task with activated plan, its start date, end date, state, and so on. The start date for the plan shown in the example is 18th.

![Sort.](../image/sort-plan.png)

The plans are displayed in sorted order. The example shows the next plan having a start date of the 20th.

![Start.](../image/sort-plan-start-date.png)

Color-coded plans offer a visually organized view.

![Color.](../image/sort-plan-color-coding.png)

## Managing task dependencies in Hierarchical view \(Gantt chart\)

To manage task dependencies, you can select **View dependencies** in the Dependencies column. This enhancement enables you to view the dependencies between tasks, including the state of the dependent plan and other relevant details.

![RT3.](../image/sort-plan-rt3.png)![View dependencies.](../image/gantt-view-task-dep.png)

After selecting **View dependencies**, a modal view is shown, displaying the dependency details, including the dependent task \(for example, RT3 is dependent on RT2\), its dependency \(RT2\), and the state of the dependent plan \(activated\). This display provides a clear understanding of task relationships and their current status.

![Details.](../image/gantt-view-task-dep-details.png)

You can visualize and manage task dependencies directly in the Gantt view. All dependencies are clearly displayed, enabling you to understand task relationships at a glance. To delete a dependency, select the link between tasks and press the Backspace or Delete key on the keyboard.

![Delete.](../image/event-task-dep-del.png)

To create a new dependency, drag from the end of one task to the start of another task and add a link. This action establishes a dependency between the two tasks, enabling you to manage their relationship effectively. When a dependency changes, all affected tasks' planned start times are updated accordingly.

![Drag.](../image/event-task-dep-drag.png)

You can create multiple links between tasks as needed, enabling for flexible dependency management directly within the Gantt chart. However, attempting to create a cyclic dependency \(for example, making Task 2 dependent on Task 1 when Task 1 is already dependent on Task 2\) results in an error, as it can cause cyclic dependencies. The system helps to prevent such configurations to maintain a valid and manageable project structure.

![Error.](../image/event-task-dep-error.png)

## Color-coded bars

The bars in the chart are color-coded, and selecting the legends reveals the color conventions for different task states, such as Closed complete, Closed duplicate, Closed incomplete, and others. This color-coding system helps to identify the status of tasks quickly.

![Color.](../image/event-task-dep-color-code.png)

The task states are represented by these color codes:

-   Green: All "Closed" states
-   Red: "Closed failed" states
-   Grey: "Hold" and "Pending" states, indicating a waiting or paused status
-   Blue: "Open" state, signifying that a task is open and ready for action
-   Yellow: "Working progress" state, indicating that a task is in progress

This color-coding system provides a clear visual representation of task statuses, making it easier to track progress and identify areas that require attention.

![Codes.](../image/event-task-de-color-code-explained.png)

In the Gantt view, tasks are color-coded based on their status: yellow for "work in progress" and blue for "open" tasks. Hovering over a task bar displays additional information, including the task state, plan start and end dates, and assignment details if applicable. The Planned start and Planned end dates are also introduced at the activated plan level, which are calculated based on the associated event tasks. It’s shown that the planned start date is 18th and the planned end date is 21st.

![Start.](../image/event-task-dep-plan-start.png)

In the example, the first event task begins on the 18th and concludes on the 21st. Since the second task is dependent on the first, it starts on the 21st and ends on the 24th. This dependency-based timeline calculation applies to all subsequent tasks. The Gantt chart is interactive, enabling you to adjust its size. Selecting **Show more** on any activated plan enables you to view detailed information, including completed plans.

![More.](../image/event-task-dep-plan-start-show-more.png)

You can view the actual start and end dates in the Gantt chart. To view the dates, select the toggle and the chart gets updated to display the actual dates, providing an accurate representation of the progress of the project.

![Start.](../image/event-task-dep-actual-start.png)![End date.](../image/event-task-dep-actual-start-end.png)

You can toggle between viewing planned dates and actual dates using the switch button, enabling for easy comparison and tracking the progress of the project.

**Parent Topic:**[Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md)

