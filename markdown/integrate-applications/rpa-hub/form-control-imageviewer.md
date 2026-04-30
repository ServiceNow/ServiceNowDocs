---
title: Methods and events of the ImageViewer element
description: The ImageViewer element in RPA Desktop Design Studio enables you to open and view image files including JPEG, GIF, WMF, and other image formats in a form. You can also stretch and shrink images, rotate the images at different angles through all axis, and save them in different formats.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Methods and events of the ImageViewer element

The ImageViewer element in RPA Desktop Design Studio enables you to open and view image files including JPEG, GIF, WMF, and other image formats in a form. You can also stretch and shrink images, rotate the images at different angles through all axis, and save them in different formats.

The methods and events of the ImageViewer element are displayed in the Object Explorer pane.

## Methods

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **FitToContent**

    Fits the image into the current element.

-   **GetImage**

    Retrieves the image from the current element.

-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **Highlight**

    Highlights a specific area of an image in the current element.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetImage**

    Sets the image to the current element.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

-   **SetVisibility**

    Gets or sets a value that indicates whether the current element and all its child elements are displayed.

    -   If true, the current element and all its child elements are displayed.
    -   If false, the current element and all its child elements aren’t displayed.
-   **UnHighlight**

    De-emphasizes the highlighted area of an image in the current element.

-   **ZoomIntoPoint**

    Zooms into a specific point by inputting the x and y values.


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

