---
title: CdmEditorApi
description: The CdmEditorApi provides endpoints that enable you to create nodes, update nodes, include existing nodes under other nodes, delete nodes, and retrieve nodes and node includes.Deletes a specified node.Returns the list of nodes that were include within a specified node path.Returns the details of a specified node or a list of child Configuration Data Management \(CDM\) nodes for a specified parent node.Includes an existing node into another node, such as a component node into a collection node or a collection node into a deployable node. After including a node, the new node has its own unique sys\_id and main\_Id.Creates a specific type of node, such as component, collection, folder, configuration data item \(CDI\), or variable.Updates the name and/or value of a specified node.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 36
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmEditorApi

The CdmEditorApi provides endpoints that enable you to create nodes, update nodes, include existing nodes under other nodes, delete nodes, and retrieve nodes and node includes.

You must have one of the following roles to access this API:

-   Scripted REST CDM View ACL \(sn\_cdm.cdm.viewer\)
-   Scripted REST CDM Editor ACL \(sn\_cdm.cdm\_editor\)

To view fields that have been encrypted, you must have the CDM Secret role.

In addition, the Configuration Data Management \(CDM\) plugin must be activated for this API to be available in an instance.

**Note:** The CdmEditorApi API cannot be used to modify any files. Only file deletion is allowed currently.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmEditorApi - DELETE /sn\_cdm/editor/nodes

Deletes a specified node.

The caller of this endpoint must have the CDM Editor role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/editor/nodes`

Default URL: `/api/sn_cdm/editor/nodes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changesetNumber

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

fullNamePath

</td><td id="fullNamePath-node-editor-entry">

Required. Path name of the node to delete. You can pass the name path in any of the following formats. For example, to delete the following node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

|Name|Description|
|----|-----------|
|None||

### cURL request

The following code example shows how to delete the node "cdi88".

```
curl "http://instance.servicenow.com/api/sn_cdm/editor/nodes?changesetNumber=Chset783&fullNamePath=%2FtestApp%2Fdeployables%2FDevelopment-1%2Fcdi88" \
--request DELETE \
--header "Accept:application/json" \
--user 'username':'password'
```

Return result:

```
None - just the associated HTTP status code
```

## CdmEditorApi - GET /sn\_cdm/editor/includes

Returns the list of nodes that were include within a specified node path.

The caller of this endpoint must have the CDM Viewer role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/editor/includes`

Default URL: `/api/sn_cdm/editor/includes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changesetNumber

</td><td>

Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr><tr><td>

sourceFullNamePath

</td><td>

Required. Path name of the source node for which to return the included nodes.You can pass the name path in any of the following formats. For example, to return the includes for the `collectionA` node in the `testApp/collections` directory:

-   Backslash format: `testApp/collections/collectionA`

**Note:** If your node name contains a backslash \("/"\), you can't use this format.

-   Backend name path with replacement characters: `testApp�collections�​collectionA`
-   Array: `['testApp','collections','collectionA']`

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_jpm_rxl_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeset\_id

</td><td>

Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

conflict

</td><td id="conflict-node-editor-entry">

Flag that indicates whether there was a conflict when processing the node.Possible values:

-   true: Conflict detected.
-   false: No conflict was detected.

Data type: Boolean

</td></tr><tr><td>

conflict\_type

</td><td id="conflict_type-node-editor-entry">

If the **conflict** parameter is true, the type of conflict detected. Null if no conflict is detected.Possible values:

-   corrupted\_node
-   deleted\_node
-   duplicated\_node
-   incomplete\_deleted\_parent
-   incomplete\_deleted\_ref
-   incomplete\_renamed\_ref
-   invalid\_include
-   orphaned\_descendant
-   related\_conflict
-   unlinked\_include
-   unrenamed\_include
-   updated\_node

Data type: String

</td></tr><tr><td>

description

</td><td id="description-node-editor-entry">

Short description of the purpose of the node.Data type: String

</td></tr><tr><td>

effective\_from

</td><td id="effective_from-node-editor-entry">

Timestamp \(converted to a long integer\) when the node was committed as part of the changeset. If the node hasn't been committed, this value is "null".Data type: Number \(Integer\)

</td></tr><tr><td>

effective\_to

</td><td id="effective_to-node-editor-entry">

Timestamp \(converted to a long integer\) of the node when it was either deleted or superseded by another node, otherwise "null".Data type: Number \(Integer\)

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

level

</td><td id="level-node-editor-entry">

Level of the node, starting from the root node, which is always 0. For example, the node `/AppA/components/compA` has two levels.Data type: String

</td></tr><tr><td>

linked\_to

</td><td id="linked_to-node-editor-entry">

The **main\_id** parameter of the referenced node to which this node is linked.If this node isn't linked to a reference node, the value is "null".

Data type: String

</td></tr><tr><td>

main\_id

</td><td id="main_id-node-editor-entry">

Primary identifier for the node. You can use this value in the CdmQuery\(\) script include to retrieve a JSON tree. For example: `CdmQuery().mainId(‘123’)/query().getTree();` Data type: String

</td></tr><tr><td>

main\_id\_encoded

</td><td id="main_id_encoded-node-editor-entry">

RADIX 57 string representation of the node's **main\_id** parameter.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the node that was included under the target path.Data type: String

</td></tr><tr><td>

node\_classifier

</td><td id="node_classifier-node-editor-entry">

Classifier hierarchy of the node. Use this information to locate a node within the folder hierarchy.For example, a deployable would have a hierarchy of `/application/deployables/env:Development`

While a collection would have a hierarchy of `/applications/collections`

Data type: String

</td></tr><tr><td>

node\_path

</td><td>

Full path name of the node that was included in the target path, such as `/Production/deployables/Development1/cdi1`. Data type: String

</td></tr><tr><td>

position

</td><td>

Node position.For example: If you upload the following array:

```
arrayNode1: [
  "literal1", 
  {"cdi1": 1},
  "literal3"
]
```

The position values are set as follows:

-   arrayNode1.literal1 = 1000
-   arrayNode1.2000 = 2000
-   arrayNode1.literal3 = 3000

If a complex object is uploaded under an array, in this case `{"cdi1": 1}`, the endpoint creates a new virtual node with the name equal to its position. In the example above, this is 2000. For includes, the position is always empty.

Data type: String

</td></tr><tr><td>

previous\_version

</td><td id="previous_version-node-editor-entry">

Details of the previous version of the node record. **Note:** If a new node was created, the endpoint returns `"previous_version" = null` for this parameter.

Data type: Object

```
"previous_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

restricted\_to

</td><td id="restricted_to-node-editor-entry">

Details of the group that has access the associated the node. Data type: Object

```
"restricted_to": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

secure\_value

</td><td>

If this value was flagged to be secured, the encrypted field \(returned masked\).A user must have the sn\_cdm.cdm\_secrets role to decrypt this information. You can direct the endpoint not to return these fields by setting the **returnFields** query parameter field.

Data type: String

</td></tr><tr><td>

status

</td><td>

Node status.Possible values:

-   DELETED
-   NEW
-   SUPERSEDED
-   UPDATED
-   VALID

Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

system\_folder

</td><td id="system_folder-node-editor-entry">

Flag that indicates whether the associated node is a system folder.Possible values:

-   true: Node is a system folder.
-   false: Node isn't a system folder.

Data type: Boolean

</td></tr><tr><td>

type

</td><td>

Node type.

Possible values:

-   sn\_cdm\_node\_cdi
-   sn\_cdm\_node\_collection
-   sn\_cdm\_node\_component
-   sn\_cdm\_node\_folder
-   sn\_cdm\_node\_variable

Data type: String

</td></tr><tr><td>

value

</td><td>

Node value.Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how retrieve the includes in the source path `/testApp/collections/collA`.

```
curl "http://instance.servicenow.com/api/sn_cdm/editor/includes?changesetNumber=Chset5&sourceFullNamePath=%2FtestApp%2Fcollections%2FcollA" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return result:

```
{ 
  "result": [ 
    { 
      "sys_id": "a1c517a953b70110a1d3ddeeff7b129b", 
      "type": "sn_cdm_node_deployable", 
      "main_id": "6", 
      "main_id_encoded": ",", 
      "node_path": "!$!+!,", 
      "level": 2, 
      "status": "valid", 
      "node_classifier": "/application/deployables/env:Development", 
      "position": null, 
      "restricted_to": null, 
      "changeset_id": "e9c517a953b70110a1d3ddeeff7b1299", 
      "previous_version": null, 
      "effective_from": "1654002206866", 
      "effective_to": null, 
      "name": "Development_1", 
      "description": null, 
      "value": null, 
      "secure_value": null, 
      "system_folder": "0", 
      "linked_to": null, 
      "conflict": "0", 
      "conflict_type": null 
    } 
  ] 
}
```

## CdmEditorApi - GET /sn\_cdm/editor/nodes

Returns the details of a specified node or a list of child Configuration Data Management \(CDM\) nodes for a specified parent node.

The caller of this endpoint must have the CDM Viewer role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/editor/nodes`

Default URL: `/api/sn_cdm/editor/nodes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changesetNumber

</td><td>

Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

decryptPassword

</td><td>

Flag that indicates whether the value should be encrypted for the leaf nodes.Valid values:

-   true: Encrypted
-   false: Not encrypted

Data type: Boolean

Default: false

</td></tr><tr><td>

name

</td><td>

Node name. If you pass this parameter, only the results for the specified node are returned.Data type: String

Default: All nodes within the parent node

</td></tr><tr><td>

parentFullNamePath

</td><td>

Required. Path name of the parent node for which to return the child nodes or to which the node specified in the **name** parameter resides.You can pass the name path in any of the following formats. For example, to return the nodes for the `collectionA` node in the `testApp/collections` directory:

-   Backslash format: `testApp/collections/collectionA`

**Note:** If your node name contains a backslash \("/"\), you can't use this format.

-   Backend name path with replacement characters: `testApp�collections�​collectionA`
-   Array: `['testApp','collections','collectionA']`

Data type: String

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr><tr><td>

type

</td><td id="type-node-editor-entry">

Node type.

Possible values:

-   sn\_cdm\_node\_cdi OR cdi
-   sn\_cdm\_node\_collection OR collection
-   sn\_cdm\_node\_component OR component
-   sn\_cdm\_node\_folder OR folder
-   sn\_cdm\_node\_variable OR variable

Data type: String

 Default: All

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_nwg_5jl_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="changeset-node-editor-row"><td>

changeset\_id

</td><td id="changeset-node-editor-entry">

Details of the changeset record associated with the node. Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="changeset_link-node-editor-row"><td>

changeset\_id.link

</td><td id="changeset_link-node-editor-entry">

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr id="changeset_value-node-editor-row"><td>

changeset\_id.value

</td><td id="changeset_value-node-editor-entry">

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr id="conflict-node-editor-row"><td>

conflict

</td><td id="conflict-node-editor-entry">

Flag that indicates whether there was a conflict when processing the node.Possible values:

-   true: Conflict detected.
-   false: No conflict was detected.

Data type: Boolean

</td></tr><tr id="conflict_type-node-editor-row"><td>

conflict\_type

</td><td id="conflict_type-node-editor-entry">

If the **conflict** parameter is true, the type of conflict detected. Null if no conflict is detected.Possible values:

-   corrupted\_node
-   deleted\_node
-   duplicated\_node
-   incomplete\_deleted\_parent
-   incomplete\_deleted\_ref
-   incomplete\_renamed\_ref
-   invalid\_include
-   orphaned\_descendant
-   related\_conflict
-   unlinked\_include
-   unrenamed\_include
-   updated\_node

Data type: String

</td></tr><tr id="description-node-editor-row"><td>

description

</td><td id="description-node-editor-entry">

Short description of the purpose of the node.Data type: String

</td></tr><tr id="effective_from-node-editor-row"><td>

effective\_from

</td><td id="effective_from-node-editor-entry">

Timestamp \(converted to a long integer\) when the node was committed as part of the changeset. If the node hasn't been committed, this value is "null".Data type: Number \(Integer\)

</td></tr><tr id="effective_to-node-editor-row"><td>

effective\_to

</td><td id="effective_to-node-editor-entry">

Timestamp \(converted to a long integer\) of the node when it was either deleted or superseded by another node, otherwise "null".Data type: Number \(Integer\)

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="level-node-editor-row"><td>

level

</td><td id="level-node-editor-entry">

Level of the node, starting from the root node, which is always 0. For example, the node `/AppA/components/compA` has two levels.Data type: String

</td></tr><tr id="linked_to-node-editor-row"><td>

linked\_to

</td><td id="linked_to-node-editor-entry">

The **main\_id** parameter of the referenced node to which this node is linked.If this node isn't linked to a reference node, the value is "null".

Data type: String

</td></tr><tr id="main_id-node-editor-row"><td>

main\_id

</td><td id="main_id-node-editor-entry">

Primary identifier for the node. You can use this value in the CdmQuery\(\) script include to retrieve a JSON tree. For example: `CdmQuery().mainId(‘123’)/query().getTree();` Data type: String

</td></tr><tr id="main_id_encoded-node-editor-row"><td>

main\_id\_encoded

</td><td id="main_id_encoded-node-editor-entry">

RADIX 57 string representation of the node's **main\_id** parameter.Data type: String

</td></tr><tr id="name-node-editor-row"><td>

name

</td><td id="name-node-editor-entry">

Name of the node.Data type: String

</td></tr><tr id="node_classifier-node-editor-row"><td>

node\_classifier

</td><td id="node_classifier-node-editor-entry">

Classifier hierarchy of the node. Use this information to locate a node within the folder hierarchy.For example, a deployable would have a hierarchy of `/application/deployables/env:Development`

While a collection would have a hierarchy of `/applications/collections`

Data type: String

</td></tr><tr id="name_path-node-editor-row"><td>

node\_path

</td><td id="name_path-node-editor-entry">

Full node path name. Data type: String

</td></tr><tr id="position-node-editor-row"><td>

position

</td><td id="position-node-editor-entry">

Node position.For example: If you upload the following array:

```
arrayNode1: [
  "literal1", 
  {"cdi1": 1},
  "literal3"
]
```

The position values are set as follows:

-   arrayNode1.literal1 = 1000
-   arrayNode1.2000 = 2000
-   arrayNode1.literal3 = 3000

If a complex object is uploaded under an array, in this case `{"cdi1": 1}`, the endpoint creates a new virtual node with the name equal to its position. In the example above, this is 2000. For includes, the position is always empty.

Data type: String

</td></tr><tr id="previous_version-node-editor-row"><td>

previous\_version

</td><td id="previous_version-node-editor-entry">

Details of the previous version of the node record. **Note:** If a new node was created, the endpoint returns `"previous_version" = null` for this parameter.

Data type: Object

```
"previous_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="previous_version_link-node-editor-row"><td>

previous\_version.link

</td><td id="previous_version_link-node-editor-entry">

Call syntax for querying this node record using the Table REST API.Data type: String

</td></tr><tr id="previous_version_value-node-editor-row"><td>

previous\_version.value

</td><td id="previous_version_value-node-editor-entry">

Sys\_id of the node record.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

reason\_for\_conflict

</td><td>

Detailed explanation of the conflict.Data type: String

</td></tr><tr id="restricted_to-node-editor-row"><td>

restricted\_to

</td><td id="restricted_to-node-editor-entry">

Details of the group that has access the associated the node. Data type: Object

```
"restricted_to": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="restricted_to_link-node-editor-row"><td>

restricted\_to.link

</td><td id="restricted_to_link-node-editor-entry">

Call syntax for querying this group record using the Table REST API.Data type: String

</td></tr><tr id="restricted_to_value-node-editor-row"><td>

restricted\_to.value

</td><td id="restricted_to_value-node-editor-entry">

Sys\_id of the group record.Data type: String

Table: CDM Group \[sys\_user\_group\]

</td></tr><tr id="secure_value-node-editor-row"><td>

secure\_value

</td><td id="secure_value-node-editor-entry">

If this value was flagged to be secured, the encrypted field \(returned masked\).A user must have the sn\_cdm.cdm\_secrets role to decrypt this information. You can direct the endpoint not to return these fields by setting the **returnFields** query parameter field.

Data type: String

</td></tr><tr id="status-node-editor-row"><td>

status

</td><td id="status-node-editor-entry">

Node status.Possible values:

-   DELETED
-   NEW
-   SUPERSEDED
-   UPDATED
-   VALID

Data type: String

</td></tr><tr id="system_folder-node-editor-row"><td>

system\_folder

</td><td id="system_folder-node-editor-entry">

Flag that indicates whether the associated node is a system folder.Possible values:

-   true: Node is a system folder.
-   false: Node isn't a system folder.

Data type: Boolean

</td></tr><tr id="sys_class_name-node-editor-row"><td>

sys\_class\_name

</td><td id="sys_class_name-node-editor-entry">

Table in which the node resides.Data type: String

</td></tr><tr id="sys_created_by-node-editor-row"><td>

sys\_created\_by

</td><td id="sys_created_by-node-editor-entry">

Name of the user that created the node.Data type: String

</td></tr><tr id="sys_created_on-node-editor-row"><td>

sys\_created\_on

</td><td id="sys_created_on-node-editor-entry">

Date and time when the node was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="sys_id-node-editor-row"><td>

sys\_id

</td><td id="sys_id-node-editor-entry">

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr id="sys_updated_by-node-editor-row"><td>

sys\_updated\_by

</td><td id="sys_updated_by-node-editor-entry">

Name of the user that updated the node.Data type: String

</td></tr><tr id="sys_updated_on-node-editor-row"><td>

sys\_updated\_on

</td><td id="sys_updated_on-node-editor-entry">

Date and time when the node was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="type-node-editor-row"><td>

type

</td><td id="d3015e3625">

Node type.

Possible values:

-   sn\_cdm\_node\_cdi
-   sn\_cdm\_node\_collection
-   sn\_cdm\_node\_component
-   sn\_cdm\_node\_folder
-   sn\_cdm\_node\_variable

Data type: String

 Default: All

</td></tr><tr id="value-node-editor-row"><td>

value

</td><td id="value-node-editor-entry">

Node value.Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to retrieve the child nodes of type sn\_cdm\_node\_cdi under the `/testApp/Fdeployables/Development_1` parent node.

```
curl "http://instance.servicenow.com/api/sn_cdm/editor/nodes?decryptPassword=true&name=cdi45&changesetNumber=Chset3&parentFullNamePath=%2FtestApp%2Fdeployables%2FDevelopment_1&type=sn_cdm_node_cdi" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return result:

```
{ 
  "result": [ 
    { 
      "changeset_id": { 
        "value": "d403648653b70110a1d3ddeeff7b12c5", 
        "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/d403648653b70110a1d3ddeeff7b12c5" 
      }, 
      "node_path": "!$!+!,![:", 
      "description": null, 
      "sys_updated_on": "2022-06-30 09:24:07", 
      "type": "sn_cdm_node_cdi", 
      "sys_class_name": "sn_cdm_node", 
      "sys_id": "c93c7c1753981110a1d3ddeeff7b12c7", 
      "sys_updated_by": "admin", 
      "previous_version": null, 
      "sys_created_on": "2022-06-30 08:53:13", 
      "value": "cdcdc", 
      "effective_from": null, 
      "linked_to": null, 
      "sys_created_by": "admin", 
      "restricted_to": null, 
      "level": "3", 
      "conflict_type": null, 
      "main_id": "2869", 
      "effective_to": null, 
      "secure_value": null, 
      "node_classifier": "/application/deployables/env:Development", 
      "main_id_encoded": "[:", 
      "name": "cdi45", 
      "position": null, 
      "reason_for_conflict": null, 
      "system_folder": false, 
      "status": "new", 
      "conflict": false 
    } 
  ] 
}
```

## CdmEditorApi - POST /sn\_cdm/editor/includes

Includes an existing node into another node, such as a component node into a collection node or a collection node into a deployable node. After including a node, the new node has its own unique sys\_id and main\_Id.

The caller of this endpoint must have the CDM Editor role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/editor/includes`

Default URL: `/api/sn_cdm/editor/includes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changesetNumber

</td><td>

Required. Unique number of the open changeset to include in the target node.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr><tr><td>

sourceFullNamePath

</td><td>

Required. Path name of the node to include in the target node.You can pass the name path in any of the following formats. For example, to include the following node `Staging/deployables/Development1/cdi1`:

-   Backslash format: `Staging/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can't use this format.

-   Backend name path with replacement characters: `Staging�deployables�​Development1​�​cdi1`
-   Array: `['Staging','deployables','Development1','cdi1']`

Data type: String

</td></tr><tr><td>

targetFullNamePath

</td><td>

Required. Path name of the node under which the source node is to be included. You can pass the name path in any of the following formats. For example, to include the following node `Production/deployables/Development1`:

-   Backslash format: `Production/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can't use this format.

-   Backend name path with replacement characters: `Production�deployables�​Development1​�​cdi1`
-   Array: `['Production','deployables','Development1','cdi1']`

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_cvv_pxl_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeset\_id

</td><td>

Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

conflict

</td><td id="conflict-node-editor-entry">

Flag that indicates whether there was a conflict when processing the node.Possible values:

-   true: Conflict detected.
-   false: No conflict was detected.

Data type: Boolean

</td></tr><tr><td>

conflict\_type

</td><td id="conflict_type-node-editor-entry">

If the **conflict** parameter is true, the type of conflict detected. Null if no conflict is detected.Possible values:

-   corrupted\_node
-   deleted\_node
-   duplicated\_node
-   incomplete\_deleted\_parent
-   incomplete\_deleted\_ref
-   incomplete\_renamed\_ref
-   invalid\_include
-   orphaned\_descendant
-   related\_conflict
-   unlinked\_include
-   unrenamed\_include
-   updated\_node

Data type: String

</td></tr><tr><td>

description

</td><td id="description-node-editor-entry">

Short description of the purpose of the node.Data type: String

</td></tr><tr><td>

effective\_from

</td><td id="effective_from-node-editor-entry">

Timestamp \(converted to a long integer\) when the node was committed as part of the changeset. If the node hasn't been committed, this value is "null".Data type: Number \(Integer\)

</td></tr><tr><td>

effective\_to

</td><td id="effective_to-node-editor-entry">

Timestamp \(converted to a long integer\) of the node when it was either deleted or superseded by another node, otherwise "null".Data type: Number \(Integer\)

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

level

</td><td id="level-node-editor-entry">

Level of the node, starting from the root node, which is always 0. For example, the node `/AppA/components/compA` has two levels.Data type: String

</td></tr><tr><td>

linked\_to

</td><td id="linked_to-node-editor-entry">

The **main\_id** parameter of the referenced node to which this node is linked.If this node isn't linked to a reference node, the value is "null".

Data type: String

</td></tr><tr><td>

main\_id

</td><td id="main_id-node-editor-entry">

Primary identifier for the node. You can use this value in the CdmQuery\(\) script include to retrieve a JSON tree. For example: `CdmQuery().mainId(‘123’)/query().getTree();` Data type: String

</td></tr><tr><td>

main\_id\_encoded

</td><td id="main_id_encoded-node-editor-entry">

RADIX 57 string representation of the node's **main\_id** parameter.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the node that was included under the target path.Data type: String

</td></tr><tr><td>

node\_classifier

</td><td id="node_classifier-node-editor-entry">

Classifier hierarchy of the node. Use this information to locate a node within the folder hierarchy.For example, a deployable would have a hierarchy of `/application/deployables/env:Development`

While a collection would have a hierarchy of `/applications/collections`

Data type: String

</td></tr><tr><td>

node\_path

</td><td>

Full path name of the node that was included in the target path, such as `/Production/deployables/Development1/cdi1`. Data type: String

</td></tr><tr><td>

position

</td><td>

Node position.For example: If you upload the following array:

```
arrayNode1: [
  "literal1", 
  {"cdi1": 1},
  "literal3"
]
```

The position values are set as follows:

-   arrayNode1.literal1 = 1000
-   arrayNode1.2000 = 2000
-   arrayNode1.literal3 = 3000

If a complex object is uploaded under an array, in this case `{"cdi1": 1}`, the endpoint creates a new virtual node with the name equal to its position. In the example above, this is 2000. For includes, the position is always empty.

Data type: String

</td></tr><tr><td>

previous\_version

</td><td id="previous_version-node-editor-entry">

Details of the previous version of the node record. **Note:** If a new node was created, the endpoint returns `"previous_version" = null` for this parameter.

Data type: Object

```
"previous_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

restricted\_to

</td><td id="restricted_to-node-editor-entry">

Details of the group that has access the associated the node. Data type: Object

```
"restricted_to": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

secure\_value

</td><td>

If this value was flagged to be secured, the encrypted field \(returned masked\).A user must have the sn\_cdm.cdm\_secrets role to decrypt this information. You can direct the endpoint not to return these fields by setting the **returnFields** query parameter field.

Data type: String

</td></tr><tr><td>

status

</td><td>

Node status.Possible values:

-   DELETED
-   NEW
-   SUPERSEDED
-   UPDATED
-   VALID

Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

system\_folder

</td><td id="system_folder-node-editor-entry">

Flag that indicates whether the associated node is a system folder.Possible values:

-   true: Node is a system folder.
-   false: Node isn't a system folder.

Data type: Boolean

</td></tr><tr><td>

type

</td><td>

Node type.

Possible values:

-   sn\_cdm\_node\_cdi
-   sn\_cdm\_node\_collection
-   sn\_cdm\_node\_component
-   sn\_cdm\_node\_folder
-   sn\_cdm\_node\_variable

Data type: String

</td></tr><tr><td>

value

</td><td>

Node value.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to include the node `/testApp/collections/collA` under `/testApp/deployables/Development_1`.

```
curl "http://instance.servicenow.com/api/sn_cdm/editor/includes?changesetNumber=Chset5&targetFullNamePath=%2FtestApp%2Fdeployables%2FDevelopment_1&sourceFullNamePath=%2FtestApp%2Fcollecti
ons%2FcollA" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Return result:

```
{ 
  "result": { 
    "changeset_id": { 
      "value": "d403648653b70110a1d3ddeeff7b12c5", 
      "link": "http://192.168.0.233:8080/api/now/table/sn_cdm_changeset/d403648653b70110a1d3ddeeff7b12c5" 
    }, 
    "node_path": "!$!+!,![?", 
    "description": null, 
    "sys_updated_on": "2022-06-30 09:19:47", 
    "type": "sn_cdm_node_linked", 
    "sys_class_name": "sn_cdm_node", 
    "sys_id": "1642015b53981110a1d3ddeeff7b1232", 
    "sys_updated_by": "admin", 
    "previous_version": null, 
    "sys_created_on": "2022-06-30 09:19:47", 
    "value": null, 
    "effective_from": null, 
    "linked_to": "2870", 
    "sys_created_by": "admin", 
    "restricted_to": null, 
    "level": "3", 
    "conflict_type": null, 
    "main_id": "2872", 
    "effective_to": null, 
    "secure_value": null, 
    "node_classifier": "/application/deployables/env:Development", 
    "main_id_encoded": "[?", 
    "name": "collA", 
    "position": null, 
    "reason_for_conflict": null, 
    "system_folder": false, 
    "status": "new", 
    "conflict": false 
  } 
}
```

## CdmEditorApi - POST /sn\_cdm/editor/nodes

Creates a specific type of node, such as component, collection, folder, configuration data item \(CDI\), or variable.

You can also specify whether to automatically generate any parent nodes that are not currently defined.

The caller of this endpoint must have either the CDM Editor or CDM Secret role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/editor/nodes`

Default URL: `/api/sn_cdm/editor/nodes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

autoCreateParents

</td><td>

Flag that indicates whether to automatically create the non-existent parents in the name path as components. Exceptions to this are the app, deployable, and collection. If you do not set this flag and the parents do not already exist, the endpoint fails.Valid values:

-   true: Automatically create the non-existent parents.
-   false: Don't automatically create the non-existent parents.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

fullNamePath

</td><td id="fullNamePath-node-editor-entry">

Required. Path name of the node. You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

Data type: String

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr><tr><td>

secure

</td><td id="secure-node-editor-entry">

Flag that indicates whether the value should be encrypted for the leaf nodes.Valid values:

-   true: Encrypted
-   false: Not encrypted

Data type: Boolean

Default: false

</td></tr><tr><td>

type

</td><td>

Required. Type of new node.Valid values:

-   sn\_cdm\_node\_collection OR collection
-   sn\_cdm\_node\_component OR component
-   sn\_cdm\_node\_folder OR folder
-   sn\_cdm\_node\_cdi OR cdi
-   sn\_cdm\_node\_variable or variable

Data type: String

</td></tr><tr><td>

value

</td><td>

Value of the new node.Data type: String

 Default: Equivalent of "null"

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_nwg_5jl_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="changeset-node-editor-row"><td>

changeset\_id

</td><td id="changeset-node-editor-entry">

Details of the changeset record associated with the node. Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="changeset_link-node-editor-row"><td>

changeset\_id.link

</td><td id="changeset_link-node-editor-entry">

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr id="changeset_value-node-editor-row"><td>

changeset\_id.value

</td><td id="changeset_value-node-editor-entry">

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr id="conflict-node-editor-row"><td>

conflict

</td><td id="conflict-node-editor-entry">

Flag that indicates whether there was a conflict when processing the node.Possible values:

-   true: Conflict detected.
-   false: No conflict was detected.

Data type: Boolean

</td></tr><tr id="conflict_type-node-editor-row"><td>

conflict\_type

</td><td id="conflict_type-node-editor-entry">

If the **conflict** parameter is true, the type of conflict detected. Null if no conflict is detected.Possible values:

-   corrupted\_node
-   deleted\_node
-   duplicated\_node
-   incomplete\_deleted\_parent
-   incomplete\_deleted\_ref
-   incomplete\_renamed\_ref
-   invalid\_include
-   orphaned\_descendant
-   related\_conflict
-   unlinked\_include
-   unrenamed\_include
-   updated\_node

Data type: String

</td></tr><tr id="description-node-editor-row"><td>

description

</td><td id="description-node-editor-entry">

Short description of the purpose of the node.Data type: String

</td></tr><tr id="effective_from-node-editor-row"><td>

effective\_from

</td><td id="effective_from-node-editor-entry">

Timestamp \(converted to a long integer\) when the node was committed as part of the changeset. If the node hasn't been committed, this value is "null".Data type: Number \(Integer\)

</td></tr><tr id="effective_to-node-editor-row"><td>

effective\_to

</td><td id="effective_to-node-editor-entry">

Timestamp \(converted to a long integer\) of the node when it was either deleted or superseded by another node, otherwise "null".Data type: Number \(Integer\)

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="level-node-editor-row"><td>

level

</td><td id="level-node-editor-entry">

Level of the node, starting from the root node, which is always 0. For example, the node `/AppA/components/compA` has two levels.Data type: String

</td></tr><tr id="linked_to-node-editor-row"><td>

linked\_to

</td><td id="linked_to-node-editor-entry">

The **main\_id** parameter of the referenced node to which this node is linked.If this node isn't linked to a reference node, the value is "null".

Data type: String

</td></tr><tr id="main_id-node-editor-row"><td>

main\_id

</td><td id="main_id-node-editor-entry">

Primary identifier for the node. You can use this value in the CdmQuery\(\) script include to retrieve a JSON tree. For example: `CdmQuery().mainId(‘123’)/query().getTree();` Data type: String

</td></tr><tr id="main_id_encoded-node-editor-row"><td>

main\_id\_encoded

</td><td id="main_id_encoded-node-editor-entry">

RADIX 57 string representation of the node's **main\_id** parameter.Data type: String

</td></tr><tr id="name-node-editor-row"><td>

name

</td><td id="name-node-editor-entry">

Name of the node.Data type: String

</td></tr><tr id="node_classifier-node-editor-row"><td>

node\_classifier

</td><td id="node_classifier-node-editor-entry">

Classifier hierarchy of the node. Use this information to locate a node within the folder hierarchy.For example, a deployable would have a hierarchy of `/application/deployables/env:Development`

While a collection would have a hierarchy of `/applications/collections`

Data type: String

</td></tr><tr id="name_path-node-editor-row"><td>

node\_path

</td><td id="name_path-node-editor-entry">

Full node path name. Data type: String

</td></tr><tr id="position-node-editor-row"><td>

position

</td><td id="position-node-editor-entry">

Node position.For example: If you upload the following array:

```
arrayNode1: [
  "literal1", 
  {"cdi1": 1},
  "literal3"
]
```

The position values are set as follows:

-   arrayNode1.literal1 = 1000
-   arrayNode1.2000 = 2000
-   arrayNode1.literal3 = 3000

If a complex object is uploaded under an array, in this case `{"cdi1": 1}`, the endpoint creates a new virtual node with the name equal to its position. In the example above, this is 2000. For includes, the position is always empty.

Data type: String

</td></tr><tr id="previous_version-node-editor-row"><td>

previous\_version

</td><td id="previous_version-node-editor-entry">

Details of the previous version of the node record. **Note:** If a new node was created, the endpoint returns `"previous_version" = null` for this parameter.

Data type: Object

```
"previous_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="previous_version_link-node-editor-row"><td>

previous\_version.link

</td><td id="previous_version_link-node-editor-entry">

Call syntax for querying this node record using the Table REST API.Data type: String

</td></tr><tr id="previous_version_value-node-editor-row"><td>

previous\_version.value

</td><td id="previous_version_value-node-editor-entry">

Sys\_id of the node record.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

reason\_for\_conflict

</td><td>

Detailed explanation of the conflict.Data type: String

</td></tr><tr id="restricted_to-node-editor-row"><td>

restricted\_to

</td><td id="restricted_to-node-editor-entry">

Details of the group that has access the associated the node. Data type: Object

```
"restricted_to": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="restricted_to_link-node-editor-row"><td>

restricted\_to.link

</td><td id="restricted_to_link-node-editor-entry">

Call syntax for querying this group record using the Table REST API.Data type: String

</td></tr><tr id="restricted_to_value-node-editor-row"><td>

restricted\_to.value

</td><td id="restricted_to_value-node-editor-entry">

Sys\_id of the group record.Data type: String

Table: CDM Group \[sys\_user\_group\]

</td></tr><tr id="secure_value-node-editor-row"><td>

secure\_value

</td><td id="secure_value-node-editor-entry">

If this value was flagged to be secured, the encrypted field \(returned masked\).A user must have the sn\_cdm.cdm\_secrets role to decrypt this information. You can direct the endpoint not to return these fields by setting the **returnFields** query parameter field.

Data type: String

</td></tr><tr id="status-node-editor-row"><td>

status

</td><td id="status-node-editor-entry">

Node status.Possible values:

-   DELETED
-   NEW
-   SUPERSEDED
-   UPDATED
-   VALID

Data type: String

</td></tr><tr id="system_folder-node-editor-row"><td>

system\_folder

</td><td id="system_folder-node-editor-entry">

Flag that indicates whether the associated node is a system folder.Possible values:

-   true: Node is a system folder.
-   false: Node isn't a system folder.

Data type: Boolean

</td></tr><tr id="sys_class_name-node-editor-row"><td>

sys\_class\_name

</td><td id="sys_class_name-node-editor-entry">

Table in which the node resides.Data type: String

</td></tr><tr id="sys_created_by-node-editor-row"><td>

sys\_created\_by

</td><td id="sys_created_by-node-editor-entry">

Name of the user that created the node.Data type: String

</td></tr><tr id="sys_created_on-node-editor-row"><td>

sys\_created\_on

</td><td id="sys_created_on-node-editor-entry">

Date and time when the node was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="sys_id-node-editor-row"><td>

sys\_id

</td><td id="sys_id-node-editor-entry">

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr id="sys_updated_by-node-editor-row"><td>

sys\_updated\_by

</td><td id="sys_updated_by-node-editor-entry">

Name of the user that updated the node.Data type: String

</td></tr><tr id="sys_updated_on-node-editor-row"><td>

sys\_updated\_on

</td><td id="sys_updated_on-node-editor-entry">

Date and time when the node was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="type-node-editor-row"><td>

type

</td><td id="type-node-editor-entry">

Node type.

Possible values:

-   sn\_cdm\_node\_cdi
-   sn\_cdm\_node\_collection
-   sn\_cdm\_node\_component
-   sn\_cdm\_node\_folder
-   sn\_cdm\_node\_variable

Data type: String

 Default: All

</td></tr><tr id="value-node-editor-row"><td>

value

</td><td id="value-node-editor-entry">

Node value.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to create a node using this endpoint.

```
curl "http://instance.servicenow.com/api/sn_cdm/editor/nodes?fullNamePath=%2FtestApp%2Fdeployables%2FDevelopment1%2Fcdi1&secure=true&value=someVal&type=cdi&changesetNumber=Chset-760" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Return result:

```
{ 
  "result": { 
    "changeset_id": { 
      "value": "d403648653b70110a1d3ddeeff7b12c5", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/d403648653b70110a1d3ddeeff7b12c5" 
    }, 
    "node_path": "!$!+!,![:", 
    "description": null, 
    "sys_updated_on": "2022-06-30 08:53:13", 
    "type": "sn_cdm_node_cdi", 
    "sys_class_name": "sn_cdm_node", 
    "sys_id": "c93c7c1753981110a1d3ddeeff7b12c7", 
    "sys_updated_by": "admin", 
    "previous_version": null, 
    "sys_created_on": "2022-06-30 08:53:13", 
    "value": null, 
    "effective_from": null, 
    "linked_to": null, 
    "sys_created_by": "admin", 
    "restricted_to": null, 
    "level": "3", 
    "conflict_type": null, 
    "main_id": "2869", 
    "effective_to": null, 
    "secure_value": "﷞﷟﷒113a0c6e53001110a1d3ddeeff7b121d﷬﷔1﷬﷭bAUA1wj-fxofbSrMyF-BAg==6qiho5f_9DhnuHT2Km5SLf0Ck4XNX_w=﷮﷯", 
    "node_classifier": "/application/deployables/env:Development", 
    "main_id_encoded": "[:", 
    "name": "cdi45", 
    "position": null, 
    "reason_for_conflict": null, 
    "system_folder": false, 
    "status": "new", 
    "conflict": false 
  } 
}
```

## CdmEditorApi - PUT /sn\_cdm/editor/nodes

Updates the name and/or value of a specified node.

The caller of this endpoint must have either the CDM Editor or CDM Secret role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/editor/nodes`

Default URL: `/api/sn_cdm/editor/nodes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changesetNumber

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

fullNamePath

</td><td id="fullNamePath-node-editor-entry">

Required. Path name of the node. You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

Data type: String

</td></tr><tr><td>

newName

</td><td>

New name for the associated node.Data type: String

</td></tr><tr><td>

newValue

</td><td>

New value for the associated node.Data type: String

</td></tr><tr><td>

secure

</td><td id="secure-node-editor-entry">

Flag that indicates whether the value should be encrypted for the leaf nodes.Valid values:

-   true: Encrypted
-   false: Not encrypted

Data type: Boolean

Default: false

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_nwg_5jl_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="changeset-node-editor-row"><td>

changeset\_id

</td><td id="changeset-node-editor-entry">

Details of the changeset record associated with the node. Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="changeset_link-node-editor-row"><td>

changeset\_id.link

</td><td id="changeset_link-node-editor-entry">

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr id="changeset_value-node-editor-row"><td>

changeset\_id.value

</td><td id="changeset_value-node-editor-entry">

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr id="conflict-node-editor-row"><td>

conflict

</td><td id="conflict-node-editor-entry">

Flag that indicates whether there was a conflict when processing the node.Possible values:

-   true: Conflict detected.
-   false: No conflict was detected.

Data type: Boolean

</td></tr><tr id="conflict_type-node-editor-row"><td>

conflict\_type

</td><td id="conflict_type-node-editor-entry">

If the **conflict** parameter is true, the type of conflict detected. Null if no conflict is detected.Possible values:

-   corrupted\_node
-   deleted\_node
-   duplicated\_node
-   incomplete\_deleted\_parent
-   incomplete\_deleted\_ref
-   incomplete\_renamed\_ref
-   invalid\_include
-   orphaned\_descendant
-   related\_conflict
-   unlinked\_include
-   unrenamed\_include
-   updated\_node

Data type: String

</td></tr><tr id="description-node-editor-row"><td>

description

</td><td id="description-node-editor-entry">

Short description of the purpose of the node.Data type: String

</td></tr><tr id="effective_from-node-editor-row"><td>

effective\_from

</td><td id="effective_from-node-editor-entry">

Timestamp \(converted to a long integer\) when the node was committed as part of the changeset. If the node hasn't been committed, this value is "null".Data type: Number \(Integer\)

</td></tr><tr id="effective_to-node-editor-row"><td>

effective\_to

</td><td id="effective_to-node-editor-entry">

Timestamp \(converted to a long integer\) of the node when it was either deleted or superseded by another node, otherwise "null".Data type: Number \(Integer\)

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="level-node-editor-row"><td>

level

</td><td id="level-node-editor-entry">

Level of the node, starting from the root node, which is always 0. For example, the node `/AppA/components/compA` has two levels.Data type: String

</td></tr><tr id="linked_to-node-editor-row"><td>

linked\_to

</td><td id="linked_to-node-editor-entry">

The **main\_id** parameter of the referenced node to which this node is linked.If this node isn't linked to a reference node, the value is "null".

Data type: String

</td></tr><tr id="main_id-node-editor-row"><td>

main\_id

</td><td id="main_id-node-editor-entry">

Primary identifier for the node. You can use this value in the CdmQuery\(\) script include to retrieve a JSON tree. For example: `CdmQuery().mainId(‘123’)/query().getTree();` Data type: String

</td></tr><tr id="main_id_encoded-node-editor-row"><td>

main\_id\_encoded

</td><td id="main_id_encoded-node-editor-entry">

RADIX 57 string representation of the node's **main\_id** parameter.Data type: String

</td></tr><tr id="name-node-editor-row"><td>

name

</td><td id="name-node-editor-entry">

Name of the node.Data type: String

</td></tr><tr id="node_classifier-node-editor-row"><td>

node\_classifier

</td><td id="node_classifier-node-editor-entry">

Classifier hierarchy of the node. Use this information to locate a node within the folder hierarchy.For example, a deployable would have a hierarchy of `/application/deployables/env:Development`

While a collection would have a hierarchy of `/applications/collections`

Data type: String

</td></tr><tr id="name_path-node-editor-row"><td>

node\_path

</td><td id="name_path-node-editor-entry">

Full node path name. Data type: String

</td></tr><tr id="position-node-editor-row"><td>

position

</td><td id="position-node-editor-entry">

Node position.For example: If you upload the following array:

```
arrayNode1: [
  "literal1", 
  {"cdi1": 1},
  "literal3"
]
```

The position values are set as follows:

-   arrayNode1.literal1 = 1000
-   arrayNode1.2000 = 2000
-   arrayNode1.literal3 = 3000

If a complex object is uploaded under an array, in this case `{"cdi1": 1}`, the endpoint creates a new virtual node with the name equal to its position. In the example above, this is 2000. For includes, the position is always empty.

Data type: String

</td></tr><tr id="previous_version-node-editor-row"><td>

previous\_version

</td><td id="previous_version-node-editor-entry">

Details of the previous version of the node record. **Note:** If a new node was created, the endpoint returns `"previous_version" = null` for this parameter.

Data type: Object

```
"previous_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="previous_version_link-node-editor-row"><td>

previous\_version.link

</td><td id="previous_version_link-node-editor-entry">

Call syntax for querying this node record using the Table REST API.Data type: String

</td></tr><tr id="previous_version_value-node-editor-row"><td>

previous\_version.value

</td><td id="previous_version_value-node-editor-entry">

Sys\_id of the node record.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

reason\_for\_conflict

</td><td>

Detailed explanation of the conflict.Data type: String

</td></tr><tr id="restricted_to-node-editor-row"><td>

restricted\_to

</td><td id="restricted_to-node-editor-entry">

Details of the group that has access the associated the node. Data type: Object

```
"restricted_to": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="restricted_to_link-node-editor-row"><td>

restricted\_to.link

</td><td id="restricted_to_link-node-editor-entry">

Call syntax for querying this group record using the Table REST API.Data type: String

</td></tr><tr id="restricted_to_value-node-editor-row"><td>

restricted\_to.value

</td><td id="restricted_to_value-node-editor-entry">

Sys\_id of the group record.Data type: String

Table: CDM Group \[sys\_user\_group\]

</td></tr><tr id="secure_value-node-editor-row"><td>

secure\_value

</td><td id="secure_value-node-editor-entry">

If this value was flagged to be secured, the encrypted field \(returned masked\).A user must have the sn\_cdm.cdm\_secrets role to decrypt this information. You can direct the endpoint not to return these fields by setting the **returnFields** query parameter field.

Data type: String

</td></tr><tr id="status-node-editor-row"><td>

status

</td><td id="status-node-editor-entry">

Node status.Possible values:

-   DELETED
-   NEW
-   SUPERSEDED
-   UPDATED
-   VALID

Data type: String

</td></tr><tr id="system_folder-node-editor-row"><td>

system\_folder

</td><td id="system_folder-node-editor-entry">

Flag that indicates whether the associated node is a system folder.Possible values:

-   true: Node is a system folder.
-   false: Node isn't a system folder.

Data type: Boolean

</td></tr><tr id="sys_class_name-node-editor-row"><td>

sys\_class\_name

</td><td id="sys_class_name-node-editor-entry">

Table in which the node resides.Data type: String

</td></tr><tr id="sys_created_by-node-editor-row"><td>

sys\_created\_by

</td><td id="sys_created_by-node-editor-entry">

Name of the user that created the node.Data type: String

</td></tr><tr id="sys_created_on-node-editor-row"><td>

sys\_created\_on

</td><td id="sys_created_on-node-editor-entry">

Date and time when the node was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="sys_id-node-editor-row"><td>

sys\_id

</td><td id="sys_id-node-editor-entry">

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr id="sys_updated_by-node-editor-row"><td>

sys\_updated\_by

</td><td id="sys_updated_by-node-editor-entry">

Name of the user that updated the node.Data type: String

</td></tr><tr id="sys_updated_on-node-editor-row"><td>

sys\_updated\_on

</td><td id="sys_updated_on-node-editor-entry">

Date and time when the node was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="type-node-editor-row"><td>

type

</td><td id="type-node-editor-entry">

Node type.

Possible values:

-   sn\_cdm\_node\_cdi
-   sn\_cdm\_node\_collection
-   sn\_cdm\_node\_component
-   sn\_cdm\_node\_folder
-   sn\_cdm\_node\_variable

Data type: String

 Default: All

</td></tr><tr id="value-node-editor-row"><td>

value

</td><td id="value-node-editor-entry">

Node value.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to update the value of a node.

```
curl "http://instance.servicenow.com/api/sn_cdm/editor/nodes?newValue=cdcdc&fullNamePath=%2FtestApp%2Fdeployables%2FDe
velopment-1%2Fcdi45&changesetNumber=Chset-5" \
--request PUT \
--header "Accept:application/json" \
--user 'username':'password'
```

Return result:

```
{ 
  "result": { 
    "changeset_id": { 
      "value": "d403648653b70110a1d3ddeeff7b12c5", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/d403648653b70110a1d3ddeeff7b12c5" 
    }, 
    "node_path": "!$!+!,![:", 
    "description": null, 
    "sys_updated_on": "2022-06-30 08:53:13", 
    "type": "sn_cdm_node_cdi", 
    "sys_class_name": "sn_cdm_node", 
    "sys_id": "c93c7c1753981110a1d3ddeeff7b12c7", 
    "sys_updated_by": "admin", 
    "previous_version": null, 
    "sys_created_on": "2022-06-30 08:53:13", 
    "value": null, 
    "effective_from": null, 
    "linked_to": null, 
    "sys_created_by": "admin", 
    "restricted_to": null, 
    "level": "3", 
    "conflict_type": null, 
    "main_id": "2869", 
    "effective_to": null, 
    "secure_value": "﷞﷟﷒113a0c6e53001110a1d3ddeeff7b121d﷬﷔1﷬﷭bAUA1wj-fxofbSrMyF-BAg==6qiho5f_9DhnuHT2Km5SLf0Ck4XNX_w=﷮﷯", 
    "node_classifier": "/application/deployables/env:Development", 
    "main_id_encoded": "[:", 
    "name": "cdi45", 
    "position": null, 
    "reason_for_conflict": null, 
    "system_folder": false, 
    "status": "new", 
    "conflict": false 
  } 
}
```

