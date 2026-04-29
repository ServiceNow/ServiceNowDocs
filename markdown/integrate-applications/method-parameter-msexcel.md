---
title: Parameters of the Microsoft Excel connector methods
description: Learn about the parameters of the Microsoft Excel connector methods in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Microsoft Excel, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Parameters of the Microsoft Excel connector methods

Learn about the parameters of the Microsoft Excel connector methods in RPA Desktop Design Studio.

<table id="table_rfq_qpm_3rb"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

CellName

</td><td>

Cell name in a Microsoft Excel worksheet to perform an operation.

</td><td>

 

</td></tr><tr><td>

ApproximateMatch

</td><td>

Boolean option to find an exact or an approximate match.

</td><td>

Not applicable

</td></tr><tr><td>

CellLocation

</td><td>

Cell location in a Microsoft Excel worksheet to perform an operation.

</td><td>

Yes

</td></tr><tr><td>

CellRange

</td><td>

Set of one or more continuous cells in a worksheet.Example: A cell range of B2:E4 represents the cells from columns B through E and rows 2 through 4.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where the data is taken to create a chart.

</td><td>

Yes

</td></tr><tr><td>

ChartType

</td><td>

Type of chart you can create in a Microsoft Excel such as an area, bar, line, and pie.

</td><td>

Yes

</td></tr><tr><td>

Color

</td><td>

Color to set on a cell.

</td><td>

 

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where the data is taken to create a Pivot table.

</td><td>

 

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from which the rows will be deleted.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where the empty columns will be deleted.

</td><td>

Yes

</td></tr><tr><td>

ColumnIndex

</td><td>

Index number of the column.**Note:** Index number must be greater than zero.

</td><td>

Yes

</td></tr><tr><td>

ColumnName

</td><td>

Column name in a Microsoft Excel worksheet from which values are to be obtained.

</td><td>

Yes

</td></tr><tr><td>

CreateNewFile

</td><td>

Boolean values to indicate whether you want to create a file. If you choose -   **True**: You must provide the filepath including the new file name.
-   **False**: You are not creating a file.

</td><td>

No

</td></tr><tr><td>

Return \(Integer\)

</td><td>

Returns the Boolean response on whether the column was deleted.

</td><td>

Not applicable

</td></tr><tr><td>

DisplayAlerts

</td><td>

Option to display alerts when the file is opened. If you choose:-   **True**: Alert is displayed.
-   **False**: Alerts are not displayed.

</td><td>

No

</td></tr><tr><td>

Return

</td><td>

Returns the Boolean value that indicates whether a file was open or created.-   **True**: A file was opened or created.
-   **False**: No file was opened or created.

</td><td>

Not applicable

</td></tr><tr><td>

Distinct

</td><td>

Option to get only unique values. Set to **True** to get only distinct values or to **False** to get all values from a cell range.

</td><td>

 

</td></tr><tr><td>

EndColumnName

</td><td>

Name of the last column in a set of columns.

</td><td>

Yes

</td></tr><tr><td>

EndRowIndex

</td><td>

Last row number in a set of rows in a Microsoft Excel worksheet for a bulk operation such as to search, set values, or get values.

</td><td>

Yes

</td></tr><tr><td>

FileName

</td><td>

Name of the Microsoft Excel file.

</td><td>

Yes

</td></tr><tr><td>

Filepath

</td><td>

Path to the file including the file name. This parameter is used for both opening existing files or creating new files.

</td><td>

Yes

</td></tr><tr><td>

Filepath

</td><td>

Path where the exported PDF will be saved. You must provide the name of the file followed by the PDF extension.

</td><td>

Yes

</td></tr><tr><td>

FillType

</td><td>

One of the following fill types values:

 -   xlFillFormats: Copy only the formats from the source range to the target range, and repeat if necessary.
-   xlFillSeries: Extend the values in the source range into the target range as a series \(for example, '1, 2' is extended as '3, 4, 5'\). Formats are copied from the source range to the target range, and repeat if necessary.
-   xlFillValues: Copy only the values from the source range to the target range, and repeat if necessary.
-   xlFillCopy: Copy the values and formats from the source range to the target range, and repeat if necessary.
-   xlFillDays: Extend the names of the days of the week in the source range into the target range. Copy the formats from the source range to the target range, and repeat if necessary.
-   xlFillWeekdays: Extend the names of the days of the workweek in the source range into the target range. Copy the formats from the source range to the target range, and repeat if necessary.
-   xlFillMonths: Extend the names of the months in the source range into the target range. Copy the formats from the source range to the target range, and repeat if necessary.
-   xlFillYears: Extend the years in the source range into the target range. Copy the formats from the source range to the target range, and repeat if necessary.
-   xlGrowthTrend: Extend the numeric values from the source range into the target range, assuming that the relationships between the numbers in the source range are multiplicative \(for example, '1, 2,' is extended as '4, 8, 16' assuming that each number is a result of multiplying the previous number by some value\). Copy the formats from the source range to the target range, and repeat if necessary.
-   xlLinearTrend: Extend the numeric values from the source range into the target range, assuming that the relationship between the numbers is additive \(for example, '1, 2,' is extended as '3, 4, 5' assuming that each number is a result of adding some value to the previous number\). Copy the formats from the source range to the target range, and repeat if necessary.

</td><td>

Yes

</td></tr><tr><td>

FilterValue

</td><td>

Filter expression that consists of alphanumeric characters and one or more of the following operators: &lt;, &gt;, \\, &amp;, \|, and =.

</td><td>

Yes

</td></tr><tr><td>

FindText

</td><td>

Text to search in a Microsoft Excel worksheet.

</td><td>

Yes

</td></tr><tr><td>

StartColumnName

</td><td>

Name of the first column in a set of columns.

</td><td>

Yes

</td></tr><tr><td>

FirstRowAsHeader

</td><td>

Option to indicate whether the first row in a Microsoft Excel worksheet is a header row.

</td><td>

Yes

</td></tr><tr><td>

FormatType

</td><td>

Format type that is supported in a Microsoft Excel.Example: Currency, Number, Long Date

</td><td>

Yes

</td></tr><tr><td>

Formula

</td><td>

Formula to be applied on a cell in a Microsoft Excel file.

</td><td>

Yes

</td></tr><tr><td>

Height

</td><td>

Height of a row in pixels.

</td><td>

Yes

</td></tr><tr><td>

HorizontalAlignment

</td><td>

Horizontal alignment formatting of the specified cells.Example: Left, Right, Center, Justify

</td><td>

Yes

</td></tr><tr><td>

IsVisible

</td><td>

Boolean value to indicate whether the file will be visible when it's open. If you choose:-   **True**: The file is displayed.
-   **False**: The file is not displayed.

</td><td>

No

</td></tr><tr><td>

IncludeHeaders

</td><td>

Option to include the header row while getting a used cell range in a Microsoft Excel.

</td><td>

No

</td></tr><tr><td>

LookupRange

</td><td>

Range of columns of data.The values in the first column of the range are the values searched.

</td><td>

Yes

</td></tr><tr><td>

OldSheetName

</td><td>

Current name of the worksheet in a Microsoft Excel file that you want to rename.

</td><td>

Yes

</td></tr><tr><td>

MacroName

</td><td>

Name of the macro to run.

</td><td>

Yes

</td></tr><tr><td>

NewSheetName

</td><td>

New name of the worksheet in a Microsoft Excel file

</td><td>

Yes

</td></tr><tr><td>

Password

</td><td>

Password to open a protected file.

</td><td>

No

</td></tr><tr><td>

PivotTableName

</td><td>

Name of the new PivotTable.

</td><td>

 

</td></tr><tr><td>

ReadOnlyMode

</td><td>

Boolean value to indicate whether the file will be opened or created in read-only mode. If you choose:-   **True**: The file is opened or created in read-only mode.
-   **False**: The file is opened or created in write mode.

</td><td>

No

</td></tr><tr><td>

DestinationRange

</td><td>

The range of cells to be filled in the Microsoft Excel file.

</td><td>

Yes

</td></tr><tr><td>

ReplaceTo

</td><td>

Text with which to replace the found text in a Microsoft Excel worksheet.

</td><td>

Yes

</td></tr><tr><td>

RowIndex

</td><td>

Index value of a row.

</td><td>

Yes

</td></tr><tr><td>

RowNumber

</td><td>

Row number in a Microsoft Excel worksheet to perform an operation.

</td><td>

Yes

</td></tr><tr><td>

SaveFolderpath

</td><td>

Folder path to save the file.

</td><td>

Yes

</td></tr><tr><td>

SearchColumn

</td><td>

Column name in a Microsoft Excel worksheet where to search the specified text.

</td><td>

Yes

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the name of the active or selected sheet.

</td><td>

Not applicable

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet that will be deleted.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where data will be exported.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

The name of the sheet where the data will be filled.

</td><td>

Yes

</td></tr><tr><td>

SearchText

</td><td>

Text to search in a Microsoft Excel worksheet.

</td><td>

Yes

</td></tr><tr><td>

saveChanges

</td><td>

Boolean values to indicate whether the changes will be saved while closing.-   **True**: The method requests inputs on whether to save changes.
-   **False**: The method closes the file and unsaved changes, if any, are lost.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

Name of the worksheet added to the file.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet where the formula will be applied.

</td><td>

 

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where the column will be deleted.

</td><td>

Yes

</td></tr><tr><td>

SortingOrder

</td><td>

Sorting order—ascending or descending—set on a column.

</td><td>

 

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where the row will be deleted.

</td><td>

Yes

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet from where the cell data will be deleted.

</td><td>

Yes

</td></tr><tr><td>

StartRowIndex

</td><td>

First row number in a set of rows in a Microsoft Excel worksheet for a bulk operation, such as to search, set values, get values.

</td><td>

Yes

</td></tr><tr><td>

Sheetname

</td><td>

Name of the sheet from where the cells will be copied.

</td><td>

Yes

</td></tr><tr><td>

Return

</td><td>

Returns the integer value of the number of columns counted.

</td><td>

Not applicable

</td></tr><tr><td>

SheetName

</td><td>

Name of the sheet on which the column count will be performed.

</td><td>

Yes

</td></tr><tr><td>

Value

</td><td>

Value to be set on a cell.

</td><td>

Yes

</td></tr><tr><td>

VerticalAlignment

</td><td>

Vertical alignment formatting of the specified cells.Example: Top, Middle, Bottom

</td><td>

No

</td></tr><tr><td>

Width

</td><td>

Width of a column in a Microsoft Excel.

</td><td>

Yes

</td></tr><tr><td>

Password

</td><td>

Option to make the Excel file password-protected. Provide the password in string format.

</td><td>

No

</td></tr></tbody>
</table>## Enter inputs for parameters

To enter inputs for the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

**Parent Topic:**[Microsoft Excel](../concept/microsoft-excel-connector.md)

