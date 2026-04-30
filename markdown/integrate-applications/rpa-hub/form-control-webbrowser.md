---
title: Methods and events of the Web Browser element
description: The Web Browser element in the RPA Desktop Design Studio enables you to host web pages and provides web browsing capabilities to your application.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Methods and events of the Web Browser element

The Web Browser element in the RPA Desktop Design Studio enables you to host web pages and provides web browsing capabilities to your application.

The methods and events of the Web Browser element are displayed in the Object Explorer pane.

## Methods

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **Navigate**

    Opens the browser with the provided URL.

-   **Refresh**

    Refreshes the webpage.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

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

