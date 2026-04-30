---
title: Methods and events of the ListBox element
description: The ListBox element in RPA Desktop Design Studio enables you to display a list of items from which you can select one or more Items.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Methods and events of the ListBox element

The ListBox element in RPA Desktop Design Studio enables you to display a list of items from which you can select one or more Items.

The methods and events of the ListBox element are displayed in the Object Explorer pane.

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

-   **GetSelectedItems**

    Gets multiple selected items that specify the currently selected items.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **SelectAll**

    Selects all the items in the current element.

-   **SelectItem**

    Selects the item in the current element.

-   **SelectItemByIndex**

    Selects the item by using the index value.

-   **SelectItems**

    Selects multiple items in the current element.

-   **SelectItemsByIndex**

    Selects multiple items by using the index value.

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
-   **UnselectAll**

    Clears all the selections in the current element.


## Events

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

