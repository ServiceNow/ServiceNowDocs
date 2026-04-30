---
title: DocumentVersionService - Scoped, Global
description: The DocumentVersionService API provides a service for creating and deleting document versions. Each version is an element containing the document content and is provided using a single URL or attachment. An attachment can only be added in the Document Versions \[ds\_document\_version\] table UI and not with the API.Instantiates a DocumentVersionService object.Creates a document version record in the Versions \[ds\_document\_version\] table.Deletes a document version.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DocumentVersionService - Scoped, Global

The DocumentVersionService API provides a service for creating and deleting document versions. Each version is an element containing the document content and is provided using a single URL or attachment. An attachment can only be added in the Document Versions \[ds\_document\_version\] table UI and not with the API.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Before creating a document version, you must first define and add a document record.

-   [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) – Define a document object.
-   [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) – Add, update, or delete a document.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DocumentVersionService - DocumentVersionService\(\)

Instantiates a DocumentVersionService object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to instantiate a DocumentVersionService object.

```
var versionSvc = new sn_doc_services.DocumentVersionService();
```

## DocumentVersionService - createDocumentVersion\(SystemDocumentVersion docVersion\)

Creates a document version record in the Versions \[ds\_document\_version\] table.

|Name|Type|Description|
|----|----|-----------|
|docVersion|[SystemDocumentVersion](../../SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#)|One or more properties representing fields of a document version.|

<table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Sys\_id of the new record in the Versions \[ds\_document\_version\] table with a success message. Error message otherwise.```
{
  "message": "String",
  "request_id": "String",
  "status": "String"
}
```

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. If successful, includes the sys\_id of the document record and the sys\_id of its new document version.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the new record in the Versions \[ds\_document\_version\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to populate SystemDocumentVersion object properties and create a new document version. See also [SystemDocumentVersion](../../SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#).

```
var versionDefinition = new sn_doc_services.SystemDocumentVersion('491efbee24187410f877a6fed1c2b0a9');

versionDefinition.type('url');
versionDefinition.url('http://one/1.0');

var versionSvc = new sn_doc_services.DocumentVersionService();
gs.info(JSON.stringify(versionSvc.createDocumentVersion(versionDefinition), null, 2));
```

Output:

```
{
  "message": "Adding an entry to DocumentVersion for the given docId : 491efbee24187410f877a6fed1c2b0a9, sysId : d5a340d9242cf810f877a6fed1c2b069 is successful.",
  "request_id": "d5a340d9242cf810f877a6fed1c2b069",
  "status": "success"
}
```

## DocumentVersionService - deleteDocumentVersion\(String docVersionSysId\)

Deletes a document version.

|Name|Type|Description|
|----|----|-----------|
|docVersionSysId|String|Sys\_id of a document version in the Versions \[ds\_document\_version\] table.|

<table id="table_x4z_2cg_tpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Success message. Error message otherwise.```
{
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. If successful, includes the sys\_id of the deleted document version.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to delete an existing document version.

```
var vId = "<versionSysId>";
var versionSvc = new sn_doc_services.DocumentVersionService();

gs.info(JSON.stringify(versionSvc.deleteDocumentVersion(vId), null, 2));
```

Output:

```
{
  "message": "Deleting an entry to DocumentVersion for the given documentVersionSysId : , sysId : <versionSysId> is successful.",
  "status": "success"
}
```

