---
title: PdfPage - Scoped, Global
description: Creates a PdfPage object representing a PDF page and its attributes; such as size, width, and color.Instantiates a new PdfPage object.Gets the Y-coordinate of the lower edge of a PDF page.Gets the X-coordinate of the left edge of a PDF page.Gets the size of a PDF pageGets the X-coordinate of the right edge of a PDF page.Gets the Y-coordinate of the upper edge of a PDF page.Gets the width of a PDF page.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PdfPage - Scoped, Global

Creates a PdfPage object representing a PDF page and its attributes; such as size, width, and color.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PdfPage - PdfPage\(String pageSize, String orientation\)

Instantiates a new PdfPage object.

<table id="table_twm_hjk_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pageSize

</td><td>

String

</td><td>

PDF page size.Valid values:

-   A4 – 595 x 842 points
-   EXECUTIVE – 522 x 756 points
-   LETTER – 612 x 792 points
-   LEDGER – 792 x 1224 points

</td></tr><tr><td>

orientation

</td><td>

String

</td><td>

Optional. PDF page orientation.Valid values:

-   LANDSCAPE
-   PORTRAIT

 Default: PORTRAIT

</td></tr></tbody>
</table>The following example shows how to create a PdfPage object.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
```

## PdfPage – getBottom\(\)

Gets the Y-coordinate of the lower edge of a PDF page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Decimal value of the Y-coordinate at the lower edge of the PDF page.|

The following example shows how to get the Y-coordinate of the lower edge of a PDF page.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
 var bottom = pdfpage.getBottom();
```

## PdfPage – getLeft\(\)

Gets the X-coordinate of the left edge of a PDF page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Decimal value of the X-coordinate on the left edge of the page.|

The following example shows how to get the X-coordinate of the left edge of a PDF page.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
 var left = pdfpage.getLeft();
```

## PdfPage – getPdfPageSize\(\)

Gets the size of a PDF page

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to get the PDF page size.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
var size = pdfpage.getPdfPageSize();
```

## PdfPage – getRight\(\)

Gets the X-coordinate of the right edge of a PDF page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Decimal value of the X-coordinate on the right edge of the page.|

The following example shows how to get the X-coordinate of the right edge of a PDF page.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
 var right = pdfpage.getRight();
```

## PdfPage – getTop\(\)

Gets the Y-coordinate of the upper edge of a PDF page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Decimal value of the Y-coordinate at the upper edge of the PDF page.|

The following example shows how to get the Y-coordinate of the upper edge of a PDF page.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
 var top  = pdfpage.getTop();
```

## PdfPage – getWidth\(\)

Gets the width of a PDF page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Size of the page width in points.|

The following example shows how to retrieve the width of a PDF page.

```
var pdfpage = new sn_pdfgeneratorutils.PdfPage("A4", "LANDSCAPE");
var width = PdfPage.getWidth();
```

