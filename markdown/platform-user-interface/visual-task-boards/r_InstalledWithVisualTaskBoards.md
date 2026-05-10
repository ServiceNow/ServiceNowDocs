---
title: Installed with Visual Task Boards
description: Several types of components are installed with Visual Task Boards.Tables are added to your instance when you activate Visual Task Boards.Properties are added to your instance when you activate Visual Task Boards.Script includes are added to your instance when you activate Visual Task Boards.Client scripts are added to your instance when you activate Visual Task Boards.Business rules are added to your instance when you activate Visual Task Boards.Notifications are added to your instance when you activate Visual Task Boards.
locale: en-US
release: australia
product: Visual Task Boards
classification: visual-task-boards
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Visual Task Boards reference, Visual Task Boards, Configure UIs and portals, Configure user experiences]
---

# Installed with Visual Task Boards

Several types of components are installed with Visual Task Boards.

**Parent Topic:**[Visual Task Boards reference](../concept/vis-task-boards-ref.md)

## Tables installed with Visual Task Boards

Tables are added to your instance when you activate Visual Task Boards.

<table id="table_mvy_5vb_dt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Board Member\[vtb\_board\_member\]

</td><td>

Stores a record for each member of each task board.

</td></tr><tr><td>

Private Task\[vtb\_task\]

</td><td>

Stores a record for each personal task on each freeform board.

</td></tr><tr><td>

Visual Task Board\[vtb\_board\]

</td><td>

Stores a record for each task board.

</td></tr><tr><td>

Visual Task Board Card\[vtb\_card\]

</td><td>

Stores a record for each task card on each task board.

</td></tr><tr><td>

Visual Task Board Card History\[vtb\_card\_history\]

</td><td>

Stores records for certain task card changes, such as lane or assignee changes. Each record indicates the previous value and the new value.

</td></tr><tr><td>

Visual Task Board Lane\[vtb\_lane\]

</td><td>

Stores a record for each lane on each task board.

</td></tr></tbody>
</table>## Properties installed with Visual Task Boards

Properties are added to your instance when you activate Visual Task Boards.

<table id="table_hhg_ybc_dt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

vtb.board.upload\_limit

</td><td>

Sets the maximum file size in megabytes allowed for each task card attachment.-   **Type**: integer
-   **Default value**: 10
-   **Location**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Script includes installed with Visual Task Boards

Script includes are added to your instance when you activate Visual Task Boards.

|Script include|Description|
|--------------|-----------|
|VisualTaskBoards|Provides general utilities for Visual Task Boards.|
|VTBBoardSecurity|Provides security utilities to control board access.|
|VTBGetBoardsByUser|Provides a method that retrieves all the boards a specified user owns or is a member of.|
|VTBTaskSecurity|Provides security utilities to control task access.|

## Client scripts installed with Visual Task Boards

Client scripts are added to your instance when you activate Visual Task Boards.

<table id="table_qmf_wwc_dt"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Kanban Choice

</td><td>

Visual Task Board\[vtb\_board\]

</td><td>

Adds the **-- Kanban Board --** option to the **Lane field** field. This option indicates that the task board is a flexible board.

</td></tr></tbody>
</table>## Business rules installed with Visual Task Boards

Business rules are added to your instance when you activate Visual Task Boards.

<table id="table_vwl_f3c_dt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add members to live group

</td><td>

Board Member\[vtb\_board\_member\]

</td><td>

If a Connect Chat conversation is created for a task board, this business rule adds the board members as conversation members.

</td></tr><tr><td>

Remove member from live group

</td><td>

Board Member\[vtb\_board\_member\]

</td><td>

If a Connect Chat conversation exists for a task board and a user is removed from the board members, this business rule removes the user from the conversation members.

</td></tr><tr><td>

Remove member from VTB

</td><td>

Live Group Member\[live\_group\_member\]

</td><td>

If a Connect Chat conversation exists for a task board and a user is removed from the conversation members, this business rule removes the user from the task board members.

</td></tr><tr><td>

Sync board name to Connect

</td><td>

Visual Task Board \[vtb\_board\]

</td><td>

If a Connect Chat conversation exists for a task board and someone updates the board name, this business rule updates the conversation name.

</td></tr><tr><td>

Sync chat name to VTB board

</td><td>

Live Group Profile\[live\_group\_profile\]

</td><td>

If a Connect Chat conversation exists for a task board and someone updates the conversation name, this business rule updates the board name.

</td></tr><tr><td>

Sync Members With VTB

</td><td>

Live Group Member\[live\_group\_member\]

</td><td>

If a Connect Chat conversation exists for a task board and a user is added to the conversation members, this business rule adds the user as a board member.

</td></tr><tr><td>

Update Board on Card Change

</td><td>

Visual Task Board Card\[vtb\_card\]

</td><td>

Triggers the system to update the task board when changes occur to the cards.

</td></tr><tr><td>

Update Board on Lane Change

</td><td>

Visual Task Board Lane\[vtb\_lane\]

</td><td>

Triggers the system to update the task board when changes occur to the lanes.

</td></tr><tr><td>

update board on lane change

</td><td>

Board Member\[vtb\_board\_member\]

</td><td>

Triggers the system to update the task board when changes occur to the board members.

</td></tr><tr><td>

VTB Previous Additional Assignees

</td><td>

Private Task\[vtb\_task\]

</td><td>

Triggers the system to send an email notification to users when they are designated as additional assignees for cards.

</td></tr></tbody>
</table>**Related topics**  


[Connect Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/c_Collaboration.md)

## Notifications installed with Visual Task Boards

Notifications are added to your instance when you activate Visual Task Boards.

|Notification|Description|
|------------|-----------|
|VTB member addition notification|Sends an email notification to the member about their addition to the board.|
|VTB member deletion notification|Sends an email notification to the member about their removal from the board.|
|VTB additional assignee notification|Sends an email notification to users when they are designated as additional assignees for tasks.|
|VTB assignee notification|Sends an email notification to users when they are designated as the primary assignees for personal tasks.|
|VTB lane change notification|Sends an email notification to a task's assignees when the task changes lanes.|
|VTB lane limit reached|Sends an email notification to the board member that the number of tasks in the lane has reached the set lane limit.|
|VTB lane limit exceeded|Sends an email notification to the board member that the number of tasks in the lane has exceeded the set lane limit.|
|VTB card movement across vertical lanes and swimlanes|Sends an email notification to the board member with the details of the card moved and the member who moved the card.|

