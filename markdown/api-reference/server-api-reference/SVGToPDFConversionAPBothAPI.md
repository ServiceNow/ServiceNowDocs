---
title: SVGToPDFConversionAPI - Scoped, Global
description: The SVGToPDFConversionAPI provides methods that enable the adding of an SVG to a PDF and converting an SVG to PDF.Instantiates a new SVGToPDFConversionAPI object.Adds an SVG image to a PDF on a specified page with image size and location coordinates.Converts an SVG provided as string to PDF.Converts an SVG provided as string to PDF with image width and height values.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SVGToPDFConversionAPI - Scoped, Global

The SVGToPDFConversionAPI provides methods that enable the adding of an SVG to a PDF and converting an SVG to PDF.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

See also [PDFGenerationAPI](../../PDFGenerationAPIBoth/concept/PDFGenerationAPIBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SVGToPDFConversionAPI - SVGToPDFConversionAPI\(\)

Instantiates a new SVGToPDFConversionAPI object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following examples shows how to create a SVGToPDFConversionAPI object.

```
var v = new sn_pdfgeneratorutils.SVGToPDFConversionAPI();
```

## SVGToPDFConversionAPI - addSVGToPDF\(String svg, String inputPdfSysId, String targetTable, String targetSysId, String nameForPdf, Number pageNo, Number x, Number y, Number svgImgWidth, Number svgImgHeight\)

Adds an SVG image to a PDF on a specified page with image size and location coordinates.

<table id="table_gms_ycm_j4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

svg

</td><td>

String

</td><td>

SVG to convert to a PDF document.

</td></tr><tr><td>

inputPdfSysId

</td><td>

String

</td><td>

Sys\_id of the target PDF in which to create a copy of with an SVG. The target PDF is in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

targetTable

</td><td>

String

</td><td>

Name of the table containing the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

targetTableSysId

</td><td>

String

</td><td>

Sys\_id of the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

targetTable

</td><td>

String

</td><td>

Name of the table on which to attach the converted PDF.

</td></tr><tr><td>

targetTableSysId

</td><td>

String

</td><td>

Sys\_id of the record on which to attach the converted PDF.

</td></tr><tr><td>

pdfName

</td><td>

String

</td><td>

Name to give the PDF.Default: Sys\_id of the PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

pageNo

</td><td>

Number

</td><td>

Page number in the attached PDF on which to place the SVG.

</td></tr><tr><td>

x

</td><td>

Number

</td><td>

Horizontal position of the SVG in the page. Value is in points.

</td></tr><tr><td>

y

</td><td>

Number

</td><td>

Vertical position of the SVG in the page. Value is in points.

</td></tr><tr><td>

svgImgWidth

</td><td>

Number

</td><td>

Width of the SVG image in pixels.

</td></tr><tr><td>

svgImgHeight

</td><td>

Number

</td><td>

Height of the SVG image in pixels.

</td></tr></tbody>
</table><table id="table_hms_ycm_j4b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="row_svg2PDF-return-svg_attach"><td>

Object

</td><td>

Object containing sys\_id of a new PDF attachment with inserted SVG if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td>

If SVG conversion is successful, sys\_id of the attached PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Adding SVG content to PDF failed.
-   Adding SVG to PDF and creating new PDF is successful.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   Input PDF attachment sys id to add the SVG content is null
-   Input SVG content is empty or null
-   PdfReader is not opened with owner password
-   The target table name to attach the modified PDF : &lt;targetTable&gt; is empty or null
-   The target table name to attach the modified PDF : &lt;targetTable&gt; is not valid

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how get SVG from the description field of an incident record and add it to page 5 of a PDF attachment. The new PDF with SVG is located in the Attachments \[sys\_attachment\] table.

```
var gr = new GlideRecord("incident");

var svg;

if (gr.get("<tableSysId>")) {
 svg = gr.description.toString();
}

var result = new sn_pdfgeneratorutils.SVGToPDFConversionAPI().addSVGToPDF(svg, "<inputPdfSysId>", "incident", "<tableSysId>", "AddSVGToPDF", 5, 30, 30, 300, 100);
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"<sys_id>","message":"Adding SVG to PDF and creating new PDF is successful.","status":"success"}
```

## SVGToPDFConversionAPI - convertSVGToPDF\(String svg, String pdfName, String targetTable, String targetTableSysId\)

Converts an SVG provided as string to PDF.

<table id="table_gms_ycm_j4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

svg

</td><td>

String

</td><td>

SVG to convert to a PDF document.

</td></tr><tr><td>

pdfName

</td><td>

String

</td><td>

Name to give the PDF.Default: Sys\_id of the PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

targetTable

</td><td>

String

</td><td>

Name of the table on which to attach the converted PDF.

</td></tr><tr><td>

targetTableSysId

</td><td>

String

</td><td>

Sys\_id of the record on which to attach the converted PDF.

</td></tr></tbody>
</table><table id="table_hms_ycm_j4b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing sys\_id of the PDF attachment converted from SVG if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td>

If SVG conversion is successful, sys\_id of the attached PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Converting SVG image to PDF document failed.
-   Exception while reading Source document contents.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   SVG to PDF conversion is successful.
-   The Target table name - &lt;tableName&gt; to attach the converted SVG is not valid
-   The Target table name - &lt;tableName&gt; to attach the converted SVG is empty or null

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how get SVG from the description field of an incident record, to convert the SVG to PDF and attach it to a record.

```
var gr = new GlideRecord("incident");

var svg;

if (gr.get("<tableSysId>")) {
 svg = gr.description.toString();
}

var v = new sn_pdfgeneratorutils.SVGToPDFConversionAPI();

var result = v.convertSVGToPDF(svg, "ConvertSVGToPDF", "incident", "<targetTableSysId>");
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"<pdf_attachment_sys_id>","message":"SVG to PDF conversion is successful.","status":"success"}
```

## SVGToPDFConversionAPI - convertSVGToPDFWithSize\(String svg, String nameForPDF, String targetTable, String targetTableSysId, Number svgImgWidth, Number svgImgHeight\)

Converts an SVG provided as string to PDF with image width and height values.

<table id="table_nqj_1dm_j4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

svg

</td><td>

String

</td><td>

SVG to convert to a PDF document.

</td></tr><tr><td>

pdfName

</td><td>

String

</td><td>

Name to give the PDF.Default: Sys\_id of the PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

targetTable

</td><td>

String

</td><td>

Name of the table on which to attach the converted PDF.

</td></tr><tr><td>

targetTableSysId

</td><td>

String

</td><td>

Sys\_id of the record on which to attach the converted PDF.

</td></tr><tr><td>

svgImgWidth

</td><td>

Number

</td><td>

Width of the SVG image in pixels.

</td></tr><tr><td>

svgImgHeight

</td><td>

Number

</td><td>

Height of the SVG image in pixels.

</td></tr></tbody>
</table><table id="table_hms_ycm_j4b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing sys\_id of the PDF attachment converted from SVG if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td>

If SVG conversion is successful, sys\_id of the attached PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Converting SVG image to PDF document failed.
-   Exception while reading Source document contents.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   The Target table name - &lt;tableName&gt; to attach the converted SVG is not valid
-   The Target table name - &lt;tableName&gt; to attach the converted SVG is empty or null
-   SVG to PDF conversion is successful.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how get SVG from the description field of an incident record, to convert the SVG to PDF, and attach it to a record.

```
var gr = new GlideRecord("incident");

var svg;

if (gr.get("<tableSysId>")) {
 svg = gr.description.toString();
}

var v = new sn_pdfgeneratorutils.SVGToPDFConversionAPI();

var result = v.convertSVGToPDFWithSize(svg, "ConvertSVGToPDF", "incident", "<targetTableSysId>", 600, 150);
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"<pdf_attachment_sys_id>","message":"SVG to PDF conversion is successful.","status":"success"}
```

