---
title: Parameters of the Microsoft Word connector methods
description: Learn about the parameters of the Microsoft Word connector methods in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsoft Word, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Parameters of the Microsoft Word connector methods

Learn about the parameters of the Microsoft Word connector methods in RPA Desktop Design Studio.

<table id="table_rfq_qpm_3rb"><thead><tr><th>

Parameter Name

</th><th>

Description

</th><th>

Mandatory?

</th></tr></thead><tbody><tr><td>

Bookmark

</td><td>

Bookmark in a Microsoft Word document.

</td><td>

Yes

</td></tr><tr><td>

CellIndex

</td><td>

Index of a cell in a table.

</td><td>

Yes

</td></tr><tr><td>

ColumnIndex

</td><td>

Column sequence in a table.

</td><td>

Yes.The column index must be equal to or greater than zero.

</td></tr><tr><td>

Data

</td><td>

Table that contains data to add into a Microsoft Word document.

</td><td>

Yes

</td></tr><tr><td>

Filepath

</td><td>

Folder location including the name of the document.

</td><td>

Yes

</td></tr><tr><td>

EndCellIndex

</td><td>

Last cell number of a range.

</td><td>

Yes

</td></tr><tr><td>

ImageFilePath

</td><td>

The path to the image with the filename that you want to insert.

</td><td>

Yes

</td></tr><tr><td>

Filepath

</td><td>

location where the document will be exported as a PDF.

</td><td>

Yes.You must provide the filename and the PDF extension.

</td></tr><tr><td>

Bookmark

</td><td>

Exact location on the Word document where the image will be inserted. You must define a bookmark in the document first.

</td><td>

Yes

</td></tr><tr><td>

FilePath

</td><td>

Path to the Microsoft Word file including the filename.

</td><td>

Yes

</td></tr><tr><td>

EndColIndex

</td><td>

Last column number of a range for a bulk operation on a table, such as merging cells, searching text, and setting or getting values.

</td><td>

Yes

</td></tr><tr><td>

EndRowIndex

</td><td>

Last row number of a range for a bulk operation on a table, such as merging cells, searching text, and setting or getting values.

</td><td>

Yes

</td></tr><tr><td>

FirstRowIsHeader

</td><td>

Boolean value to indicate whether the method should treat the first row as a header of the table.

</td><td>

No

</td></tr><tr><td>

PageIndex

</td><td>

Page index value.

</td><td>

No.

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to indicate whether the request was successful.

</td><td>

Not applicable

</td></tr><tr><td>

Timeout

</td><td>

Seconds after which the request to open the document will time out if no response is received.

</td><td>

No

</td></tr><tr><td>

StartCellIndex

</td><td>

First cell number of a range.

</td><td>

Yes

</td></tr><tr><td>

StartColIndex

</td><td>

First column number of a range for a bulk operation on a table, such as merging cells, searching text, and setting or getting values.

</td><td>

Yes

</td></tr><tr><td>

StartRowIndex

</td><td>

First row number of a range for a bulk operation on a table, such as merging cells, searching text, and setting or getting values.

</td><td>

Yes

</td></tr><tr><td>

RowIndex

</td><td>

Row sequence in a table in the document.

</td><td>

Yes.The row index value must be equal or greater than zero.

</td></tr><tr><td>

Table

</td><td>

The table data.

</td><td>

Yes

</td></tr><tr><td>

TableIndex

</td><td>

Index of a table in a Microsoft Word document.

</td><td>

No

</td></tr><tr><td>

Text Or, FindText

 Or, ReplaceText

</td><td>

Text to be added in a Microsoft Word document in the AddFooter, AddHeader, or InsertText methods.Text to be searched in the document in the Find method.

 Text to be replaced within the ReplaceBookmark, ReplaceFooterText, ReplaceHeaderText, or ReplaceText methods.

</td><td>

Yes

</td></tr><tr><td>

Value

</td><td>

Value in a cell.

</td><td>

Yes

</td></tr><tr><td>

Text

</td><td>

Text to be added to the footer.

</td><td>

Yes

</td></tr><tr><td>

FontSize

</td><td>

Font size of the footer text.

</td><td>

No

</td></tr><tr><td>

Text

</td><td>

Custom text to be added to the header.

</td><td>

Yes

</td></tr><tr><td>

FontSize

</td><td>

Font size of the header text.

</td><td>

Yes

</td></tr><tr><td>

Text

</td><td>

Text to find in the document.

</td><td>

Yes

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the footer text.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Integer\)

</td><td>

Returns the number of pages.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the header text.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(String\)

</td><td>

Returns the text content.

</td><td>

Not applicable

</td></tr><tr><td>

Text

</td><td>

Text that is inserted in the Word document.

</td><td>

Yes

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Returns the Boolean value to indicate whether a Word document is open.

</td><td>

Not applicable

</td></tr><tr><td>

saveChanges

</td><td>

Boolean response to indicate whether you want to save the changes before closing the document.

</td><td>

No

</td></tr><tr><td>

Return \(Boolean\)

</td><td>

Boolean response to whether the text was found in the document.

</td><td>

Not applicable

</td></tr><tr><td>

Table \(Object\)

</td><td>

Returns the data in a table as an object.

</td><td>

Not applicable

</td></tr><tr><td>

Data \(DataTable\)

</td><td>

Returns the data in the table.

</td><td>

Not applicable

</td></tr><tr><td>

Cell Index \(Object\)

</td><td>

Returns the value of the cell.

</td><td>

Not applicable

</td></tr><tr><td>

Return \(Integer\)

</td><td>

Returns the total count of tables in the Microsoft Word document.

</td><td>

Not applicable

</td></tr><tr><td>

Row index \(Object\)

</td><td>

Returns the data in the cell based on the index value.

</td><td>

Not applicable

</td></tr><tr><td>

ColumnIndex

</td><td>

The index value of the column based on which the position of the new column is determined.

</td><td>

No.

</td></tr><tr><td>

RowIndex

</td><td>

Index value of the row based on which the position of the row is determined.

</td><td>

No

</td></tr><tr><td>

Bookmark

</td><td>

Specific position in the Word document where the table will be inserted.Before inserting the table, you must add a bookmark.

</td><td>

Yes

</td></tr><tr><td>

Data \(DataTable\)

</td><td>

Table that will be inserted.

</td><td>

Yes

</td></tr><tr><td>

FindText

</td><td>

Footer text that will be replaced.

</td><td>

Yes

</td></tr><tr><td>

ReplaceText

</td><td>

Text that will replace the footer text.

</td><td>

Yes

</td></tr><tr><td>

FindText

</td><td>

Header text that will be replaced.

</td><td>

Yes

</td></tr><tr><td>

ReplaceText

</td><td>

Text that will replace the header text.

</td><td>

Yes

</td></tr><tr><td>

Object

</td><td>

Text to replace the text in the document.

</td><td>

Yes

</td></tr><tr><td>

FindText \(String\)

</td><td>

Text to be replaced.

</td><td>

Yes

</td></tr><tr><td>

ReplaceText

</td><td>

Text that will replace the existing text.

</td><td>

Yes

</td></tr><tr><td>

Left

</td><td>

Resize value from the left margin.

</td><td>

Yes

</td></tr><tr><td>

Top

</td><td>

Resize value from the top margin.

</td><td>

Yes

</td></tr><tr><td>

Width

</td><td>

Resize width value.

</td><td>

Yes

</td></tr><tr><td>

Height

</td><td>

Resize height value.

</td><td>

Yes

</td></tr></tbody>
</table>## Enter inputs for parameters

To enter inputs for the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

**Parent Topic:**[Microsoft Word](../concept/microsoft-word-connector.md)

