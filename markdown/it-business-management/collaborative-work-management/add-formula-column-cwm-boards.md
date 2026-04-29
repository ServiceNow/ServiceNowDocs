---
title: Add a formula column in CWM Boards
description: Gain deeper insights into your work by adding formula columns to your List view in CWM Boards. Create calculations that automatically compute values for your tasks, such as summing hours, calculating date differences, or deriving metrics from existing fields.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [formula column, CWM, formula builder, List view, add column, formula syntax, Math, Date and Time]
breadcrumb: [Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Add a formula column in CWM Boards

Gain deeper insights into your work by adding formula columns to your List view in CWM Boards. Create calculations that automatically compute values for your tasks, such as summing hours, calculating date differences, or deriving metrics from existing fields.

## Before you begin

[Create a Board in CWM](create-boards-in-cwm.md).

Role required: sn\_cwm.cwm\_user

You need to have either Editor or Owner access to the Space to add a custom column.

## About this task

Formula columns in the List view of a CWM Board compute values from existing CWM columns. Examples include calculating date differences from existing Date columns or deriving metrics such as Profit from existing values of Revenue and Cost columns.

Use the built-in Math, String, Date &amp; Time, and Logical functions in the Formula Builder side panel to define a formula expression. To automatically generate a formula from a plain language description using Now Assist instead, see [Generate a formula using Now Assist for CWM](../../now-assist-cwm/task/generate-formula-cwm-board-now-assist.md).

The steps in this procedure use the example of a formula column that calculates the number of days remaining until a task's due date. Follow the steps as guidelines to build a formula of your choice.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, open the Board where you want to add a formula column.

3.  In the List view of the Board, select **Add column** from the column header and select **Formula**.

    ![Add column menu in the List view of a CWM Board, with the Formula option selected.](../images/cwm-formula-column.png)

4.  Provide a name for your formula column.

    In this example, the column is named **Days until due**.![Formula column name field with "Days until due" entered as the column name.](../images/cwm-formula-column-name.png)

5.  In the Define Formula side panel, use the Math, String, Date &amp; Time, and Logical functions to build your formula.

    To arrive at the number of days remaining from the due date, use the Date &amp; Time functions to build a formula that calculates difference \(in days\) between the current day and the due date.

    **DATEDIF\(TODAY\(\),"Due Date","D"\)**

    ![Define Formula side panel showing the DATEDIF(TODAY(),"Due Date","D") formula entered to calculate days remaining until the due date.](../images/cwm-formula-definition.png)

6.  Select **Set Formula** to save and apply the formula column.


## Result

-   The Board refreshes to display the new formula column, and its values populated per the formula you defined.
-   If your formula contains any syntax errors, you are notified of the same and then you can review it and correct it.

![CWM Board List view displaying the new formula column with computed values populated for each task.](../images/cwm-formula-on-board.png)

**Parent Topic:**[Managing work using Boards in CWM](../concept/cwm-boards.md)

**Related topics**  


[Add custom columns for tasks in a CWM Board](add-custom-columns-for-tasks-in-board.md)

[Generate a formula using Now Assist for CWM](../../now-assist-cwm/task/generate-formula-cwm-board-now-assist.md)

