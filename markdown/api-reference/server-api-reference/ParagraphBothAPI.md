---
title: Paragraph - Scoped, Global
description: Creates a Paragraph object representing a block of text in a PDF.Instantiates a new Paragraph object containing a string.Adds an empty line after a paragraph in a document.Adds a paragraph. You can use this method to create a block of paragraphs with automatic line breaks.Adds a string of text to a paragraph. This method does not automatically insert a space preceding the content.Applies a predefined style to paragraph text.Sets a paragraph element to a fixed position on the page.Sets each paragraph margin.Sets the bottom margin of a paragraph.Sets the left margin of a paragraph.Sets the right margin of a paragraph.Sets a size for each paragraph margin.Sets the top margin of a paragraph.Sets the text alignment of this paragraph.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Paragraph - Scoped, Global

Creates a Paragraph object representing a block of text in a PDF.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Paragraph - Paragraph\(String text\)

Instantiates a new Paragraph object containing a string.

|Name|Type|Description|
|----|----|-----------|
|text|String|Paragraph block of text.|

The following example shows how to create a Paragraph object. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var para = new Paragraph("hello");
```

## Paragraph – addNewLine\(\)

Adds an empty line after a paragraph in a document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a new line after a paragraph in a document. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
        
var myPara = new sn_pdfgeneratorutils.Paragraph("This is a paragraph.");
myPara.addNewLine();

document.addParagraph(myPara);       
// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "addText.pdf");
```

## Paragraph – addParagraph\(Paragraph paragraph\)

Adds a paragraph. You can use this method to create a block of paragraphs with automatic line breaks.

|Name|Type|Description|
|----|----|-----------|
|paragraph|[Paragraph](ParagraphBothAPI.md#)|Paragraph object.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a section of paragraphs to a document. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var sectionPara = new sn_pdfgeneratorutils.Paragraph("This is the first paragraph.");
var subPara1 = new sn_pdfgeneratorutils.Paragraph("Pellentesque nec neque interdum turpis ultricies tristique at ut lacus. Nam eget sollicitudin.");
var subPara2 = new sn_pdfgeneratorutils.Paragraph("Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla vel ultrices erat.");
var subPara3 = new sn_pdfgeneratorutils.Paragraph("Aenean fermentum lorem congue metus faucibus, vitae viverra quam eleifend. Donec sed risus quis eros suscipit efficitur.");

sectionPara.addParagraph(subPara1);
sectionPara.addParagraph(subPara2);
sectionPara.addParagraph(subPara3);

document.addParagraph(sectionPara);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Paragraph – addString\(String content\)

Adds a string of text to a paragraph. This method does not automatically insert a space preceding the content.

|Name|Type|Description|
|----|----|-----------|
|content|String|Information to include in a paragraph.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a new sentence to a paragraph. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var myPara = new sn_pdfgeneratorutils.Paragraph("This is the first sentence.");

myPara.addString(" This is the second sentence in the same paragraph. Spaces are not inserted automatically.")

document.addParagraph(myPara);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "filename.pdf");
```

## Paragraph – addStyle\(Style style\)

Applies a predefined style to paragraph text.

|Name|Type|Description|
|----|----|-----------|
|style|[Style](../../StyleBoth/concept/StyleBothAPI.md#)|Style to apply to this element.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to apply a style to a paragraph. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

// Create a font color (result is purple)
var fontColor = new sn_pdfgeneratorutils.Color([0.5,0.0,0.5]);

// Create a style for your paragraph
var paraStyle = new sn_pdfgeneratorutils.Style();
paraStyle.setFontColor(fontColor);
paraStyle.setFontSize(10);

var myPara = new sn_pdfgeneratorutils.Paragraph("This paragraph has style.");

myPara.addStyle(paraStyle);


document.addParagraph(myPara);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "addStyle.pdf");
```

## Paragraph – setFixedPosition\(Number left, Number bottom, Number width\)

Sets a paragraph element to a fixed position on the page.

|Name|Type|Description|
|----|----|-----------|
|left|Number|Indentation from the left side of the PDF page in points.|
|bottom|Number|Position from the bottom of the PDF page in points.|
|width|Number|Width of the paragraph element in points. This value determines the length at which the line breaks.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a fixed position on a page. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("A4");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

// Create a style
var paraStyle = new sn_pdfgeneratorutils.Style();
paraStyle.setFontSize(48);
paraStyle.setBold();

// my paragraph
var para = new sn_pdfgeneratorutils.Paragraph("Document Title");

para.setFixedPosition(204,400,240);

para.setTextAlignment("text-center");
para.addStyle(paraStyle);


document.addParagraph(para);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "fileName.pdf");
```

## Paragraph – setMargin\(Number margin\)

Sets each paragraph margin.

To set all four margins with one or more unique values, use [setMargins\(\)](ParagraphBothAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Value of the top, right, bottom, and left margins in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the all margins of the paragraph to 48 points.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var margins = 48.0;

var myPara = new sn_pdfgeneratorutils.Paragraph("Paragraph text with all margins set to the same value.");
myPara.setMargin(margins);

document.addParagraph(myPara);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "docName.pdf");
```

## Paragraph – setMarginBottom\(Number margin\)

Sets the bottom margin of a paragraph.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Height of the bottom margin in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the bottom margin of a paragraph to one point.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var marginVal = 1.0;

var paraMarginBottom = new sn_pdfgeneratorutils.Paragraph("Paragraph text with bottom margin set.");
paraMarginBottom.setMarginBottom(marginVal);

document.addParagraph(paraMarginBottom);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "docName.pdf");
```

## Paragraph – setMarginLeft\(Number margin\)

Sets the left margin of a paragraph.

|Name|Type|Description|
|----|----|-----------|
|leftMargin|Number|Width of the left margin in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the left margin of a paragraph to one point.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var marginVal = 1.0;

var paraMarginLeft = new sn_pdfgeneratorutils.Paragraph("Paragraph text with left margin set.");
paraMarginLeft.setMarginLeft(marginVal);

document.addParagraph(paraMarginLeft);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "docName.pdf");
```

## Paragraph – setMarginRight\(Number margin\)

Sets the right margin of a paragraph.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Width of the right margin in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the right margin of a paragraph to one point.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var marginVal = 1.0;

var paraMarginRight = new sn_pdfgeneratorutils.Paragraph("Paragraph text with right margin set.");
paraMarginRight.setMarginRight(marginVal);

document.addParagraph(paraMarginRight);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "docName.pdf");
```

## Paragraph – setMargins\(Number marginTop, Number marginRight, Number marginBottom, Number marginLeft\)

Sets a size for each paragraph margin.

To set each margin to the same value, use [setMargin\(\)](ParagraphBothAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|topMargin|Number|Height of the top margin in points.|
|rightMargin|Number|Width of the right margin in points.|
|bottomMargin|Number|Height of the bottom margin in points.|
|leftMargin|Number|Width of the left margin in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set paragraph margins.For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var para = new sn_pdfgeneratorutils.Paragraph("Paragraph text.");

var topMargin = 1.0;
var rightMargin = 1.0;
var bottomMargin = 1.0;
var leftMargin = 1.5;

para.setMargins(marginTop, marginRight, marginBottom, marginLeft);
```

## Paragraph – setMarginTop\(Number margin\)

Sets the top margin of a paragraph.

|Name|Type|Description|
|----|----|-----------|
|margin|Number|Height of the top margin in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the top margin of a paragraph to one point.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var marginVal = 1.0;

var paraMarginTop = new sn_pdfgeneratorutils.Paragraph("Paragraph text with top margin set.");
paraMarginTop.setMarginTop(marginVal);

document.addParagraph(paraMarginTop);

// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<record_sys_id>", "docName.pdf");
```

## Paragraph – setTextAlignment\(String alignment\)

Sets the text alignment of this paragraph.

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

Text alignment position.Valid values:

-   text-center: Aligns text to the center.
-   text-justified: Modifies the space between characters to completely fill text between the left and right sides. The final line is left-aligned.
-   text-justified-all: Justifies text alignment including the final line.
-   text-left: Align text to the left.
-   text-right: Align text to the right.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the paragraph text to left alignment.

```
var paragraph = new sn_pdfgeneratorutils.Paragraph("This paragraph text is centered.");
        
var alignment = "text-center";
       
paragraph.setTextAlignment(alignment);
```

