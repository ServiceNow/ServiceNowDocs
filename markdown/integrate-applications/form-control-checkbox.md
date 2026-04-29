---
title: Methods and events of the CheckBox element
description: The CheckBox element in RPA Desktop Design Studio enables you to capture true or false, yes or no, or on or off inputs from users. It helps in decision-making, enabling or disabling features, and controlling workflow execution.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Methods and events of elements, Reference, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Methods and events of the CheckBox element

The CheckBox element in RPA Desktop Design Studio enables you to capture true or false, yes or no, or on or off inputs from users. It helps in decision-making, enabling or disabling features, and controlling workflow execution.

The methods and events of the CheckBox element are displayed in the Object Explorer pane. You can use this element to present yes or no or true or false selections.

## Use cases

-   User preferences selection - Allows users to enable/disable specific options, such as "Run in background" or "Send email notification".
-   Conditional execution - Based on whether the checkbox is checked, the automation can execute or skip certain steps.
-   Multi-selection options - You can also use the check box element in groups to display multiple choices in a form. When multiple checkboxes are available, users can select multiple options. For example, selecting multiple file formats for export.
-   Validation and confirmation - Ensures that a user has acknowledged terms, agreements, or completed a required step before proceeding.

## Methods

-   **Checked**

    Sets a value of the current element.

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **IsChecked**

    Returns a Boolean value whether the current element is selected or cleared.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

-   **SetVisibility**

    Gets or sets a value that indicates whether the current element and all its child elements are displayed.

    -   If true, the current element and all its child elements are displayed.
    -   If false, the current element and all its child elements aren’t displayed.

## Events

-   **OnStateChanged**

    Occurs when a state is changed.

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

