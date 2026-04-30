---
title: Methods and events of the Form Renderer element
description: The Form Renderer element in RPA Desktop Design Studio enables you to build forms quickly with controls such as TextBox, ComboBox, CheckBox, RadioButton, ToggleButton, Date, Time, and PasswordBox.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Methods and events of the Form Renderer element

The Form Renderer element in RPA Desktop Design Studio enables you to build forms quickly with controls such as TextBox, ComboBox, CheckBox, RadioButton, ToggleButton, Date, Time, and PasswordBox.

The methods and events of the Form Renderer element are displayed in the Object Explorer pane.

## Methods

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **GetData**

    Gets the current element data.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **Reset**

    Resets the data for the fields defined in the current element.

-   **SetChoices**

    Sets choices for list controls such as a radio button and ComboBox via a program.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetData**

    Sets the data into the current element.

-   **SetHelpContent**

    Sets the field help content so that you can provide the related data.

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

**Related topics**  


[Configure the form fields for the Form Renderer element](../task/configure-form-fields.md)

