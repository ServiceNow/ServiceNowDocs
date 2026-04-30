---
title: Use the Mouse component
description: Simulate a mouse action, including alternative mouse device buttons, moves, drags, scrolls, and paste operations.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Mouse component

Simulate a mouse action, including alternative mouse device buttons, moves, drags, scrolls, and paste operations.

## Before you begin

Role required: none

## About this task

The Mouse component uses hardware interrupts to simulate the actions of a computer mouse. You can use it to simulate a manual click, drag, move, scroll, or paste operation at an area that you specify in the [ActionSet Settings](../reference/actionset-actions-properties.md) window. Additionally, you can use it to interact with files, objects, menus, or any other items that typically respond to mouse input.

Many properties of the Mouse component are common with other Actions UI components, to configure these properties, see [Properties of Actions \(UI\) components](../reference/properties-actions-ui-components.md).

The properties unique to the Mouse component are given.

|Property|Description|
|--------|-----------|
|Mouse Action Type|Type of mouse device action that the component will perform. The default action is Left Click.|

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **Mouse**.

2.  Drag the Mouse component to the Design surface.

3.  In the Mouse component, click the camera icon \(![Camera icon.](../image/camera-icon.png)\).

    The `Press "CTRL+SHIFT" for selection` message appears.

4.  Press the **Ctrl + Shift** keys.

    The mouse device turns into a crossover icon \(![Crossover icon.](../image/crossover-icon.png)\)

5.  Drag the cursor over the application to capture the area where you want the component to perform an action.

    **Tip:** Include a part of the image that does not change in your selection. This can help the automation find the capture area when the unchanging part is used as an anchor. To designate an anchor, see Step 7.

    The selected part of the program is captured as an image in the Mouse component.

6.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) over the captured image and place on the location where the component will perform an action.

7.  In the Properties pane, select the mouse device action from the Type list.

    The Type list located under the Misc. heading. The default Mouse action is LeftClick.

    You can also select one of the following actions:

    -   LeftDoubleClick
    -   MiddleClick
    -   RightClick
    -   RightDoubleClick
    -   Move
    -   Drag
    -   Drop
    -   ScrollDown
    -   ScrollUp
    -   Paste
    **Note:** To copy an item to the clipboard for pasting, use a Clipboard action.

8.  Add an anchor to the captured image by doing the following actions:

    An anchor is a unique identifier that enables the Mouse component to identify the application where the component will perform an action. Although adding an anchor is a good approach, it's optional. If you don't add an anchor, the Mouse component treats the whole captured image as an anchor. To know more about the anchor, see the steps to use the [Anchor](../concept/anchor.md).

    1.  In the Mouse component, right-click the image and click **Add Anchor**.

        The anchor appears as a yellow rectangle with red borders.

    2.  To identify the content for the Mouse component, drag and place the anchor at the unique location on the image.

        **Tip:**

        To change the dimensions of the anchor, position the mouse device along the edge of the anchor until the mouse device turns into a diagonal two-sided arrow \(![Two-sided arrow.](../image/bi-sided-arrow.png)\) and then drag the anchor.

9.  Capture alternate images by doing the following actions:

    Alternate images prevent an execution failure when the Mouse component does not find the image that was captured first. In that case, the Mouse component then searches for alternate images to execute. You can add as many alternate images as you need.

    1.  In the Mouse component, click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

    2.  In the ALTERNATE IMAGES window, click the add Image icon \(![Add image icon.](../image/add-image-icon.png)\).

    3.  Click the camera icon \(![Camera icon.](../image/camera-icon.png)\).

        The `Press "CTRL+SHIFT" for selection` message appears.

    4.  Press the **Ctrl + Shift** keys.

        The cursor turns into a crossover icon \(![Crossover icon.](../image/crossover-icon.png)\).

    5.  Drag the cursor over the part of the application program on which you want to perform a mouse device action and then release.

        The selected part of the program is captured as an image in the Mouse component.

    6.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) over the captured image and place on the location where the component will perform an action.

    7.  Navigate to the Properties pane.

    8.  In the Misc heading, select the mouse device action from the Type list.

    9.  Click **OK**.

10. To test the component, right-click the component bar and then click **Run From Here**.


## Drag a folder to another folder

Two Mouse components are used in this example. The first identifies the folder and drags it. The second identifies the destination folder and moves the folder inside.![Move a folder to another folder](../image/mouse-example.png)

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

