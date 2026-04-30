---
title: Actions \(UI\)
description: The Actions \(UI\) group of components work on and with browsers, browser elements, applications, and the desktop in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Actions \(UI\)

The Actions \(UI\) group of components work on and with browsers, browser elements, applications, and the desktop in the RPA Desktop Design Studio.

You can, for example, perform the following actions.

-   Execute a JavaScript on a web page
-   Extract text using the Optical Character Recognition \(OCR\) technology
-   Simulate the mouse device clicks
-   Extract data from a table

Using Actions \(UI\) components, your automation can interact with browsers, forms, applications, and objects in a way that is similar to how a user might interact with them using a mouse and keyboard.

-   **[Use the ActionSet component](../task/use-actionsui-actionset.md)**  
The ActionSet component lets an automation interact with Windows applications \(such as web browsers\) and with Citrix applications. Using this single component in RPA Desktop Design Studio, you can click, drag, read and set text, interact with tables, and more, combining several user actions into a single task.
-   **[Use the Get Table component](../task/use-actionsui-get-table.md)**  
Extract and display data and the count of rows from the grids, lists, combo boxes, and HTML tables, by using the Get Table component in the RPA Desktop Design Studio.
-   **[Use the Get Text component](../task/use-actionsui-get-text.md)**  
The Get Text component captures text from an area that you specify in the target application. You can use it to receive data that exists in text format. To capture text from an image, see Use the OCR Text component.
-   **[Use the Click component](../task/use-actionsui-click.md)**  
Simulate the click actions of a mouse device by using the Click component in RPA Desktop Design Studio.
-   **[Use the Mouse component](../task/use-actionsui-mouse.md)**  
Simulate a mouse action, including alternative mouse device buttons, moves, drags, scrolls, and paste operations.
-   **[Use the OCR Text component](../task/use-actionsui-ocr-text.md)**  
Extract the text from an image by using the OCR Text component in RPA Desktop Design Studio.
-   **[Use the Send Keys component](../task/use-actionsui-send-keys.md)**  
Send text to fields in web pages, Windows applications, or the Windows desktop using the Send Keys component in RPA Desktop Design Studio. Use the component to enter data to fields such as text boxes and lists and to send special keys such as Shift, Control, F1, and F2.
-   **[Use the Set Text component](../task/use-actionsui-set-text.md)**  
Set text in text boxes and drop-down lists within applications, check boxes, radio button controls, web pages on Internet Explorer browser or Windows applications by using the Set Text component in RPA Desktop Design Studio.
-   **[Supported keys and functions](../reference/supported-keys-and-functions.md)**  
The Send keys component in the RPA Desktop Design Studio supports multiple keys, special keys, and functions. The keyboard keys must be enclosed within \[\]. For example, \[Back\].
-   **[Properties of Actions \(UI\) components](../reference/properties-actions-ui-components.md)**  
Learn about the properties of the Actions \(UI\) group components. All components under the Actions \(UI\) group have both unique and common properties.
-   **[ActionSet actions properties](../reference/actionset-actions-properties.md)**  
The ActionSet component performs multiple actions and each action has distinct properties. You can update the properties to modify the behavior of the actions.
-   **[Anchor](anchor.md)**  
An anchor is a unique identifier which is identified on the screen. It helps specify the target area for a simulated user interaction by defining a static area from which actions can be defined at a relative distance. The position of actions is calculated based on the anchor and the actions are performed relative to it.

**Parent Topic:**[Automation components](rpa-studio-automation-components.md)

