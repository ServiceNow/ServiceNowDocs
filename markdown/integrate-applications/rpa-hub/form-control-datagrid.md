---
title: Methods and events of the DataGrid element
description: The DataGrid element in RPA Desktop Design Studio enables you to display and manipulate tabular data.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Methods and events of elements, RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Methods and events of the DataGrid element

The DataGrid element in RPA Desktop Design Studio enables you to display and manipulate tabular data.

The methods and events of the DataGrid element are displayed in the Object Explorer pane.

## Methods

-   **ClearData**

    Clears all the rows in the current element.

-   **Enable**

    Gets or sets a value indicating whether the element can respond to user interaction.

    -   If true, the element is enabled
    -   If false, the element is not enabled.
-   **GetCellValue**

    Gets the value of a specified cell in the current element.

-   **GetCount**

    Gets the count of rows and columns of the current element.

-   **GetData**

    Gets the current element data.

-   **GetNativeProperty**

    Gets the value of the built-in property of the current element.

-   **GetRow**

    Gets the row data that is based on the index value.

-   **GetSelectedRow**

    Gets the index value of the selected row.

-   **InvokeNativeMethod**

    Invokes the built-in method of the current element.

-   **SetCellColor**

    Sets the color in a cell that is based on the row value and column value.

-   **SetCellValue**

    Sets the cell value for a particular row and column.

-   **SetContextMenu**

    Sets the context menu for the UI element. It accepts the input in either a string array or a comma-separated string.

-   **SetData**

    Sets the data into the current element.

-   **SetNativeProperty**

    Sets the value of the built-in property of the current element.

-   **SetReadOnly**

    Sets a value that indicates whether the current element is in read-only mode.

-   **SetRowColor**

    Sets the row color that is based on the row index.

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

