---
title: PDFGenerationAPI - Scoped, Global
description: The PDFGenerationAPI provides support for PDF conversion and handling PDF fields.Instantiates a new PDFGenerationAPI object.Converts an HTML string to a PDF document.Stages a job that converts an HTML string to a PDF document asynchronously. Asynchronous processing enables you to work in the instance while the PDF conversion is in progress. This is especially helpful for larger PDF exports.Converts an HTML string into a PDF with header and footer content.Stages a job that converts an HTML string into a PDF with header and footer content asynchronously. Asynchronous processing enables you to work in the instance while the PDF conversion is in progress. This is especially helpful for larger PDF exports.Fills fields in an editable PDF and attaches it to the provided record.Fills fields in an editable PDF, flattens the data fields, and attaches it to the provided record.Fills fields in an editable PDF, adds signature image, flattens the data fields, and attaches it to the provided record.Gets a list of editable fields in a PDF document. Enables listing editable PDF fields without manually opening the file to check.Gets the field type of set of editable fields from a PDF document.Fills fields in an editable PDF, creates an image, and converts it to a Base64-encoded PDF.Gets the page size of a PDF document.Checks if the PDF document contains editable fields.Applies redaction to a PDF document based on the given rectangle coordinates, search keywords, or both. A redacted copy of the original PDF is generated in the Attachments \[sys\_attachment\] table.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-01-15"
reading_time_minutes: 46
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PDFGenerationAPI - Scoped, Global

The PDFGenerationAPI provides support for PDF conversion and handling PDF fields.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

Use the **glide.pdf.url.whitelist** property to add an extra layer of validation to ensure whether any external URL introduced should be included in the generated PDF. If the system property glide.pdf.url.whitelisting.enabled is set to true, the PDF does not process URL content unless it is listed in the Value field of the com.snc.pdf.whitelisted\_urls system property. These properties are listed in the System Properties \[sys\_properties\] table. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:** The maximum PDF size is 50 MB.

The methods in this class enable the following tasks:

-   Dynamically generate a PDF from an HTML string and attach it to a record
    -   A4 size without headers or footers – [PDFGenerationAPI – convertToPDF\(String html, String targetTable, String targetTableSysId, String pdfName, String fontFamilySysId, Object documentConfiguration\)](PDFGenerationAPIBothAPI.md#)
    -   Customizable page size with options for header and footer – [PDFGenerationAPI – convertToPDFWithHeaderFooter\(String html, String targetTable, String targetTableSysId, String pdfName, Object headerFooterInfo, String fontFamilySysId, Object documentConfiguration\)](PDFGenerationAPIBothAPI.md#)
-   Queue a PDF to be generated from an HTML string and attached to a record
    -   A4 size without headers or footers – [PDFGenerationAPI – convertToPDFAsync\(String html, String targetTable, String targetTableSysId, String pdfName, String fontFamilySysId, Object documentConfiguration\)](PDFGenerationAPIBothAPI.md#)
    -   Customizable page size with options for header and footer – [PDFGenerationAPI – convertToPDFWithHeaderFooterAsync\(String html, String targetTable, String targetTableSysId, String pdfName, Object headerFooterInfo, String fontFamilySysId, Object documentConfiguration\)](PDFGenerationAPIBothAPI.md#)
-   Fill fields in a PDF
    -   [PDFGenerationAPI – fillDocumentFieldsAndFlatten\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName, Object flatten\)](PDFGenerationAPIBothAPI.md#)
    -   [PDFGenerationAPI – fillDocumentFields\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName\)](PDFGenerationAPIBothAPI.md#)
    -   [PDFGenerationAPI – isDocumentFillable\(String sysId\)](PDFGenerationAPIBothAPI.md#)
-   Sign a PDF
    -   [PDFGenerationAPI – fillFieldsAndMergeSignature\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName, PdfMergeSignRequestor requestor, Object flatten\)](PDFGenerationAPIBothAPI.md#)
    -   [PDFGenerationAPI – getFilledDocumentWithSignatureAsBase64\(Object fieldsMap, String sysId, PdfMergeSignRequestor requestor, Object flatten\)](PDFGenerationAPIBothAPI.md#)
-   Restrict editing filled fields as flattened or partially flattened – [PDFGenerationAPI – fillDocumentFieldsAndFlatten\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName, Object flatten\)](PDFGenerationAPIBothAPI.md#)
-   Retrieve PDF page size and field data
    -   [PDFGenerationAPI – getPdfPageSizes\(String sysId\)](PDFGenerationAPIBothAPI.md#)
    -   [PDFGenerationAPI – getDocumentFieldsType\(String sysId\)](PDFGenerationAPIBothAPI.md#)
    -   [PDFGenerationAPI – getDocumentFields\(String sysId\)](PDFGenerationAPIBothAPI.md#)
-   Redact information in a PDF – [PDFGenerationAPI – redact\(Object inputJson\)](PDFGenerationAPIBothAPI.md#)

**Note:** These methods can also be used for documents created by non-catalog items.

Related APIs:

-   [PdfMergeSignRequestor](../../PdfMergeSignRequestorBoth/concept/PdfMergeSignRequestorBothAPI.md#)
-   [SVGToPDFConversionAPI](../../SVGToPDFConversionAPIBoth/concept/SVGToPDFConversionAPBothAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PDFGenerationAPI – PDFGenerationAPI\(\)

Instantiates a new PDFGenerationAPI object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to create a PDFGenerationAPI object.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
```

## PDFGenerationAPI – convertToPDF\(String html, String targetTable, String targetTableSysId, String pdfName, String fontFamilySysId, Object documentConfiguration\)

Converts an HTML string to a PDF document.

This method creates a PDF using the page size A4 – 595 × 842 points. Content will be truncated if it exceeds this size.

To generate a PDF with additional settings, such as page size, orientation, and page numbers, use [convertToPDFWithHeaderFooter\(\)](PDFGenerationAPIBothAPI.md#).

<table id="table_sj4_p5j_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

html

</td><td>

String

</td><td>

HTML to convert to a PDF document.

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

fontFamilySysId

</td><td>

String

</td><td>

Optional. Sys\_id of the font family to use for the PDF. This sys\_id is from the PDF Generation Font Family \[sys\_pdf\_generation\_font\_family\] table.Default: none

</td></tr><tr><td>

documentConfiguration

</td><td>

Object

</td><td>

Optional. Object containing a table of contents configuration and a page number configuration.```
{​
   "accessibilityEnabled" : Boolean,
   "toc_config" : "String",​
   "page_number_config": "String"​
}​
```

</td></tr><tr><td>

documentConfiguration.accessibilityEnabled

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to format the generated PDF to support accessibility. When this feature is enabled, accessibility tags will be available in the PDF tag tree to help users who rely on screen readers to navigate, understand, and interact with the generated PDF documents.Valid values:

-   true: The generated PDF is formatted for accessibility.
-   false: The generated PDF is not formatted for accessibility.

Default: False

</td></tr><tr><td>

documentConfiguration.toc\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the table of contents configuration to use for the PDF. This sys\_id is from the Table of Contents Configuration \[doc\_toc\_config\] table.Default: none

</td></tr><tr><td>

documentConfiguration.page\_number\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the page number configuration to use for the PDF. This sys\_id is from the Page Number Configuration \[doc\_page\_number\_config\] table.Default: none

</td></tr></tbody>
</table><table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing sys\_id of the PDF attachment if conversion is successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "request_id": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td>

If HTML conversion is successful, sys\_id of the converted and attached PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Conversion failed. – No PDF created. Make sure the values provided are accurate.
-   Conversion is successful. – The HTML successfully converted to PDF.
-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.
-   &lt;URL&gt; is not listed in whitelisted URL, please check URL whitelisting property : "glide.pdf.url.whitelisting.enabled" and "com.snc.pdf.whitelisted\_urls" – If the system property glide.pdf.url.whitelisting.enabled is set to true, the PDF does not process URL content unless it is listed in the Value field of the com.snc.pdf.whitelisted\_urls system property. These properties are listed in the System Properties \[sys\_properties\] table.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the change producer request record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to convert HTML to a PDF and attach it to a record in the Incident \[incident\] table.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;

//  (Option) get HTML from the description field of an incident record
var gr = new GlideRecord("incident");
var html;

if (gr.get("<tableSysId>")) {
 html = gr.description.toString();
}

var result = v.convertToPDF(html, "incident", "<target_sys_id>", "myPDF");
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"<sys_id>","message":"Conversion is successful.","request_id":"<change_sys_id>","status":"success"}
```

## PDFGenerationAPI – convertToPDFAsync\(String html, String targetTable, String targetTableSysId, String pdfName, String fontFamilySysId, Object documentConfiguration\)

Stages a job that converts an HTML string to a PDF document asynchronously. Asynchronous processing enables you to work in the instance while the PDF conversion is in progress. This is especially helpful for larger PDF exports.

This API creates a PDF using the page size A4 – 595 × 842 points. Content will be truncated if it exceeds this size.

To generate a PDF with additional settings, such as page size, orientation, and page numbers, use [convertToPDFWithHeaderFooterAsync\(\)](PDFGenerationAPIBothAPI.md#).

<table id="table_sj4_p5j_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

html

</td><td>

String

</td><td>

HTML to convert to a PDF document.

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

fontFamilySysId

</td><td>

String

</td><td>

Optional. Sys\_id of the font family to use for the PDF. This sys\_id is from the PDF Generation Font Family \[sys\_pdf\_generation\_font\_family\] table.Default: none

</td></tr><tr><td>

documentConfiguration

</td><td>

Object

</td><td>

Optional. Object containing a table of contents configuration and a page number configuration.```
{​
   "accessibilityEnabled" : Boolean,
   "toc_config" : "String",​
   "page_number_config": "String"​
}​
```

</td></tr><tr><td>

documentConfiguration.accessibilityEnabled

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to format the generated PDF to support accessibility. When this feature is enabled, accessibility tags will be available in the PDF tag tree to help users who rely on screen readers to navigate, understand, and interact with the generated PDF documents.Valid values:

-   true: The generated PDF is formatted for accessibility.
-   false: The generated PDF is not formatted for accessibility.

Default: False

</td></tr><tr><td>

documentConfiguration.toc\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the table of contents configuration to use for the PDF. This sys\_id is from the Table of Contents Configuration \[doc\_toc\_config\] table.Default: none

</td></tr><tr><td>

documentConfiguration.page\_number\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the page number configuration to use for the PDF. This sys\_id is from the Page Number Configuration \[doc\_page\_number\_config\] table.Default: none

</td></tr></tbody>
</table><table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object indicating whether the PDF conversion is in progress. You can review the conversion status in the PDF Generation Status \[sys\_pdf\_generation\_status\] table.```
{
  "message": "String",
  "request_id": "String"
}
```

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   HTML to PDF Conversion is in progress. – Request to convert HTML to a PDF document is successful.
-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.
-   &lt;URL&gt; is not listed in whitelisted URL, please check URL whitelisting property : "glide.pdf.url.whitelisting.enabled" and "com.snc.pdf.whitelisted\_urls" – If the system property glide.pdf.url.whitelisting.enabled is set to true, the PDF does not process URL content unless it is listed in the Value field of the com.snc.pdf.whitelisted\_urls system property. These properties are listed in the System Properties \[sys\_properties\] table.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the change producer request record.Data type: String

</td></tr></tbody>
</table>The following example shows how to queue a task that converts HTML to a PDF. When the conversion is complete, the PDF named "myPDF" is attached to the target record in the Incident \[incident\] table.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;

//  (Option) get HTML from the description field of an incident record
var gr = new GlideRecord("incident");
var html;

if (gr.get("<tableSysId>")) {
 html = gr.description.toString();
}

var result = v.convertToPDFAsync(html, "incident", "<target_sys_id>", "myPDF");
gs.info(JSON.stringify(result));
```

Output:

```
{"message":"HTML to PDF Conversion is in progress.","request_id":"<sys_id>"}
```

## PDFGenerationAPI – convertToPDFWithHeaderFooter\(String html, String targetTable, String targetTableSysId, String pdfName, Object headerFooterInfo, String fontFamilySysId, Object documentConfiguration\)

Converts an HTML string into a PDF with header and footer content.

Use this method to generate PDFs with page settings:

-   Header and footer information
-   Margin sizes
-   Orientation
-   Enumeration
-   Page size

<table id="table_hmj_q5j_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

html

</td><td>

String

</td><td>

HTML to convert to a PDF document.

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

headerFooterInfo

</td><td>

Object

</td><td>

Defines PDF header and footer details.```
{
  "FooterImageAlignment": "String",
  "FooterImageAttachmentId": "String",
  "FooterImageHeight": "String",
  "FooterText": "String",
  "FooterTextAlignment": "String",
  "GeneratePageNumber": "String",
  "HeaderImageAlignment": "String",
  "HeaderImageAttachmentId": "String",
  "HeaderImageHeight": "String",
  "LeftOrRightMargin": "String",
  "PageOrientation": "String",
  "PageSize": "String",
  "TopOrBottomMargin": "String"
}
```

</td></tr><tr><td>

headerFooterInfo.​FooterImageAlignment

</td><td>

String

</td><td>

Sets the image position in the footer.Valid values:

-   BOTTOM\_CENTER: Position the image in the bottom center of the footer.
-   BOTTOM\_LEFT: Position the image in the bottom left area of the footer.
-   BOTTOM\_RIGHT: Position the image in the bottom right area of the footer.
-   TOP\_CENTER: Position the image in the top center of the footer.
-   TOP\_LEFT: Position the image in the top left area of the footer.
-   TOP\_RIGHT: Position the image in the top right area of the footer.

</td></tr><tr><td>

headerFooterInfo.​FooterImageAttachmentId

</td><td>

String

</td><td>

Sys\_id of the footer image in the Attachments \[sys\_attachment\] table.To determine if the file type is supported in your instance, Navigate to **System Properties**, **Security**, and check if it's listed in **List of file extensions \(comma-separated\) that can be attached** field.

</td></tr><tr><td>

headerFooterInfo.​FooterImageHeight

</td><td>

String

</td><td>

Height of footer image.Default: 50 points

</td></tr><tr><td>

headerFooterInfo.​FooterText

</td><td>

String

</td><td>

Footer text to place at the bottom of each PDF page.

</td></tr><tr><td>

headerFooterInfo.​FooterTextAlignment

</td><td>

String

</td><td>

Sets the text position in the footer. Make sure this value does not match or conflict with the area provided in **headerFooterInfo.FooterImageAlignment**.Valid values:

-   BOTTOM\_CENTER: Position the text in the bottom center of the footer.
-   BOTTOM\_LEFT: Position the text in the bottom left area of the footer.
-   BOTTOM\_RIGHT: Position the text in the bottom right area of the footer.
-   TOP\_CENTER: Position the text in the top center of the footer.
-   TOP\_LEFT: Position the text in the top left area of the footer.
-   TOP\_RIGHT: Position the text in the top right area of the footer.

</td></tr><tr><td>

headerFooterInfo.​GeneratePageNumber

</td><td>

String

</td><td>

Flag that indicates whether to generate a PDF page number.Valid values:

-   true: Generate page numbers.
-   false: Do not generate page numbers.

 Default: true

</td></tr><tr><td>

headerFooterInfo.​HeaderImageAlignment

</td><td>

String

</td><td>

Sets the image position in the header.Valid values:

-   center: Position the image in the center of the header.
-   left: Position the image on the left side of the header.
-   right: Position the image on the right side of the header.

</td></tr><tr><td>

headerFooterInfo.​HeaderImageAttachmentId

</td><td>

String

</td><td>

Sys\_id of the header image in the Attachments \[sys\_attachment\] table.To determine if the file type is supported in your instance, Navigate to **System Properties**, **Security**, and check if it's listed in **List of file extensions \(comma-separated\) that can be attached** field.

</td></tr><tr><td>

headerFooterInfo.​HeaderImageHeight

</td><td>

String

</td><td>

Height of the header image. Default: 50 points

</td></tr><tr><td>

headerFooterInfo.​LeftOrRightMargin

</td><td>

String

</td><td>

Size of the left and right margins. If positioned in the left or right side of the page, header/footer details are placed within in this area.Default: 36 points

</td></tr><tr><td>

headerFooterInfo.​PageOrientation

</td><td>

String

</td><td>

Page orientation.Valid values:

-   PORTRAIT
-   LANDSCAPE

Default: Portrait

</td></tr><tr><td>

headerFooterInfo.​PageSize

</td><td>

String

</td><td>

Document page size.Valid values:

-   A4 – 595 × 842 points
-   LETTER – 612 × 792 points
-   LEDGER – 792 x 1224 points

Content will be truncated if it exceeds the page size.

</td></tr><tr><td>

headerFooterInfo.​TopOrBottomMargin

</td><td>

String

</td><td>

Size of the top and bottom margins. Header and footer details are placed within in this area.Default: 72 points

</td></tr><tr><td>

fontFamilySysId

</td><td>

String

</td><td>

Optional. Sys\_id of the font family to use for the PDF. This sys\_id is from the PDF Generation Font Family \[sys\_pdf\_generation\_font\_family\] table.Default: none

</td></tr><tr><td>

documentConfiguration

</td><td>

Object

</td><td>

Optional. Object containing a table of contents configuration and a page number configuration.```
{​
   "accessibilityEnabled" : Boolean,
   "toc_config" : "String",​
   "page_number_config": "String"​
}​
```

</td></tr><tr><td>

documentConfiguration.accessibilityEnabled

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to format the generated PDF to support accessibility. When this feature is enabled, accessibility tags will be available in the PDF tag tree to help users who rely on screen readers to navigate, understand, and interact with the generated PDF documents.Valid values:

-   true: The generated PDF is formatted for accessibility.
-   false: The generated PDF is not formatted for accessibility.

Default: False

</td></tr><tr><td>

documentConfiguration.toc\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the table of contents configuration to use for the PDF. This sys\_id is from the Table of Contents Configuration \[doc\_toc\_config\] table.Default: none

</td></tr><tr><td>

documentConfiguration.page\_number\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the page number configuration to use for the PDF. This sys\_id is from the Page Number Configuration \[doc\_page\_number\_config\] table.Default: none

</td></tr></tbody>
</table><table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing sys\_id of the PDF attachment if conversion is successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "request_id": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td>

If HTML conversion is successful, sys\_id of the converted and attached PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.​message

</td><td>

Message confirming success or error. Possible values:

-   Conversion failed. – No PDF created. Make sure the values provided are accurate.
-   Conversion is successful. – The HTML successfully converted to PDF.
-   Footer Image alignment and text alignment cannot be in the same region with same alignment: &lt;footerImageAlignment value&gt; – Make sure that **headerFooterInfo.​FooterImageAlignment** and **headerFooterInfo.​FooterTextAlignment** values are not in the same area.
-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   Invalid footer image alignment: &lt;invalid\_option&gt; is provided. – Provide a valid option in the **headerFooterInfo.​FooterImageAlignment** property.
-   Invalid footer text alignment: " + &lt;invalid\_option&gt; + " is provided. – Provide a valid option in the **headerFooterInfo.​footerTextAlignment** property.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Unable to get the footer image. sysId: + &lt;value provided&gt; – Make sure the sys\_id provided for **headerFooterInfo.​footerImageId** is accurate.
-   Unable to get the header image. sysId: + &lt;value provided&gt; – Make sure the sys\_id provided for **headerFooterInfo.​headerImageId** is accurate.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.
-   &lt;URL&gt; is not listed in whitelisted URL, please check URL whitelisting property : "glide.pdf.url.whitelisting.enabled" and "com.snc.pdf.whitelisted\_urls" – If the system property glide.pdf.url.whitelisting.enabled is set to true, the PDF does not process URL content unless it is listed in the Value field of the com.snc.pdf.whitelisted\_urls system property. These properties are listed in the System Properties \[sys\_properties\] table.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the change producer request record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to convert HTML to a PDF named "myPDF" and add the PDF as an attachment to a record in the Incident \[incident\] table. The PDF contains header and footer provided via attachment.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;

//  (Option) get HTML from the description field of an incident record
var gr = new GlideRecord("incident");
var html;

if (gr.get("<tableSysId>")) {
 html = gr.description.toString();
}

var hfInfo = new Object();
hfInfo["HeaderImageAttachmentId"] = "<hdrImgAttSysId>";
hfInfo["HeaderImageAlignment"] = "left";
hfInfo["FooterImageAttachmentId"] = "<ftrImgAttSysId>";
hfInfo["FooterImageAlignment"] = "TOP_CENTER";
hfInfo["FooterText"] = "Sample Footer Message";
hfInfo["PageSize"] = "A4";
hfInfo["GeneratePageNumber"] = "false";
hfInfo["TopOrBottomMargin"] = "36";
hfInfo["LeftOrRightMargin"] = "24";

var result = v.convertToPDFWithHeaderFooter(html, "incident", "<targetTbl_sys_id>", "myPDF", hfInfo);
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"<sys_id>","message":"Conversion is successful.","request_id":"<change_sys_id>","status":"success"}
```

## PDFGenerationAPI – convertToPDFWithHeaderFooterAsync\(String html, String targetTable, String targetTableSysId, String pdfName, Object headerFooterInfo, String fontFamilySysId, Object documentConfiguration\)

Stages a job that converts an HTML string into a PDF with header and footer content asynchronously. Asynchronous processing enables you to work in the instance while the PDF conversion is in progress. This is especially helpful for larger PDF exports.

Use this method to generate PDFs with page settings:

-   Header and footer information
-   Margin sizes
-   Orientation
-   Enumeration
-   Page size

<table id="table_hmj_q5j_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

html

</td><td>

String

</td><td>

HTML to convert to a PDF document.

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

headerFooterInfo

</td><td>

Object

</td><td>

Defines PDF header and footer details.```
{
  "FooterImageAlignment": "String",
  "FooterImageAttachmentId": "String",
  "FooterImageHeight": "String",
  "FooterText": "String",
  "FooterTextAlignment": "String",
  "GeneratePageNumber": "String",
  "HeaderImageAlignment": "String",
  "HeaderImageAttachmentId": "String",
  "HeaderImageHeight": "String",
  "LeftOrRightMargin": "String",
  "PageOrientation": "String",
  "PageSize": "String",
  "TopOrBottomMargin": "String"
}
```

</td></tr><tr><td>

headerFooterInfo.​FooterImageAlignment

</td><td>

String

</td><td>

Sets the image position in the footer.Valid values:

-   BOTTOM\_CENTER: Position the image in the bottom center of the footer.
-   BOTTOM\_LEFT: Position the image in the bottom left area of the footer.
-   BOTTOM\_RIGHT: Position the image in the bottom right area of the footer.
-   TOP\_CENTER: Position the image in the top center of the footer.
-   TOP\_LEFT: Position the image in the top left area of the footer.
-   TOP\_RIGHT: Position the image in the top right area of the footer.

</td></tr><tr><td>

headerFooterInfo.​FooterImageAttachmentId

</td><td>

String

</td><td>

Sys\_id of the footer image in the Attachments \[sys\_attachment\] table.To determine if the file type is supported in your instance, Navigate to **System Properties**, **Security**, and check if it's listed in **List of file extensions \(comma-separated\) that can be attached** field.

</td></tr><tr><td>

headerFooterInfo.​FooterImageHeight

</td><td>

String

</td><td>

Height of footer image.Default: 50 points

</td></tr><tr><td>

headerFooterInfo.​FooterText

</td><td>

String

</td><td>

Footer text to place at the bottom of each PDF page.

</td></tr><tr><td>

headerFooterInfo.​FooterTextAlignment

</td><td>

String

</td><td>

Sets the text position in the footer. Make sure this value does not match or conflict with the area provided in **headerFooterInfo.FooterImageAlignment**.Valid values:

-   BOTTOM\_CENTER: Position the text in the bottom center of the footer.
-   BOTTOM\_LEFT: Position the text in the bottom left area of the footer.
-   BOTTOM\_RIGHT: Position the text in the bottom right area of the footer.
-   TOP\_CENTER: Position the text in the top center of the footer.
-   TOP\_LEFT: Position the text in the top left area of the footer.
-   TOP\_RIGHT: Position the text in the top right area of the footer.

</td></tr><tr><td>

headerFooterInfo.​GeneratePageNumber

</td><td>

String

</td><td>

Flag that indicates whether to generate a PDF page number.Valid values:

-   true: Generate page numbers.
-   false: Do not generate page numbers.

 Default: true

</td></tr><tr><td>

headerFooterInfo.​HeaderImageAlignment

</td><td>

String

</td><td>

Sets the image position in the header.Valid values:

-   center: Position the image in the center of the header.
-   left: Position the image on the left side of the header.
-   right: Position the image on the right side of the header.

</td></tr><tr><td>

headerFooterInfo.​HeaderImageAttachmentId

</td><td>

String

</td><td>

Sys\_id of the header image in the Attachments \[sys\_attachment\] table.To determine if the file type is supported in your instance, Navigate to **System Properties**, **Security**, and check if it's listed in **List of file extensions \(comma-separated\) that can be attached** field.

</td></tr><tr><td>

headerFooterInfo.​HeaderImageHeight

</td><td>

String

</td><td>

Height of the header image. Default: 50 points

</td></tr><tr><td>

headerFooterInfo.​LeftOrRightMargin

</td><td>

String

</td><td>

Size of the left and right margins. If positioned in the left or right side of the page, header/footer details are placed within in this area.Default: 36 points

</td></tr><tr><td>

headerFooterInfo.​PageOrientation

</td><td>

String

</td><td>

Page orientation.Valid values:

-   PORTRAIT
-   LANDSCAPE

Default: Portrait

</td></tr><tr><td>

headerFooterInfo.​PageSize

</td><td>

String

</td><td>

Document page size.Valid values:

-   A4 – 595 × 842 points
-   LETTER – 612 × 792 points
-   LEDGER – 792 x 1224 points

Content will be truncated if it exceeds the page size.

</td></tr><tr><td>

headerFooterInfo.​TopOrBottomMargin

</td><td>

String

</td><td>

Size of the top and bottom margins. Header and footer details are placed within in this area.Default: 72 points

</td></tr><tr><td>

fontFamilySysId

</td><td>

String

</td><td>

Optional. Sys\_id of the font family to use for the PDF. This sys\_id is from the PDF Generation Font Family \[sys\_pdf\_generation\_font\_family\] table.Default: none

</td></tr><tr><td>

documentConfiguration

</td><td>

Object

</td><td>

Optional. Object containing a table of contents configuration and a page number configuration.```
{​
   "accessibilityEnabled" : Boolean,
   "toc_config" : "String",​
   "page_number_config": "String"​
}​
```

</td></tr><tr><td>

documentConfiguration.accessibilityEnabled

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to format the generated PDF to support accessibility. When this feature is enabled, accessibility tags will be available in the PDF tag tree to help users who rely on screen readers to navigate, understand, and interact with the generated PDF documents.Valid values:

-   true: The generated PDF is formatted for accessibility.
-   false: The generated PDF is not formatted for accessibility.

Default: False

</td></tr><tr><td>

documentConfiguration.toc\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the table of contents configuration to use for the PDF. This sys\_id is from the Table of Contents Configuration \[doc\_toc\_config\] table.Default: none

</td></tr><tr><td>

documentConfiguration.page\_number\_config

</td><td>

String

</td><td>

Optional. Sys\_id of the page number configuration to use for the PDF. This sys\_id is from the Page Number Configuration \[doc\_page\_number\_config\] table.Default: none

</td></tr></tbody>
</table><table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

 

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.​message

</td><td>

Message confirming success or error. Possible values:

-   HTML to PDF Conversion is in progress. – Request to convert HTML to a PDF document is successful.
-   Footer Image alignment and text alignment cannot be in the same region with same alignment: &lt;footerImageAlignment value&gt; – Make sure that **headerFooterInfo.​FooterImageAlignment** and **headerFooterInfo.​FooterTextAlignment** values are not in the same area.
-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   Invalid footer image alignment: &lt;invalid\_option&gt; is provided. – Provide a valid option in the **headerFooterInfo.​FooterImageAlignment** property.
-   Invalid footer text alignment: " + &lt;invalid\_option&gt; + " is provided. – Provide a valid option in the **headerFooterInfo.​footerTextAlignment** property.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Unable to get the footer image. sysId: + &lt;value provided&gt; – Make sure the sys\_id provided for **headerFooterInfo.​footerImageId** is accurate.
-   Unable to get the header image. sysId: + &lt;value provided&gt; – Make sure the sys\_id provided for **headerFooterInfo.​headerImageId** is accurate.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.
-   &lt;URL&gt; is not listed in whitelisted URL, please check URL whitelisting property : "glide.pdf.url.whitelisting.enabled" and "com.snc.pdf.whitelisted\_urls" – If the system property glide.pdf.url.whitelisting.enabled is set to true, the PDF does not process URL content unless it is listed in the Value field of the com.snc.pdf.whitelisted\_urls system property. These properties are listed in the System Properties \[sys\_properties\] table.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the change producer request record.Data type: String

</td></tr></tbody>
</table>The following example shows how to queue a task that converts HTML to a PDF. The PDF contains header and footer provided via attachment. When the conversion is complete, the PDF named "myPDF" is attached to the target record in the Incident \[incident\] table.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;

//  (Option) get HTML from the description field of an incident record
var gr = new GlideRecord("incident");
var html;

if (gr.get("<tableSysId>")) {
 html = gr.description.toString();
}

var hfInfo = new Object();
hfInfo["HeaderImageAttachmentId"] = "<hdrImgAttSysId>";
hfInfo["HeaderImageAlignment"] = "left";
hfInfo["FooterImageAttachmentId"] = "<ftrImgAttSysId>";
hfInfo["FooterImageAlignment"] = "TOP_CENTER";
hfInfo["FooterText"] = "Sample Footer Message";
hfInfo["PageSize"] = "A4";
hfInfo["GeneratePageNumber"] = "false";
hfInfo["TopOrBottomMargin"] = "36";
hfInfo["LeftOrRightMargin"] = "24";

var result = v.convertToPDFWithHeaderFooterAsync(html, "incident", "<targetTbl_sys_id>", "myPDF", hfInfo);
gs.info(JSON.stringify(result));
```

Output:

```
{"message":"HTML to PDF Conversion is in progress.","request_id":"<sys_id>"}
```

## PDFGenerationAPI – fillDocumentFields\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName\)

Fills fields in an editable PDF and attaches it to the provided record.

Use the following methods to determine if the PDF is fillable and get field information:

-   [isDocumentFillable\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFields\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFieldsType\(\)](PDFGenerationAPIBothAPI.md#)

PDFGenerationAPI provides additional fill methods with different options:

-   [fillDocumentFieldsAndFlatten\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, flattens the data fields, and attaches it to the provided record.
-   [fillFieldsAndMergeSignature\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, adds signature image, flattens the data fields, and attaches it to the provided record.
-   [getFilledDocumentWithSignatureAsBase64\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, creates an image, and converts it to a Base64-encoded PDF.

<table id="table_ohl_lzj_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldsMap

</td><td>

Object

</td><td>

Optional. Key value map by PDF field name and value to fill. Use the getDocumentFields\(\) method to get the list of available fields.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td id="ent_api_pdfgen_parm_attSysIDesc">

Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td id="entry-api-pdfgen-tblName">

Name of the table containing the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

tableSysId

</td><td>

String

</td><td id="entry-api-pdfgen-tblID">

Sys\_id of the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

pdfName

</td><td>

String

</td><td>

Name to give the PDF.Default: Sys\_id of the PDF in the Attachments \[sys\_attachment\] table.

</td></tr></tbody>
</table><table id="table_phl_lzj_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td id="desc-fill-only">

Object containing sys\_id of the updated PDF attachment if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td id="desc_pdfgen_ret_attID_Fill">

If the operation is successful, sys\_id of the filled PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Valid values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to fill fields in an editable PDF.

```
var fieldMap = new Object();
fieldMap["Address"] = "Address value here";
fieldMap["State"] = "State value here";

var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.fillDocumentFields(fieldMap, "<attachmentSysId>", "<tableName>", "<tableSysId>", "pdfName");
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"<sys_id>","message":"Request completed successfully.","status":"success"}
```

## PDFGenerationAPI – fillDocumentFieldsAndFlatten\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName, Object flatten\)

Fills fields in an editable PDF, flattens the data fields, and attaches it to the provided record.

Use the following methods to determine if the PDF is fillable and get field information:

-   [isDocumentFillable\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFields\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFieldsType\(\)](PDFGenerationAPIBothAPI.md#)

PDFGenerationAPI provides additional fill methods with different options:

-   [fillDocumentFields\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF and attaches it to the provided record.
-   [fillFieldsAndMergeSignature\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, adds signature image, flattens the data fields, and attaches it to the provided record.
-   [getFilledDocumentWithSignatureAsBase64\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, creates an image, and converts it to a Base64-encoded PDF.

<table id="table_xp4_thk_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldsMap

</td><td>

Object

</td><td>

Optional. Key value map by PDF field name and value to fill. Use the getDocumentFields\(\) method to get the list of available fields.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td id="ent_api_pdfgen_parm_attSysIDesc">

Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td id="entry-api-pdfgen-tblName">

Name of the table containing the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

tableSysId

</td><td>

String

</td><td id="entry-api-pdfgen-tblID">

Sys\_id of the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

pdfName

</td><td>

String

</td><td>

Name to give the PDF.Default: Sys\_id of the PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

flatten

</td><td>

Object

</td><td>

Optional. Flattening fields enable locking the fields so that other users cannot change the information. Specify the key as "FlattenType" and provide a flattening option as a string.Valid values:

-   donot\_flatten - Do not flatten any fields.
-   partially\_flatten - Flatten only the fields which are modified.
-   fully\_flatten - Flattens all the fields.

Default: fully\_flatten

```
{
  "FlattenType": "String" 
}
```

</td></tr></tbody>
</table><table id="table_phl_lzj_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td id="desc-fill-only">

Object containing sys\_id of the updated PDF attachment if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td id="desc_pdfgen_ret_attID_Fill">

If the operation is successful, sys\_id of the filled PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Valid values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to fill fields and flatten an editable PDF.

```
var fieldMap = new Object();
fieldMap["Last Name First Name Middle Initial"] = "Tuter Abel E.";
fieldMap["Date of Birth"] = "08101952";
fieldMap["US SSN"] = "111-22-9999";
fieldMap["Address"] = "PO Box 344";
fieldMap["City"] = "Jerome";
fieldMap["State"] = "AZ";
fieldMap["Zip"] = "86331";

var flatten = new Object();
flatten["FlattenType"] = "partially_flatten";

var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.fillDocumentFieldsAndFlatten(fieldMap, "<attachmentSysId>", "<tableName>", "<tableSysId>", "pdfName", flatten);
gs.info(JSON.stringify(result));
```

Output:

```
"attachment_id":"<sys_id>","message":"Request completed successfully.","status":"success"
```

## PDFGenerationAPI – fillFieldsAndMergeSignature\(Object fieldsMap, String sysId, String tableName, String tableSysId, String pdfName, PdfMergeSignRequestor requestor, Object flatten\)

Fills fields in an editable PDF, adds signature image, flattens the data fields, and attaches it to the provided record.

Use the following methods to determine if the PDF is fillable and get field information:

-   [isDocumentFillable\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFields\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFieldsType\(\)](PDFGenerationAPIBothAPI.md#)

PDFGenerationAPI provides additional fill methods with different options:

-   [fillDocumentFields\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF and attaches it to the provided record.
-   [fillDocumentFieldsAndFlatten\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, flattens the data fields, and attaches it to the provided record.
-   [getFilledDocumentWithSignatureAsBase64\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, creates an image, and converts it to a Base64-encoded PDF.

<table id="table_xp4_thk_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldsMap

</td><td>

Object

</td><td>

Optional. Key value map by PDF field name and value to fill. Use the getDocumentFields\(\) method to get the list of available fields.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td id="ent_api_pdfgen_parm_attSysIDesc">

Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td id="entry-api-pdfgen-tblName">

Name of the table containing the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

tableSysId

</td><td>

String

</td><td id="entry-api-pdfgen-tblID">

Sys\_id of the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

pdfName

</td><td>

String

</td><td>

Name to give the PDF.Default: Sys\_id of the PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

requestor

</td><td>

[PdfMergeSign​Requestor](../../PdfMergeSignRequestorBoth/concept/PdfMergeSignRequestorBothAPI.md#)

</td><td>

Signature input returned from pdfMergeSignRequestor.

</td></tr><tr><td>

flatten

</td><td>

Object

</td><td>

Optional. Flattening fields enable locking the fields so that other users cannot change the information. Specify the key as "FlattenType" and provide a flattening option as a string.Valid values:

-   donot\_flatten - Do not flatten any fields.
-   partially\_flatten - Flatten only the fields which are modified.
-   fully\_flatten - Flattens all the fields.

Default: fully\_flatten

```
{
  "FlattenType": "String" 
}
```

</td></tr></tbody>
</table><table id="table_anm_5hk_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td id="desc-fill-only">

Object containing sys\_id of the updated PDF attachment if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td id="desc_pdfgen_ret_attID_Fill">

If the operation is successful, sys\_id of the filled PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Valid values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to fill fields with signature with default settings to completely flatten the fields.

```
var fieldMap = new Object();
fieldMap["Address_Salutation"] = "Address value here";

var paramMap = new Object();
paramMap["FlattenType"] = "partially_flatten";

var requestor = new sn_pdfgeneratorutils.PdfMergeSignRequestor;
requestor.createRequest("<attachmentSysId>", "incident", "<tableSysId>", "filledPdf");
requestor.addSignatureMapping(6, 40, 50, 188, 44, "<signatureSysId>");

var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.fillFieldsAndMergeSignature(fieldMap, "<attachmentSysId>", "incident", "<tableSysId>", requestor, "filledPdf", paramMap);
gs.info(JSON.stringify(result));
```

Output:

```
{"attachment_id":"5440d993dbed3010d66be1191396194e","message":"Request completed successfully.","status":"success"}
```

## PDFGenerationAPI – getDocumentFields\(String sysId\)

Gets a list of editable fields in a PDF document. Enables listing editable PDF fields without manually opening the file to check.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.|

<table id="table_v1y_g3k_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing ID of the signed PDF, error message otherwise. ```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.fields

</td><td>

If the request is successful, list containing the name of each field in the PDF.Data type: Array of strings

 ```
"fields": ["field_name"]
```

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to retrieve fields in a PDF attachment.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.getDocumentFields("attachmentSysId");
gs.info(JSON.stringify(result));

```

Output:

```
{"message":"Request completed successfully.","fields":["NP_formFillable","reset","print","1SSN","Signature.1","5sigDate","Check Box21"],"status":"success"}
```

## PDFGenerationAPI – getDocumentFieldsType\(String sysId\)

Gets the field type of set of editable fields from a PDF document.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.|

<table id="table_jxx_whk_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing each PDF field type if successful, error message otherwise. ```
{
  "fields_type": {Object},
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.fields\_type

</td><td>

Object listing each field in the specified PDF if successful, error message otherwise.Data type: Object

 ```
"fields_type": {
  "<field type>": {Object},
}
```

</td></tr><tr><td>

&lt;Object&gt;.fields\_type.​&lt;field&gt;

</td><td>

Object containing page number of each field. The &lt;field&gt; name represents the field label, for example, "SSN", or an automated label representing the type.Data type: Object

 ```
"<field>": { 
  "fieldsDetails": [Array], // Check boxes, radio buttons, choice boxes only
  "pageNumber": "String",
  "type": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.fields\_type.​&lt;field&gt;.fieldsDetails

</td><td>

List of objects containing field name and corresponding value of each option for choice field types.Applicable types:

-   Check box
-   Choice box
-   Combo box
-   Multi select choice box

 Data type: Array

 ```
"fieldsDetails": [ 
  "fieldName": "String",
  "value": "String"
]
```

</td></tr><tr><td>

&lt;Object&gt;.fields\_type.​&lt;field&gt;.fieldsDetails.fieldName

</td><td>

Name of a choice field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.fields\_type.​&lt;field&gt;.fieldsDetails.value

</td><td>

Value of a choice field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.fields\_type.​&lt;field&gt;.pageNumber

</td><td>

PDF page number corresponding to this field.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.fields\_type.​&lt;field&gt;.type

</td><td>

PDF field type.Possible values:

-   check\_box
-   choice\_box
-   combo\_box
-   multi\_select\_choice\_box
-   push\_button
-   radio\_button
-   signature
-   text

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to retrieve field types in a PDF attachment. Results include manual returns for readability and are truncated for brevity.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.getDocumentFieldsType("<attachmentSysId>");
gs.info(JSON.stringify(result));

```

Output:

```
{"fields_type":{"1ADDLINE2.25":{"pageNumber":2,"type":"text"},"1ADDLINE2.24":{"pageNumber":2,"type":"text"},
"1ADDLINE2.23":{"pageNumber":2,"type":"text"},"1ADDLINE2.22":{"pageNumber":2,"type":"text"},
"1ADDLINE2.11":{"pageNumber":2,"type":"text"},
"Check Box1":{"fieldsDetails":[{"fieldName":"Yes"}],"pageNumber":2,"type":"check_box"},
"4consentDate.6":{"pageNumber":4,"type":"text"},"4consentDate.7":{"pageNumber":4,"type":"text"},
"3SSN.9":{"pageNumber":3,"type":"text"},"3SSN.8":{"pageNumber":3,"type":"text"},"3SSN.7":{"pageNumber":3,"type":"text"},
"pageNumber":2,"type":"check_box"},"Check Box8":{"fieldsDetails":[{"fieldName":"Off"},{"fieldName":"yes"}],
"4planAdminDate.8":{"pageNumber":4,"type":"text"},"4planAdminDate.7":{"pageNumber":4,"type":"text"},
"1FirstName_ID.7":{"pageNumber":2,"type":"text"},
"Check Box9":{"fieldsDetails":[{"fieldName":"Yes"}],"pageNumber":3,"type":"check_box"},
"1LN.1":{"pageNumber":2,"type":"text"},"1LN.2":{"pageNumber":2,"type":"text"},
"Check Box11":{"fieldsDetails":[{"fieldName":"Yes"}],"pageNumber":3,"type":"check_box"},
"1LN.9":{"pageNumber":2,"type":"text"},
"Check Box17":{"fieldsDetails":[{"fieldName":"Yes"}],"pageNumber":3,"type":"check_box"},
"Check Box16":{"fieldsDetails":[{"fieldName":"Yes"}],"pageNumber":3,"type":"check_box"},
"1LN.7":{"pageNumber":2,"type":"text"},"Check Box19":{"fieldsDetails":[{"fieldName":"Yes"}],
"1LN.8":{"pageNumber":2,"type":"text"},"Check Box18":{"fieldsDetails":[{"fieldName":"Yes"}],
"print":{"pageNumber":2,"type":"push_button"},"4planAdministrator.1":{"pageNumber":4,"type":"text"},
"1TaxID.9":{"pageNumber":2,"type":"text"},"4SSN.1":{"pageNumber":3,"type":"text"},"4SSN.2":{"pageNumber":3,"type":"text"},
"Signature.1":{"pageNumber":4,"type":"text"},"1ZIP.2":{"pageNumber":2,"type":"text"},"1ZIP.3":{"pageNumber":2,"type":"text"},
"message":"Request completed successfully.","status":"success"}
```

## PDFGenerationAPI – getFilledDocumentWithSignatureAsBase64\(Object fieldsMap, String sysId, PdfMergeSignRequestor requestor, Object flatten\)

Fills fields in an editable PDF, creates an image, and converts it to a Base64-encoded PDF.

Base64 encoding enables you to output a PDF as a string within a text document, such as HTML or JSON, without damaging the binary character syntax.

Use the following methods to determine if the PDF is fillable and get field information:

-   [isDocumentFillable\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFields\(\)](PDFGenerationAPIBothAPI.md#)
-   [getDocumentFieldsType\(\)](PDFGenerationAPIBothAPI.md#)

PDFGenerationAPI provides additional fill methods with different options:

-   [fillDocumentFields\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF and attaches it to the provided record.
-   [fillDocumentFieldsAndFlatten\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, flattens the data fields, and attaches it to the provided record.
-   [fillFieldsAndMergeSignature\(\)](PDFGenerationAPIBothAPI.md#) – Fills fields in an editable PDF, adds signature image, flattens the data fields, and attaches it to the provided record.

<table id="table_w4w_xhk_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldsMap

</td><td>

Object

</td><td>

Optional. Key value map by PDF field name and value to fill. Use the getDocumentFields\(\) method to get the list of available fields.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td id="ent_api_pdfgen_parm_attSysIDesc">

Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

requestor

</td><td>

[PdfMergeSign​Requestor](../../PdfMergeSignRequestorBoth/concept/PdfMergeSignRequestorBothAPI.md#)

</td><td>

Signature input returned from pdfMergeSignRequestor.

</td></tr><tr><td>

flatten

</td><td>

Object

</td><td>

Optional. Flattening fields enable locking the fields so that other users cannot change the information. Specify the key as "FlattenType" and provide a flattening option as a string.Valid values:

-   donot\_flatten - Do not flatten any fields.
-   partially\_flatten - Flatten only the fields which are modified.
-   fully\_flatten - Flattens all the fields.

Default: fully\_flatten

```
{
  "FlattenType": "String" 
}
```

</td></tr></tbody>
</table><table id="table_x4w_xhk_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

If successful, PDF converted to Base64 format is added to the Attachments table \[sys\_attachment\]. Contents reflect the PDF attachment provided with fields and signature filled. The fields are not editable unless an alternative flattening option was provided with the **flatten** parameter.

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Valid values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Given target record \[&lt;tableName&gt; - &lt;targetTableSysId&gt;\] does not exist. – Target table sys\_id is not in the table provided. Make sure you include the correct table name for the record.
-   No Form associated with pdf to fill. attachmentSysId: &lt;sys\_id&gt;
-   No editable fields exist with specified names. Please check and try again. field names: &lt;field names&gt;
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to load two fields in a PDF attachment, flatten the fields, and convert the PDF to Base64 format.

```
var mymap = new Object();
mymap["City"] = "City value here";
mymap["State"] = "XX";

// create a requestor
var requestor = new sn_pdfgeneratorutils.PdfMergeSignRequestor;
requestor.createRequest("<sys_id>", "tableName", "<tableSysId>", "pdfName");
requestor.addSignatureMapping(6, 40, 50, 188, 44, "<signImgSysId>");
var processedRequestObj = requestor.processRequest();

var v = new sn_pdfgeneratorutils.PDFGenerationAPI;

var result = v.getFilledDocumentWithSignatureAsBase64(mymap, "<attachmentSysId>", processedRequestObj);
gs.info (JSON.stringify(result));
```

## PDFGenerationAPI – getPdfPageSizes\(String sysId\)

Gets the page size of a PDF document.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.|

<table id="table_v1y_g3k_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the size of each page if successful, error message otherwise. ```
{
  "pages_size": {Object},
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.pages\_size

</td><td>

If the operation is successful, width and height of each PDF page in points. The page number is returned as a string and the measurement values are returned as number data types.Data type: Object

 ```
"pages_size": {"<page number>":[<width>,<height>]}
```

</td></tr><tr id="row_pdfgen_ret_msg"><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to display the width and height of each page in a PDF attachment.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.getPdfPageSizes ("<attachmentSysId>");
gs.info(JSON.stringify(result));

```

Output:

```
{"pages_size":{"1":[612,792],"2":[612,792],"3":[612,792],"4":[612,792],"5":[612,792]},"message":"Request completed successfully.","status":"success"}

```

## PDFGenerationAPI – isDocumentFillable\(String sysId\)

Checks if the PDF document contains editable fields.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.|

<table id="table_erx_h3k_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the size of each page if successful, error message otherwise. ```
{
  "document_editable": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​document\_editable

</td><td>

If the operation is successful, flag indicating whether the document is editable.Valid values:

-   true: PDF document has editable fields.
-   false: PDF document does not have editable fields.

 Data type: Boolean value provided as a string

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to determine if PDF document fields are editable.

```
var v = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = v.isDocumentFillable("<attachmentSysId>");
gs.info(JSON.stringify(result));

```

Output:

```
{"message":"Request completed successfully.","document_editable":"true","status":"success"}
```

## PDFGenerationAPI – redact\(Object inputJson\)

Applies redaction to a PDF document based on the given rectangle coordinates, search keywords, or both. A redacted copy of the original PDF is generated in the Attachments \[sys\_attachment\] table.

**Note:**

-   Redaction results might include an unexpected white redacted text block that overwrites text not intended to be redacted. If this event occurs, you can manually select the content for redaction using the **highlightedSections** property or the PDF Generation Utilities plugin. For more information, see [Redact data from documents](https://www.servicenow.com/docs/access?context=redact-sensitive-data&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   This method doesn’t support redaction in PDFs containing JBIG2 images.

<table id="table_drx_h3k_34b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputJson

</td><td>

Object

</td><td>

Identifies the PDF and its content to be redacted.```
{
  "sysId": "String",
  "highlightedSections": [Array],
  "searchedKeywords": [Array]
}
```

</td></tr><tr><td>

inputJson.sysId

</td><td>

String

</td><td id="ent_api_pdfgen_parm_attSysIDesc">

Sys\_id of a PDF in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

inputJson. highlightedSections

</td><td>

Array of Objects

</td><td>

List of rectangles coordinates provided as an object. Each coordinate represents the location of the content to be redacted on each page.Optional if including the **searchedKeywords** property.

```
[
   {
     "pageNumber": Number,
     "x": Number,
     "y": Number,
     "width": Number,
     "height": Number
   }
]
```

</td></tr><tr><td>

inputJson. highlightedSections. pageNumber

</td><td>

Number

</td><td>

PDF page number containing the content to select for redaction.

</td></tr><tr><td>

inputJson. highlightedSections. x

</td><td>

Number

</td><td>

The X-axis \(horizontal position\) of the redaction rectangle on the PDF in points. The value at the bottom-left corner of the PDF page is 0. For example, a value of `306` places the rectangle approximately in the horizontal center of a letter-size PDF page.

</td></tr><tr><td>

inputJson. highlightedSections. y

</td><td>

Number

</td><td>

The Y-axis \(vertical position\) of the redaction rectangle on the PDF in points. The value at the bottom-left corner of the PDF page is 0. For example, a value of `396` places the rectangle approximately in the vertical center of a letter-size PDF page.

</td></tr><tr><td>

inputJson. highlightedSections. width

</td><td>

Number

</td><td>

Width of the redaction rectangle is in points. This value increases the size of the rectangle horizontally from the lower left point at which the x an y axes intersect.

</td></tr><tr><td>

inputJson. highlightedSections. height

</td><td>

Number

</td><td>

Height of the redaction rectangle in points. This value increases the size of the rectangle vertically from the lower left point at which the x an y axes intersect.

</td></tr><tr><td>

inputJson. searchedKeywords

</td><td>

Array

</td><td>

List of one or more strings used to find text for redaction. The redaction rectangle size matches the height and width of the text that is blocked out as a result.Optional if including the **highlightedSections** property.

**Note:** In some cases, text strings containing special characters or punctuation such as `"items:"` and `"PDF."` aren't redacted. You can alternatively remove the character from the string or highlight the area to remove the text.

</td></tr></tbody>
</table><table id="table_phl_lzj_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td id="desc-fill-only">

Object containing sys\_id of the updated PDF attachment if successful, error message otherwise.```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.​attachment\_id

</td><td id="desc_pdfgen_ret_attID_Fill">

If the operation is successful, sys\_id of the filled PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Can't parse this format – Unable to process an image embedded in the PDF. The PDF contains one or more images in an unsupported format, such as a JBIG2 image.
-   Exception while reading Source document contents. PDF header not found. – Input attachment provided is not a valid PDF. Provide the correct attachment sys\_id.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.
-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] is pending security scan – The PDF requires an antivirus scan.
-   Request completed successfully – Operation is successful.
-   Undefined – Sys\_id provided does not exist or is not a PDF attachment.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to redact by rectangle and key word. On the redacted PDF, the areas selected on page 2 are blocked out. The string '23' is redacted on any page that it's found on.

```
var pdfRequest = {
  sysId: 'e4b3ae35fc128210f877789781ea59f3',
  highlightedSections: [
    {
      "pageNumber": 2,
      "x": 261.75,
      "y": 480,
      "width": 21,
      "height": 14.25
    },
    {
      "pageNumber": 2,
      "x": 249,
      "y": 390.75,
      "width": 63.75,
      "height": 15.75
    }
    // Add more coordinates as needed
  ],
  searchedKeywords: ['23']
};

// Convert the JSON object to a string
var jsonRequest = JSON.stringify(pdfRequest);
gs.info('JSON Request: ' + jsonRequest + '\n');

var PDFRedaction = new sn_pdfgeneratorutils.PDFGenerationAPI;
var result = PDFRedaction.redact(jsonRequest);
gs.info(JSON.stringify(result));
```

Output:

```
JSON Request: {"sysId":"e4b3ae35fc128210f877789781ea59f3","highlightedSections":[{"pageNumber":2,"x":261.75,"y":480,"width":21,"height":14.25},{"pageNumber":2,"x":249,"y":390.75,"width":63.75,"height":15.75}],"searchedKeywords":[23]}

{"attachment_id":"1744ae35fc128210f877789781ea59fc","message":"Request completed successfully.","status":"success"}
```

