---
title: Table - Scoped, Global
description: Creates a Table object to add to a PDF document. Defines the data to use in each cell and sets styles, margins, and alignment.Instantiates a new Table object with text direction, column width, and layout settings.Adds a cell element to the table.Adds a cell element with an applied style to the table.Adds a header Cell object to the table.Adds a cell that contains an image to the table.Adds a cell that contains a paragraph to the table.Adds a cell that contains a string to the table.Indicates that all the intended content has been added to a large table.Prevents splitting a row across two pages, when possible.Adds additional content to a table that is already added to a document.Returns the default style.Returns the style applied to the table's header.Sets a border of designated width around the outer edges of the table.Sets the table's default background color.Sets the default style to apply to the table.Sets the table to a fixed position on the page.Sets the Style object to apply to the table's header.Sets the horizontal alignment of the table.Sets all margins around the table to the same width.Sets the margin at the bottom of the page.Sets the margin at the left side of the page.Sets the margin at the right side of the page.Sets a margin at the top of the page.Sets the table's total width.Expands the table to use the entire width available on the page.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 18
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Table - Scoped, Global

Creates a Table object to add to a PDF document. Defines the data to use in each cell and sets styles, margins, and alignment.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

Build a Table object using the methods in this class. You can use these additional classes to add cells, paragraphs, and styles to your table:

-   **[Cell API](../../CellBoth/concept/CellBothAPI.md#)**

    Create a cell using the Cell API. Then, add the cell to your table using one of these methods:

    -   Table.addCell\(\)
    -   Table.addCellWithStyle\(\)
    -   Table.addHeaderCell\(\)
    -   Table.addImageCell\(\)
    -   Table.addParagraphCell\(\)
    -   Table.addTextCell\(\)
-   **[Paragraph API](../../ParagraphBoth/concept/ParagraphBothAPI.md#)**

    Create a paragraph using the Paragraph API. Add the paragraph to a cell in the table using Cell.addParagraph\(\).

-   **[Style API](../../StyleBoth/concept/StyleBothAPI.md#)**

    Set styles, colors, and borders using the Style API. Add the styles to the table using one of these methods:

    -   Table.setDefaultStyle\(\)
    -   Table.setHeaderStyle\(\)

You can then apply the Table object to a PDF document using the following class and method.

-   **[Document API](../../DocumentBoth/concept/DocumentBothAPI.md#)**

    Use the Document.addTable\(\) method to add your table to a PDF document. You can use the Document.saveAsAttachment\(\) method to attach the document to a record.


**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Table - Table\(Boolean ltr, Array columnWidths, Boolean largeTable\)

Instantiates a new Table object with text direction, column width, and layout settings.

<table id="table_twm_hjk_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ltr

</td><td>

Boolean

</td><td>

Flag that indicates text direction of the language in the table. For information, see [W3C: Script direction and languages](https://www.w3.org/International/questions/qa-scripts.en).

 Valid values:

-   true: Text direction is left-to-right.
-   false: Text direction is right-to-left.

</td></tr><tr><td>

columnWidths

</td><td>

Array

</td><td>

Numbers specifying the width of each column in a table. Sizes are based proportionally. For example, `var columnWidths = [2, 1, 1];` is a three-column table with a first column twice as large as the other two.Default: Each column is equal width.

</td></tr><tr><td>

largeTable

</td><td>

Boolean

</td><td>

Flag that indicates whether 100% width and fixed layout are set implicitly.Valid values:

-   true: Table uses 100% width with a fixed layout. If true, use the complete\(\) method when all content has been added to indicate that the table is complete.
-   false: Automatic table size.

 Default: false

</td></tr></tbody>
</table>The following example shows how to create a 2-column Table object.

```
var table = new sn_pdfgeneratorutils.Table(true, [70,200], false);
```

## Table – addCell\(Cell cell\)

Adds a cell element to the table.

|Name|Type|Description|
|----|----|-----------|
|cell|[Cell](../../CellBoth/concept/CellBothAPI.md#)|Cell element to add to the table.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to create a Table object from the incident table and add a Number and a Short Description cell to each row.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query Incident
var gr = new GlideRecord("incident");
gr.query();
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [70,200], false);
 
var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);
 
var nParagraph = new sn_pdfgeneratorutils.Paragraph("Number");
var sParagraph = new sn_pdfgeneratorutils.Paragraph("Short Description");
 
var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
 
hdrCell1.addParagraph(nParagraph);
hdrCell2.addParagraph(sParagraph);
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);
 
var row = 0;
 
while(gr.next()) {
   var numCell = new sn_pdfgeneratorutils.Cell;
   var sdCell = new sn_pdfgeneratorutils.Cell;
 
   var numberParagraph = new sn_pdfgeneratorutils.Paragraph(gr.number);
   var sdParagraph = new sn_pdfgeneratorutils.Paragraph(gr.short_description);
  
   numCell.addParagraph(numberParagraph);
   sdCell.addParagraph(sdParagraph);
 
   if (row % 2 == 1) {
      table.setDefaultbackGroundColor(greyColor);
   } else {
      table.setDefaultbackGroundColor(whiteColor);
   }
 
   table.addCell(numCell);
   table.addCell(sdCell);
 
   row = row + 1;
 
}
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – addCellWithStyle\(Cell cell, Style style\)

Adds a cell element with an applied style to the table.

|Name|Type|Description|
|----|----|-----------|
|cell|[Cell](../../CellBoth/concept/CellBothAPI.md#)|Cell object to add to the table.|
|style|[Style](../../StyleBoth/concept/StyleBothAPI.md#)|Style to apply to the cell.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to apply a style to a specified Cell object and save the document as an attachment to a record.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var cellBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query Incident
var gr = new GlideRecord("incident");
gr.query();
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [70,200], false);
 
var cellStyle = new sn_pdfgeneratorutils.Style;
cellStyle.setBackgroundColor(cellBgColor);
cellStyle.setTextAlignment("text-center");
cellStyle.setBold();
cellStyle.setFontColor(whiteColor);
 
var nParagraph = new sn_pdfgeneratorutils.Paragraph("Number");
var sParagraph = new sn_pdfgeneratorutils.Paragraph("Short Description");
 
var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
 
hdrCell1.addParagraph(nParagraph);
hdrCell2.addParagraph(sParagraph);
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);
 
var row = 0;
 
while(gr.next()) {
   var numCell = new sn_pdfgeneratorutils.Cell;
   var sdCell = new sn_pdfgeneratorutils.Cell;
 
   var numberParagraph = new sn_pdfgeneratorutils.Paragraph(gr.number);
   var sdParagraph = new sn_pdfgeneratorutils.Paragraph(gr.short_description);
  
   numCell.addParagraph(numberParagraph);
   sdCell.addParagraph(sdParagraph);
 
   if (row % 2 == 1) {
      table.setDefaultbackGroundColor(greyColor);
   } else {
      table.setDefaultbackGroundColor(whiteColor);
   }
 
   table.addCellWithStyle(numCell, cellStyle);
   table.addCell(sdCell);
 
   row = row + 1;
 
}
 
document.addTable(table);
document.saveAsAttachment("incident", "sys_id", "filename.pdf");
```

## Table – addHeaderCell\(Cell cell\)

Adds a header Cell object to the table.

|Name|Type|Description|
|----|----|-----------|
|cell|[Cell](../../CellBoth/concept/CellBothAPI.md#)|Header cell to add to the table.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to add a header cell to a table that contains a Paragraph object. For more information on Paragraph objects, see the [Paragraph API](../../ParagraphBoth/concept/ParagraphBothAPI.md#).

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query Incident
var gr = new GlideRecord("incident");
gr.query();
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [70,200], false);
 
var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);
 
var nParagraph = new sn_pdfgeneratorutils.Paragraph("Number");
var sParagraph = new sn_pdfgeneratorutils.Paragraph("Short Description");
 
var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
 
hdrCell1.addParagraph(nParagraph);
hdrCell2.addParagraph(sParagraph);
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);
 
var row = 0;
 
while(gr.next()) {
   var numCell = new sn_pdfgeneratorutils.Cell;
   var sdCell = new sn_pdfgeneratorutils.Cell;
 
   var numberParagraph = new sn_pdfgeneratorutils.Paragraph(gr.number);
   var sdParagraph = new sn_pdfgeneratorutils.Paragraph(gr.short_description);
  
   numCell.addParagraph(numberParagraph);
   sdCell.addParagraph(sdParagraph);
 
   if (row % 2 == 1) {
      table.setDefaultbackGroundColor(greyColor);
   } else {
      table.setDefaultbackGroundColor(whiteColor);
   }
 
   table.addCell(numCell);
   table.addCell(sdCell);
 
   row = row + 1;
 
}
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – addImageCell\(Image image\)

Adds a cell that contains an image to the table.

|Name|Type|Description|
|----|----|-----------|
|image|[Image](../../ImageBoth/concept/ImageBothAPI.md#)|Image object to add to the cell.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to create a table with two image cells and attach the document to a record.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [70,200], false);
 
var icon = new sn_pdfgeneratorutils.Image("<sys_id>");
var picture = new sn_pdfgeneratorutils.Image("<sys_id>");
 
table.addImageCell(icon);
table.addImageCell(picture);
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – addParagraphCell\(Paragraph p\)

Adds a cell that contains a paragraph to the table.

|Name|Type|Description|
|----|----|-----------|
|p|[Paragraph](../../ParagraphBoth/concept/ParagraphBothAPI.md#)|Paragraph object to add to the cell.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to create a table with a single cell containing paragraph content.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
var paragraph = new sn_pdfgeneratorutils.Paragraph("Content to add to the cell");
 
table.addParagraphCell(paragraph);
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – addTextCell\(String text\)

Adds a cell that contains a string to the table.

|Name|Type|Description|
|----|----|-----------|
|text|String|Text to add to the cell.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to create a table with a single cell containing a string.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
 
document.addTable(table);
document.saveAsAttachment("incident", "record_sys_id", "filename.pdf");
```

## Table – complete\(\)

Indicates that all the intended content has been added to a large table.

Use with the Table.flush\(\) method to add additional content to a table already added to a document. This method only applies when the **largeTable** parameter in the constructor is set to true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example shows how to indicate adding content to a table already added to a document is complete.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query Incident
var gr = new GlideRecord("incident");
gr.query();
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1,2,1,1], true);
 
var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);
 
var numberParagraph = new sn_pdfgeneratorutils.Paragraph("Number");
var descParagraph = new sn_pdfgeneratorutils.Paragraph("Short Description");
var stateParagraph = new sn_pdfgeneratorutils.Paragraph("State");
var assignedParagraph = new sn_pdfgeneratorutils.Paragraph("Assigned to");

 
var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
var hdrCell3 = new sn_pdfgeneratorutils.Cell;
var hdrCell4 = new sn_pdfgeneratorutils.Cell;
 
hdrCell1.addParagraph(numberParagraph);
hdrCell2.addParagraph(descParagraph);
hdrCell3.addParagraph(stateParagraph);
hdrCell4.addParagraph(assignedParagraph);
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);
table.addHeaderCell(hdrCell3);
table.addHeaderCell(hdrCell4);

var row = 0;
 
while(gr.next()) {
   var numCell = new sn_pdfgeneratorutils.Cell;
   var sdCell = new sn_pdfgeneratorutils.Cell;
   var stateCell = new sn_pdfgeneratorutils.Cell;
   var assignedCell = new sn_pdfgeneratorutils.Cell;

 
   var numberParagraph = new sn_pdfgeneratorutils.Paragraph(gr.number);
   var sdParagraph = new sn_pdfgeneratorutils.Paragraph(gr.short_description);
   var stateParagraph = new sn_pdfgeneratorutils.Paragraph(gr.state);
   var assignedParagraph = new sn_pdfgeneratorutils.Paragraph(gr.assigned_to);
  
   numCell.addParagraph(numberParagraph);
   sdCell.addParagraph(sdParagraph);
   stateCell.addParagraph(stateParagraph);
   assignedCell.addParagraph(assignedParagraph);

 
   if (row % 2 == 1) {
      table.setDefaultbackGroundColor(greyColor);
   } else {
      table.setDefaultbackGroundColor(whiteColor);
   }
 
   table.addCell(numCell);
   table.addCell(sdCell);
   table.addCell(stateCell);
   table.addCell(assignedCell);
 
   row = row + 1;
 
}

document.addTable(table);
table.addTextCell("A cell added later");
table.flush();
table.complete();
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – donotSplitRowOnPageBreak\(Boolean value\)

Prevents splitting a row across two pages, when possible.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

value

</td><td>

Boolean

</td><td>

Flag that indicates whether to split a row across two pages, or move the entire row onto the second page. However, this property does not apply when the row spans more than a single page.Valid values:

-   true: If the remaining part of a page is not large enough for the row, adds the entire row to a new page.
-   false: If the remaining part of a page is not large enough for the row, splits the row across two pages.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to prevent splitting a row across two pages.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [25,25,25,75,400], false);
 
table.addTextCell("Text to add to the cell");
table.addTextCell("More text to add to the cell");
table.addTextCell("Even more text to add to the cell");
table.addTextCell("Even more text to add to the cell");
table.addTextCell("Even more text to add to the cell");

table.donotSplitRowOnPageBreak(true);
 
document.addTable(table);
document.saveAsAttachment("incident", "record_sys_id", "filename.pdf");
```

## Table – flush\(\)

Adds additional content to a table that is already added to a document.

Use with the Table.complete\(\) method to indicate that you have added all additional content to the table. This method only applies when the **largeTable** parameter in the constructor is set to true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example shows how to add a text cell to a table that is already added to a document.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query Incident
var gr = new GlideRecord("incident");
gr.query();
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1,2,1,1], true);
 
var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);
 
var numberParagraph = new sn_pdfgeneratorutils.Paragraph("Number");
var descParagraph = new sn_pdfgeneratorutils.Paragraph("Short Description");
var stateParagraph = new sn_pdfgeneratorutils.Paragraph("State");
var assignedParagraph = new sn_pdfgeneratorutils.Paragraph("Assigned to");

 
var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
var hdrCell3 = new sn_pdfgeneratorutils.Cell;
var hdrCell4 = new sn_pdfgeneratorutils.Cell;
 
hdrCell1.addParagraph(numberParagraph);
hdrCell2.addParagraph(descParagraph);
hdrCell3.addParagraph(stateParagraph);
hdrCell4.addParagraph(assignedParagraph);
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);
table.addHeaderCell(hdrCell3);
table.addHeaderCell(hdrCell4);

var row = 0;
 
while(gr.next()) {
   var numCell = new sn_pdfgeneratorutils.Cell;
   var sdCell = new sn_pdfgeneratorutils.Cell;
   var stateCell = new sn_pdfgeneratorutils.Cell;
   var assignedCell = new sn_pdfgeneratorutils.Cell;

 
   var numberParagraph = new sn_pdfgeneratorutils.Paragraph(gr.number);
   var sdParagraph = new sn_pdfgeneratorutils.Paragraph(gr.short_description);
   var stateParagraph = new sn_pdfgeneratorutils.Paragraph(gr.state);
   var assignedParagraph = new sn_pdfgeneratorutils.Paragraph(gr.assigned_to);
  
   numCell.addParagraph(numberParagraph);
   sdCell.addParagraph(sdParagraph);
   stateCell.addParagraph(stateParagraph);
   assignedCell.addParagraph(assignedParagraph);

 
   if (row % 2 == 1) {
      table.setDefaultbackGroundColor(greyColor);
   } else {
      table.setDefaultbackGroundColor(whiteColor);
   }
 
   table.addCell(numCell);
   table.addCell(sdCell);
   table.addCell(stateCell);
   table.addCell(assignedCell);
 
   row = row + 1;
 
}

document.addTable(table);
table.addTextCell("A cell added later");
table.flush();
table.complete();
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – getDefaultStyle\(\)

Returns the default style.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Style|Default style.|

This example shows how to set and then return the default style.

```
var table = new sn_pdfgeneratorutils.Table(true, [1], false);

var style = new sn_pdfgeneratorutils.Style();

style.setItalic();

table.setDefaultStyle(style);
 
table.addTextCell("Text to add to the cell");

var defaultStyle = table.getDefaultStyle();

gs.info(defaultStyle);
```

## Table – getHeaderStyle\(\)

Returns the style applied to the table's header.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Style|Style applied to the table's header.|

This example shows how to set and return the table's header style.

```
var table = new sn_pdfgeneratorutils.Table(true, [1,1], false);

var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);

var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);

var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);

var styleObject = table.getHeaderStyle();

gs.info(styleObject);
```

## Table – setBorder\(Number width\)

Sets a border of designated width around the outer edges of the table.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

width

</td><td>

Number

</td><td>

Width of the border. Unit: Points

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to create a table with two-pixel border and attach the table to a record.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setBorder(2);
 
document.addTable(table);
"document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setDefaultbackGroundColor\(Color color\)

Sets the table's default background color.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Color object used as the default background color for the table.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set the default background color for the table.

```
// declare table by providing width array with automatic table size
var table = new sn_pdfgeneratorutils.Table(true, [1], false);

var color = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);

table.setDefaultbackGroundColor(color);
 
table.addTextCell("Text to add to the cell");
```

## Table – setDefaultStyle\(Style defaultStyle\)

Sets the default style to apply to the table.

|Name|Type|Description|
|----|----|-----------|
|defaultStyle|Style|Default style to apply to the table.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to apply a default style to a table.

```
var table = new sn_pdfgeneratorutils.Table(true, [1], false);

var style = new sn_pdfgeneratorutils.Style();

style.setItalic();

table.setDefaultStyle(style);
 
table.addTextCell("Text to add to the cell");

var defaultStyle = table.getDefaultStyle();

gs.info(defaultStyle);
```

## Table – setFixedPosition\(Number pageNumber, Number left, Number bottom, Number width\)

Sets the table to a fixed position on the page.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pageNumber

</td><td>

Number

</td><td>

Number of the page to add the table to.

</td></tr><tr><td>

left

</td><td>

Number

</td><td>

Number of pixels from the left margin to add the table. Unit: Points

</td></tr><tr><td>

bottom

</td><td>

Number

</td><td>

Number of pixels from the bottom margin to add the table. Unit: Points

</td></tr><tr><td>

width

</td><td>

Number

</td><td>

Width of the table. Unit: Points

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to reposition the table into the bottom left corner of the page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setFixedPosition(1,36,36,500);
 
document.addTable(table);
"document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setHeaderStyle\(Style headerStyle\)

Sets the Style object to apply to the table's header.

|Name|Type|Description|
|----|----|-----------|
|headerStyle|[Style](../../StyleBoth/concept/StyleBothAPI.md#)|Style object to apply to the table's header.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set and return the table's header style.

```
var table = new sn_pdfgeneratorutils.Table(true, [1,1], false);

var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);

var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);

var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);

var styleObject = table.getHeaderStyle();

gs.info(styleObject);
```

## Table – setHorizontalAlignment\(String alignment\)

Sets the horizontal alignment of the table.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alignment

</td><td>

String

</td><td>

Alignment for the table. Valid values:

-   center: Align contents to the center.
-   left: Align contents to the left.
-   right: Align contents to the right.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to create a small table aligned in the center of the page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setWidth(90);
table.setHorizontalAlignment("center");
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setMargin\(Number margin\)

Sets all margins around the table to the same width.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Value of the top, right, bottom, and left margins in points.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set a margin for the entire table.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setMargin(3);
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setMarginBottom\(Number margin\)

Sets the margin at the bottom of the page.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Height of the bottom margin in points.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set a margin for the bottom of the page to three points.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query Incident
var gr = new GlideRecord("incident");
gr.query();
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [70,200], false);
 
var headerStyle = new sn_pdfgeneratorutils.Style;
headerStyle.setBackgroundColor(headerBgColor);
headerStyle.setTextAlignment("text-center");
headerStyle.setBold();
headerStyle.setFontColor(whiteColor);
 
table.setHeaderStyle(headerStyle);
 
var nParagraph = new sn_pdfgeneratorutils.Paragraph("Number");
var sParagraph = new sn_pdfgeneratorutils.Paragraph("Short Description");
 
var hdrCell1 = new sn_pdfgeneratorutils.Cell;
var hdrCell2 = new sn_pdfgeneratorutils.Cell;
 
hdrCell1.addParagraph(nParagraph);
hdrCell2.addParagraph(sParagraph);
 
table.addHeaderCell(hdrCell1);
table.addHeaderCell(hdrCell2);

// set the bottom margin to three points
table.setBottomMargin(3);
 
var row = 0;
 
while(gr.next()) {
   var numCell = new sn_pdfgeneratorutils.Cell;
   var sdCell = new sn_pdfgeneratorutils.Cell;
 
   var numberParagraph = new sn_pdfgeneratorutils.Paragraph(gr.number);
   var sdParagraph = new sn_pdfgeneratorutils.Paragraph(gr.short_description);
  
   numCell.addParagraph(numberParagraph);
   sdCell.addParagraph(sdParagraph);
 
   if (row % 2 == 1) {
      table.setDefaultbackGroundColor(greyColor);
   } else {
      table.setDefaultbackGroundColor(whiteColor);
   }
 
   table.addCell(numCell);
   table.addCell(sdCell);
 
   row = row + 1;
 
}
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setMarginLeft\(Number margin\)

Sets the margin at the left side of the page.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Width of the left margin in points.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set a margin for the left side of the page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setMarginLeft(100);
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setMarginRight\(Number margin\)

Sets the margin at the right side of the page.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Width of the right margin in points.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set a margin for the left side of the page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setMarginRight(100);
 
document.addTable(table);
"document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setMarginTop\(Number margin\)

Sets a margin at the top of the page.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Height of the top margin in points.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set a margin at the top of the page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setMarginTop(100);
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – setWidth\(Number width\)

Sets the table's total width.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

width

</td><td>

Number

</td><td>

Width of the table.Unit: Points

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to create a table 90 points wide and attach the document to a record.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.setWidth(90);
table.setHorizontalAlignment("center");
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Table – useAllAvailableWidth\(\)

Expands the table to use the entire width available on the page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

This example shows how to create a table that expands to the available width on the page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare table by providing width array and Boolean for large table
var table = new sn_pdfgeneratorutils.Table(true, [1], false);
 
table.addTextCell("Text to add to the cell");
table.useAllAvailableWidth();
 
document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

