---
title: Additional options for application screens and elements in Universal App Connector
description: Validate and perform additional operations for the added application screens and their captured elements. The additional options for the application screens are categorized based on the application type.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Additional options for application screens and elements in Universal App Connector

Validate and perform additional operations for the added application screens and their captured elements. The additional options for the application screens are categorized based on the application type.

## Type of application screens, their additional options, and descriptions

In the Screens and elements pane, right-click the application screen to perform the following additional operations.

<table id="table_mjq_mgx_gwb"><thead><tr><th>

Type of application

</th><th>

Additional options

</th></tr></thead><tbody><tr><td>

Java

</td><td>

-   Refresh screen
-   Refresh screen and elements
-   Focus
-   Capture element
-   Delete

</td></tr><tr><td>

Windows

</td><td>

-   Refresh screen
-   Refresh screen and elements
-   Focus
-   Capture element
-   Show elements
-   Delete

</td></tr><tr><td>

Google Chrome or Microsoft Edge

</td><td>

-   Refresh screen
-   Refresh screen and elements
-   Focus
-   Capture element
-   Add custom element
-   Delete

</td></tr></tbody>
</table><table id="table_rs1_d3x_gwb"><thead><tr><th>

Additional action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh screen

</td><td>

Rematches the selected screen based on the screen match rules or locators that you defined.

</td></tr><tr><td>

Refresh screen and elements

</td><td>

Rematches the selected screen and its child elements based on the screen match rules or locators that you defined.

</td></tr><tr><td>

Focus

</td><td>

Sets the targeted application screen into focus.

</td></tr><tr><td>

Capture element

</td><td>

Captures elements from the application screen. For more information, see [Use the Universal App Connector](../task/configure-uac.md).

</td></tr><tr><td>

Add custom element

</td><td>

Adds a custom element to the application screen. For example, you can interact with hidden elements that you cannot directly capture from the web page.

</td></tr><tr><td>

Show elements

</td><td>

Displays the Windows Elements dialog that displays all the existing elements in the target application screen in a tree view. You can select the required element from here and add it to the application screen.For Windows application screens, the elements are displayed in two modes. They are **UI Automation** and **Active Accessibility**. **UI Automation** is the default mode.

For example, when you capture a notepad windows screen and right-click and select **Show Elements**, the following modes are displayed.

![Displays elements in the UI Automation mode for a Notepad.](../image/uac-show-elements-ui-mode.png "Elements displayed in UI Automation mode for a Notepad")

![Displays elements in the Active Accessibility mode for a Notepad.](../image/uac-show-elements-aa-mode.png "Elements displayed in Active Accessibility mode for a Notepad")

</td></tr><tr><td>

Delete

</td><td>

Deletes the application screen.

</td></tr></tbody>
</table>## Additional options for elements and their descriptions

In the Screens and elements pane, right-click the application element to perform the following additional operations. For example, for a Windows screen.

![Additional options for elements, for example, for a Windows screen.](../image/uac-addi-options-elements.png "Additional options for elements, for example, for a Windows screen")

<table id="table_sdh_zjx_gwb"><thead><tr><th>

Additional option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh

</td><td>

Rematches the selected element based on the element match attributes or locators that you defined.When you capture an element in both UIA and AA modes of a Windows application screen, you view both elements in the Screens and elements pane. For example, Text Editor\_UIA and Text Editor\_AA.![Elements in the Screens and elements pane with Text Editor types in 2 modes.](../image/uac-refresh-element-mode.png)

When you capture a Text Editor element in Active Accessibility mode and perform the **Refresh** action on that element, the Target objects preview pane displays two text editors with different types, such as window and editable text.![Types of Text Editor of active accessibility mode.](../image/uac-text-types-options.png)

</td></tr><tr><td>

Highlight

</td><td>

Highlights the element on the target application screen.

</td></tr><tr><td>

Re-capture

</td><td>

Recaptures an element from the application screen retaining the same name.

</td></tr><tr><td>

Delete

</td><td>

Deletes the element.

</td></tr><tr><td>

Do Default Action

</td><td>

Executes the default action of the target object. This the same action you perform by clicking, pressing Enter, or using another common method of activation.The default actions are listed for the following UI elements.

-   Button: Clicks the button
-   Check box: Toggles the check \(select/clear\)
-   Link: Opens the link \(navigate\)
-   Combo Box: Opens the drop-down
-   List Item: Selects the item
-   Tree View Node: Expands or collapses the node

</td></tr><tr><td>

Get Value

</td><td>

Retrieves the value of the target object, which typically represents the data the object holds or displays \(not the label or name\).

</td></tr><tr><td>

Set Value

</td><td>

Sets the value property of the target object.

</td></tr><tr><td>

Set text

</td><td>

Sets text to the element if applicable.

</td></tr><tr><td>

Get text

</td><td>

Retrieves text from the element if applicable.

</td></tr><tr><td>

Click

</td><td>

Clicks the elements if applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

