---
title: Line - Scoped, Global
description: Creates a Line object using methods to draw a line in a PDF.Instantiates a new Line object.Places a line on a document page.Sets the color of a line.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Line - Scoped, Global

Creates a Line object using methods to draw a line in a PDF.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Line - Line\(\)

Instantiates a new Line object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

The following examples shows how to create a Line object.

```
var line = new sn_pdfgeneratorutils.Line();
```

## Line – drawLine\(Document document, Number pageNo, Number xPos, Number yPos, Number width, Number lineWidth\)

Places a line on a document page.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document

</td><td>

[Document](../../DocumentBoth/concept/DocumentBothAPI.md#)

</td><td>

Name of the document object.

</td></tr><tr><td>

pageNo

</td><td>

Number

</td><td>

Page number on which you want to place the line.

</td></tr><tr><td>

xPos

</td><td>

Number

</td><td>

X-coordinate area of the page on which to place the line.

</td></tr><tr><td>

yPos

</td><td>

Number

</td><td>

Y-coordinate area of the page on which to place the line.

</td></tr><tr><td>

width

</td><td>

Number

</td><td>

Width area of the page in which you want to draw the line. Values are in points.

</td></tr><tr><td>

lineWidth

</td><td>

Number

</td><td>

Optional. Value of line thickness in points.Default: 1

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to create a line at the lower margin of a document page. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var num = 1;
var xpos = 100;
var ypos = 100;
var width = 450;
var linewidth = 2.5;

document.addNewPage();

var line = new sn_pdfgeneratorutils.Line();

line.drawLine(document, num, xpos, ypos, width, linewidth);

document.saveAsAttachment("incident", "<sys_id>", "line.pdf");
```

## Line – setColor\(Color color\)

Sets the color of a line.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Line color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to create a line and set its color in a document. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var num = 1;
var xpos = 100;
var ypos = 100;
var width = 450;
var linewidth = 2.5;

var color = new sn_pdfgeneratorutils.Color([0.5,0.5,0.8]);   //given as array of RGB values;

document.addNewPage();

var line = new sn_pdfgeneratorutils.Line();

line.setColor(color);

line.drawLine(document, num, xpos, ypos, width, linewidth);

document.saveAsAttachment("incident", "<sys_id>", "lineWithColor.pdf");
```

