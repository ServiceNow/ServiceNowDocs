---
title: Style - Scoped, Global
description: Creates a style for defining properties such font size, border, and alignment. You can apply the same style to multiple objects simultaneously.Instantiates a new Style object.Specifies a background color of an element.Sets a style to bold font.Sets the style border on all four sides of an element.Sets the style border to the bottom of an element.Sets the style border on the left side of an element.Sets the style border on the right side of an element.Sets the style border to the top of an element.Sets style border with color on all four sides of an element.Sets style border with color to the bottom side of an element.Sets style border with color on the left side of an element.Sets style border with color on the right side of an element.Sets style border with color to the top side of an element.Sets a font color.Sets a style font size.Sets the horizontal alignment for a style.Sets a style to italic font.Sets the padding of all four sides of an element to the same width.Sets the value of the bottom padding width of an element.Sets the value of the left padding width of an element.Sets the value of the right padding width of a style.Sets the value of the top padding width of an element.Sets the text alignment for a style.Sets the vertical alignment for this element.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Style - Scoped, Global

Creates a style for defining properties such font size, border, and alignment. You can apply the same style to multiple objects simultaneously.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

You can apply custom styles to the following API elements:

-   [Cell](../../CellBoth/concept/CellBothAPI.md#)
-   [Paragraph](../../ParagraphBoth/concept/ParagraphBothAPI.md#)
-   [Table](../../TableBoth/concept/TableBothAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Style - Style\(\)

Instantiates a new Style object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

The following examples shows how to create a Style object that you can add to a [Cell](../../CellBoth/concept/CellBothAPI.md#), [Paragraph](../../ParagraphBoth/concept/ParagraphBothAPI.md#) or [Table](../../TableBoth/concept/TableBothAPI.md#) element.

```
var style = new sn_pdfgeneratorutils.Style();
```

## Style – setBackgroundColor\(Color color\)

Specifies a background color of an element.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Background color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set element background color. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var color = new sn_pdfgeneratorutils.Color([1, 0.9, 0.9]); // provided as array of RGB float values

style.setBackGroundColor(color);
```

## Style – setBold\(\)

Sets a style to bold font.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style to bold font.

```
var style = new sn_pdfgeneratorutils.Style();
style.setBold();
```

## Style – setBorder\(Number width\)

Sets the style border on all four sides of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 2;

style.setBorder(width);
```

## Style – setBorderBottom\(Number width\)

Sets the style border to the bottom of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border to the bottom of an element. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 2;

style.setBorderBottom(width);
```

## Style – setBorderLeft\(Number width\)

Sets the style border on the left side of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border on the left side of an element. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 2;

style.setBorderLeft(width);
```

## Style – setBorderRight\(Number width\)

Sets the style border on the right side of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border on the right side of an element. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 2;

style.setBorderRight(width);
```

## Style – setBorderTop\(Number width\)

Sets the style border to the top of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border to the top of an element. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 2;

style.setBorderTop(width);
```

## Style – setColoredBorder\(Number width, Color color\)

Sets style border with color on all four sides of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Style border color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border with color. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 1.0;
var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);

style.setColoredBorder(width, borderColor);
```

## Style – setColoredBorderBottom\(Number width, Color color\)

Sets style border with color to the bottom side of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Style border color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border to the bottom of an element.For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 1.0;
var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);

style.setColoredBorderBottom(width, borderColor);
```

## Style – setColoredBorderLeft\(Number width, Color color\)

Sets style border with color on the left side of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Style border color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 1.0;
var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);

style.setColoredBorderLeft(width, borderColor);
```

## Style – setColoredBorderRight\(Number width, Color color\)

Sets style border with color on the right side of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Style border color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border with color. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 1.0;
var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);

style.setColoredBorderRight(width, borderColor);
```

## Style – setColoredBorderTop\(Number width, Color color\)

Sets style border with color to the top side of an element.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Style border width in points.|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Style border color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a style border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var width = 1.0;
var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);

style.setColoredBorderTop(width, borderColor);
```

## Style – setFontColor\(Color color\)

Sets a font color.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Font color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a font color. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var fontColor = new sn_pdfgeneratorutils.Color([1,0.5,0.5]);

style.setFontColor(fontColor);
```

## Style – setFontSize\(Number fontSize\)

Sets a style font size.

|Name|Type|Description|
|----|----|-----------|
|fontSize|Number|Font size in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a font size.

```
var style = new sn_pdfgeneratorutils.Style();

style.setFontSize(12);
```

## Style – setHorizontalAlignment\(String alignment\)

Sets the horizontal alignment for a style.

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

Horizontal alignment setting.Valid values:

-   center: Align contents to the center.
-   left: Align contents to the left.
-   right: Align contents to the right.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set horizontal alignment on an element. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var alignment = "Center";

style.setHorizontalAlignment(alignment);

```

## Style – setItalic\(\)

Sets a style to italic font.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set an element style to an italic font.

```
var style = new sn_pdfgeneratorutils.Style();
style.setItalic();
```

## Style – setPadding\(Number padding\)

Sets the padding of all four sides of an element to the same width.

See also:

-   [setPaddingBottom\(\)](StyleBothAPI.md#)
-   [setPaddingLeft\(\)](StyleBothAPI.md#)
-   [setPaddingRight\(\)](StyleBothAPI.md#)
-   [setPaddingTop\(\)](StyleBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set bottom style to 2.5 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var padding = 2.5;

style.setPadding(padding);
```

## Style – setPaddingBottom\(Number padding\)

Sets the value of the bottom padding width of an element.

See also:

-   [setPadding\(\)](StyleBothAPI.md#)
-   [setPaddingLeft\(\)](StyleBothAPI.md#)
-   [setPaddingRight\(\)](StyleBothAPI.md#)
-   [setPaddingTop\(\)](StyleBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set bottom element padding to 2.5 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var padding = 2.5;

style.setPaddingBottom(padding);
```

## Style – setPaddingLeft\(Number padding\)

Sets the value of the left padding width of an element.

See also:

-   [setPadding\(\)](StyleBothAPI.md#)
-   [setPaddingBottom\(\)](StyleBothAPI.md#)
-   [setPaddingRight\(\)](StyleBothAPI.md#)
-   [setPaddingTop\(\)](StyleBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set left element padding to 2.5 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var padding = 2.5;

style.setPaddingLeft(padding);
```

## Style – setPaddingRight\(Number padding\)

Sets the value of the right padding width of a style.

See also:

-   [setPadding\(\)](StyleBothAPI.md#)
-   [setPaddingBottom\(\)](StyleBothAPI.md#)
-   [setPaddingLeft\(\)](StyleBothAPI.md#)
-   [setPaddingTop\(\)](StyleBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set right element padding to 2.5 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var padding = 2.5;

style.setPaddingRight(padding);
```

## Style – setPaddingTop\(Number padding\)

Sets the value of the top padding width of an element.

See also:

-   [setPadding\(\)](StyleBothAPI.md#)
-   [setPaddingBottom\(\)](StyleBothAPI.md#)
-   [setPaddingLeft\(\)](StyleBothAPI.md#)
-   [setPaddingRight\(\)](StyleBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set top element padding to 2.5 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var padding = 2.5;

style.setPaddingTop(padding);
```

## Style – setTextAlignment\(String alignment\)

Sets the text alignment for a style.

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

The following example shows how to set the element text to center alignment.

```
var style = new sn_pdfgeneratorutils.Style();

String alignment = "text-center";

style.setTextAlignment(alignment);
```

## Style – setVerticalAlignment\(String alignment\)

Sets the vertical alignment for this element.

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

Vertical alignment setting.Valid values:

-   bottom: Aligns contents to the bottom.
-   mid: Aligns contents to the center.
-   top: Aligns contents to the top.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set vertical alignment on an element. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var style = new sn_pdfgeneratorutils.Style();

var alignment = "Mid";

style.setVerticalAlignment(alignment);

```

