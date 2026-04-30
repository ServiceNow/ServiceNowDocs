---
title: Image - Scoped, Global
description: Creates an Image object representing an image and its layout insert in a PDF. Enables defining attributes such as scale, alignment, and border color.Instantiates a new Image object. Used to verify if an image attachment exists and is available for modification.Scales an image to absolute width and height sizes. This setting does not preserve the width-height ratio of the image and might result in undesired stretching if settings are not precise.Scales an image to an absolute size while preserving the width-height ratio.Enables scaling width and height to a page or cell while retaining dimensions.Sets a border on a PDF in the specified color.Sets the horizontal alignment of the image.Sets an image to have no border.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Image - Scoped, Global

Creates an Image object representing an image and its layout insert in a PDF. Enables defining attributes such as scale, alignment, and border color.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

You can add an image to a PDF using one of the following methods:

-   [Cell – addImage\(Image image\)](../../CellBoth/concept/CellBothAPI.md#) – Adds an image to a table cell
-   [Table – addImageCell\(Image image\)](../../TableBoth/concept/TableBothAPI.md#) – Adds a cell that contains an image to a table.
-   [Document – addImage\(Image image\)](../../DocumentBoth/concept/DocumentBothAPI.md#) - Adds an image to a page

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Image - Image\(String attachmentSysId\)

Instantiates a new Image object. Used to verify if an image attachment exists and is available for modification.

|Name|Type|Description|
|----|----|-----------|
|attachmentSysId|String|Sys\_id of an image in the Attachments \[sys\_attachment\] table.|

The following example shows how to create a Image object.

```
var image = new sn_pdfgeneratorutils.Image("<sys_id>");
```

## Image – scaleAbsolute\(Number width, Number height\)

Scales an image to absolute width and height sizes. This setting does not preserve the width-height ratio of the image and might result in undesired stretching if settings are not precise.

To scale to an absolute size that preserves width-height ratio of an image, use the [scaleToFit\(\)](ImageBothAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Image width in points.|
|height|Number|Image height in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add an image to a PDF with absolute width and height settings.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var scaleAbsPic = new sn_pdfgeneratorutils.Image("<img_sys_id>");
scaleAbsPic.scaleAbsolute(25,50);

document.addImage(scaleAbsPic);

document.saveAsAttachment("incident", "<record_sys_id>", "docWithImg.pdf");
```

## Image – scaleToFit\(Number width, Number height\)

Scales an image to an absolute size while preserving the width-height ratio.

Resulting output varies by image aspect ratio. If the width and height parameter values do not match the image aspect ratio, one value renders smaller in output than the value given.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Maximum image width in points.|
|height|Number|Maximum image height in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to insert an image scaled to fit using the [Cell – addImage\(\)](../../CellBoth/concept/CellBothAPI.md#) method.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// add a table
var table = new sn_pdfgeneratorutils.Table([1,3],false);

// text for the left column
var text = "sample image";

// add a table cell for the image in the right column
var imgCell = new sn_pdfgeneratorutils.Cell(1, 1);

// add an image and set it scale-to-fit
var scaleToFitPic = new sn_pdfgeneratorutils.Image("<img_sys_id>");
scaleToFitPic.scaleToFit(90,175);

// add the image to the cell
imgCell.addImage(scaleToFitPic);
 
table.addTextCell(text);
table.addCell(imgCell);

// Here's a paragraph
var para = new sn_pdfgeneratorutils.Paragraph("The following table image uses scale to fit.");

document.addParagraph(para);
document.addTable(table);

document.saveAsAttachment("incident", "<record_sys_id>", "imgScaleToFit.pdf");
```

## Image – setAutoScale\(Boolean value\)

Enables scaling width and height to a page or cell while retaining dimensions.

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

Flag that indicates whether to automatically scale an image.

 Valid values:

-   true: Automatically scales the image
-   false: Image does not scale

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to add an image to a PDF with automatic scaling. The image is added using the [Table – addImageCell\(\)](../../TableBoth/concept/TableBothAPI.md#) method.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

// Add a table
var table = new sn_pdfgeneratorutils.Table([1,2],false);

// Text in left column
var text = "sample image";

// Image in right column
var autoScaledPic = new sn_pdfgeneratorutils.Image("<image_sys_id>");
autoScaledPic.setAutoScale(true);

table.addTextCell(text);
table.addImageCell(autoScaledPic);

document.addTable(table);
document.saveAsAttachment("incident", "<record_sys_id>", "imgAutoScale.pdf");
```

## Image – setColoredBorder\(Color color, Number width\)

Sets a border on a PDF in the specified color.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Image border color.|
|width|Number|Width of the border in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a five-point red-colored border on an image.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);

var borderColor = new sn_pdfgeneratorutils.Color([1.0,0.0,0.0]);
 
// declare image using sys attachment
var image = new sn_pdfgeneratorutils.Image("<imgAttachment_sys_id>");

image.setColoredBorder(borderColor, 5);

document.addImage(image);
document.saveAsAttachment("incident", "<record_sys_id>", "docWithBorderedImage.pdf");
```

## Image – setHorizontalAlignment\(String alignment\)

Sets the horizontal alignment of the image.

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

Positions image alignment on a page or block element.Valid values:

-   Center
-   Left
-   Right

 Default: Left

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a centered image on a PDF page.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare image using sys attachment
var image = new sn_pdfgeneratorutils.Image("<imgAttachment_sys_id>");

String alignment = "Center";
image.setHorizontalAlignment(alignment);

document.addImage(image);
// save pdf as attachment to target record in the Incident table
document.saveAsAttachment("incident", "<sys_id>", "docWithImageCentered.pdf");
```

## Image – setNoBorder\(\)

Sets an image to have no border.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add an image to a document without a border.

```
var pageSize = new sn_pdfgeneratorutils.PdfPage("LETTER");
var document = new sn_pdfgeneratorutils.Document.createDocument(pageSize);
 
// declare image using sys attachment
var image = new sn_pdfgeneratorutils.Image("<imgAttachment_sys_id>");

image.setNoBorder();

document.addImage(image);
document.saveAsAttachment("incident", "<sys_id>", "docWithImgNoBorder.pdf");
```

