---
title: SAP element-level method descriptions
description: The SAP connector provides various element-level methods that you can use to automate actions on the SAP screen UI elements, for example, a button or a check box.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [SAP Connector methods, SAP connector, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# SAP element-level method descriptions

The SAP connector provides various element-level methods that you can use to automate actions on the SAP screen UI elements, for example, a button or a check box.

## Common methods

The following methods apply to all elements on the SAP screen.

**Note:** Any other elements that you see on the SAP screen that aren’t listed in this topic support only the common methods.

-   **Highlight**

    Highlights the element on the SAP screen.

-   **IsCreated**

    Returns `true` if the element is present on the SAP screen, and `false` if the element is not present.

-   **MouseClick**

    Performs a mouse-click action on the element on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |clickType|Option to select the type of mouse click: left or right.|Data In|Enum|Left|No|

-   **SendKeys**

    Sends the keyboard strokes such as Enter or Ctrl, to the element on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |keys|Keyboard strokes that you want to send to the element.|Data In|String|NA|Yes|
    |clearExistingValue|Option to specify whether to clear the existing value of the element before entering the keys value.|Data In|Boolean|False|No|
    |typeDelay|Option to specify the time delay in seconds between each key stroke.|Data In|Double|0.09|No|

-   **SetFocus**

    Sets focus on the element on the SAP screen.

-   **WaitForCreate**

    Waits for the specified duration while the element is being loaded. This enables all the dynamic controls to load.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |timeoutInSeconds|Duration in seconds after which the method times out.|Data In|Integer|30 seconds|No|


## GuiButton methods

-   **Click**

    Selects the button on the SAP screen.


## GuiCheckbox methods

-   **Check**

    Selects the check box on the SAP screen.

-   **IsChecked**

    Returns `true` if the element is selected on the SAP screen, and `false` if the element isn’t selected.

-   **Uncheck**

    Clears the check box on the SAP screen.


## GuiComboBox

-   **Get**

    Gets the selected value of the combo box on the SAP screen.

-   **GetIconName**

    Gets the property icon name of the element on the SAP screen.

-   **GetList**

    Gets all the list of values from the combo box on the SAP screen.

-   **Set**

    Sets the value of the combo box against the key passed.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |value|Value that you want to set for the combo box.|Data In|String|None|Yes|
    |selectedItem|Option to specify whether you want to set the value for "Key" or "Value".|Data In|Enum|None|Yes|


## GuiCtrlGridView

-   **ClickButtonCell**

    Selects a button in the grid cell defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the grid.|Data In|Integer|None|Yes|
    |columnCode|The column identifier of the grid cell.|Data In|String|None|Yes|

-   **ClickCell**

    Selects a grid cell defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the grid.|Data In|Integer|None|Yes|
    |columnCode|The column identifier of the grid cell.|Data In|String|None|Yes|

-   **DeselectAllRows**

    Deselects all the rows that are selected in the grid.

-   **GetCellType**

    Retrieves the type of the grid cell defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the grid.|Data In|Integer|None|Yes|
    |columnCode|The column identifier of the grid cell.|Data In|String|None|Yes|

-   **GetCellValue**

    Retrieves the value of the grid cell defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the grid.|Data In|Integer|None|Yes|
    |columnCode|The column identifier of the grid cell.|Data In|String|None|Yes|

-   **GetColumns**

    Retrieves the list of active column headers of the grid.

-   **GetColumnsKeyValuePair**

    Retrieves the column name and column code as key-value pair from the columns of the grid.

-   **GetRowCount**

    Retrieves the number of the rows of the grid.

-   **GetRows**

    Retrieves the number of grid rows defined in the rowNumber parameter, starting from the row defined in the startIndex parameter.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |startIndex|The starting row index to begin retrieving rows.|Data In|Integer|None|Yes|
    |rowNumber|Indicates the number of rows to retrieve from the grid|Data In|Integer|None|Yes|

-   **GetRowsByColumn**

    Retrieves a subset of rows from a specific column based on the startIndex, rowNumber, and columnCode parameters.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |startIndex|The starting index of the row to begin retrieving the data in the specified column \(columnCode\).|Data In|Integer|None|Yes|
    |rowNumber|The number of rows to retrieve starting from the startIndex.|Data In|Integer|None|Yes|
    |columnCode|The column from which the row data is retrieved.|Data In|String|None|Yes|

-   **GetSelectedColumns**

    Retrieves the columns that are selected.

-   **GetSelectedRows**

    Retrieves the rows that are selected.

-   **GetSingleRow**

    Retrieves a specific row of the grid defined by the row number.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index \(or row number\) specifying which row of the grid you want to retrieve data for.|Data In|Integer|None|Yes|

-   **GetVisibleRows**

    Retrieves the rows that are visible.

-   **SelectAllRows**

    Selects all rows of the grid.

-   **SelectCell**

    Selects the grid cell defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the grid.|Data In|Integer|None|Yes|
    |columnCode|The column identifier of the grid cell.|Data In|String|None|Yes|

-   **SelectContextMenuItemById**

    Selects the context menu item from the grid based on the ID that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |Id|The unique identifier of the context menu item you want to select.|Data In|String|None|Yes|

-   **SelectContextMenuItemByPosition**

    Selects the context menu item from the grid based on the position that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuItemPosition|The position of the context menu item that you want to select.|Data In|String|None|Yes|

-   **SelectContextMenuItemByText**

    Selects the context menu item from the grid based on the text that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuItemText|The text of the context menu item that you want to select.|Data In|String|None|Yes|

-   **SelectSingleRow**

    Selects the row of the grid defined by the row number.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row number that the method uses to select a row in the grid.|Data In|String|None|Yes|

-   **SelectToolbarMenuItemById**

    Selects the toolbar menu item from the grid based on the ID that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |Id|The unique identifier of the toolbar menu item you want to select.|Data In|String|None|Yes|

-   **SelectToolbarMenuItemByPosition**

    Selects the toolbar menu item from the grid based on the position that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuItemPosition|The position \(or index\) of a menu item in the toolbar.|Data In|Integer|None|Yes|

-   **SelectToolbarMenuItemByText**

    Selects the toolbar menu item from the grid based on the text that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuItemText|The text displayed on the toolbar menu item that you want to select.|Data In|String|None|Yes|

-   **SetCellValue**

    Sets the value of a cell in a grid defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |value|The value is set for the cell.|Data In|String|None|Yes|
    |rowNumber|The row number of the cell to modify.|Data In|Integer|None|Yes|
    |columnCode|The code \(or identifier\) for the column of the cell to modify.|Data In|String|None|Yes|


## GuiLabel

-   **GetText**

    Retrieves the text of the label on the SAP screen.


## GuiPassword

-   **SetText**

    Sets a given value as a password in the Password element on the SAP screen.


## GuiRadioButton

-   **IsChecked**

    Returns `true` if the radio button is selected, and `false` if not selected.

-   **Select**

    Select the radio button on the SAP screen.


## GuiStatusBar

-   **GetStatus**

    Retrieves the status information of a specific SAP screen.


## GuiTab

-   **SelectTab**

    Selects the tab on the SAP screen.


## GuiTableControl

-   **DeselectVisibleRow**

    Clears a visible row based on the row number that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the table.|Data In|Integer|None|Yes|

-   **DeselectAllVisibleRows**

    Clears all the selected rows.

-   **DeselectRow**

    Clears a particular row based on the row number that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the table.|Data In|Integer|None|Yes|

-   **GetAllVisibleRows**

    Returns all the visible rows in the table.

-   **GetColumnNames**

    Gets the list of active column headers in the table.

-   **GetMaximumScrollOffset**

    Gets the maximum value up to which scrolling is possible within the table.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |type|Option to select the type of scroll: horizontal or vertical.|Data In|Enum|None|Yes|

-   **GetScrollPosition**

    Gets the current position of the scroll bar.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |type|Option to select the type of scroll: horizontal or vertical.|Data In|Enum|None|Yes|

-   **GetSingleRow**

    Retrieves a specific row of the table defined by the row number.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the table.|Data In|Integer|None|Yes|

-   **GetTable**

    Fetches the entire table.

-   **GetVisibleRowCount**

    Returns count of visible rows.

-   **ScrollDownByOneRow**

    Scrolls down to move the focus to the next row.

-   **ScrollToHorizontalPosition**

    Scrolls horizontally to move focus to the specified position.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |position|Position of the scroll.|Data In|Integer|None|Yes|

-   **ScrollToNextPage**

    Scrolls down to move the focus to the next page.

-   **ScrollToPreviousPage**

    Scrolls up to move the focus to the previous page.

-   **ScrollToVerticalPosition**

    Scrolls vertically to move focus to the specified position.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |position|Position of the scroll.|Data In|Integer|None|Yes|

-   **ScrollUpByOneRow**

    Scrolls up to move the focus to the previous row.

-   **SelectAllRows**

    Selects all the rows of the table, whether they are visible.

-   **SelectSingleRow**

    Selects the row of the table defined by the row number.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the table.|Data In|Integer|None|Yes|

-   **SelectCell**

    Selects a cell in the table defined by the row number and the column code.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the table.|Data In|Integer|None|Yes|
    |columnCode|Code number of the column in the cell.|Data In|String|None|Yes|

-   **SelectVisibleRow**

    Selects a visible row of the table defined by the row number.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |rowNumber|The row index or row number of a cell in the table.|Data In|Integer|None|Yes|


## GuiTextBox

-   **GetText**

    Retrieves the text of the text box on the SAP screen.

-   **SetCaretPosition**

    Sets the caret to the specified position in the text box on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |position|Position of the caret.|Data In|Integer|None|Yes|

-   **SetText**

    Sets a given value in the text box on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |text|Text value that you want to set in the text box.|Data In|String|None|Yes|


## GuiTree

-   **Check**

    Selects a particular item in a node on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|

-   **ClickNodeItem**

    Clicks a particular item in a node on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|

-   **CollapseNodeItem**

    Collapses a particular node item on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|

-   **DoubleClickNode**

    Performs a double-click mouse action on a particular node on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|

-   **DoubleClickNodeItem**

    Performs a double-click mouse action on a particular item in a node on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|

-   **GetColumnsKeyValuePair**

    Retrieves the column name and column code as key-value pair from the columns of the tree.

-   **GetTreeType**

    Retrieves the type of the tree, such as simple, list, or column. If the type isn’t one of these, the method returns an empty value.

-   **GetNodeKeyByPath**

    Retrieves the node key based on the path that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |path|Route or hierarchy to find a specific node in the tree.|Data In|String|None|Yes|

-   **GetNodeKeyByText**

    Retrieves the node key based on the text that you specify.

<table id="table_wf3_jsw_12c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port entry type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

nodeText

</td><td>

The text value that you want to match with a node key. The value is matched to any node's text, ignoring case and extra spaces.

</td><td>

Data In

</td><td>

String

</td><td>

None

</td><td>

Yes

</td></tr></tbody>
</table>-   **GetNodeItemText**

    Retrieves the text of the node item based on the key and name that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |key|The key associated with the node. This key is the unique identifier of the node that you want to retrieve the text of.|Data In|String|None|Yes|
    |name|The name of the specific item or property within the node, used to filter or further identify the node.|Data In|String|None|Yes|

-   **GetSelectedNodes**

    Retrieves the values of the selected nodes.

-   **GetNodeItemCheckBoxState**

    Retrieves the state of a check box in a node item.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|

-   **PressNodeItemButton**

    Clicks the button in a specified node item on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|

-   **SelectNodeItem**

    Selects the specified node item on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|

-   **SelectNode**

    Selects the specified node on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|

-   **SelectContextMenuItemById**

    Selects a context menu item based on the ID that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |type|The type of context menu \(Tree,Node,Node Item\).|Data In|Enum|None|Yes|
    |menuId|The identifier of the context menu item that must be selected.|Data In|String|None|Yes|
    |nodeKey|Unique identifier for a specific node in the tree on which the context menu is to be invoked.|Data In|String|None|Yes|
    |ColumnName|The name of the column within the node. This helps narrow down which specific column in the node the context menu should apply to.|Data In|String|None|Yes|

-   **SelectContextMenuItemByText**

    Selects a context menu item based on the text that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |type|The type of context menu \(Tree,Node,Node Item\).|Data In|Enum|None|Yes|
    |menuText|The visible text of the context menu item that you want to select.|Data In|String|None|Yes|
    |nodeKey|Unique identifier for a specific node in the tree on which the context menu is to be invoked.|Data In|String|None|Yes|
    |ColumnName|The name of the column within the node. This name helps narrow down which specific column in the node the context menu should apply to.|Data In|String|None|Yes|

-   **SelectContextMenuItemByPosition**

    Selects a context menu item based on the position that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |type|The type of context menu \(Tree,Node,Node Item\).|Data In|Enum|None|Yes|
    |menuPosition|The position of the context menu item that you want to select. It could be the index or a string representing the position.|Data In|String|None|Yes|
    |nodeKey|Unique identifier for a specific node in the tree on which the context menu is to be invoked.|Data In|String|None|Yes|
    |ColumnName|The name of the column within the node. This name helps narrow down which specific column in the node the context menu should apply to.|Data In|String|None|Yes|

-   **Uncheck**

    Clears a particular item in a node from the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |nodeKey|Unique identifier for a specific node within the tree.|Data In|String|None|Yes|
    |column|The column name or identifier within the specified node.|Data In|String|None|Yes|


## GuiUserArea

-   **ScrollToNextPage**

    Scrolls down to move the focus to the next page.

-   **ScrollToPreviousPage**

    Scrolls up to move the focus to the previous page.

-   **SetHorizontalScroll**

    Scrolls horizontally to a value that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |scrolVal|Numeric value for scroll bar.|Data In|Integer|None|Yes|

-   **SetVerticalScroll**

    Scrolls vertically to a value that you specify.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |scrolVal|Numeric value for scroll bar.|Data In|Integer|None|Yes|


