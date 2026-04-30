---
title: Methods and events of the TextBlock element
description: The TextBlock element in RPA Desktop Design Studio enables you to add a label on the form so that your user can view that label as read-only information.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Methods and events of the TextBlock element

The TextBlock element in RPA Desktop Design Studio enables you to add a label on the form so that your user can view that label as read-only information.

The methods and events of the TextBlock element are displayed in the Object Explorer pane.

## Methods

-   **ClearText**

    Clears the text from the current element.

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **GetText**

    Gets the text from the current element.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

-   **SetText**

    Sets the text data to the current element.

-   **SetVisibility**

    Gets or sets a value that indicates whether the current element and all its child elements are displayed.

    -   If true, the current element and all its child elements are displayed.
    -   If false, the current element and all its child elements aren’t displayed.

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

