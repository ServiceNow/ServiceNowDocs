---
title: SystemDocumentList - Scoped, Global
description: The SystemDocumentList API provides methods for setting the record fields in the Document Lists \[ds\_document\_lists\] table.Instantiates a SystemDocumentList object.Sets the Description field of a new document list record.Sets the Name field of a document list record.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SystemDocumentList - Scoped, Global

The SystemDocumentList API provides methods for setting the record fields in the Document Lists \[ds\_document\_lists\] table.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

To create or manage a document list, use the [DocumentListService API](../../DocumentListService/concept/DocumentListServiceBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SystemDocumentList - SystemDocumentList\(String docListName\)

Instantiates a SystemDocumentList object.

|Name|Type|Description|
|----|----|-----------|
|docListName|String|Name of the document list.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate a SystemDocumentList object.

```
var docList = new sn_doc_services.SystemDocumentList();
```

## SystemDocumentList - description\(String description\)

Sets the Description field of a new document list record.

|Name|Type|Description|
|----|----|-----------|
|description|String|Description of the document list.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a description to the document list. See also [DocumentListService API](../../DocumentListService/concept/DocumentListServiceBothAPI.md#).

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

## SystemDocumentList - name\(String docListName\)

Sets the Name field of a document list record.

**Note:** You can also set the name as a parameter in the SystemDocumentList\(\) constructor.

|Name|Type|Description|
|----|----|-----------|
|docListName|String|Name of the document list.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to rename an existing document list. See also [DocumentListService](../../DocumentListService/concept/DocumentListServiceBothAPI.md#).

```
var docListID = 'b2c021a924683c10f877a6fed1c2b0b1';
var docListUpdate = new sn_doc_services.SystemDocumentList();

docListUpdate.name('name change');

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

