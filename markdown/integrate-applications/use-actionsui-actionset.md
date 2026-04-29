---
title: Use the ActionSet component
description: The ActionSet component lets an automation interact with Windows applications \(such as web browsers\) and with Citrix applications. Using this single component in RPA Desktop Design Studio, you can click, drag, read and set text, interact with tables, and more, combining several user actions into a single task.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ActionSet component

The ActionSet component lets an automation interact with Windows applications \(such as web browsers\) and with Citrix applications. Using this single component in RPA Desktop Design Studio, you can click, drag, read and set text, interact with tables, and more, combining several user actions into a single task.

## Before you begin

Role required: none

## About this task

Using the ActionSet component, you can simulate a user interaction in an automation by specifying multiple user actions.

You can configure the properties for the ActionSet component settings. For more information about these properties, see [Properties of Actions \(UI\) components](../reference/properties-actions-ui-components.md).

Using the controls in the window, you capture an area of an application window, set one or more anchors, and define the user interactions that you want to simulate in that window. An anchor helps specify the target area for the interaction by defining a static area from which actions can be defined at a relative distance. For more information about anchors, see [Anchor](../concept/anchor.md).

![ActionSet Settings Window.](../image/action-set-settings-window-rpa.png "The ActionSet Settings Window")

**Note:** The ActionSet component is compatible with the Internet Explorer browser, Windows, and Citrix applications.

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **ActionSet**.

2.  Drag the ActionSet component to the Design surface.

3.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\), or, double-click the header of the component.

    The ACTIONSET SETTINGS window appears.

4.  Do the following actions:

    Capture the area of the external application’s window that you want the automation to interact with. For example, capture the area surrounding a button or a text field in a web browser.

    1.  Click **Capture Image**.

        The `Press "CTRL+SHIFT" for selection` message appears.

    2.  Switch to the external application.

    3.  Press the **Ctrl + Shift** keys at the same time, then release them.

        The mouse device turns into a crossover icon \(![Crossover icon.](../image/crossover-icon.png)\).

    4.  Drag the mouse device over the element on which you want the ActionSet component to perform an action and its surrounding area and release.

        For example, if you want the component to click a button, drag the mouse device to capture the button and its surrounding areas.

        The selected area is captured as an image in the ACTIONSET SETTINGS window.

        All ActionSet actions take place in the selected window. To run actions in more than one window, use more than one ActionSet component in your workflow.

5.  To add one or more anchors, follow these steps:

    1.  Return to RPA Desktop Design Studio and in the ACTIONSET SETTINGS window, click **ADD ANCHOR**.

        The anchor appears as a yellow rectangle with red borders.

    2.  If necessary, move the anchor to a part of the captured image that will not change.

        For example, move the anchor to a title or field label.

        If the area under the anchor does not exactly match the corresponding area of the captured image, the anchor will not be recognized, and the ActionSet component will not work as intended. Choose a static area of the image to set your anchor.

        You can define more than one anchor. Multiple anchors let you define the geographical relationship between anchor and target with greater accuracy when targeting different locations in the image.

6.  Right-click the anchor and select an action to perform in the contextual menu.

7.  To do the actions that the ActionSet component can perform, see the following steps in the appropriate topic to configure the action:

    |Action|Reference|
    |------|---------|
    |Simulate a mouse click|[Use the ActionSet Click action](use-actionset-click.md).|
    |Enter text in a field|[Use the ActionSet SetText action](use-actionset-set-text.md).|
    |Capture text from a window or web page|[Use the ActionSet GetText action](use-actionset-get-text.md).|
    |Capture a table|[Use the ActionSet Get Table action](use-actionset-get-table.md).|
    |Select, copy, or delete text|[Use the ActionSet Text Selection action](use-actionset-text-selection.md).|
    |Read text in an image|[Use the ActionSet OCR Read Text action](use-actionset-ocr-read-text.md).|
    |Read a table in an image|[Use the ActionSet OCR Read Table action](use-actionset-ocr-read-table.md).|
    |Read text in an image and click it when found|[Use the ActionSet OCR Read Text action](use-actionset-ocr-read-text.md).|
    |Simulate a key press or a key function|[Use the ActionSet SendKeys action](use-actionset-send-keys.md).|
    |Simulate an alternative mouse action \(for example, right-click, drag, scroll, or paste\)|[Use the ActionSet Mouse action](use-actionset-mouse-action.md).|

8.  To add more actions, repeat step 6 and 7.

9.  To delete the anchor, right-click the anchor and click **Delete**.

10. Connect the data and control ports of the ActionSet component to the corresponding ports of the other components as described in the following table.

    The ActionSet component has one optional parameter, which you can use to specify the handle of the window where the action takes place. A window handle may identify a specific window more quickly than is possible using image matching. You can also specify match rules to help the automation find the target window by testing available windows against the rules you specify.

    To specify the window handle, connect the Window Handle Data Out port of another component \(such as the Start App component\) to the Window Handle Data In port of the ActionSet component. For more information about the Window Handle parameter, see the following table.

    |Port type|Port name|Data type|Purpose of connection|Notes|
    |---------|---------|---------|---------------------|-----|
    |Data In|Window Handle|Integer|The numeric handle of the window where the action will be performed. This must be the window from which the image in the ACTIONSET SETTINGS window was captured.|You must provide the handle of the window from which you have captured the image of the screen.|


-   **[Use the ActionSet Click action](use-actionset-click.md)**  
Simulate a simple left-click on the target area as part of a series of actions in the ActionSet component.
-   **[Use the ActionSet SetText action](use-actionset-set-text.md)**  
Set text to fields on the Windows applications or the Internet Explorer browser by using the Set Text action in RPA Desktop Design Studio.
-   **[Use the ActionSet GetText action](use-actionset-get-text.md)**  
Capture text from the Windows applications, and web pages on the Internet Explorer browser by using the Get Text action in RPA Desktop Design Studio.
-   **[Use the ActionSet Text Selection action](use-actionset-text-selection.md)**  
Select, copy, or delete text from the Desktop and Windows applications, and the Internet Explorer browser by using the Text Selection action in RPA Desktop Design Studio.
-   **[Use the ActionSet Get Table action](use-actionset-get-table.md)**  
Capture a table from the Windows applications, and web pages on the Internet Explorer browser by using the Get Table component in RPA Desktop Design Studio.
-   **[Use the ActionSet GetImage action](use-actionset-get-image.md)**  
Capture images from the desktop, Windows applications, and web pages on the Internet Explorer browser by using the GetImage component in RPA Desktop Design Studio.
-   **[Use the ActionSet OCR Read Text action](use-actionset-ocr-read-text.md)**  
Extract text from images in the desktop, Windows applications, and the Internet Explorer browser by using the OCR Read Text action in RPA Desktop Design Studio.
-   **[Use the ActionSet OCR Read Table action](use-actionset-ocr-read-table.md)**  
Extract a table from images in the desktop, Windows applications, and web pages on the Internet Explorer browser by using the OCR Read Table action in RPA Desktop Design Studio.
-   **[Use the ActionSet OCR ClickText action](use-actionset-ocr-clicktext.md)**  
Perform a mouse device action on a text in an image in the Internet Explorer browser or Windows applications by specifying the text using the OCR ClickText action.
-   **[Use the ActionSet SendKeys action](use-actionset-send-keys.md)**  
Set text or perform keyboard shortcuts on fields and elements on the desktop, Windows applications, and web pages on the Internet Explorer browser using the ActionSet Send Keys action in RPA Desktop Design Studio.
-   **[Use the ActionSet Mouse action](use-actionset-mouse-action.md)**  
Do various mouse device actions on the desktop, Windows applications, and web pages on the Internet Explorer browser using the ActionSet Mouse action in RPA Desktop Design Studio.

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

