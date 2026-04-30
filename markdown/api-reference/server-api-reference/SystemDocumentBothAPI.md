---
title: SystemDocument - Scoped, Global
description: The SystemDocument API provides methods for setting fields of a record in the Documents \[ds\_document\] table.Instantiates a SystemDocument object.Sets the Audience field of a document record to specify external or internal availability. Represents the Audience field in a Document Management form.Sets the Classification field of a document record to identify the level of information sensitivity. Represents the Classification field in a Document Management form.Sets the template from which to generate a document. When the document is generated, the specified template is listed in the Created From Template field in the Documents \[ds\_document\_list\] table.Sets the Department field of a document record.Sets the Description field of a document record.Sets the Name field of a document record.Sets the Owner field of a document record.Sets the Reviewers field of a document record.Sets the State field of a document record.Specifies whether a document record is a template.Sets the Type field of a document record.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SystemDocument - Scoped, Global

The SystemDocument API provides methods for setting fields of a record in the Documents \[ds\_document\] table.

This API requires the Document Management plugin \(com.snc.platform\_document\_management\) and is provided within the `sn_doc_services` namespace. For information, see [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

To create a document, use the [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SystemDocument - SystemDocument\(String docName\)

Instantiates a SystemDocument object.

|Name|Type|Description|
|----|----|-----------|
|docName|String|Name of the document.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to instantiate a SystemDocument object and set several fields for a document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

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

## SystemDocument - audience\(String audience\)

Sets the Audience field of a document record to specify external or internal availability. Represents the Audience field in a Document Management form.

<table id="table_o12_jrk_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

audience

</td><td>

String

</td><td>

String representing the intended audience of the document.Possible values:

-   external
-   internal

Default: internal

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the Audience field in a new document record. See also [DocumentService - Scoped, Global](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');
var s = new sn_doc_services.DocumentService();

d.audience('external');

gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 1193fd4624103410f877a6fed1c2b016 is successful.",
  "request_id": "1193fd4624103410f877a6fed1c2b016",
  "status": "success"
}
```

## SystemDocument - classification\(String classification\)

Sets the Classification field of a document record to identify the level of information sensitivity. Represents the Classification field in a Document Management form.

<table id="table_o12_jrk_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

classification

</td><td>

String

</td><td>

Classification of the document.Possible values:

-   confidential
-   public
-   restricted

Default: public

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The value of the classification property of a SystemDocument object.|

The following example shows how to set the classification field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My restricted document');
var s = new sn_doc_services.DocumentService();

d.classification('restricted');

gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : d80435c624103410f877a6fed1c2b0d0 is successful.",
  "request_id": "d80435c624103410f877a6fed1c2b0d0",
  "status": "success"
}
```

## SystemDocument - createdFromTemplate\(String docTemplate\)

Sets the template from which to generate a document. When the document is generated, the specified template is listed in the Created From Template field in the Documents \[ds\_document\_list\] table.

|Name|Type|Description|
|----|----|-----------|
|docTemplate|String|Sys\_id of a document listed in the Documents \[ds\_document\_list\] table. The document must have the Template checkbox selected \(true\). See also [DocumentVersionService API](../../DocumentVersionService/concept/DocumentVersionServiceBothAPI.md#).|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to create a new document record from an existing template. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('New doc from template');
var s = new sn_doc_services.DocumentService();

d.createdFromTemplate('<doc_template_sys_id>');

gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : deaef1ce24103410f877a6fed1c2b085 is successful.",
  "request_id": "deaef1ce24103410f877a6fed1c2b085",
  "status": "success"
}
```

## SystemDocument - department\(String docDept\)

Sets the Department field of a document record.

|Name|Type|Description|
|----|----|-----------|
|docDept|String|Sys\_id of a department listed in the Departments \[cmn\_department\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the department field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');

// Assign the doc to the human resources department
d.department('<dept_sys_id>');

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 491efbee24187410f877a6fed1c2b0a9 is successful.",
  "request_id": "491efbee24187410f877a6fed1c2b0a9",
  "status": "success"
}
```

## SystemDocument - description\(String description\)

Sets the Description field of a document record.

|Name|Type|Description|
|----|----|-----------|
|description|String|Description of the document.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the description field in a document record. See also: [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');

d.description('Information describing the doc.');

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 9acd7fea24587410f877a6fed1c2b060 is successful.",
  "request_id": "9acd7fea24587410f877a6fed1c2b060",
  "status": "success"
}
```

## SystemDocument - name\(String docName\)

Sets the Name field of a document record.

**Note:** You can also set the name as a parameter in the SystemDocument\(\) constructor.

|Name|Type|Description|
|----|----|-----------|
|docName|String|Name of the document.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the Name field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument();

d.name('Document named using method instead of constructor');

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : c19d7f2624587410f877a6fed1c2b0eb is successful.",
  "request_id": "c19d7f2624587410f877a6fed1c2b0eb",
  "status": "success"
}
```

## SystemDocument - owner\(String owner\)

Sets the Owner field of a document record.

<table id="table_o12_jrk_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

owner

</td><td>

String

</td><td>

Sys\_id of a user listed in the Users \[sys\_user\] table. Role required: admin

 Default: Current user

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the owner field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');
var s = new sn_doc_services.DocumentService();

d.owner('aa826bf03710200044e0bfc8bcbe5dd6');

gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 4235318a24103410f877a6fed1c2b0ff is successful.",
  "request_id": "4235318a24103410f877a6fed1c2b0ff",
  "status": "success"
}
```

## SystemDocument - reviewers\(String reviewers\)

Sets the Reviewers field of a document record.

|Name|Type|Description|
|----|----|-----------|
|reviewers|String|List of one or more document reviewers by sys\_id. The reviewer must be a user listed in the Users \[sys\_user\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the reviewers field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');

var reviewers = '62826bf03710200044e0bfc8bcbe5df1,a8f98bb0eb32010045e1a5115206fe3a';
d.reviewers(reviewers);

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 8d19f9ca24103410f877a6fed1c2b0aa is successful.",
  "request_id": "8d19f9ca24103410f877a6fed1c2b0aa",
  "status": "success"
}
```

## SystemDocument - state\(String state\)

Sets the State field of a document record.

<table id="table_o12_jrk_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

state

</td><td>

String

</td><td>

State of the document representing where the document is in the workflow.Valid values:

-   draft
-   submit
-   review
-   complete

Default: draft

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the state field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');
var s = new sn_doc_services.DocumentService();

d.state('submit');

gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 19aab54e24103410f877a6fed1c2b03d is successful.",
  "request_id": "19aab54e24103410f877a6fed1c2b03d",
  "status": "success"
}
```

## SystemDocument - template\(Boolean template\)

Specifies whether a document record is a template.

<table id="table_o12_jrk_spb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

template

</td><td>

Boolean

</td><td>

Flag that specifies whether a document record is a template.

 Valid values:

-   true: The default version of this document is a template.
-   false: This document is not a template.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to indicate that a document record is a template. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('My document');

d.template(true);

var s = new sn_doc_services.DocumentService();
gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : f7f006ce24103410f877a6fed1c2b053 is successful.",
  "request_id": "f7f006ce24103410f877a6fed1c2b053",
  "status": "success"
}
```

## SystemDocument - type\(String docType\)

Sets the Type field of a document record.

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

Type of document.Valid values:

-   contract
-   guideline
-   policy
-   procedure

Default: None

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the type field in a new document record. See also [DocumentService API](../../DocumentService/concept/DocumentServiceBothAPI.md#).

```
var d = new sn_doc_services.SystemDocument('How to use the document mgmt API');
var s = new sn_doc_services.DocumentService();

d.type('guideline');

gs.info(JSON.stringify(s.createDocument(d), null, 2));
```

Output:

```
{
  "message": "Create document sysId : 8adfb10224503410f877a6fed1c2b0e4 is successful.",
  "request_id": "8adfb10224503410f877a6fed1c2b0e4",
  "status": "success"
}
```

