---
title: Configure a Visual Task Board with swimlanes
description: Swimlanes enable you to create an environment with horizontal lanes in addition to vertical lanes. Swimlanes use only compact cards in Visual Task Board.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/visual-task-boards/configureswimlanes.html
release: zurich
product: Visual Task Boards
classification: visual-task-boards
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing and configuring VTB, Use, Visual Task Boards, Personalize your experience, Configure user experiences]
---

# Configure a Visual Task Board with swimlanes

Swimlanes enable you to create an environment with horizontal lanes in addition to vertical lanes. Swimlanes use only compact cards in Visual Task Board.

## Before you begin

Role required: none

## About this task

You can add swimlanes in all types of Visual Task Boards. For more information see [Add or modify Visual Task Board lanes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/visual-task-boards/t_AddOrModifyALane.md).

When you select swimlanes in Visual Task Boards, you can do the following:

-   Name and rename the swimlanes.
-   Move the tasks horizontally and vertically from one user to another.
-   Drag the cards across swimlanes.
-   Reorder swimlanes by dragging them or from **Lane Configuration**.\[Omitted image "laneconfiguration.png"\] Alt text: Lane configuration
-   Collapse and expand swimlanes.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Self-service** &gt; **Visual Task Boards**.

2.  Click **New** and select the board type.

    -   Freeform Board
    -   Data Driven Board
3.  Configure swimlanes in the boards.

    -   In a freeform board, activate the swimlanes by sliding the **Swimlanes** toggle switch in the **Info** tab.

        \[Omitted image "Swimlanesactivate.png"\] Alt text: Activate swimlanes for a freeform board

        The following figure shows a sample freeform board created with swimlanes.

        \[Omitted image "Freeformboardswimlanes.png"\] Alt text: Freeform board with swimlanes

    -   In a data driven flexible board, do the following:

        1.  Select **None** in **Vertical Lane Field** from the drop-down.
        2.  Click **Next** and slide the toggle under the **Info** tab to the right.
<table id="table_pww_dwv_hhb"><tbody><tr><td>

\[Omitted image "flexibleboard.png"\] Alt text: Activate swimlanes for a data driven flexible board

</td><td>

\[Omitted image "Swimlanesactivate.png"\] Alt text: Activate swimlanes by toggle button

</td></tr></tbody>
</table>        The following figure shows a data driven guided board created with swimlanes.

        \[Omitted image "datadrivenswimlanes.png"\] Alt text: Data driven guided board with swimlanes

    -   In a data driven guided board, select **Vertical Lane Field** and **Swimlane Field** while creating the board. You must have created a freeform board in order to create a guided board.

        You can also add swimlanes to the existing guided board by selecting **Swimlane Field** under **Info** tab in the board.

<table id="table_qsc_2yv_hhb"><tbody><tr><td>

\[Omitted image "swimlanedata.png"\] Alt text: Activate a data driven swim lane

</td><td>

\[Omitted image "guidedswimlanes2.png"\] Alt text: Activate swimlanes in existing board

</td></tr></tbody>
</table>
**Parent Topic:**[Customizing and configuring Visual Task Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/visual-task-boards/configuring-vis-task-boards.md)

