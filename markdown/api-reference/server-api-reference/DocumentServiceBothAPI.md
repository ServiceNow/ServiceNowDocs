---
title: DocumentService - Scoped, Global
description: The DocumentService API provides methods for creating, deleting, and updating a document.Instantiates a DocumentService object.Creates a document record in the Documents \[ds\_document\] table.Removes a document record from the Documents \[ds\_document\] table.Updates the field values of an existing document record.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DocumentService - Scoped, Global

The DocumentService API provides methods for creating, deleting, and updating a document.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

A document is a collection of information about a document record. The methods used to create or update a record modify fields using the [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) object.

Document content is managed using versions. The following APIs enable you to define and manage document versions:

-   [SystemDocumentVersion](../../SystemDocumentVersion/concept/SystemDocumentVersionBothAPI.md#) – Define a document version as the source of the document content. Each version is an element containing the document content and is provided using a single URL or attachment. An attachment can only be added in the Document Versions \[ds\_document\_version\] table UI and not with the API.
-   [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#) – Document content is managed using versions.

Use the [DocumentReferenceService](../../DocumentReferenceService/concept/DocumentReferenceServiceBothAPI.md#) API to manage documents referenced in a target table, such as the Incidents \[incident\] or Knowledge \[kb\_knowledge\] table.

The Document Management plugin also supports creating lists of document templates to associate with your document. For example, a job application requiring multiple documents such as a diploma, ID, or passport.

-   [SystemDocumentList](../../SystemDocumentList/concept/SystemDocumentListBothAPI.md#) – Define a list of document templates.
-   [DocumentListService](../../DocumentListService/concept/DocumentListServiceBothAPI.md#) – Add or remove a document template list.
-   [SystemDocumentListEntry](../../SystemDocumentListEntry/concept/SystemDocumentListEntryBothAPI.md#) – Define a document template list entry.
-   [DocumentListEntryService](../../DocumentListEntryService/concept/DocumentListEntryServiceBothAPI.md#) – Add or remove a document template list entry.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DocumentService - DocumentService\(\)

Instantiates a DocumentService object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to instantiate a DocumentService object.

```
var s = new sn_doc_services.DocumentService();
```

## DocumentService - createDocument\(SystemDocument doc\)

Creates a document record in the Documents \[ds\_document\] table.

|Name|Type|Description|
|----|----|-----------|
|doc|[SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#)|One or more properties representing fields of a new record. The name property is required and can be set using the SystemDocument constructor or name\(\) method.|

<table id="table_tj4_p5j_34b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Sys\_id of the new record in the Documents \[ds\_document\] table with a success message. Error message otherwise.```
{
  "message": "String",
  "request_id": "String",
  "status": "String"
}
```

</td></tr><tr id="row_pdfgen_ret_msgCnv"><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. Possible values:

-   Create document sysId : &lt;sys\_id&gt; is successful.
-   Document Name is mandatory and should be valid.
-   Document Name is mandatory and it should not be null or empty.
-   &lt;[SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) property requiring sys\_id input&gt; with SysId: "&lt;sys\_id&gt;" does not exist

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.request\_id

</td><td>

Sys\_id of the record in the Documents \[ds\_document\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to populate SystemDocument object properties and create a new document record.

```
var d = new sn_doc_services.SystemDocument('My document');

// Define the document fields
var reviewers = '62826bf03710200044e0bfc8bcbe5df1,a8f98bb0eb32010045e1a5115206fe3a';
d.description('description');
d.classification('restricted');
d.state('review');
d.department('93b25282c0a8000b0b55c8ab34e2f1e6');
d.template(false);
d.type('policy');
d.reviewers(reviewers);
d.audience('external');

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 1040420224503410f877a6fed1c2b031 is successful.",
  "request_id": "1040420224503410f877a6fed1c2b031",
  "status": "success"
}
```

## DocumentService - deleteDocument\(String docSysId\)

Removes a document record from the Documents \[ds\_document\] table.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table.|

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

Sys\_id of the record in the Documents \[ds\_document\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to delete an existing document record.

```
var docid = "<sys_id>";
var svc = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(svc.deleteDocument(docid), null, 2));
```

Output:

```
{
  "message": "Delete document sysId : <sys_id> is successful.",
  "request_id": "<sys_id>",
  "status": "success"
}
```

## DocumentService - updateDocument\(String docSysId, SystemDocument doc\)

Updates the field values of an existing document record.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table.|
|doc|[SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#)|One or more properties representing document fields to be updated.|

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

Sys\_id of the record in the Documents \[ds\_document\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to change a document name. See also [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#).

```
var dId = "19aab54e24103410f877a6fed1c2b03d";
var d = new sn_doc_services.SystemDocument();
d.name("c22.txt");

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.updateDocument(dId, d), null, 2));
```

Output:

```
{
  "message": "Update document sysId : 19aab54e24103410f877a6fed1c2b03d is successful.",
  "request_id": "19aab54e24103410f877a6fed1c2b03d",
  "status": "success"
}
```

