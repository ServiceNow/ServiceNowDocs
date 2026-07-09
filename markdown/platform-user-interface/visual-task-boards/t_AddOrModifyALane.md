---
title: Add or modify Visual Task Board lanes
description: Any board member can change the names and add new lanes to accommodate the task workflow you want to track. When you create a freeform or flexible task board, it includes the default lanes To Do, Doing, and Done.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/visual-task-boards/t\_AddOrModifyALane.html
release: zurich
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating VTB, Use, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Add or modify Visual Task Board lanes

Any board member can change the names and add new lanes to accommodate the task workflow you want to track. When you create a freeform or flexible task board, it includes the default lanes **To Do**, **Doing**, and **Done**.

## Before you begin

Role required: none

## About this task

Unlike guided boards, the lanes on a freeform or flexible task board do not match possible field values.

**Note:** You cannot remove lanes from guided boards.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Visual Task Boards**.

2.  Open a task board.

3.  Perform any of the following actions.

<table id="choicetable_chv_rys_kv"><tbody><tr><td id="d48801e113">

**Create a new lane**

</td><td>

1.  Scroll past the last lane and click **Add Lane**.
2.  Enter a title for the lane, then press the Enter key.
 The **Add Lane** option is always available for freeform and flexible boards. It is available for guided boards only if the lanes are based on a reference field, such as **Assigned to**.

</td></tr><tr><td id="d48801e143">

**Edit a lane name**

</td><td>

1.  Select the lane name in the lane header.
2.  Enter a title for the lane, then press the Enter key.


</td></tr><tr><td id="d48801e161">

**Rearrange lanes**

</td><td>

Select a lane header and drag the lane to the desired drop zone. To cancel the move, press the Escape key while you drag the lane.You can also change the lane order from the board configuration menu.

</td></tr><tr><td id="d48801e173">

**Hide a lane**

</td><td>

1.  Select the lane menu \(\[Omitted image "IconMoreOptions.png"\] Alt text: Lane menu icon\) in a lane header.
2.  Select **Hide Lane**.


</td></tr><tr><td id="d48801e200">

**Unhide a lane**

</td><td>

1.  Select the configuration menu \(\[Omitted image "icon-configuration.jpg"\] Alt text: Configuration menu\).
2.  Select **Advanced Settings**.
3.  Select the hidden lane in the **Lane Configuration** section.


</td></tr><tr><td id="d48801e234">

**Delete a lane**

</td><td>

1.  Select the lane menu in a lane header.
2.  Select **Delete Lane**.
3.  In the confirmation dialog box, click **Delete**. When you delete a lane on a freeform or flexible board, all the cards in the deleted lane are archived.
 The **Delete Lane** option is always available for freeform and flexible boards. It is available for guided boards only if the lanes are based on a reference field, and only for lanes that contain no cards.

</td></tr><tr><td id="d48801e267">

**Exclude Child Table Records**

</td><td>

1.  Select **Info** icon \(\[Omitted image "BoardInfoIcon.png"\] Alt text: Info icon
2.  Under **Structure** menu, select **Exclude Child Table Records** \[Omitted image "excludechildtables.png"\] Alt text: Exclude Child Tables

The Child table lanes and records are excluded.

**Note:** **Exclude Child Table Records** check box is only visible for choice type field.

</td></tr></tbody>
</table>    **Note:** When moving the card from lane to another, if you get an error message while having write access to the record then create a system property **glide.vtb.enable\_list\_edit\_acl** and set it to **false**.


**Parent Topic:**[Creating Visual Task Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/visual-task-boards/c_VisualTaskBoardUse.md)

**Related topics**  


[Freeform Visual Task Boards]()

[Data driven Visual Task Boards]()

[Add a task to a flexible or guided Visual Task Board]()

[Add or remove a Visual Task Board member]()

[Delete a Visual Task Board]()

