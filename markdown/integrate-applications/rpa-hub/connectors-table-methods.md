---
title: Table connector methods
description: The Table connector provides multiple methods that perform various actions on tabular data as part of an automation Workflow in the RPA Desktop Design Studio. For example, tasks such as getting a table, getting a row data, and removing empty rows.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
breadcrumb: [Table, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Table connector methods

The Table connector provides multiple methods that perform various actions on tabular data as part of an automation Workflow in the RPA Desktop Design Studio. For example, tasks such as getting a table, getting a row data, and removing empty rows.

## SetTable

Inserts a table into the workflow. The SetTable method must be used before you do any other operations on a data table. You must provide the table object that needs to be set.

<table id="table_ln5_kgj_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table that you want to add or modify.-   **Example**

DataTable


</td><td>

Data In

</td><td>

DataTable

</td></tr></tbody>
</table>## AddColumn

Adds a column to a table. The position of the column is determined by the column index value that you specify. You must provide the name of the new column and the column index at which the new column needs to be added.

<table id="table_rq2_b3j_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the new column that you want to add.-   **Example**

Customer data


</td><td>

String

</td></tr><tr><td>

ColumnIndex

</td><td>

Index of the column where the new column needs to be added. By default, -1 is the index value that you can update. For example, 0, 1, 2 can indicate the positions of columns from the left to the right.

</td><td>

Integer

</td></tr></tbody>
</table>## AddColumns

Adds multiple columns to a table by accepting column names from another method or component. To view the columns added, use the GetTable method. You must provide a list of names of new columns which needs to be added in the datatable.

<table id="table_y54_j3j_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Names

</td><td>

Accepts names of columns in the form of an array, array list, or list.-   **Example**

\{ "OrderID", "CustomerName", "OrderDate", "Status"\};


</td><td>

IEnumerable

</td></tr></tbody>
</table>## AddRow

Adds a row and its contents at the specified index. You must provide the RowIndex at which the row needs to be added.

To set the index values where you add the contents of the row, do the following actions:

1.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).
2.  Click the add index icon \(![Add index icon.](../image/add-image-icon.png)\).
3.  Enter the index.
4.  Repeat the steps to add multiple indexes.
5.  Click **OK**.

    **Note:** A Data In port is added with each row that you add.


|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|RowIndex|Index of row at which the new row needs to be added.|Data In|Integer|

## GetTable

Returns the table that you created with the AddColumn, AddColumns, and AddRow methods.

**Note:** You must execute this method after executing the AddColumn, AddColumns, and AddRow methods.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|DataTable|Returns DataTable type representing underlying DataTable object.|Data Out|DataTable|

## ClearColumns

Clears all column values from a table.

## ClearRows

Clears all row values from a table.

## DeleteColumnByIndex

Deletes a column based on the index value that you specify. You must provide the index of the column to be deleted to the Index parameter.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Index|Index value of the column that must be deleted.|Data In|Integer|

## DeleteColumnByName

Deletes a column based on the name that you specify. You must provide the name of the column that needs to be deleted.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Name|Name of the column that must be deleted.|Data In|String|

## DeleteRow

Deletes a row based on the index value provided. Before executing this method, you must assign custom index values to the rows. You must provide index of the row which needs to be deleted.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Index|Index of the row which needs to be deleted.|Data In|Integer|

## FilterAndSort

Filters and sorts the table based on a expression that you specify. You must provide the expression to calculate the value of a column, column name to be sorted in SortColumnName and Order. It returns the count of the rows available based on the criteria set and also returns the complete data table.

<table id="table_t4c_bpj_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Expression

</td><td>

Expression to calculate the value of a column.-   **Example**

"Status = 'Pending'" - Based on this query expression, the data is filtered.


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SortColumnName

</td><td>

Column name by which the method will sort the data.-   **Example**

Date - The method will sort the data based on the Date column.


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Order

</td><td>

Order of the column name

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

DataTable

</td><td>

Returns the data table containing filtered data from the underlying DataTable object.

</td><td>

Data Out

</td><td>

DataTable

</td></tr><tr><td>

Count

</td><td>

Returns the count of rows after sort.

</td><td>

Data Out

</td><td>

Integer

</td></tr></tbody>
</table>## FilterByRegEx

Filters the table data based on a regular expression or RegEx that you specify. You must provide the column index to ColumnIndex parameter and the regular expression to RegExpression parameter, which are used for filtering. This method returns the rows count and the data table.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|ColumnIndex|Index of column on which filtering logic needs to be applied. The default index value is -1 for the first column. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|
|RegExpression|Regular expression which is used as a filtering logic.|Data In|String|
|Return|Returns a DataTable containing filtered data from the underlying DataTable object.|Data Out|DataTable|
|RowsCount|Returns the number of rows available based on the filter using RegExpression.|Data Out|Integer|

## FindText

Finds the text in the table that you specify based on one or more criteria and returns cell value. You must provide the text to search in SearchText parameter, position from where the search should start in StartPosition and the type of match required.

<table id="table_hrj_vpj_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SearchText

</td><td>

Text to be searched in the table.-   **Example**

"John Doe"


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

StartPosition

</td><td>

Position of the column from where the search should start.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

MatchType

</td><td>

Type of match of the text:-   **ExactMatch**: The specified text and the searched text must match exactly. This is a default value.
-   **MatchCase**: The specified text case should match the case of the searched text.
-   **Contains**: The specified text should contain one or more characters of the searched text.

</td><td>

Data In

</td><td>

MatchType

</td></tr><tr><td>

CellValue

</td><td>

Returns the value in the cell based on the search.

</td><td>

Data Out

</td><td>

Object

</td></tr><tr><td>

ColIndex

</td><td>

Returns the index of the column that has that searched text.

</td><td>

Data Out

</td><td>

Integer

</td></tr><tr><td>

RowIndex

</td><td>

Returns the index of the row that has that searched text.

</td><td>

Data Out

</td><td>

Integer

</td></tr></tbody>
</table>## GetCellValue

Returns the value in a cell based on the row and column index values that you specify. You must provide the row number and column number of the cell from which value needs to be retrieved.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Row|Row number of the required cell.|Data In|Integer|
|Column|Column number of the required cell.|Data In|Integer|
|Return|Returns Object type representing cell value from underlying DataTable object.|Data Out|Object|

## GetCellValueIfRowHas

Returns True if the method finds the text that you specify and the row values based on the index values that you specify. You must provide the text to be searched. Perform the search on a particular column provided by SearchColumnIndex and start searching the text from a particular row provided to StartRowIndex. Default value is 1 meaning 1st row of the table.

To specify the row values, you must configure the method.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add row index icon \(![Add row index.](../image/add-image-icon.png)\).
3.  Update the row index value data type.
4.  Enter the row index value.
5.  Click **OK**.

<table id="table_q2d_gsj_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

SearchText

</td><td>

Text to be searched in the row.-   **Example**

"John Doe"


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SearchColumnIndex

</td><td>

Index of column in which the text needs to be searched.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

StartRowIndex

</td><td>

Starting row from which the search needs to be performed.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Found

</td><td>

Returns True if the text matched.

</td><td>

Data Out

</td><td>

Boolean

</td></tr></tbody>
</table>## GetCellValues

Returns values of the multiple cells based on the index values that you specify. You must provide the row index of the cell whose value needs to be retrieved. Additional row indexes can also be added to get those cell values using the config window.

To configure, do the following actions:

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Click the add row index icon \(![Add row index.](../image/add-image-icon.png)\).
3.  Update the row index value data type.
4.  Enter the row index value.
5.  Click **OK**.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|RowIndex|Index of the row whose cell value is required.|Data In|Integer|

## GetCount

Returns the total count of rows and columns of a data table.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Row|Returns the total count of rows created.|Data Out|Integer|
|Column|Returns the total count of columns created.|Data Out|Integer|

## GetRowData

Returns row data based on the index value that you specify. You must provide the index value of the row from which data needs to be retrieved.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|RowIndex|Index value of the row from which data needs to be retrieved.|Data In|Integer|
|Return|Returns list Of Object type representing row data from underlying DataTable object. The **IEnumerable** data type accepts the row value data as array, list, or array list and returns as object.|Data Out|IEnumerable|

## GetTableAsCSV

Saves the table data in the CSV format to the local drive. You must provide the file path to which the CSV file needs to be written to and also provide the separator between the two records.

<table id="table_m3c_1zj_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Filepath

</td><td>

Folder path in the local drive where the method saves the table data as CSV. In the file path, you must include the filename.-   **Example**

D:\\Projects\\Customer data.csv


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

Delimiter

</td><td>

Delimiter that separates the table data.-   **Example**

Comma \(","\)


</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## GetTableAsHTML

Returns the table data in an HTML file format. Before you execute this method, you must create columns, rows, and data and then execute them with the GetTable method.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Return|Returns the tabular data in the HTML format.|Data In|String|

## GetTableAsJson

Returns the table data in a JSON file format. Before you execute this method, you must create columns, rows, and data and then execute them with the GetTable method.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Return|Returns the tabular data as a JSON object.|Data In|String|

## LoadFromExcel

Imports the sheet or data from the specified Excel file to the data table. You must provide the path of the Excel file from which the data needs to be loaded. Give the sheet name or provide a query to SheetOrQuery parameter. If a query is provided, then set the IsQuery Boolean to True, and if a sheet name is provided, then set the IsQuery Boolean to False. You can test whether the data was imported correctly with the GetTable method.

<table id="table_iln_rzj_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

FilePath

</td><td>

Path to the Excel file from which the data is imported.-   ****

D:\\Projects\\Sales\\Sales data.xlsx


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

SheetOrQuery

</td><td>

Indicates whether data is imported from a sheet in the Excel file or through a query to the file.

</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

IsQuery

</td><td>

Boolean value to indicate whether the data is loaded through a query.

</td><td>

Data In

</td><td>

Boolean

</td></tr></tbody>
</table>## MatchColumn

Matches another datatable's columns with the current table's column based on the column index. You must provide the datatable whose columns need to be matched provided in dtTable with the index of column in current table in ColumnIndex parameter. Before you execute this method, you must execute the GetTable method.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|dtTable|Data table whose columns need to be matched.|Data In|DataTable|
|ColumnIndex|Index of the column with which it has to be matched.|Data In|Integer|
|Return|Returns a true or false value indicating whether the specified column is matched.|Data Out|Boolean|

## RemoveEmptyColumns

Removes all the empty columns in the table and returns the data table after the operation.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Return|Returns the data table after removing the empty columns.|Data Out|DataTable|

## RemoveEmptyRows

Removes all the empty rows in the table and returns the data table after the operation.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Return|Returns the data table after removing the empty rows.|Data Out|DataTable|

## SetCellValue

Adds data to a cell based on column and row index values. You must provide the row number, column number and the value in Value parameter that needs to be set.

Before you execute this method, you must create columns, rows, and data and then execute them with the GetTable method.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Row|Index number of the row which the method will use to fill data.|Data In|Integer|
|Column|Index number of the column which the method will use to fill data.|Data In|Integer|
|Value|Value that must be set in the cell.|Data In|Object|

## SetCellValueIfRowHas

Sets cell value\(s\) of a particular row if row contains specified text. You must provide the row index in the Row Index configuration dialog. The name of the row index parameter added is considered for setting the value and the value provide to that parameter is the actual value that will be set to the row of the table.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|SearchText|Text to be searched in the row.|Data In|String|
|SearchColumnIndex|Index of the column in which the text needs to be searched.|Data In|Integer|
|StartRowIndex|Starting row from which the text needs to be searched.|Data In|Integer|
|Found|Returns True if the text matches.|Data Out|Boolean|

## SetColumnName

Updates a column name based on the column index and name that you specify. You must first create or import a table by using the SetTable method.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|ColumnIndex|Index of the column which needs to be named.|Data In|Integer|
|Name|New name of the column.|Data In|String|

## SetJson

Converts a JSON object to a DataTable. Provide JSON data that needs to be converted to DataTable.

**Tip:** To create a JSON object, use the GetTableAsJson method and then pass the values to the SetJson method.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|JSON|JSON object needs to be converted to a DataTable.|Data In|String|

## SetList

Converts a list to a DataTable. Provide the data list that needs to be converted to table.

<table id="table_szb_tfk_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Data

</td><td>

List type data that needs to be converted to table. The **IEnumerable** input data type accepts the data as array, list, or array list.-   ****

\{ "OrderID": 102, "CustomerName": "John Doe", "OrderDate": "2024-02-02", "Status": "Shipped" \};


</td><td>

Data In

</td><td>

IEnumerable

</td></tr></tbody>
</table>## SetRowData

Inserts the specified row data into a data table. You must provide the index number of the row to the RowIndex parameter and data that needs to be added to the row to the Data parameter.

<table id="table_os3_xfk_32c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

RowIndex

</td><td>

Index number of the row that needs to be modified.

</td><td>

Data In

</td><td>

Integer

</td></tr><tr><td>

Data

</td><td>

Data in a row that is inserted into a data table. The **IEnumerable** input data type accepts the data as array, list, or array list.-   ****

\{ "OrderID": 102, "CustomerName": "John Doe", "OrderDate": "2024-02-02", "Status": "Shipped" \};


</td><td>

Data In

</td><td>

IEnumerable

</td></tr></tbody>
</table>## ToList

Converts the specified table to a list.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Return|Returns an IEnumerable representing a DataTable object converted into a List. The **IEnumerable** data type accepts the data as array, list, or array list and returns the list.|Data Out|IEnumerable|

## VLookUp

Gets cell value\(s\) of a particular row if row contains specified text.

To input the values, do the following actions:

1.  Click the method settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).
2.  Click ![Add value icon.](../image/add-image-icon.png).
3.  Enter the values.
4.  Click **OK**.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Port name|Name of the port of the component.|Data In|String|
|SearchText|Text that the method will search in the rows and columns.|Data In|String|
|DataColumnIndex|Integer value that indicates the order of the column from the left. The default index value is -1 for the first column. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|
|SearchColumnIndex|Integer value that indicates the order of the column from the left. The default index value is -1 for the first column. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|
|StartRowIndex|Integer value that indicates the order of the column from the left. The default index value is -1 for the first row. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|

## VLookUpSet

Sets cell value\(s\) of a particular row if row contains specified text.

To input the values, do the following actions:

1.  Click the method settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).
2.  Click ![Add value icon.](../image/add-image-icon.png).
3.  Enter the values.
4.  Click **OK**.

|Parameter Name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Port name|Name of the port of the component.|Data In|String|
|SearchText|Text that the method will search in the rows and columns.|Data In|String|
|DataColumnIndex|Integer value that indicates the order of the column from the left. The default index value is -1 for the first column. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|
|SearchColumnIndex|Integer value that indicates the order of the column from the left. The default index value is -1 for the first column. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|
|StartRowIndex|Integer value that indicates the order of the column from the left. The default index value is -1 for the first row. Providing a custom index value is optional. If the field receives no custom index value, the method automatically sets the order of the columns.|Data In|Integer|

**Parent Topic:**[Table](../concept/table-connector.md)

