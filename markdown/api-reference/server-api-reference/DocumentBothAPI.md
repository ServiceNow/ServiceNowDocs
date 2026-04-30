---
title: Document - Scoped, Global
description: The Document API provides methods to initialize a PDF, add content, and close the PDF. After adding content, the document can be attached to a target record.Instantiates a Document object and generates a PDF document.Adds a page to the document by terminating the current page and creating a new one.Adds a name to the author field in PDF document properties.Adds an image to a document.Adds a new empty line to the document.Adds a new blank page to the document. Use to force a page break to start a new chapter or section in your document.Adds a new page at the specified index of the document. For example, setting the index to 6 inserts a page six or inserts the page at the position of the existing page six in a document. The original page six becomes page seven.Adds a paragraph to a document.Adds a table to a document.Closes a document.Creates a document with the specified page size.Gets the number of pages in the document.Gets the default page size of the document.Indicates whether a document is closed or open.Attaches the document file to the specified target table.Sets the base text flow direction to reorder from based on character recognitionSets the page margin sizes in the document.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 14
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Document - Scoped, Global

The Document API provides methods to initialize a PDF, add content, and close the PDF. After adding content, the document can be attached to a target record.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API depends on the a suite of classes to build various elements comprising a PDF.

-   [Cell](../../CellBoth/concept/CellBothAPI.md#) – Creates a Cell object as a cell in a table. You can use this API to format the cell and include additional blocks, such as paragraphs and images.
-   [Color](../../ColorBoth/concept/ColorBothAPI.md#) – Creates a Color object used to define color attributes that you can apply to elements in a PDF; such as cells, tables, and lines.
-   [Image](../../ImageBoth/concept/ImageBothAPI.md#) – Creates an Image object representing an image and its layout insert in a PDF. Enables defining attributes such as scale, alignment, and border color.
-   [Line](../../LineBoth/concept/LineBothAPI.md#) – Creates a Line object using methods to draw a line in a PDF.
-   [Paragraph](../../ParagraphBoth/concept/ParagraphBothAPI.md#) – Creates a Paragraph object representing a block of text in a PDF.
-   [PdfPage](../../PdfPageBoth/concept/PdfPageBothAPI.md#) – Creates a PdfPage object representing a PDF page and its attributes; such as size, width, and color.
-   [Style](../../StyleBoth/concept/StyleBothAPI.md#) – Creates a style for defining properties such font size, border, and alignment. You can apply the same style to multiple objects simultaneously.
-   [Table](../../TableBoth/concept/TableBothAPI.md#) – Creates a Table object to add to a PDF document. Defines the data to use in each cell and sets styles, margins, and alignment.

The following example shows how to create a basic PDF using the Document API and several components, such as a table, cell, and paragraph. The result is a list of Incidents from the Incident \[incident\] table listed in a PDF. You can test this example in your instance if you replace `<sys_id>` with the sys\_id of an incident record.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var whiteColor =  sn_pdfgeneratorutils.Color([1,1,1]);
var greyColor =  sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var headerBgColor = new sn_pdfgeneratorutils.Color([0.4,0.6,0.8]);
 
// Query the Incident table
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
document.saveAsAttachment("incident", "<sys_id>", "SampleGenerationTest.pdf");
```

The PDF attachment is listed in the Attachments \[sys\_attachment\] table.

![Example PDF with output as 2-column table listing incident numbers and descriptions.](../image/document-api-pdf-output.png)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Document - Document\(PdfPage pageSize\)

Instantiates a Document object and generates a PDF document.

|Name|Type|Description|
|----|----|-----------|
|pageSize|[PdfPage](../../PdfPageBoth/concept/PdfPageBothAPI.md#)|PDF page size.|

|Type|Description|
|----|-----------|
|Object|PDF document.|

The following example shows how to create a Document object and return a PDF.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document(pageSize);
```

## Document – addAndStartNewPage\(\)

Adds a page to the document by terminating the current page and creating a new one.

Additional methods for adding a new page in a document:

-   [addNewPage\(\)](DocumentBothAPI.md#) – Adds a new blank page to the document. Use to force a page break to start a new chapter or section in your document.
-   [addNewPageAtIndex\(\)](DocumentBothAPI.md#) – Adds a new page at the specified index of the document. For example, setting the index to 6 inserts a page six or inserts the page at the position of the existing page six in a document. The original page six becomes page seven.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a new page to a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var para1 = new sn_pdfgeneratorutils.Paragraph("This text lands on the first page.");
var para2 = new sn_pdfgeneratorutils.Paragraph("This text lands on the new page.");

document.addParagraph(para1);

document.addAndStartNewPage();

document.addParagraph(para2);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "newPage.pdf");
```

## Document – addAuthor\(String author\)

Adds a name to the author field in PDF document properties.

|Name|Type|Description|
|----|----|-----------|
|author|String|Name of the document's author.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a name to the author field in PDF document properties. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var author = "John Do";

document.addAuthor(author);
```

## Document – addImage\(Image image\)

Adds an image to a document.

|Name|Type|Description|
|----|----|-----------|
|image|[Image](../../ImageBoth/concept/ImageBothAPI.md#)|Image to add to a document.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add an image to a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare image using sys attachment
var image = new sn_pdfgeneratorutils.Image("<imgAttachment_sys_id>");

// add the image to the doc
document.addImage(image);

document.saveAsAttachment("incident", "<record_sys_id>", "docWithImage.pdf");
```

## Document – addNewLine\(\)

Adds a new empty line to the document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a new line to a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");

var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

document.addNewLine();
```

## Document – addNewPage\(\)

Adds a new blank page to the document. Use to force a page break to start a new chapter or section in your document.

Additional methods for adding a new page in a document:

-   [addAndStartNewPage\(\)](DocumentBothAPI.md#)– Adds a page to the document by terminating the current page and creating a new one.
-   [addNewPageAtIndex\(\)](DocumentBothAPI.md#) – Adds a new page at the specified index of the document. For example, setting the index to 6 inserts a page six or inserts the page at the position of the existing page six in a document. The original page six becomes page seven.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a new blank page to a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
Usage:
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

document.addNewPage();
```

## Document – addNewPageAtIndex\(Number index\)

Adds a new page at the specified index of the document. For example, setting the index to 6 inserts a page six or inserts the page at the position of the existing page six in a document. The original page six becomes page seven.

Additional methods for adding a new page in a document:

-   [addAndStartNewPage\(\)](DocumentBothAPI.md#)– Adds a page to the document by terminating the current page and creating a new one.
-   [addNewPage\(\)](DocumentBothAPI.md#) – Adds a new blank page to the document. Use to force a page break to start a new chapter or section in your document.

|Name|Type|Description|
|----|----|-----------|
|index|Number|Position at which to insert a new page.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a new PDF page to position 6 of a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");

var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var index = 6;

document.addNewPageAtIndex(index);
```

## Document – addParagraph\(Paragraph paragraph\)

Adds a paragraph to a document.

|Name|Type|Description|
|----|----|-----------|
|paragraph|[Paragraph](../../ParagraphBoth/concept/ParagraphBothAPI.md#)|Block of text provided as a paragraph object.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a paragraph to a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var para = "Lorem ipsum dolor sit amet.";

document.addParagraph(para);
```

## Document – addTable\(Table table\)

Adds a table to a document.

|Name|Type|Description|
|----|----|-----------|
|table|[Table](../../TableBoth/concept/TableBothAPI.md#)|Table to be inserted into the document.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a table to a document. See the [Table API](../../TableBoth/concept/TableBothAPI.md#) for more details on how to define a table. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var table = new sn_pdfgeneratorutils.Table([70,200], false);

document.addTable(table);
```

## Document – close\(\)

Closes a document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to close a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

document.close();
```

## Document – createDocument\(PdfPage pageSize\)

Creates a document with the specified page size.

|Name|Type|Description|
|----|----|-----------|
|pageSize|[PdfPage](../../PdfPageBoth/concept/PdfPageBothAPI.md#)|Document page size.|

|Type|Description|
|----|-----------|
|Object|PDF document.|

The following example shows how to create a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");

var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
```

## Document – getPageCount\(\)

Gets the number of pages in the document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of pages in the document.|

The following example shows how to get the page count of a nine-page document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var count = document.getPageCount();

gs.info("The number of pages is " + count);
```

Output:

```
The number of pages is 9
```

## Document – getPageSize\(\)

Gets the default page size of the document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wv5_52h_44b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Value of the default page size set using the [PdfPage](../../PdfPageBoth/concept/PdfPageBothAPI.md#) API.Possible values:

-   A4 – 595 x 842 points
-   EXECUTIVE – 522 x 756 points
-   LETTER – 612 x 792 points
-   LEDGER – 792 x 1224 points

</td></tr></tbody>
</table>The following example shows how to get the page size of a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");

var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
var pagesize = document.getPageSize();
```

## Document – isClosed\(\)

Indicates whether a document is closed or open.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wv5_52h_44b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

Flag that indicates whether a document is open or closed.Valid values:

-   true: Document is closed.
-   false: Document is open.

 Default: true

</td></tr></tbody>
</table>The following example shows how to get the page size of a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");

var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var closed = document.isClosed();
```

## Document – saveAsAttachment\(String tableName, String tableSysId, String fileName\)

Attaches the document file to the specified target table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table on which to attach the document.|
|tableSysId|String|Sys\_id of the record on which to attach the document.|
|fileName|String|Name of the document to attach.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the attached document in the Attachments \[sys\_attachment\] table.|

The following example shows how to attach a document to an incident record. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

// Additional document properties

document.saveAsAttachment("incident", "<record_sys_id>", "SampleDocGeneration.pdf");
```

## Document – setBaseDirection\(String direction\)

Sets the base text flow direction to reorder from based on character recognition

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

direction

</td><td>

String

</td><td>

Text flow direction.Valid values:

-   LEFT\_TO\_RIGHT: Order text flow left to right. The text direction is only reordered if left-to-right language characters are detected.
-   RIGHT\_TO\_LEFT: Order text flow right to left. The text direction is only reordered if right-to-left language characters are detected.

 Default: LEFT\_TO\_RIGHT

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set text flow left to right. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");

var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

document.setBaseDirection("RIGHT_TO_LEFT");
```

## Document – setMargins\(Number topMargin, Number rightMargin, Number bottomMargin, Number leftMargin\)

Sets the page margin sizes in the document.

|Name|Type|Description|
|----|----|-----------|
|topMargin|Number|Height of the top margin in points.|
|rightMargin|Number|Width of the right margin in points.|
|bottomMargin|Number|Height of the bottom margin in points.|
|leftMargin|Number|Width of the left margin in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set page margins in a document. For a document usage example, see [Document](DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

document.setMargins(72,36,36,36);
```

