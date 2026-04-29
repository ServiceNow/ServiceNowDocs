---
title: Generate a formula using Now Assist for CWM
description: Use Now Assist to automatically generate formulas to compute values such as summing hours, calculating date differences, or deriving metrics from existing fields.
locale: en-US
release: australia
product: Now Assist for Collaborative Work Management \(CWM\)
classification: now-assist-for-collaborative-work-management-cwm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [formula column, Now Assist, CWM, formula builder, List view, generate formula, formula syntax]
breadcrumb: [Use, Now Assist for CWM, Strategic Portfolio Management]
---

# Generate a formula using Now Assist for CWM

Use Now Assist to automatically generate formulas to compute values such as summing hours, calculating date differences, or deriving metrics from existing fields.

## Before you begin

Role required: sn\_cwm\_ai.cwm\_ai\_user

## About this task

Generate a formula in CWM using Now Assist 

Formula columns in the List view of a CWM Board compute values from existing CWM columns. Examples include calculating date differences from existing Date columns or deriving metrics such as Profit from existing values of Revenue and Cost columns.

Instead of building the formula syntax manually, you can describe your calculation in plain language, and Now Assist generates a valid formula that you can insert directly into the column with a single click.

The steps in this procedure use the example of a formula column that calculates the number of days remaining until a task's due date. Follow the steps as guidelines to build a formula of your choice.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, open the Board where you want to add a formula column.

3.  In the List view of the Board, select **Add column** from the column header and select **Formula**.

    ![Add column menu in the List view of a CWM Board, with the Formula option selected.](../../collab-work-mgmt/images/cwm-formula-column.png)

4.  Provide a name for your formula column.

    In this example, the column is named **Days until due**.![Formula column name field with "Days until due" entered as the column name.](../../collab-work-mgmt/images/cwm-formula-column-name.png)

5.  In the Define Formula side panel, describe your formula in natural language in the Now Assist input field and submit.

    In this example, the input is `Count the number of days remaining from today until the due date.`

    ![The Define Formula side panel showing a natural language description entered in the Now Assist input field.](../images/na-cwm-formula-instruction.png)

    Now Assist generates a formula syntax based on your instruction.

6.  Review the generated formula and select **Insert** to add it to the Formula field.

    ![The Define Formula side panel showing the Now Assist-generated formula syntax with the Insert button available.](../images/na-cwm-formula-insert.png)

7.  Select **Set Formula** to save and apply to the formula column.


## Result

The Board refreshes to display the new formula column, and its values populated per the formula you defined.![CWM Board List view displaying the new formula column with computed values populated for each task.](../../collab-work-mgmt/images/cwm-formula-on-board.png)

**Related topics**  


[Add a formula column in CWM Boards](../../collab-work-mgmt/task/add-formula-column-cwm-boards.md)

[Add custom columns for tasks in a CWM Board](../../collab-work-mgmt/task/add-custom-columns-for-tasks-in-board.md)

