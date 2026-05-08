---
title: DocumentListEntryService - Scoped, Global
description: The DocumentListEntryService API provides methods for maintaining document templates in a document list.Instantiates a DocumentListEntryService object.Adds a document template entry to a document list.Removes a document list entry from the Document List Entries \[ds\_document\_list\_entry\] table.Updates the field values of an existing document list entry.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DocumentListEntryService - Scoped, Global

The DocumentListEntryService API provides methods for maintaining document templates in a document list.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see Document Services.

Before using the methods in this API, add a document template with its version and create a document list. Use the [SystemDocumentListEntry](../../SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#) API to add or remove documents from a document list.

Before using the methods in this API, you must add a document with its default version and create a document list.

-   [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) – Define a document object.
-   [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) – Add, update, or delete a document.
-   [SystemDocumentVersion](../../SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#) – Define a document version.
-   [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#) – Add, update, or delete a document version.
-   [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#) – Define a document list.
-   [DocumentListService](../../DocumentListService/concept/DocumentListServiceBothAPI.md#) – Add, update, or delete a document list.

To define a document as a template:

-   Define the document object setting the [SystemDocument – template\(\)](../../SystemDocument/concept/SystemDocumentBothAPI.md#) method to true. Create or update the document record with the methods in the [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) API.
-   Select the Template check box of a document in the Documents \[ds\_document\] table.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DocumentListEntryService - DocumentListEntryService\(\)

Instantiates a DocumentListEntryService object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to instantiate a DocumentListEntryService object.

```
var s = new sn_doc_services.DocumentListEntryService();
```

## DocumentListEntryService - createDocumentListEntry\(SystemDocumentListEntry entry\)

Adds a document template entry to a document list.

|Name|Type|Description|
|----|----|-----------|
|entry|[SystemDocumentListEntry](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#)|One or more properties representing fields of a document list entry object.|

<table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Sys\_id of the new record in the Document List Entries \[ds\_document\_list\_entry\] table with a success message. Error message otherwise.```
{
  "message": "String",
  "request_id": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the record in the Document List Entries \[ds\_document\_list\_entry\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to define a document entry and add it to a document list. See also [SystemDocumentListEntry](../../SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#).

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

## DocumentListEntryService - deleteDocumentListEntry\(String listEntryId\)

Removes a document list entry from the Document List Entries \[ds\_document\_list\_entry\] table.

|Name|Type|Description|
|----|----|-----------|
|listEntryId|String|Sys\_id of a document list record in the Document List Entries \[ds\_document\_list\_entry\] table.|

<table id="table_x4z_2cg_tpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Success or error message. ```
{
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to delete a document list record. See also [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#).

```
var listEntryId = 'd3f0b13624e8fc10f877a6fed1c2b0d9';

var dlEntrySvc = new sn_doc_services.DocumentListEntryService();
gs.info(JSON.stringify(dlEntrySvc.deleteDocumentListEntry(listEntryId), null, 2));
```

Output:

```
{
  "message": "Deleting an entry for the given documentListEntrySysId : d3f0b13624e8fc10f877a6fed1c2b0d9 is successful.",
  "status": "success"
}
```

## DocumentListEntryService - updateDocumentListEntry\(String listEntryId, SystemDocumentListEntry entry\)

Updates the field values of an existing document list entry.

|Name|Type|Description|
|----|----|-----------|
|listEntryId|String|Sys\_id of a document list record in the Document List Entries \[ds\_document\_list\_entry\] table.|
|entry|[SystemDocumentListEntry](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#)|One or more properties representing fields of a document list entry object.|

<table id="table_x4z_2cg_tpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td id="entry-docserv-ret-obj-basic">

Success or error message. ```
{
  "message": "String",
  "request_id": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the record in the Document List Entries \[ds\_document\_list\_entry\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to update a document list entry description. See also [SystemDocumentListEntry](../../SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#).

```
var listEntryId = 'd3f0b13624e8fc10f877a6fed1c2b0d9';

var entry = new sn_doc_services.SystemDocumentListEntry();
entry.description('description update');

var dlEntrySvc = new sn_doc_services.DocumentListEntryService();
gs.info(JSON.stringify(dlEntrySvc.updateDocumentListEntry(listEntryId, entry), null, 2));
```

Output:

```
{
  "message": "Updating an entry for the given documentListEntrySysId : d3f0b13624e8fc10f877a6fed1c2b0d9 is successful.",
  "request_id": "d3f0b13624e8fc10f877a6fed1c2b0d9",
  "status": "success"
}
```

