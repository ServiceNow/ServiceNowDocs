---
title: DocumentReferenceService - Scoped, Global
description: The DocumentReferenceService API provides methods for managing document references within a target table, such as the Incidents \[incident\] or Knowledge \[kb\_knowledge\] table. You can use document references to associate information with a record.Instantiates a DocumentReferenceService object.Adds a document reference to a target table record.Removes a document reference from the Document References \[ds\_document\_reference\] table.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DocumentReferenceService - Scoped, Global

The DocumentReferenceService API provides methods for managing document references within a target table, such as the Incidents \[incident\] or Knowledge \[kb\_knowledge\] table. You can use document references to associate information with a record.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/document-services-landing-page.md).

The following APIs enable you to define and manage documents:

-   [SystemDocument](../../SystemDocument/concept/SystemDocumentBothAPI.md#) – Define a document object.
-   [DocumentService](../../DocumentService/concept/DocumentServiceBothAPI.md#) – Add, update, or delete a document.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DocumentReferenceService - DocumentReferenceService\(\)

Instantiates a DocumentReferenceService object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

The following example shows how to instantiate a DocumentReferenceService object.

```
var result = new sn_doc_services.DocumentReferenceService();
```

## DocumentReferenceService - addDocumentReference\(String docSysId, String targetTable, String tableSysId\)

Adds a document reference to a target table record.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table.|
|targetTable|String|Name of the target table on which to provide a document reference.|
|tableSysId|String|Sys\_id of the target table record to which the document reference is to be added.|

<table id="table_x4z_2cg_tpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Sys\_id of the new record in the Document References \[ds\_document\_reference\] table with a success message. Error message otherwise.```
{
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.message

</td><td>

Message confirming success or error. If successful, includes the sys\_id of the record the document reference was added to.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to add a document reference to a record in the Incidents \[incident\] table.

```
var docReference = new sn_doc_services.DocumentReferenceService();

var result = docReference.addDocumentReference("<docSysId>", "incident", "<tableSysId>");

gs.info(JSON.stringify(result, null, 2));
```

Output:

```
{
  "message": "Adding an entry to DocumentReference for the given docId to target table : incident, sysId : <tableSysId> is successful.",
  "status": "success"
}
```

## DocumentReferenceService - removeDocumentReference\(String docSysId, String targetTable, String tableSysId\)

Removes a document reference from the Document References \[ds\_document\_reference\] table.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table.|
|targetTable|String|Name of the table containing the document reference. This information is listed with the document in the Document References \[ds\_document\_reference\] table.|
|tableSysId|String|Sys\_id of the record from which the document is referenced. You can find related information listed with the document in the Document References \[ds\_document\_reference\] table.|

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

Message confirming success or error. If successful, includes the sys\_id of the record the document reference was removed from.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status indicating whether the operation is successful.Possible values:

-   success - The operation was successful.
-   failure – The operation was not successful. The **message** provides details.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to remove a document reference from a record in the Incidents \[incident\] table.

```
var docReference = new sn_doc_services.DocumentReferenceService();

var result = docReference.removeDocumentReference("<docSysId>", "incident", "<tableSysId>");

gs.info(JSON.stringify(result, null, 2));
```

Output:

```
{
  "message": "Deleting an entry to DocumentReference for the given docId to target table : incident, sysId : <tableSysId> is successful.",
  "status": "success"
}
```

