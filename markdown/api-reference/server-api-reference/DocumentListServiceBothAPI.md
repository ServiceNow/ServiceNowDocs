---
title: DocumentListService - Scoped, Global
description: The DocumentListService API provides methods for creating, deleting, and updating a document list.Instantiates a DocumentListService object.Creates a document list in the Document Lists \[ds\_document\_lists\] table.Creates documents from a list of document templates.Removes a document record from the Document Lists \[ds\_document\_lists\] table.Updates the field values of an existing document list.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DocumentListService - Scoped, Global

The DocumentListService API provides methods for creating, deleting, and updating a document list.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

The Document Management plugin also supports creating lists of document templates to associate with your document. For example, a job application requiring multiple documents such as a diploma, ID, or passport. After you add your document list, you can add document templates:

-   [SystemDocumentListEntry](../../SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#) – Define a document template list entry.
-   [DocumentListEntryService](../../DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#) – Add or remove a document template list entry.

To define a document as a template:

-   Define the document object setting the [SystemDocument – template\(\)](../../SystemDocument/concept/SystemDocumentBothAPI.md#) method to true. Create or update the document record with the methods in the [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) API.
-   Select the Template check box of a document in the Documents \[ds\_document\] table.

The following APIs enable you to define and manage documents:

-   [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) – Define a document object.
-   [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) – Add, update, or delete a document.

To define a document as a template:

-   Define the document object setting the [SystemDocument – template\(\)](../../SystemDocument/concept/SystemDocumentBothAPI.md#) method to true. Create or update the document record with the methods in the [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) API.
-   Select the Template check box of a document in the Documents \[ds\_document\] table.

See also [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DocumentListService - DocumentListService\(\)

Instantiates a DocumentListService object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to instantiate a DocumentListService object. See also [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#).

```
var s = new sn_doc_services.DocumentListService();
```

## DocumentListService - createDocumentList\(SystemDocumentList doc\)

Creates a document list in the Document Lists \[ds\_document\_lists\] table.

The Document Management plugin also supports creating lists of document templates to associate with your document. For example, a job application requiring multiple documents such as a diploma, ID, or passport. After you add your document list, you can add document templates:

-   [SystemDocumentListEntry](../../SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#) – Define a document template list entry.
-   [DocumentListEntryService](../../DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#) – Add or remove a document template list entry.

Use the [createDocumentsFromList\(\)](DocumentListServiceBothAPI.md#) method to create documents from the document template list.

|Name|Type|Description|
|----|----|-----------|
|doc|[SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#)|One or more properties representing fields of a new record. The name property is required and can be set using the SystemDocumentList constructor or name\(\) method.|

<table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Sys\_id of the new record in the Document Lists \[ds\_document\_lists\] table with a success message. Error message otherwise.```
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

Sys\_id of the record in the Document Lists \[ds\_document\_lists\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to create a document list. See also [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#).

```
var dL = new sn_doc_services.SystemDocumentList('My document list');

// Define the document list field
dL.description('description');

var docList = new sn_doc_services.DocumentListService();
gs.info(JSON.stringify(docList.createDocumentList(dL), null, 2));
```

Output:

```
{
  "message": "Create List for the given name : My document list, List sysId : b2c021a924683c10f877a6fed1c2b0b1 is successful.",
  "request_id": "b2c021a924683c10f877a6fed1c2b0b1",
  "status": "success"
}
```

## DocumentListService - createDocumentsFromList\(String listSysId, String tableName, String tableSysId\)

Creates documents from a list of document templates.

**Note:** Before using this method, create a document template list using the [createDocumentList\(\)](DocumentListServiceBothAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|listSysId|String|Sys\_id of a document list record in the Document Lists \[ds\_document\_lists\] table.|
|tableName|String|Name of the table containing the record on which add a list of document template references.|
|tableSysId|String|Sys\_id of the record containing the content from which to add a list of document template references.|

<table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

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

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.message

</td><td>

Message containing the number of document templates in the document list.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the record in the Document Lists \[ds\_document\_lists\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how add a list of document template references to a record. The documentation is added to a record in the Incidents \[incident\] table.

```
var result = new sn_doc_services.DocumentListService().createDocumentsFromList('21afddea2460fc10f877a6fed1c2b0dd', 'incident', 'd7158da0c0a8016700eef46c8d1f3661');
gs.info(JSON.stringify(result, null, 2));
```

Output:

```
{
  "message": "Created 1 document references for the given table name: incident, table sysId : d7158da0c0a8016700eef46c8d1f3661 with list SysId 21afddea2460fc10f877a6fed1c2b0dd",
  "request_id": "21afddea2460fc10f877a6fed1c2b0dd",
  "status": "success"
}
```

## DocumentListService - deleteDocumentList\(String listSysId\)

Removes a document record from the Document Lists \[ds\_document\_lists\] table.

|Name|Type|Description|
|----|----|-----------|
|listSysId|String|Sys\_id of a document list record in the Document Lists \[ds\_document\_lists\] table.|

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

Sys\_id of the record in the Document Lists \[ds\_document\_lists\] table.Data type: String

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
var docListID = 'b2c021a924683c10f877a6fed1c2b0b1';

var docListSvc = new sn_doc_services.DocumentListService();
gs.info(JSON.stringify(docListSvc.deleteDocumentList(docListID), null, 2));
```

Output:

```
{
  "message": "Delete List for the given sysId : b2c021a924683c10f877a6fed1c2b0b1 is successful.",
  "request_id": "b2c021a924683c10f877a6fed1c2b0b1",
  "status": "success"
}
```

## DocumentListService - updateDocumentList\(String docSysId, SystemDocumentList doc\)

Updates the field values of an existing document list.

|Name|Type|Description|
|----|----|-----------|
|listSysId|String|Sys\_id of a document list record in the Document Lists \[ds\_document\_lists\] table.|
|doc|[SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#)|One or more properties representing document list fields to be updated.|

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

Sys\_id of the record in the Document Lists \[ds\_document\_lists\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to update a document list name and description. See also [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#).

```
var docListID = 'b2c021a924683c10f877a6fed1c2b0b1';

var docListUpdate = new sn_doc_services.SystemDocumentList();
docListUpdate.name('name change');
docListUpdate.description('description update');

var docListSvc = new sn_doc_services.DocumentListService();
gs.info(JSON.stringify(docListSvc.updateDocumentList(docListID , docListUpdate), null, 2));
```

Output:

```
{
  "message": "Update List for the given sysId : b2c021a924683c10f877a6fed1c2b0b1 is successful.",
  "request_id": "b2c021a924683c10f877a6fed1c2b0b1",
  "status": "success"
}
```

