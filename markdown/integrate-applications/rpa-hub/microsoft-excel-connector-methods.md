---
title: Microsoft Excel connector methods
description: The Microsoft Excel connector methods perform various actions on Microsoft Excel documents. In an automation flow, the methods are connected with other methods and components. To use the methods, you must first expose them.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 32
breadcrumb: [Microsoft Excel, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Microsoft Excel connector methods

The Microsoft Excel connector methods perform various actions on Microsoft Excel documents. In an automation flow, the methods are connected with other methods and components. To use the methods, you must first expose them.

## Open

Creates or opens an existing Microsoft Excel file depending on the inputs.

**Note:** You must execute this method before any other method.

<table id="table_l1y_t4r_4tb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Filepath

</td><td>

Path to the existing file that the method opens.

 To create a file, you must set the value of the CreateNewFile parameter to True.

 **Note:** The path must contain the filename.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

CreateNewFile

</td><td>

Specifies whether a new Excel file should be created if the specified file does not exist.If CreateNewFile parameter is set to true, a new file is created at the specified file path. If set to False, it will try to open the excel from the given file path.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

DisplayAlerts

</td><td>

Specifies whether Excel displays alerts or prompts during the opening process.If set to true, Excel displays alerts for issues such as file conflicts or compatibility warnings. If set to false, these alerts are suppressed.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

IsVisible

</td><td>

Specifies if the Excel application window is visible to the user when the file is opened or not.If set to true, the Excel window is displayed on the screen. If set to false, Excel runs in the background without a visible interface.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

ReadOnlyMode

</td><td>

Specifies if the Excel file should be opened in the read-only mode.If set to true, the file opens in the read-only mode, preventing any changes from being made. If set to false, the file opens in the normal mode, allowing modifications.

</td><td>

Data in

</td><td>

Boolean

</td></tr><tr><td>

Password

</td><td>

Password required to open the Excel file if it is password-protected.If the file is not password-protected, this parameter can be left blank.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

Return

</td><td>

Returns True orFalse value. If the value is True, the file is successfully opened or created.

</td><td>

Data out

</td><td>

Boolean

</td></tr></tbody>
</table>## AddNewWorkSheet

Adds a new worksheet to the file. This method requires a sheet name as input parameter of type string that specifies the name of the new sheet.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the new worksheet that the method adds to the file.|Data in|String|

## AutoFill

Automatically populates cells within a specified range based on the content of adjacent cells or a predefined pattern. This method is useful for copying data or formatting across multiple cells. Microsoft Excel analyzes the content of the initial selection and extrapolates it to fill the desired range. It can be used to extend a series of numbers, duplicate formulas, replicate text patterns, or perform any other data entry processing.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data in|String|
|SourceRange|Range of cells with the data or formulas to replicate.|Data in|String|

## GetSheetNames

Returns the names of all the sheets in the opened Microsoft Excel document.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the names of the sheets in the opened Microsoft Excel document.|Data Out|String|

## Close

Closes the active Microsoft Excel document if it is already opened and releases the memory. This method helps in memory handling.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|saveChanges|If the value is set to True, changes to the file are saved before closing. If set to False, no changes are saved.|Data in|Boolean|

## ColumnsCount

Returns the total number of columns in a specified worksheet of a Microsoft Excel file. This method requires the SheetName parameter to specify the worksheet, and then returns the column count for that sheet.

**Note:** You must execute the Open method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet that the method uses to count the number of columns.|Data in|String|
|Return|Returns the count of columns in the worksheet.|Data out|Integer|

## Copy

Copies the contents from a range of cells in a worksheet.

**Tip:** You can paste the copied contents with the Paste method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Sheetname|Name of the sheet that contains source data.|Data in|String|
|Cellrange|Range of cells to be copied.|Data in|String|

## Paste

Pastes the clipboard content into specific cells provided in the CellLocation parameter of a worksheet. It can also be a range of cells.

**Note:** You must execute the Copy method before executing this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|Sheetname|Name of the sheet where the clipboard content will be pasted.|Data in|String|
|CellLocation|Indicates the location \(cell reference\) where the clipboard content will be pasted.|Data in|String|

## FillBlankValues

Fills empty cells in a specified column of a worksheet in a Microsoft Excel file with a given value. It requires the SheetName parameter to specify the worksheet, the ColumnName parameter to identify the column, and the Value parameter to provide the replacement value for the empty cells.

**Note:** You must execute the Open method before executing this method.

<table id="table_zv3_ssx_3dc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Sheetname

</td><td>

Name of the sheet to fill blank values.

</td><td>

Data in

</td><td>

String

</td></tr><tr><td>

ColumnName

</td><td>

Name of the column in the worksheet that needs to be filled with a value.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data in

</td><td>

ColumnName

</td></tr><tr><td>

Value

</td><td>

Value to be filled in the column.

</td><td>

Data in

</td><td>

String

</td></tr></tbody>
</table>## CreateChart

Creates a chart for a specific range in a specific worksheet. This method is used to automate creation of charts.

**Note:** You must execute the Open method before this method.

<table id="table_xny_h3j_25b"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the sheet where the chart is created.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

CellRange

</td><td>

Range of cells from which the chart is created.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

ChartType

</td><td>

Specifies the type of chart to be created.The available chart types depend on the specific implementation of the Excel connector being used.

</td><td>

Data In

</td><td>

ExcelChartType

</td></tr><tr><td>

Return

</td><td>

If True, the chart is successfully created. If False, the chart creation is failed.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## CreatePivotTable

Generates a pivot table on the specified sheet, utilizing the settings configured in the 'Pivot Table Settings' window.

**Note:** You must execute the Open method before this method.

|Parameter|Description|Data port type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet from where the pivot table has to be created.|Data In|String|
|PivotTableName|Name of the pivot table.|Data In|String|

## DeleteColumn

Deletes a column in a given sheet based on the specified index of the column.

<table id="table_uvm_l21_g5b"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the sheet from which the column is deleted.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

ColumnIndex

</td><td>

Index of the column that must be deleted.In Excel, columns are labeled alphabetically \(A, B, C, etc.\), and each column has a corresponding numeric index \(1 for column A, 2 for column B, and so on\).

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Return

</td><td>

Returns the Boolean value that indicates whether the column was deleted. If True, the column is deleted. If False, the column was not deleted.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## DeleteContentFromRange

Deletes contents from the specified range of cells.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet from which the contents will be deleted.|Data In|String|
|CellRange|Specifies the range of cells from which data is deleted.|Data In|String|
|Return|Returns the Boolean value that indicates whether the content from range of cells was deleted. If True, the content is deleted. If False, the content is not deleted.|Data Out|Boolean|

## DeleteEmptyColumns

Deletes columns that have no content in a specified worksheet of a Microsoft Excel file. This method requires the SheetName parameter to identify the worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet containing the empty column.|Data In|String|

## DeleteEmptyRows

Deletes rows that have no content in a specified worksheet of a Microsoft Excel file. This method requires the SheetName parameter to identify the worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet containing the empty rows.|Data In|String|

## DeleteRow

Deletes a row from the worksheet based on the RowNumber parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet from which the row is deleted.|Data In|String|
|RowNumber|Indicates the number of the row that must be deleted.|Data In|Integer|
|Return|Returns the Boolean value that indicates whether the row is deleted. If True, the row is deleted. If False, the row is not deleted.|Data Out|Boolean|

## DeleteWorksheet

Deletes the specified worksheet. This method requires the SheetName parameter to identify the worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet which must be deleted.|Data In|String|
|Return|Returns the Boolean value that indicates whether the worksheet was deleted. If True, the worksheet is deleted. If False, the worksheet is not deleted.|Data Out|Boolean|

## ExportChartAsImages

Exports and saves a chart present in a sheet into an image file that is saved in the specified path. This process separates the chart from the Excel workbook, providing a standalone visual representation that can be easily shared or inserted into various documents, presentations, or reports.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the sheet that contains the chart.|Data In|String|
|SaveFolderpath|Specifies the folder path where the charts are saved as image files.|Data In|String|

## ExportToPDF

Exports an Excel file as a PDF file to the path location mentioned in the FilePath parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Filepath|Specifies the file path to which the PDF file is exported.|Data In|String|

## FindAndReplace

Locates the text given in the FindText parameter in a given worksheet specified by the SheetName parameter and replaces it with another text given in the ReplaceTo parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the text will be replaced.|Data In|String|
|FindText|The text that is searched for within the cells of the worksheet.|Data In|String|
|ReplaceTo|The desired text to replace the text found using the FindText parameter.|Data In|String|
|Return|Returns the Boolean value that indicates whether the text is replaced. If True, the text is replaced. If False, the text is not replaced.|Data Out|Boolean|

## GetActiveSheetName

Returns the name of the active worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns the name of the active worksheet in a string format.|Data Out|String|

## GetCellAddressIfRowHas

Searches a given text in the specified sheet. It scans through the specified column name, starting from the indicated row index. If the text is found, it returns true. Else, it returns false. Additionally, the matched cell address can be stored in the configured value.

**Note:** Execute the Open method before executing this method.

<table id="table_j1m_jgy_3dc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet to search within.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchText

</td><td>

The text to search for within the specified column.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchColumn

</td><td>

The column where the search will be conducted.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

StartRowIndex

</td><td>

The row index from which the search will begin.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Return

</td><td>

Returns a Boolean value indicating whether the SearchText was found. If True, the text is found. If False, the text is not found.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## GetCellFormula

Retrieves the cell formula from a worksheet.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet to retrieve the cell formula from.|Data In|String|
|CellName|Specifies the name or reference of the cell to retrieve the formula from.|Data In|String|
|Return|Returns the specified cell formula in a string format.|Data Out|String|

## GetCellValue

Retrieves the value of a cell from a worksheet specified by the CellName parameter.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet from which the cell value will be retrieved.|Data In|String|
|CellName|Returns the cell value or display text based on the configuration set in GetCellValue.|Data In|String|
|Return|Returns the value in a specified cell in the string format.|Data Out|String|

## GetCellValueIfRowHas

Searches the specified sheet for a given text. It scans through the specified column, starting from the indicated row index. If the text is found, it returns true. Else, it returns false. Additionally, the matched cell value can be stored in the configured value.

**Note:** Execute the Open method before executing this method.

<table id="table_zyq_33y_3dc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet to search within.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchText

</td><td>

The text to search for within the specified column.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchColumn

</td><td>

The column where the search is conducted.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

StartRowIndex

</td><td>

The row index from which the search begins.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Return

</td><td>

Returns a Boolean value indicating whether the SearchText was found. If True, the text is found. If False, the text is not found.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## GetCellValues

Returns the values of cells from a worksheet.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|

## GetColor

Returns the RGB value of a cell specified in the CellName parameter from a worksheet.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet to retrieve the cell color from.|Data In|String|
|CellName|Name or reference of the cell to retrieve the color of.|Data In|String|
|Return|Returns the color of the specified cell in the string format.|Data Out|String|

## GetColumnNameByIndex

Returns the column name corresponding to the given column number, where, for example, 1 corresponds to 'A'.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|ColumnNumber|The column number that you want to retrieve the name of.|Data In|Integer|
|Return|Returns the name of the column in the string format.|Data Out|String|

## GetFilterData

Returns filtered data from a worksheet based on the specified filter criteria. Data is obtained starting from the row number provided in the RowNumber parameter.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|RowNumber|The row number of the row that is the starting row for the extraction of data.|Data In|Integer|
|FirstRowAsHeader|Determines whether the first row of the filtered data should be treated as header row. If set to true, the first row will be considered as header row and not included in the extracted data rows. If set to false, the first row will be included as part of the extracted data rows.|Data In|Boolean|
|Return|Returns the filtered data in a table format. Operations can be performed on the rows and columns of this table.|Data Out|Data table|

## GetFilteredDataAddress

Returns the address of the filtered data in the worksheet provided in the SheetName parameter.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet to retrieve the address of filtered data from.|Data In|String|
|Return|Returns a list or collection of strings where the strings are filtered data addresses.|Data Out|List\(Of string\)|

## GetRowValues

Returns cell values from the specified SheetName parameter to extract the values from. By default, if RowNumber is not specified \(or set to -1\), it reads values from the last row. Additionally, you can include output parameters to add column names and store their values in the output.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Specifies the name of the worksheet to retrieve the values from.|Data In|String|
|RowNumber|The row to read values from. If set to -1, it defaults to the last row.|Data In|Integer|

## GetSelectedRange

Returns the currently selected range of cells from the worksheet specified in the SheetName parameter. Data is extracted from the specific areas of the worksheet that have been highlighted or chosen.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|Return|Returns the range of cells selected in a sheet in the string format.|Data Out|String|

## GetSheetNames

Returns a list of all worksheet names present in an Excel file.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Return|Returns all the available sheet names in a string array format.|Data Out|String\[\]|

## GetUsedRange

Returns the range of used cells of the specified sheet.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet to read the range from.|Data In|String|
|IncludeHeaders|Indicates whether headers should be included.|Data In|Boolean|
|Return|Returns the range of used cells in string format.|Data Out|String|

## GetValuesByColumn

Returns a list of values from a specified ColumnName in the given SheetName based on the Distinct, FirstRowAsHeader, and ValueType parameters criteria.

**Note:** Execute the Open method before executing this method.

<table id="table_t3f_4gy_3dc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet that contains the source data.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

ColumnName

</td><td>

Denotes the name of the column from which values are retrieved.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

FirstRowAsHeader

</td><td>

Indicates whether the first row in the specified column contains headers.

</td><td>

Data In

</td><td>

Boolean

</td></tr><tr><td>

Distinct

</td><td>

Specifies whether the retrieved values should be distinct or unique.

</td><td>

Data In

</td><td>

Boolean

</td></tr><tr><td>

ValueType

</td><td>

Extracts values based on visibility.

</td><td>

Data In

</td><td>

ValueT

</td></tr><tr><td>

Return

</td><td>

Returns the number of rows.

</td><td>

Data Out

</td><td>

Integer

</td></tr></tbody>
</table>## InsertNewColumn

Inserts a new column at the index provided in the ColumnNumber parameter in the specified worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the column must be inserted.|Data In|String|
|ColumnIndex|Specifies the index of the column where the new column is inserted. For example, 1 is A, 2 is B, and so on.|Data In|Integer|

## InsertNewRow

Inserts a new row at the specified index in the specified worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the row will be inserted.|Data In|String|
|RowIndex|Index of the row. The row will be inserted at the specified index.|Data In|Integer|
|Return|Returns the Boolean value that indicates whether a row is inserted. If True, the row is inserted. If False, the row is not inserted.|Data Out|Boolean|

## InsertObject

Inserts an embedded object into a cell identified by the index value in the CellName parameter in the specified worksheet. The path to that embedded object is provided in the Filepath parameter. Example of an object could be an excel file, an image, or a PDF file.

**Note:** Execute the Open method before executing this method.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the method inserts the object.|Data In|String|
|CellName|Name of the cell where the method inserts the object. For example, A1.|Data In|String|
|Filepath|File path of the object that the method inserts.|Data In|String|

## IsOpen

Checks whether a Microsoft Excel workbook or file at the location provided in the Filepath parameter is open or not.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Filepath|Path to the Excel file in the local drive.|Data In|String|
|Return|Returns the Boolean value that indicates whether the Excel file is open. If True, the Excel file is open. If False, the Excel file is not open.|Data Out|Boolean|

## MergeCells

Merges the cells specified in the range in the specified worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Sheetname|Name of the worksheet on which the cells will be merged.|Data In|String|
|CellRange|Range of cells. All cells within the range are merged.|Data In|String|

## ReadFromRange

Retrieves data from a specified worksheet and returns it. You need to provide the worksheet name to indicate from which worksheet to extract the cell range, specify the cell range to determine the range of cells to read, and indicate whether the first row is a header in the FirstRowAsHeader parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet from where the method reads the data.|Data In|String|
|CellRange|Range of cells. The method reads data from these cells.|Data In|String|
|FirstRowAsHeader|Boolean value that indicates whether the method treats the first row as the header. If True, the first row is treated as a header. If False, the first row is not treated as a header.|Data In|Boolean|
|Return|Returns the data table that comprises the data from the cells.|Data Out|Data Table|

## ReadFromSheet

Extracts data from a worksheet and convert it into a structured format, such as a DataTable.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Sheetname|Name of the worksheet from which the method reads the data.|Data In|String|
|Return|Returns all the data in the specified worksheet.|Data Out|DataTable|

## RenameSheetName

Renames an existing worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|OldSheetName|The existing name of the worksheet.|Data In|String|
|NewSheetName|The new name of the worksheet.|Data In|String|
|Return|Returns the Boolean response that indicates whether the worksheet is renamed. If True, the worksheet is renamed. If False, the worksheet is not renamed.|Data Out|Boolean|

## RowsCount

Returns the count of rows in the specified worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet from where the count of rows are returned.|Data In|String|
|Return|Returns the number of rows.|Data Out|Integer|

## RunMacro

Executes an existing macro in the Excel file. The method requires the name of the macro that the user intends to run.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|MacroName|The name of the Macro to execute.|Data In|String|
|Return|Returns boolean value indicating if macro was successfully run or not.|Data Out|Boolean|

## Resize

Changes Excel application window's width and height dimensions. Layout and appearance of the Excel application can be customized to accommodate specific display requirements.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Left|This parameter specifies the horizontal position of the top-left corner of the Excel application window relative to the screen's left edge. It defines the distance, in pixels or points, from the left edge of the screen to the left edge of the Excel window.|Data In|Integer|
|Top|This parameter indicates the vertical position of the top-left corner of the Excel application window relative to the screen's top edge. It defines the distance, in pixels or points, from the top edge of the screen to the top edge of the Excel window.|Data In|Integer|
|Width|This parameter specifies the width of the Excel application window in pixels or points. It determines the horizontal size of the window, extending from the left edge to the right edge.|Data In|Integer|
|Height|This parameter indicates the height of the Excel application window in pixels or points. It defines the vertical size of the window, extending from the top edge to the bottom edge.|Data In|Integer|

## RemoveFilter

Removes filters from a worksheet given in the SheetName parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Sheetname|Name of the worksheet from which the method removes the filters.|Data In|String|

## Save

Saves any updates, changes, additions, or deletions made to the data or formatting within a Microsoft Excel document to ensure that the work is preserved and that the Excel file reflects the most recent updates.

## SaveAs

Saves an Excel file with a different name or format to a file path provided in the Filepath parameter. The file can also be password protected by providing the value in the Password parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Filepath|The file path where the Excel file is saved with a different name or format.|Data In|String|
|Password|Password to protect the Excel file that will be saved. This parameter is optional and has a default value of an empty string.|Data In|String|

## SaveCopyAs

Saves a copy of the Excel file to a specified path that serves as a destination for the saved copy.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Filepath|The file path where the Excel file is saved with a different name or format.|Data In|String|
|Password|Password to protect the Excel file that is saved. This parameter is optional and has a default value of an empty string.|Data In|String|

## SelectRange

Specifies and highlights a range of cells within an Excel worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|CellRange|The range of cells that are selected within the specified worksheet. It defines the group of cells, typically identified by the starting and ending cell references, that will be highlighted or activated.|Data In|String|

## SelectRowByIndex

Selects the entire row based on the index provided in the RowNumber parameter in the worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the row is selected.|Data In|String|
|RowNumber|The index of the row to be selected.|Data In|Integer|

## SetActiveWorksheet

Marks the worksheet specified in the Sheetname as the active worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet which needs to be set as active.|Data In|String|
|Return|Returns the boolean value indicating if the provided sheet has been set as active or not.|Data Out|Boolean|

## SetAlignment

Adjusts the alignment settings of cells given in the CellRange to control the presentation and appearance of data within the Excel worksheet and enhancing the visual appeal and readability of spreadsheet data, improving data presentation, and communication.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|CellRange|Range of cells to which the alignment settings or properties are applied.|Data In|String|
|HorizantalAlignment|Horizontal alignment of cell contents within the specified range. It determines how the content \(such as text or numbers\) is positioned within each cell horizontally. Possible values include left, center, right, justified, or distributed.|Data In|HorizantalAlignment|
|VerticalAlignment|Vertical alignment of cell contents within the specified range. It determines how the content is positioned within each cell vertically. Possible values include top, middle, bottom, or justified.|Data In|VerticalAlignment|

## SetCellColor

Sets a color given in the Color parameter on a particular cell specified in the CellName parameter in a worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the cell is located.|Data In|String|
|CellName|Indicates the name or reference of the cell for which the color will be set.|Data In|String|
|Color|Specifies the RGB color value to be applied to the cell.|Data In|ExcelRgbColor|
|Return|Returns boolean value indicating if the formula is set for a particular cell provided.|Data Out|Boolean|

## SetCellFormula

Assigns a formula to a specified cell in the Excel file. This method requires the SheetName, CellName, and Formula parameters to determine the worksheet, cell, and formula to be set, respectively.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the action will be performed.|Data In|String|
|CellName|The cell within the worksheet where the operation will take place.|Data In|String|
|Formula|The mathematical or logical expression to be applied to the specified cell.|Data In|String|
|Return|Returns boolean value indicating if the formula is set for the specified cell.|Data Out|Boolean|

## SetCellValue

Assigns a value to a specific cell in a worksheet, replacing any existing content in that cell.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|CellName|This parameter indicates the reference or identifier of the target cell within the specified worksheet. It can be represented by the cell address \(e.g., 'A1', 'B2', 'C3'\).|Data In|String|
|Value|Value that will be assigned to the specified cell which can be of any data type supported by Excel, including numbers, text, dates, formulas, or logical values.|Data In|String|

## SetCellValues

Sets values in multiple cells as configured in the method editor dialog within a specified sheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the cell values will be set.|Data In|String|

## SetCellValuesIfRowHas

Scans the specified sheet for a provided text, examining the designated column name from the indicated row index. If the text is found, it sets the value of the specified cell with the provided values. It returns true if the value was successfully set, otherwise false.

<table id="table_ov2_n5f_jdc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet to search within.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchText

</td><td>

The text to search for within the specified column.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchColumn

</td><td>

The column where the search is conducted.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

StartRowIndex

</td><td>

The row index from which the search begins.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Return

</td><td>

Returns True if SearchText is found in the specified column. Else, it returns False.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## SetColumnType

Modify the data type of a specified column within a worksheet. For example, users can convert a column containing numeric values to a text format or change a column of text data to numeric format. It is possible to adjust the data format to better suit analysis or reporting needs, ensuring consistency and accuracy in data representation. Useful for tasks such as data conversion, formatting, and manipulation in Excel.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|FormatType|The desired format type the column is converted to. This parameter determines how the data within the column is interpreted or displayed. Possible values may include numeric, text, date, time, currency, percentage, or custom formats.|Data In|String|
|Column|The column reference or identifier within the specified worksheet for which the data type is changed. It could be represented by the column letter \(e.g., 'A', 'B', 'C'\).|Data In|String|
|Return|Returns boolean value identifying if the column type has been set or not.|Data Out|Boolean|

## SetColumnWidth

Sets the width of all the columns provided in the width parameter.

<table id="table_oyg_n5f_jdc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet where the column width is adjusted.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Width

</td><td>

The width in characters to which the column is set.Only integer value is accepted. Decimal values are not accepted.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Return

</td><td>

Returns boolean value identifying if the column type has been set or not.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## SetFilter

Applies a filter to a specific column. This method finds the worksheet based on the given sheet name and then applies the provided filter value.

<table id="table_i13_n5f_jdc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet where the column is located.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

ColumnName

</td><td>

Column where the filter is applied.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

FilterValue

</td><td>

The value to filter by within the identified column.

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## SetFilterByRow

Applies a filter to a specified column, starting from a given row number. This method finds the worksheet based on the given sheet name and then applies the provided filter value.

<table id="table_sbj_n5f_jdc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet that contains the source data.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

RowNumber

</td><td>

Indicates the row number within the specified worksheet where the filtering criteria are defined. It identifies the row containing the criteria that will be used to filter the data.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

ColumnName

</td><td>

Name or identifier of the column based on which the filtering will be performed. It represents the column to which the filtering criteria apply.ColumnName is an Enum data type that represents Excel columns from A to AZ.

The provided ColumnName refers to the column name relative to the starting column of your data. For example, if your data begins at column B in the Excel sheet, the relative column index A corresponds to column B, the relative column index B corresponds to column C, and so on.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

FilterValue

</td><td>

Value or condition used as the filter criteria. It represents the specific value that the data in the designated column must match to be displayed after the filter is applied.

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## SetFontStyle

Formats the cells within a specified range by setting parameters such as Color, FontStyle, FontName, Bold, and Underline.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet where the font style will be set.|Data In|String|
|CellRange|The range of cells for which the font style will be set.|Data In|String|
|Color|Specifies the RGB color value of the font.|Data In|ExcelRgbColor|
|FontSize|Specifies the size of the font. The default value is 11.|Data In|Integer|
|FontName|Specifies the name of the font. The default value is Calibri.|Data In|String|
|Bold|Indicates whether the font should be bold. The default value is False.|Data In|Boolean|
|Underline|Specifies the underline style for the font. The default value is None.|Data In|Underline|

## SetRowHeight

Modifies the height of a specific row within an Excel worksheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|The name of the worksheet where the rows are located.|Data In|String|
|Height|Specifies the desired height.|Data In|Integer|
|StartIndex|The starting row index.|Data In|String|
|EndIndex|The ending row index.|Data In|String|
|Return|Returns boolean value indicating if the row height was set successfully or not.|Data Out|Boolean|

## SetRowValues

Sets values for a specific row in an Excel spreadsheet. By default, when the RowIndex parameter is set to -1, the function inserts the values at the end of the spreadsheet. This means that if you don't specify a specific row index, the values are appended to the bottom of the existing data in the spreadsheet.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|RowNumber|Denotes row number where the values will be set or updated. In Excel, rows are numbered sequentially from top to bottom, starting with 1 by specifying the RowNumber, you indicate the specific row where the values should be placed. If -1 is passed as the RowNumber, it typically indicates that the values will be inserted at the end of the spreadsheet.|Data In|Integer|

## Sort

Organizes data within a specified cell range in either ascending or descending order.

<table id="table_knn_n5f_jdc"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port Type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SheetName

</td><td>

Name of the worksheet where the data will be sorted.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

CellRange

</td><td>

The range of cells containing the data to be sorted.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

ColumnName

</td><td>

The name of the column by which the data will be sorted.ColumnName is an Enum data type that represents Excel columns from A to AZ.

</td><td>

Data In

</td><td>

ColumnName

</td></tr><tr><td>

SortingOrder

</td><td>

The sorting order \(ascending or descending\) for the data.

</td><td>

Data In

</td><td>

SortingOrder

</td></tr></tbody>
</table>## VLookUp

Searches for a specific value in the first column of a specified cell range and then returns a corresponding value from a column you designate within the same row.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|Sheetname|Name of the worksheet to search within.|Data In|String|
|SearchText|The text to search for within the specified column.|Data In|String|
|LookupRange|Range to scan for the text.|Data In|String|
|ApproximateMatch|This is a logical value that specifies whether you want an exact match or an approximate match.|Data In|Boolean|
|Return|Returns boolean value indicating if macro was successfully run or not.|Data Out|Boolean|

## WrapText

Enable text wrapping for all cells in a specified row in an Excel worksheet. Text wrapping ensures that long text strings are displayed within the cell boundaries, automatically adjusting the row height to accommodate the wrapped text. By using the WrapText method, users can improve the readability of their data by ensuring that all text is fully visible within each cell, even if it extends beyond the cell's original width. This can be particularly useful for displaying lengthy text entries or multi-line content within spreadsheet cells.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet that contains the source data.|Data In|String|
|RowNumber|The row number within the specified worksheet where text wrapping is set for all cells in that row.|Data In|Integer|

## WriteToRange

Writes a datatable provided in the Data parameter into a worksheet starting from the cell provided in the CellName parameter. Headers can also be included by setting the IncludeHeaders parameter.

|Parameter|Description|Data Port Type|Data type|
|---------|-----------|--------------|---------|
|SheetName|Name of the worksheet on which the data is written.|Data In|String|
|CellName|Name of the cell on which the data is written.|Data In|String|
|Data|Data that is written.|Data In|Data Table|
|IncludeHeaders|Boolean value that Indicates whether to include headers when writing the data. The default value is set to True.|Data In|Boolean|

**Parent Topic:**[Microsoft Excel](../concept/microsoft-excel-connector.md)

