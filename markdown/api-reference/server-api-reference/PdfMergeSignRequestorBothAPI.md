---
title: PdfMergeSignRequestor - Scoped, Global
description: The PdfMergeSignRequestor API provides methods to add an image representing a signature to a PDF document.Instantiates a new PdfMergeSignRequestor object.Assigns signature size and position requirements in the PDF.Creates a signature request with source and target inputs.Processes requests and adds the signatures.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PdfMergeSignRequestor - Scoped, Global

The PdfMergeSignRequestor API provides methods to add an image representing a signature to a PDF document.

This API is part of the ServiceNow PDF Generation Utilities plugin \(com.snc.apppdfgenerator\) and is provided within the `sn_pdfgeneratorutils` namespace. The plugin is activated by default.

This API creates a signature object that can be implemented in a PDF using [PDFGenerationAPI](../../PDFGenerationAPIBoth/concept/PDFGenerationAPIBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PdfMergeSignRequestor - PdfMergeSignRequestor\(\)

Instantiates a new PdfMergeSignRequestor object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following examples shows how to create a PdfMergeSignRequestor object.

```
var v = new sn_pdfgeneratorutils.PdfMergeSignRequestor;
```

## PdfMergeSignRequestor - addSignatureMapping\(Number pageNumber, Number leftMargin, Number topMargin, Number boxWidth, Number boxHeight, String sysId\)

Assigns signature size and position requirements in the PDF.

|Name|Type|Description|
|----|----|-----------|
|pageNumber|Number|Number of the page on which to insert the signature.|
|leftMargin|Number|Value in points representing the left margin area of the page at which to insert the signature.|
|topMargin|Number|Value in points representing the top margin area of the page at which to insert the signature image.|
|boxWidth|Number|Value in points representing width of the box to contain the signature.|
|boxHeight|Number|Value in points representing height of the box to contain the signature image.|
|sysId|String|Sys\_id of the signature image in the Attachments \[sys\_attachment\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add the signature mapping. For a complete example, see processRequest\(\).

```
var requestor = new sn_pdfgeneratorutils.PdfMergeSignRequestor;

// For the purpose of this example, set signature sizes and page number for signature placement
var page = 2;
var leftMargin = 48;
var topMargin = 60;
var signatureWidth = 96;
var signatureHeight = 36; 

requestor.addSignatureMapping(page, leftMargin, topMargin, signatureWidth, signatureHeight, "<signatureSysId>");
```

## PdfMergeSignRequestor - createRequest\(String targetSysId, String targetTable, String tableSysId, String targetFileName\)

Creates a signature request with source and target inputs.

|Name|Type|Description|
|----|----|-----------|
|targetSysId|String|Sys\_id of a PDF in the Attachments \[sys\_attachment\] table. Use this value as the target PDF on which to add a signature.|
|targetTable|String|Name of the table containing the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.|
|tableSysId|String|Sys\_id of the record to which the PDF is attached. You can find this value in the same row as the attachment listed in the Attachments \[sys\_attachment\] table.|
|targetFileName|String|Name of the target PDF without extension.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to create a signature request. For a complete example, see processRequest\(\).

```
var requestor = new sn_pdfgeneratorutils.PdfMergeSignRequestor;

requestor.createRequest("<sys_id>", "tableName", "<tableSysId>", "pdfFileName");
```

## PdfMergeSignRequestor - processRequest\(\)

Processes requests and adds the signatures.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_erx_h3k_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the size of each page if successful, error message otherwise. ```
{
  "attachment_id": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr id="row_pdfgen_ret_attID"><td>

&lt;Object&gt;.attachment\_id

</td><td>

If the request is successful, sys\_id of the signed and attached PDF. The file is listed in the Attachments \[sys\_attachment\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Possible values:

-   Request cannot proceed as the attachment with sys\_id \[\{0\}\] did not pass security scan – The PDF did not pass the antivirus scan.

-   No signature mapping specified. Cannot process this request – Provide signature mapping using the addSignatureMapping\(\) method.
-   Request completed successfully.
-   Request failure. Exceptions while trying to add signatures to document. Please check again.
-   This request cannot be completed as the requested page does not exist. page No: &lt;page number&gt;

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - Operation was successful.
-   failure – Operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to process the signature request.

```
var requestor = new sn_pdfgeneratorutils.PdfMergeSignRequestor;

requestor.createRequest("<sys_id>", "tableName", "<tableSysId>", pdfFileName);

// For the purpose of this example, set signature sizes and page number for signature placement
var page = 6;
var leftMargin = 40;
var topMargin = 50;
var signatureWidth = 188;
var signatureHeight = 44; 

requestor.addSignatureMapping(page, leftMargin, topMargin, signatureWidth, signatureHeight, "<signatureSysId>");

var result = requestor.processRequest();
gs.info(JSON.stringify(result));
```

