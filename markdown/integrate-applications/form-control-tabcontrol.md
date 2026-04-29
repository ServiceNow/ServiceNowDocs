---
title: Methods and events of the TabControl element
description: The TabControl element in the RPA Desktop Design Studio enables you to add one or more tabs in your form.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, Reference, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Methods and events of the TabControl element

The TabControl element in the RPA Desktop Design Studio enables you to add one or more tabs in your form.

The methods and events of the TabControl element are displayed in the Object Explorer pane.

## Methods

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **SelectTabByIndex**

    Selects the tab with a specific index.

-   **SelectTabByName**

    Selects the tab with a specific name.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

-   **SetTabState**

    Enables or deactivates the tab.

-   **SetTabVisibility**

    Gets or sets a value that indicates whether the tab and all its child elements are displayed.

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

