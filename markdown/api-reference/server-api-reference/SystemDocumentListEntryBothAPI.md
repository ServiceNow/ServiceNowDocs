---
title: SystemDocumentListEntry - Scoped, Global
description: The SystemDocumentListEntry API provides methods for setting the record fields in the Document List Entries \[ds\_document\_list\_entry\] table.Instantiates a SystemDocumentListEntry object.Sets the Description field of a document list entry record.Specifies the document template to add to a document list.Specifies the document list in which to add a document.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SystemDocumentListEntry - Scoped, Global

The SystemDocumentListEntry API provides methods for setting the record fields in the Document List Entries \[ds\_document\_list\_entry\] table.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see Document Services.

Before using the methods in this API, you must add a document with its versions, and create a document list.

-   [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) – Define a document object.
-   [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) – Add, update, or delete a document.
-   [SystemDocumentVersion](../../SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#) – Define a document version.
-   [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#) – Add, update, or delete a document version.
-   [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#) – Define a document list.
-   [DocumentListService](../../DocumentListService/concept/DocumentListServiceBothAPI.md#) – Add, update, or delete a document list.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SystemDocumentListEntry - SystemDocumentListEntry\(String listID\)

Instantiates a SystemDocumentListEntry object.

|Name|Type|Description|
|----|----|-----------|
|listSysId|String|Sys\_id of a document list record in the Document Lists \[ds\_document\_lists\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate a SystemDocumentListEntry object.

```
var docList = new sn_doc_services.SystemDocumentListEntry("<docListSysId>");
```

## SystemDocumentListEntry - description\(String description\)

Sets the Description field of a document list entry record.

|Name|Type|Description|
|----|----|-----------|
|description|String|Description of the document list entry.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a description to the document list entry provided using the constructor. See also [DocumentListEntryService](../../DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#) API.

```
var docListEntry = new sn_doc_services.SystemDocumentListEntry('21afddea2460fc10f877a6fed1c2b0dd');

docListEntry.description('birth');

var dlEntrySvc = new sn_doc_services.DocumentListEntryService();
gs.info(JSON.stringify(dlEntrySvc.createDocumentListEntry(docListEntry), null, 2));
```

Output:

```
{
  "message": "Create List Entry , List Entry sysId : d3f0b13624e8fc10f877a6fed1c2b0d9is successful.",
  "request_id": "d3f0b13624e8fc10f877a6fed1c2b0d9",
  "status": "success"
}
```

## SystemDocumentListEntry - document\(String docSysId\)

Specifies the document template to add to a document list.

To define a document as a template:

-   Define the document object setting the [SystemDocument – template\(\)](../../SystemDocument/concept/SystemDocumentBothAPI.md#) method to true. Create or update the document record with the methods in the [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) API.
-   Select the Template check box of a document in the Documents \[ds\_document\] table.

The document record specified must have a version. Use the following APIs to define and add a document version:

-   [SystemDocumentVersion](../../SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#) – Define a document version.
-   [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#) – Add, update, or delete a document version.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table. The document specified must be a template and have a version.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a document template as a document list entry. See also [DocumentListEntryService API](../../DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#).

```
var docListEntry = new sn_doc_services.SystemDocumentListEntry('21afddea2460fc10f877a6fed1c2b0dd');
docListEntry.document("9acd7fea24587410f877a6fed1c2b060");
docListEntry.description('birth certificate');

var dlEntrySvc = new sn_doc_services.DocumentListEntryService();
gs.info(JSON.stringify(dlEntrySvc.createDocumentListEntry(docListEntry), null, 2));
```

Output:

```
{
  "message": "Create List Entry , List Entry sysId : d3f0b13624e8fc10f877a6fed1c2b0d9is successful.",
  "request_id": "d3f0b13624e8fc10f877a6fed1c2b0d9",
  "status": "success"
}
```

## SystemDocumentListEntry - documentList\(String listSysId\)

Specifies the document list in which to add a document.

**Note:** You can alternatively set the document list as a parameter in the SystemDocumentListEntry\(\) constructor.

Use the following APIs to define and create a document list:

-   [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#) – Define a document list.
-   [DocumentListService](../../DocumentListService/concept/DocumentListServiceBothAPI.md#) – Add, update, or delete a document list.

|Name|Type|Description|
|----|----|-----------|
|listSysId|String|Sys\_id of a document list record in the Document Lists \[ds\_document\_lists\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the document list in which to add a document. See also [DocumentListEntryService API](../../DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#).

```
var docListEntry = new sn_doc_services.SystemDocumentListEntry();

docListEntry.documentList('21afddea2460fc10f877a6fed1c2b0dd');
docListEntry.document('deaef1ce24103410f877a6fed1c2b085');
docListEntry.description('passport');

var dlEntrySvc = new sn_doc_services.DocumentListEntryService();
gs.info(JSON.stringify(dlEntrySvc.createDocumentListEntry(docListEntry), null, 2));
```

Output:

```
{
  "message": "Create List Entry , List Entry sysId : c4ccaa8b24283050f877a6fed1c2b003is successful.",
  "request_id": "c4ccaa8b24283050f877a6fed1c2b003",
  "status": "success"
}
```

