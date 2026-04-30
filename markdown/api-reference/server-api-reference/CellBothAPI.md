---
title: Cell - Scoped, Global
description: Creates a Cell object as a cell in a table. You can use this API to format the cell and include additional blocks, such as paragraphs and images.Instantiates a new Cell object. Creates a cell which takes a custom amount of cell spaces in the table.Adds an image to a table cell.Adds text to a table cell.Applies a predefined style to table cells.Adds a table to a cell.Gets the number of the column in which the cell is located.Gets the number of rows in which the cell is located.Specifies a background color for the cell.Sets a border for all four edges of a cell.Sets a border for the lower limit of a cell.Sets a border for the left limit of a cell.Sets a border for the right limit of a cell.Sets a border for the upper limit of a cell.Sets a colored border for all four edges of a cell.Sets a colored border for the lower limit of a cell.Sets a colored border for the left limit of a cell.Sets a colored border for the right limit of a cell.Sets a colored border for the upper limit of a cell.Sets the height of a cell.Sets the horizontal alignment for this cell.Sets the maximum height of a cell.Sets the maximum width of a cell.Sets the minimum height of a cell.Sets the minimum width of a cell.Sets the opacity of cell content, borders, and background.Sets the padding of all four sides of a cell to the same width.Sets the value of the bottom padding width of a cell.Sets the value of the left padding width of a cell.Sets the value of the right padding width of a cell.Sets the value of the top padding width of a cell.Sets the text alignment of this cell.Sets the vertical alignment for this cell.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 17
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Cell - Scoped, Global

Creates a Cell object as a cell in a table. You can use this API to format the cell and include additional blocks, such as paragraphs and images.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Cell - Cell\(Number rowspan, Number colspan\)

Instantiates a new Cell object. Creates a cell which takes a custom amount of cell spaces in the table.

**Note:** If you provide a negative number for either parameter, the value sets to 1.

<table id="table_twm_hjk_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

rowspan

</td><td>

Number

</td><td>

Number of rows this cell is to occupy.Default: 0

</td></tr><tr><td>

colspan

</td><td>

Number

</td><td>

Number of columns this cell is to occupy.Default: 0

</td></tr></tbody>
</table>The following example shows how to create a Cell object spanning a single row and single column.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 1);
```

## Cell – addImage\(Image image\)

Adds an image to a table cell.

|Name|Type|Description|
|----|----|-----------|
|image|[Image](../../ImageBoth/concept/ImageBothAPI.md#)|Image to add to a table cell.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate an existing image attachment and add it to a cell in a table. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 1);

var image = new Image("<attachment_sys_id>");

cell.addImage(image);
```

## Cell – addParagraph\(Paragraph paragraph\)

Adds text to a table cell.

|Name|Type|Description|
|----|----|-----------|
|paragraph|[Paragraph](../../ParagraphBoth/concept/ParagraphBothAPI.md#)|Text to add to a table cell.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate paragraph objects and add the content cells in a table. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);
var para = new sn_pdfgeneratorutils.Paragraph("Paragraph text.");
cell.addParagraph(para);
```

## Cell – addStyle\(Style style\)

Applies a predefined style to table cells.

|Name|Type|Description|
|----|----|-----------|
|style|[Style](../../StyleBoth/concept/StyleBothAPI.md#)|Style to apply to this element.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to apply a style to a table cell. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);
var style = new sn_pdfgeneratorutils.Style();
style.setBold();
     
cell.addStyle(style);
```

## Cell – addTable\(Table table\)

Adds a table to a cell.

|Name|Type|Description|
|----|----|-----------|
|table|[Table](../../TableBoth/concept/TableBothAPI.md#)|Table to add to a cell.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate a table object and add it to a cell. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 1);

var columnWidths = [100, 50, 50];

var table = new Table(columnWidths, false);

cell.addTable(table);
```

## Cell – getColumn\(\)

Gets the number of the column in which the cell is located.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of the column position for a cell.|

The following example shows how to get the number of a column position for a cell.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 1);

var columnWidths = [100, 50, 50];

var table = new sn_pdfgeneratorutils.Table(true, columnWidths, false);

table.addCell(cell);

var colNum = cell.getColumn();

gs.info("The column position for cell is " + colNum);
```

Output:

```
The column position for cell is 1
```

## Cell – getRow\(\)

Gets the number of rows in which the cell is located.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of the row position for a cell.|

The following example shows how to get the number of a row position for a cell.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 1);

var rowWidths = [100, 50, 50];

var table = new sn_pdfgeneratorutils.Table(true, rowWidths, false);

table.addCell(cell);

var rowNum = cell.getRow();

gs.info("The row position for cell is " + rowNum);
```

Output:

```
The row position for cell is 4927
```

## Cell – setBackGroundColor\(Color color\)

Specifies a background color for the cell.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Background color.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set cell background color. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var color = new sn_pdfgeneratorutils.Color([1, 0.9, 0.9]); // provided as array of RGB float values

cell.setBackGroundColor(color);
```

## Cell – setBorder\(Number width\)

Sets a border for all four edges of a cell.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a cell border of one point to all four edges of a cell. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 1.0;

cell.setBorder(width);
```

## Cell – setBorderBottom\(Number width\)

Sets a border for the lower limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 1.0;

cell.setBorder(width);
```

## Cell – setBorderLeft\(Number width\)

Sets a border for the left limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how set a left-side cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 1.0;

cell.setLeftBorder(width);
```

## Cell – setBorderRight\(Number width\)

Sets a border for the right limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a right-side cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 1.0;

cell.setRightBorder(width);
```

## Cell – setBorderTop\(Number width\)

Sets a border for the upper limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a top cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 1.0;

cell.setBorderTop(width);
```

## Cell – setColoredBorder\(Color color, Number width\)

Sets a colored border for all four edges of a cell.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Cell border color.|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a colored cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var width = 1.0;

cell.setColoredBorder(borderColor, width);
```

## Cell – setColoredBorderBottom\(Color color, Number width\)

Sets a colored border for the lower limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Cell border color.|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a colored lower cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var width = 1.0;

cell.setColoredBorderBottom(borderColor, width);
```

## Cell – setColoredBorderLeft\(Color color, Number width\)

Sets a colored border for the left limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Cell border color.|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a colored left cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var width = 1.0;

cell.setColoredBorderLeft(borderColor, width);
```

## Cell – setColoredBorderRight\(Color color, Number width\)

Sets a colored border for the right limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Cell border color.|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a colored right cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var width = 1.0;

cell.setColoredBorderRight(borderColor, width);
```

## Cell – setColoredBorderTop\(Color color, Number width\)

Sets a colored border for the upper limit of a cell.

|Name|Type|Description|
|----|----|-----------|
|color|[Color](../../ColorBoth/concept/ColorBothAPI.md#)|Cell border color.|
|width|Number|Cell border width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a colored top cell border. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var borderColor = new sn_pdfgeneratorutils.Color([0.8,0.8,0.8]);
var width = 1.0;

cell.setColoredBorderTop(borderColor, width);
```

## Cell – setHeight\(Number height\)

Sets the height of a cell.

|Name|Type|Description|
|----|----|-----------|
|value|Number|Cell height in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how set a cell height of 10 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var height = 10;

cell.setHeight(height);
```

## Cell – setHorizontalAlignment\(String alignment\)

Sets the horizontal alignment for this cell.

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

The following example shows how to set horizontal alignment on a cell. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var alignment = "center";

cell.setHorizontalAlignment(alignment);
```

## Cell – setMaxHeight\(Number value\)

Sets the maximum height of a cell.

|Name|Type|Description|
|----|----|-----------|
|value|Number|Maximum cell height in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how set a maximum cell height of 409 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var height = 409;

cell.setMaxHeight(height);
```

## Cell – setMaxWidth\(float value\)

Sets the maximum width of a cell.

|Name|Type|Description|
|----|----|-----------|
|value|Number|Maximum cell width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how set a maximum cell width of 1530 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 1530;

cell.setMaxWidth(width);
```

## Cell – setMinHeight\(Number value\)

Sets the minimum height of a cell.

|Name|Type|Description|
|----|----|-----------|
|value|Number|Minimum cell height in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how set a minimum cell height of 12.75 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var height = 12.75;

cell.setMinHeight(height);
```

## Cell – setMinWidth\(Number value\)

Sets the minimum width of a cell.

|Name|Type|Description|
|----|----|-----------|
|value|Number|Minimum cell width in points.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how set a minimum cell width of 50.58 points. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var width = 50.58;

cell.setMinWidth(width);
```

## Cell – setOpacity\(Number opacity\)

Sets the opacity of cell content, borders, and background.

**Note:** This setting affects all child elements of the cell.

<table id="table_vv5_52h_44b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

opacity

</td><td>

Number

</td><td>

Float decimal value from 0 through 1, in which 0 is transparent and 1 is fully opaque.Default: 0

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the opacity of a cell.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var opacity = 0.5;

cell.setOpacity(opacity);
```

## Cell – setPadding\(Number padding\)

Sets the padding of all four sides of a cell to the same width.

See also:

-   [setPaddingBottom\(\)](CellBothAPI.md#)
-   [setPaddingLeft\(\)](CellBothAPI.md#)
-   [setPaddingRight\(\)](CellBothAPI.md#)
-   [setPaddingTop\(\)](CellBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the bottom cell to one point. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var padding = 1.0;

cell.setPadding(padding);
```

## Cell – setPaddingBottom\(Number padding\)

Sets the value of the bottom padding width of a cell.

See also:

-   [setPadding\(\)](CellBothAPI.md#)
-   [setPaddingLeft\(\)](CellBothAPI.md#)
-   [setPaddingRight\(\)](CellBothAPI.md#)
-   [setPaddingTop\(\)](CellBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set bottom cell padding to one point. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var padding = 1.0;

cell.setPaddingBottom(padding);
```

## Cell – setPaddingLeft\(Number padding\)

Sets the value of the left padding width of a cell.

See also:

-   [setPadding\(\)](CellBothAPI.md#)
-   [setPaddingBottom\(\)](CellBothAPI.md#)
-   [setPaddingRight\(\)](CellBothAPI.md#)
-   [setPaddingTop\(\)](CellBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set left cell padding to one point. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var padding = 1.0;

cell.setPaddingLeft(padding);
```

## Cell – setPaddingRight\(Number padding\)

Sets the value of the right padding width of a cell.

See also:

-   [setPadding\(\)](CellBothAPI.md#)
-   [setPaddingBottom\(\)](CellBothAPI.md#)
-   [setPaddingLeft\(\)](CellBothAPI.md#)
-   [setPaddingTop\(\)](CellBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set right cell padding to one point. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var padding = 1.0;

cell.setPaddingRight(padding);
```

## Cell – setPaddingTop\(Number padding\)

Sets the value of the top padding width of a cell.

See also:

-   [setPadding\(\)](CellBothAPI.md#)
-   [setPaddingBottom\(\)](CellBothAPI.md#)
-   [setPaddingLeft\(\)](CellBothAPI.md#)
-   [setPaddingRight\(\)](CellBothAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|padding|Number|Padding width in points as a decimal value.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set top cell padding to one point. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var padding = 1.0;

cell.setPaddingTop(padding);
```

## Cell – setTextAlignment\(String alignment\)

Sets the text alignment of this cell.

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

The following example shows how to set the cell text to left alignment.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var alignment = "text-left";

cell.setTextAlignment(alignment);
```

## Cell – setVerticalAlignment\(String alignment\)

Sets the vertical alignment for this cell.

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

The following example shows how to set vertical alignment on a cell. For a document usage example, see [Document](../../DocumentBoth/concept/DocumentBothAPI.md#) API.

```
var cell = new sn_pdfgeneratorutils.Cell(1, 3);

var alignment = "mid";

cell.setVerticalAlignment(alignment);
```

