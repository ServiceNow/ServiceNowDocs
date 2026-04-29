---
title: Methods and events of the ComboBox element
description: The ComboBox element in RPA Desktop Design Studio enables you to display the data in a drop-down combination box.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Methods and events of elements, Reference, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Methods and events of the ComboBox element

The ComboBox element in RPA Desktop Design Studio enables you to display the data in a drop-down combination box.

The methods and events of the ComboBox element are displayed in the Object Explorer pane. By default, the ComboBox element appears in two parts: the top part is a text box that enables you to type a list item. The second part is a list box that displays a list of items from which you can select one.

## Methods

-   **ClearItems**

    Removes all the items from the current element.

-   **ClearSelection**

    Clears the current selection from the current element.

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetItems**

    Gets an object that represents the collection of the items that are contained in the current element.

-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **GetSelectedIndex**

    Gets the index value that specifies the currently selected item.

-   **GetSelectedItem**

    Gets the selected item that specifies the currently selected item.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **SelectItem**

    Selects the item in the current element.

-   **SelectItemByIndex**

    Selects the item by using the index value.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetItems**

    Sets an object that represents the collection of the items that are contained in the current element.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

-   **SetVisibility**

    Gets or sets a value that indicates whether the current element and all its child elements are displayed.

    -   If true, the current element and all its child elements are displayed.
    -   If false, the current element and all its child elements aren’t displayed.

## Events

-   **MouseClick**

    Occurs when a cell within the table is clicked.

-   **MouseDoubleClick**

    Occurs when a user double-clicks the selected item.

-   **SelectionChanged**

    Occurs when a value is selected from the element.

-   **OnContextMenuClick**

    Occurs when an option on the context menu is clicked.

-   **MouseEnter**

    Occurs when the mouse device enters that element field.

-   **MouseLeave**

    Occurs when the mouse device leaves that element field.

-   **OnMouseClick**

    Occurs when the element is clicked.

-   **GotFocus**

    Occurs when the focus is on the current element.

-   **LostFocus**

    Occurs when the focus moves out of the current element.


**Parent Topic:**[Methods and events of elements](form-control-methods-events.md)

