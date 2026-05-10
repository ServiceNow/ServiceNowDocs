---
title: SystemDocumentVersion - Scoped, Global
description: The SystemDocumentVersion API provides methods for setting the values of a document's source version in the Versions \[ds\_document\_version\] table.Instantiates a SystemDocumentVersion object.Specifies the document record for this version.Sets the Type field of a document version.Sets the URL of a document version.Sets the number of a document version.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SystemDocumentVersion - Scoped, Global

The SystemDocumentVersion API provides methods for setting the values of a document's source version in the Versions \[ds\_document\_version\] table.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/document-services-landing-page.md).

To create a document version, use the [DocumentVersionService API](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SystemDocumentVersion - SystemDocumentVersion\(String docSysId\)

Instantiates a SystemDocumentVersion object.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate a SystemDocumentVersion object and create a document version. See also [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).

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

## SystemDocumentVersion - document\(String docSysId\)

Specifies the document record for this version.

**Note:** You can alternatively set the name as a parameter in the SystemDocumentVersion\(\) constructor.

|Name|Type|Description|
|----|----|-----------|
|docSysId|String|Sys\_id of a document record in the Documents \[ds\_document\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the name field of a document version. See also DocumentVersionService – [createDocumentVersion\(\)](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).

```
var versionDefinition = new sn_doc_services.SystemDocumentVersion();

versionDefinition.document('491efbee24187410f877a6fed1c2b0a9');

var versionSvc = new sn_doc_services.DocumentVersionService();
gs.info(JSON.stringify(versionSvc.createDocumentVersion(versionDefinition), null, 2));
```

Output:

```
{
  "message": "Adding an entry to DocumentVersion for the given docId : 491efbee24187410f877a6fed1c2b0a9, sysId : 1c504c91242cf810f877a6fed1c2b08b is successful.",
  "request_id": "1c504c91242cf810f877a6fed1c2b08b",
  "status": "success"
}
```

## SystemDocumentVersion - type\(String docType\)

Sets the Type field of a document version.

<table id="table_o12_jrk_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

docType

</td><td>

String

</td><td>

Document source type.Valid values:

-   url
-   attachment

Default: attachment

 **Note:** An attachment can currently only be added in the Document Versions \[ds\_document\_version\] table UI and not with the API.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the type field and create a document version. See also [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).

```
var versionDefinition = new sn_doc_services.SystemDocumentVersion('491efbee24187410f877a6fed1c2b0a9');

versionDefinition.type('url');
versionDefinition.url('http://one/1.0');

var versionSvc = new sn_doc_services.DocumentVersionService();
gs.info(JSON.stringify(versionSvc.createDocumentVersion(versionDefinition), null, 2));
```

```
{
  "message": "Adding an entry to DocumentVersion for the given docId : 491efbee24187410f877a6fed1c2b0a9, sysId : d5a340d9242cf810f877a6fed1c2b069 is successful.",
  "request_id": "d5a340d9242cf810f877a6fed1c2b069",
  "status": "success"
}
```

## SystemDocumentVersion - url\(String url\)

Sets the URL of a document version.

|Name|Type|Description|
|----|----|-----------|
|url|String|URL of the source document for this version.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the URL field as the source of a document version. See also [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).

```
var versionDefinition = new sn_doc_services.SystemDocumentVersion('491efbee24187410f877a6fed1c2b0a9');

versionDefinition.type('url');
versionDefinition.url('http://one/1.0');

var versionSvc = new sn_doc_services.DocumentVersionService();
gs.info(JSON.stringify(versionSvc.createDocumentVersion(versionDefinition), null, 2));
```

```
{
  "message": "Adding an entry to DocumentVersion for the given docId : 491efbee24187410f877a6fed1c2b0a9, sysId : d5a340d9242cf810f877a6fed1c2b069 is successful.",
  "request_id": "d5a340d9242cf810f877a6fed1c2b069",
  "status": "success"
}
```

## SystemDocumentVersion - versionNumber\(Number versionNumber\)

Sets the number of a document version.

|Name|Type|Description|
|----|----|-----------|
|versionNumber|Number|Version number for this document.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the version number and create a document version. See also [DocumentVersionService](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).

```
var versionDefinition = new sn_doc_services.SystemDocumentVersion('491efbee24187410f877a6fed1c2b0a9');

versionDefinition.type('url');
versionDefinition.url('http://one/1.0');
versionDefinition.versionNumber(5);

var versionSvc = new sn_doc_services.DocumentVersionService();
gs.info(JSON.stringify(versionSvc.createDocumentVersion(versionDefinition), null, 2));
```

Output:

```
{
  "message": "Adding an entry to DocumentVersion for the given docId : 491efbee24187410f877a6fed1c2b0a9, sysId : ff47449d242cf810f877a6fed1c2b06c is successful.",
  "request_id": "ff47449d242cf810f877a6fed1c2b06c",
  "status": "success"
}
```

