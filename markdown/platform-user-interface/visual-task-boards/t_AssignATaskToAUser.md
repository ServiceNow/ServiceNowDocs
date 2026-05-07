---
title: Assign a Visual Task Board card to a user
description: Assignees represent ownership of task cards and the associated records. Each task card can have one primary assignee and multiple additional assignees.
locale: en-US
release: australia
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with Visual Task Board cards, Using Visual Task Boards, Visual Task Boards, Configure UIs and portals, Configure user experiences]
---

# Assign a Visual Task Board card to a user

Assignees represent ownership of task cards and the associated records. Each task card can have one primary assignee and multiple additional assignees.

## Before you begin

Role required: admin

## About this task

You can filter the visible tasks on a board to show only tasks assigned to a certain user. Assignees appear on cards as avatars.

![Task card assignees](../image/AssigneeOnCardHelsinki.png "Task card assignees")

When a card changes lanes, all the assignees receive an email notification.

For flexible and guided boards, the primary assignee corresponds to the underlying task's **Assigned to** field. For example, on a board created from the Incident table, if you add Joe Employee as the primary assignee for a card, the associated incident is assigned to Joe. Note that assignment rules on the associated table may restrict who you can make the primary assignee of a card. If you attempt to assign a task card to a user in a way that violates an assignment rule, a notification appears and the assignment does not take place.

**Note:** Assignees are not automatically granted access to the board. Only members can access the board.

## Procedure

1.  Do one of the following actions.

<table id="choicetable_l4n_x4d_pt"><tbody><tr><td id="d59364e91">

**Add an assignee from the quick panel**

</td><td>

1.  Drag a user's avatar from the quick panel directly to the task card.
2.  Drop the avatar in the **Primary** or **Additional** drop zone.


</td></tr><tr><td id="d59364e115">

**Add an assignee from the card details**

</td><td>

1.  Open the card details for a task.
2.  Click the assignees tab \(![Assignees tab](../image/AssigneesTab.png)\).
3.  Click **Add Primary Assignee** or **Add Additional Assignee**. The **Add Primary Assignee** option is not available if there is already a primary assignee.
4.  Select a user.
5.  Close the card detail pop-up window.


</td></tr></tbody>
</table>    The system sends an email notification to inform the new assignee of the change.


**Parent Topic:**[Working with Visual Task Board cards](../reference/r_TaskCards.md)

