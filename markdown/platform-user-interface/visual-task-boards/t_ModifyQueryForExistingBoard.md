---
title: Modify the query or lane field for an existing Visual Task Board
description: For flexible and guided Visual Task Boards, you can edit the board query or lane field. This ability enables you to change the board contents while preserving the member list, board configuration settings, and, if applicable, Connect Chat conversation history.
locale: en-US
release: australia
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customizing and configuring Visual Task Boards, Using Visual Task Boards, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Modify the query or lane field for an existing Visual Task Board

For flexible and guided Visual Task Boards, you can edit the board query or lane field. This ability enables you to change the board contents while preserving the member list, board configuration settings, and, if applicable, Connect Chat conversation history.

## Before you begin

Inform the board members that you plan to change the board query or lane field. If you or any members have manually sorted cards within a lane, the order may be reset.

Role required: none, but you must be the board owner

## About this task

The board query consists of filter conditions that determine which tasks the board tracks. For example, you might edit the query so the board shows only active incidents, rather than all incidents.

The lane field is the field on the underlying table that defines the lanes. For example, you might change the lane field so the lanes represent incident states, rather than assignees. This change is called a lane field pivot. Lane field pivots also make it possible to convert a flexible board to a guided board or vice versa.

## Procedure

1.  Open a Visual Task Board.

2.  Select the information icon \(![Board information icon](../image/BoardInfoIcon.png)\) by the board name.

3.  Perform one of the following actions.

<table id="choicetable_uxv_q2g_pv"><tbody><tr><td id="d116170e77">

**Edit the board query**

</td><td>

1.  Under **Board Filter**, select**Edit Filter** to open the condition builder.
2.  Add and remove conditions as needed to edit the query.
3.  Select **Save**.


</td></tr><tr><td id="d116170e107">

**Change the lane field**

</td><td>

1.  Select the **Vertical Lane Field** picker and select a field or the **None** option.

Guided boards have the **Vertical Lane Field** set to a field, such as **State**. Flexible boards have the **Vertical Lane Field** set to **None**. You can change the **Vertical Lane Field** value accordingly to change the board type.

2.  In the confirmation dialog, select **OK**.


</td></tr></tbody>
</table>    The board reloads to reflect the changes.


**Parent Topic:**[Customizing and configuring Visual Task Boards](../concept/configuring-vis-task-boards.md)

