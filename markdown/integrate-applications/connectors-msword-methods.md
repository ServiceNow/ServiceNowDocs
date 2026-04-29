---
title: Microsoft Word connector methods
description: The Microsoft Word connector methods enable you to perform various day-to-day tasks with Microsoft Word documents and automate them. For example, add a page footer.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [Microsoft Word, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Microsoft Word connector methods

The Microsoft Word connector methods enable you to perform various day-to-day tasks with Microsoft Word documents and automate them. For example, add a page footer.

## Open

Opens a Microsoft Word file saved on the local disk.

**Note:** You must execute this method before executing any other method on the Microsoft Word connector.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Filepath|Specifies the path to the Microsoft Word file in the local disk.|Data in|String|
|Timeout|Specifies the time after which the operation times out.|Data in|Integer|
|Password|Use a password if the document is password protected.|Data in|String|
|Return|Returns the boolean value based on the outcome of the operation. If True, the file is opened. Else, if False, the file failed to open.|Data out|Boolean|

For details on the issues related to the Open method, see [KB article KB1123558](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123558) and [KB article KB1123548](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123548).

## AddFooter

Adds a footer to the Microsoft Word document in the specified font size.

To use this method, provide the text to be added to the Text parameter and the font size in which the footer text needs to be displayed to the FontSize parameter. Default value of the FontSize parameter is 12.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Text|Specifies the text in the footer.|Data in|String|
|FontSize|Specifies the font size of the text in the footer. Default value is 12.|Data in|Integer|

To provide inputs, see [Configure port properties](../task/configure-input-port-properties.md)

## AddHeader

Adds a header to a Microsoft Word document in specified font size.

To use this method, provide the text to be added to the Text parameter and the font size in which the header text needs to be displayed to the FontSize parameter. Default value of the FontSize parameter is 12.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Text|Specifies the text in the header.|Data in|String|
|FontSize|Specifies the font size of the text in the header. Default value is 12.|Data in|Integer|

## CellCopy

Copies the content of a table cell identified using the row index and column index of the table in a Microsoft Word document.

To use this method, provide the row index to the RowIndex parameter and column index to the ColumnIndex parameter. The default value for RowIndex and ColumnIndex is -1 each.

**Note:** You must execute the SetTable method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|RowIndex|Index of the row of the cell that needs to be copied. The row index value must be equal or greater than zero. Default value is -1, which means there is no cell available.|Data in|Integer|
|ColumnIndex|Index of the column of the cell that needs to be copied. The column index must be equal to or greater than zero. Default value is -1 which means there is no cell available.|Data in|Integer|

## CellPaste

Pastes the copied table cell content into a table cell identified using the row index and column index of the table in a Microsoft Word document.

To use this method, provide the row index to the RowIndex parameter and column index to the ColumnIndex parameter. The default value for RowIndex and ColumnIndex is -1 each.

**Note:** You must execute the SetTable and CellCopy methods before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|RowIndex|Index of the row of the cell to which data needs to be pasted. The row index value must be equal or greater than zero. Default value is -1, which means there is no row available to paste data.|Data in|Integer|
|ColumnIndex|Index of the column of the cell to which data needs to be pasted. The column index must be equal to or greater than zero. Default value is -1 which means there is no column available to paste data.|Data in|Integer|

## Close

Closes the last opened Microsoft Word document. While closing the document, it is optional to save changes.

If modification done to the word document needs to be saved then set the saveChanges boolean parameter to True, else set it to False. By default the saveChanges boolean parameter is set to True.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|saveChanges|Specifies whether to save the changes made in the word document before closing. By default, it is set to True, meaning the changes will be saved before closing. If changes are not required to be saved before closing, set to False.|Data in|Boolean|

## DeleteColumn

Deletes a column from a table based on a specified index value of the column in a Microsoft Word document.

To use this method, provide the index of the column that needs to be deleted to the ColumnIndex parameter. Default value is -1.

**Note:** You must execute the SetTable method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|ColumnIndex|Index of the column that needs to be deleted. The column index must be equal to or greater than zero. Default value is -1 which means there is no column available to be deleted.|Data in|Integer|

## DeletePage

Deletes a page based on a specified index value from a Microsoft Word document.

To use this method, provide the index value of the page that needs to be deleted to the PageIndex parameter.

**Note:** You must execute the Open method before executing this method.

<table id="table_zg5_tyw_xtb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

PageIndex

</td><td>

Specifies the index number of the page that needs to be removed or deleted.If you don't provide any index number, the method deletes the first page by default.

</td><td>

Data in

</td><td>

Integer

</td></tr></tbody>
</table>## DeleteRow

Deletes a row based on the specified index value from a table in a Microsoft Word document.

To use this method, provide the index of the row that needs to be deleted to the RowIndex parameter. Default value is -1.

**Note:** You must execute the SetTable method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|RowIndex|Index of the row that needs to be deleted. The row index value must be equal or greater than zero. Default value is -1, which means there is no row available to be deleted.|Data in|Integer|

## DeleteTable

Deletes a table from a Microsoft Word document.

If the document has multiple tables, the method deletes the first table in the document.

**Note:** You must execute the SetTable method before executing this method.

## ExportToPDF

Exports a Microsoft Word document to a PDF document at a specified path.

To use this method, provide the path where the PDF file needs to be extracted to the Filepath parameter.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Filepath|Specifies the folder path where the Word document is exported to PDF.|Data in|String|

## Find

Finds the text you specify in a Microsoft Word document and returns a Boolean response.

To use this method, provide the text that you want to find in the document to the Text parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Text|Text to find in the Word document.|Data in|string|
|Return|Returns a true/false value indicating whether the text is found in the Word document.|Data out|Boolean|

## GetCellValueByIndex

Returns the value of a cell in a table in a Microsoft Word document.

To use this method, provide the index of the cell to retrieve the cell value to the CellIndex parameter.

**Note:** You must execute the SetTable method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|CellIndex|Index of a cell to retrieve the value.|Data in|String|
|Return|Returns the value present in the required cell.|Data out|String|

## GetFooterText

Returns the footer text in a Microsoft Word document.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the footer text in the string format.|Data out|String|

## GetHeaderText

Returns the header text in a Microsoft Word document.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the header text in the string format.|Data out|String|

## GetPageCount

Returns the total number of pages in a Microsoft Word document.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the integer number or numeric value of the total pages in a Word document.|Data out|Integer|

## GetRowIndexByValue

Returns the row index value of a row based on the specified value of a cell in the row.

To use this method, provide the document table to the Table parameter to retrieve the index of the row based on the value provided to the Value parameter.

**Note:** You must execute the GetTable and SetTable methods before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Table|Table object in the word document as a reference to perform further actions on it.|Data in|Object|
|Value|Search text that corresponds to a certain row in the table.|Data in|String|

## GetTable

Returns the data in a table of a Microsoft Word document as a table object and data table. If the document contains multiple tables, you can specify the table index to identify the table for the method. You can also specify the table type, if needed.

To use this method, provide the index of the expected table to the TableIndex parameter. Set the FirstRowIsHeader parameter to True if the first row needs to be treated as header, else it is set to False.

Depending on the table structure, you can optionally configure the table type for the method. To configure the table, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Select the table type.
3.  Click **OK**.

<table id="table_w45_xn3_rcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td><td>

Data in

</td><td>

 

</td></tr><tr><td>

TableIndex

</td><td>

Index of a table in a Microsoft Word document.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

FirstRowIsHeader

</td><td>

Boolean value to indicate whether the method should treat the first row as a header of the table.By default, it is set to True, which means that the first row is considered as a header. If first row is not header, then set this parameter to False.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

Table

</td><td>

Returns the data in a table as an object.

</td><td>

Data out

</td><td>

Object

</td></tr><tr><td>

Data

</td><td>

Returns the data in the table.

</td><td>

Data out

</td><td>

Data

</td></tr></tbody>
</table>## GetTableCellValues

Returns the values in one or more table cells.

To use this method, provide the indices of the table cells whose value is required, in the configuration window.

To specify the number of cells, you must configure the index values of the cells. To configure, do the following.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click \(![Click to add cell index icon.](../image/add-image-icon.png)\).
3.  Enter the index values for the cells.
4.  Repeat the steps to add more index values.
5.  Click **OK**.

## GetTableCount

Returns the number of tables in a Microsoft Word document. You can optionally specify the type of table for the method to identify.

Select the table type from the config window. If you expect to receive total number of tables in a word document, then the table type is set to 'Default'. If a count of nested tables within a cell in a table is expected then set the table type to 'Nested'. Provide the index of table which has nested tables to the TableIndex parameter and table cell index from which count of nested tables is expected to CellIndex parameter.

To configure the type of table, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Select the table type.
3.  Click **OK**.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the integer value of total number of tables in word document.|Data in|Integer|

## GetTableRowData

Returns the values in one or more cells of a row in a Microsoft Word document. You can specify the index values of the cells of the row.

**Note:** You must execute the SetTable method before executing this method.

You can configure the index values of the cells in a row. To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add index value icon \(![Add index value icon.](../image/add-image-icon.png)\).
3.  Enter the index value of the cell.
4.  Repeat the steps to add more index values.
5.  Click **OK**.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|RowIndex|Index of the row from which data needs to be retrieved. Default value is 0, meaning the data will be fetched from the first row.|Data in|Integer|

## GetText

Returns all the text content in a Microsoft Word document.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the complete document's text in a string format.|Data Out|String|

## InsertNewColumn

Inserts a new column in the first table in the document based on the specified index value.

To use this method, provide the index number at which a new column needs to be inserted to the ColumnIndex parameter. Default value is -1, which means that a column is inserted before the first column.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|ColumnIndex|Index at which new column must be inserted. Default value is -1, which means there are no columns in the table.|Data in|Integer|

## InsertNewRow

Inserts a new row based on the index value.

To use this method, provide the index number at which a new row needs to be inserted to the RowIndex parameter. Default value is -1, which means a row is inserted before the first row.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|RowIndex|Index at which new row must be inserted. Default value is -1, which means there are no rows in the table.|Data in|Integer|

## InsertPicture

Inserts an image into Microsoft Word document from the file path provided at a particular bookmark.

To use this method, provide the file path of the image that needs to be inserted to the ImageFilePath parameter. Provide the identification place at which the image needs to be inserted in the Word document to the Bookmark parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|ImageFilePath|System folder path to the image that needs to be inserted.|Data in|String|
|Bookmark|Point at which the image needs to be added.|Data in|String|

## InsertTable

Inserts a table into a Microsoft Word document. You can optionally customize the document by configuring it before inserting.

To use this method, the point at which the table needs to be added is provided to the Bookmark parameter and the table that needs to be added should be passed to the Data parameter.

**Note:** Before executing this method, you must execute the GetTable and SetTable methods.

To customize the table before inserting, do the following steps.

1.  Click the method settings icon\(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Select Include Headers.
3.  Select border style and autofit behavior.
4.  Select Include Empty Rows.
5.  To ignore specific columns, click the add index value icon \(![Add index value](../image/add-image-icon.png)\).
6.  Enter the index value of the column.
7.  Click **OK**.

<table id="table_czt_kx3_rcc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Bookmark

</td><td>

Specific position in the Word document where the table will be inserted.Before inserting the table, you must add a bookmark.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Data

</td><td>

Table data that will be inserted at the bookmark point.

</td><td>

Data in

</td><td>

Data

</td></tr></tbody>
</table>## InsertText

Inserts text in the beginning of the Microsoft Word document.

To use this method, provide a value that needs to be inserted to the text parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|text|Text value that needs to be inserted.|Data In|String|

## IsOpen

Checks whether a Microsoft Word document is open.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Filepath|System folder path to word document or file.|Data in|String|
|Return|System folder path to word document or file.|Data Out|Boolean|

## MergeByCellIndices

Merges the range of cells specified in the form of index value range.

To use this method, provide the starting cell index value to the StartCellIndex parameter and ending cell index value to the EndCellIndex parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|StartCellIndex|Index of starting cell point to start merging cells.|Data in|Integer|
|EndCellIndex|Index of ending cell point to end merging cells.|Data in|Integer|

## MergeByRowCol

Merges a range of cells of a table in a Microsoft Word document.

To use this method, provide the starting row index to the StartRowIndex parameter, ending row index to the EndRowIndex parameter, and starting column index to the StartColIndex parameter and ending column index to the EndColIndex parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|StartRowIndex|Index of starting row.|Data in|Integer|
|StartColIndex|Index of starting column.|Data in|Integer|
|EndRowIndex|Index of ending row.|Data in|Integer|
|EndColIndex|Index of ending column.|Data in|Integer|

## ReplaceBookmark

Replaces a bookmark in a Microsoft Word document with the specified text.

To use this method, provide the identification bookmark to Bookmark parameter with the text to be replaced given to the ReplaceText parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Bookmark|Identification bookmark in the word document.|Data in|String|
|ReplaceText|Replace text at the bookmarked location with the new value provided.|Data in|String|

## ReplaceBookmarks

Finds and replaces multiple bookmarks in a Microsoft Word document with the specified text.

To use this method, provide value to the added field\(s\) which is the text with which the bookmark needs to be replaced.

Provide more details of the bookmark text to replace as follows:

1.  Double-click the component.
2.  In the PROVIDE LABELS/BOOKMARKS dialog box, click the click to add label icon \(![Click to add label icon.](../image/add-image-icon.png)\) and enter the bookmark to replace it.

    Repeat this step to add more bookmarks.

3.  Click **OK**.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Text|Text to be replaced in a Microsoft Word document.|Data in|String|

## ReplaceFooterText

Finds and replaces the footer text in a Microsoft Word document with the specified text.

Provide the original footer text value that is present in the word document to the FindText parameter and the text with which original footer text has to be replaced to the ReplaceText parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|FindText|Current value that is present in the footer.|Data in|String|
|ReplaceText|Value that is required to replace the FindText value with, in the footer.|Data in|String|

## ReplaceHeaderText

Finds and replaces the header text in a Microsoft Word document with the specified text.

Provide the original header text value that is present in the word document to the FindText parameter and the text with which original header text has to be replaced to the ReplaceText parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|FindText|Current value that is present in the header.|Data in|String|
|ReplaceText|Value that is required to replace the FindText value with, in the header.|Data in|String|

## ReplaceStaticText

Finds and replaces the text in a Microsoft Word document with the specified text. Replaces bookmarks, headings, or any text based on the configuration.

To use this method, provide a value to the added field which is the text with which the label / bookmark needs to be replaced.

You must configure the method before executing. To configure, do the steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add text icon \(![Add text icon.](../image/add-image-icon.png)\)
3.  Enter the heading, bookmark, or text that you want to replace.
4.  Repeat the steps to enter more text.
5.  Click **OK**.

## ReplaceText

Finds and replaces the text in a Microsoft Word document with the specified text.

Provide the original text value that is present in the word document to the FindText parameter and the text with which original text has to be replaced to the ReplaceText parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|FindText|Current value that is present in the Word document.|Data in|String|
|ReplaceText|Value that is required to replace the FindText value with, in the Word document.|Data in|String|

## Resize

Resizes the window of a Microsoft Word document according to the left, top, width and height parameters.

To use this method, specify the Left and Top margins and the Width and Height parameters for the content.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Left|Left margin of content in word document.|Data in|Integer|
|Top|Top margin of content in word document.|Data in|Integer|
|Width|Width of the word document.|Data in|Integer|
|Height|Height of the word document.|Data in|Integer|

## Save

Saves the opened Microsoft Word document.

## SaveAs

Saves a copy of the opened Microsoft Word document with another name at a location provided in the Filepath parameter.

To use this method, provide the new location to which the Microsoft Word document needs to be saved in the Filepath parameter. If the file needs to be password protected, pass the value to the Password parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Filepath|System folder path to the word document or file.|Data in|String|
|Password|Open a password protected word document with the password provided. The default value is empty.|Data in|String|

## SetTable

Sets a table in a Microsoft Word document.

To use this method, it is necessary to pass the table object to the Table parameter.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Table|Table that needs to be set in the word document.|Data in|Object|

## SetTableCellValues

Sets the content of a table cell in a Microsoft Word document.

To use this method, provide the indices of the table cells whose value needs to be set in the configuration window.

Provide one or more cell indexes and value types as follows:

1.  Double-click the component.
2.  In the PROVIDE CELL INDEXES dialog box, click the click to add cell index icon \(![Click to add cell index icon.](../image/add-image-icon.png)\) and enter a cell index and select a value type.

    Repeat this step to add more cell indexes and value types.

3.  Click **OK**.

## SetTableRowData

Sets the content in a row of a table in a Microsoft Word document.

To use this method, index of the table row at which the data needs to be set is passed to the RowIndex parameter.

**Note:** You must execute the SetTable method before executing this method.

-   **Input**

    [RowIndex](method-parameter-msword.md#RowIndex)

    Provide the column index as follows:

    1.  Double-click the component.
    2.  In the PROVIDE COLUMN INDEXES dialog box, click the click to add cell index icon \(![Click to add cell index icon.](../image/add-image-icon.png)\) and enter a column index.
    3.  Click **OK**.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|RowIndex|Index of row at which data needs to be set. Default value is 0, meaning the data will be set to the first row.|Data in|Integer|

**Parent Topic:**[Microsoft Word](../concept/microsoft-word-connector.md)

