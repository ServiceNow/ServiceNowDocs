---
title: Color - Scoped, Global
description: Creates a Color object used to define color attributes that you can apply to elements in a PDF; such as cells, tables, and lines.Instantiates a new Color object with RGB values.Indicates whether the values of two different color objects match.Returns a black, gray, or white color object.Creates color with given values and enables you to change the values of an existing color. Each of the values must be from 0 through 1.Sets the level of color opacity.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Color- Scoped, Global

Creates a Color object used to define color attributes that you can apply to elements in a PDF; such as cells, tables, and lines.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API is a component used with the [Document API](../../DocumentBoth/concept/DocumentBothAPI.md#) to generate a PDF.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Color - Color\(Array colors\)

Instantiates a new Color object with RGB values.

Color can be applied to the following scenarios:

|Name|Type|Description|
|----|----|-----------|
|colors|Array|Three numbers indicating RGB values using a decimal value from 0 through 1. For example, in `[0.1, 0.9, 0.5]`, the value of the first position is red, second is green, and third is blue. Also, `[0, 0, 0]` is solid black, `[0.5, 0.5, 0.5]` is solid gray, and `[1, 1, 1]` is solid white.|

The following example shows how to create a Color object.

```
var color = new sn_pdfgeneratorutils.Color([0.1, 0.9, 0.5]); //given as object containing RGB values
```

## Color – equals\(Color color\)

Indicates whether the values of two different color objects match.

|Name|Type|Description|
|----|----|-----------|
|color|Color|Color object to check for a match.|

<table id="table_wv5_52h_44b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the values of two color objects match.

 Valid values:

-   true: The colors match.
-   false: The colors do not match.

</td></tr></tbody>
</table>The following example shows how to create two color objects and determine if the colors match.

```
var color1 = new sn_pdfgeneratorutils.Color([1,0.5,0.5]);  // given as an array of RGB values
var color2 = new sn_pdfgeneratorutils.Color([0.8,0.5,0.5]);         // given as an array of RGB values
var isequal = color1.equals(color2);
```

## Color – getGrayColor\(Number grayScale\)

Returns a black, gray, or white color object.

|Name|Type|Description|
|----|----|-----------|
|grayScale|Number|Decimal value in the range 0 through 1, in which 0 is black and 1 is white.|

|Type|Description|
|----|-----------|
|Object|Color object reflecting the provided grayscale value.|

The following example shows how to create a color object that is 50% grayscale.

```
var grayColor = new sn_pdfgeneratorutils.Color.getGrayColor(0.5);
```

## Color – setColorValue\(Array colors\)

Creates color with given values and enables you to change the values of an existing color. Each of the values must be from 0 through 1.

|Name|Type|Description|
|----|----|-----------|
|colors|Array|Three numbers indicating RGB values using a decimal value from 0 through 1. For example, in `[0.1, 0.9, 0.5]`, the value of the first position is red, second is green, and third is blue. Also, `[0, 0, 0]` is solid black, `[0.5, 0.5, 0.5]` is solid gray, and `[1, 1, 1]` is solid white.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to change the values of an existing color.

```
var color = new sn_pdfgeneratorutils.Color([1,0.5,0.5]);   //given as array of RGB values;
color.setColorValue(color);
```

## Color – setOpacity\(Number opacity\)

Sets the level of color opacity.

|Name|Type|Description|
|----|----|-----------|
|color|Color|Floating decimal value from 0 through 1, in which 0 is fully transparent and 1 is fully opaque.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to create a color object and set its opacity to 50 percent.

```
var color = new Color([1,0.5,0.5]);
color.setOpacity(0.5);
```

