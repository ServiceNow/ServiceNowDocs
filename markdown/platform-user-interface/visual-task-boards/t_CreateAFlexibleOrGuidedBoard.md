---
title: Create a data driven Visual Task Board
description: You can create a flexible or guided data-driven Visual Task Board \(VTB\) for any table that extends Task, such as Incident or Change.
locale: en-US
release: yokohama
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data driven Visual Task Boards, Creating Visual Task Boards, Using Visual Task Boards, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Create a data driven Visual Task Board

You can create a flexible or guided data-driven Visual Task Board \(VTB\) for any table that extends Task, such as Incident or Change.

## Before you begin

Role required: none

## About this task

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Visual Task Boards**.

2.  Next to My Task Boards, click **New**, or if you have never created a task board before click **Create New Visual Task Board**.

3.  From the Create New Board window, click **Data Driven Board**.

4.  From the Task Table list, select a base table of tasks on which to base your board, for example, an incident table.

5.  From the Lane Field list, select the field you want to use for the lane headers.

    To create a flexible board with editable lane headers, select **None**.

    The type of board that is created and the lanes that appear on the board depend on which type of column you select. If you select a reference or choice column, the board is a guided board. Each lane in a guided board represents one possible value for that column and the cards appear in the appropriate lane. For example, if you create a guided task board for incidents using the **State** column, the board shows one lane for each incident state, such as **New** or **Closed**. If you select a column that is not a reference or choice, the board is a flexible board and the board shows the default lanes, **To Do**, **Doing**, and **Done**, with all cards in the **To Do** lane.

6.  [Create a filter](../../using-lists/task/t_CreatingFilters.md) to show only the records you want to work with.

    For example, you might filter out incidents that are not assigned to you.

    Any card that no longer fits the parameters of the filter is automatically removed from the task board.

7.  Click the board name and enter a new name.

    **Note:**

    -   For guided boards created from choice fields, such as **State**, the system creates a lane for each possible choice value. For guided boards created from reference fields, the system creates a lane only for each value in use by a task card. Lanes are added as needed if the reference field values change.
    -   Be sure to enable Card View for more options. Clear the option **Show Compact Cards** &gt; **Show Card Info**.

        ![Compact card view](../image/compact-card-option.png)


## What to do next

[Add a task to a flexible or guided Visual Task Board](t_AddATaskToAFlexibleOrGuidedBoard.md)

**Parent Topic:**[Data driven Visual Task Boards](../concept/data-driven-tasks.md)

