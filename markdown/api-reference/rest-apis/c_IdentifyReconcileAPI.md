---
title: Identification and Reconciliation API
description: The Identification and Reconciliation API provides endpoints that use the Identification and Reconciliation engine \(IRE\) to minimize creation of duplicate Configuration Items \(CIs\) and to reconcile CI attributes by only accepting information from authorized sources when updating the Configuration Management Database \(CMDB\).Inserts or updates configuration items \(CIs\) in the CMDB by applying identification and reconciliation rules to the specified payload \(request body\). Use this API instead of updating the CMDB directly.Inserts or updates configuration items \(CIs\) in the CMDB by applying identification and reconciliation rules to the specified payload \(request body\). Use this API instead of updating the CMDB directly.Determines the CMDB operation \(insert/update\) to perform with the specified payload \(request body\), without committing the operations in the database.Determines the CMDB operation \(insert/update\) to perform with the specified payload \(request body\), without committing the operations in the database.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 98
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Identification and Reconciliation API

The Identification and Reconciliation API provides endpoints that use the Identification and Reconciliation engine \(IRE\) to minimize creation of duplicate Configuration Items \(CIs\) and to reconcile CI attributes by only accepting information from authorized sources when updating the Configuration Management Database \(CMDB\).

Users must have the itil or asset role to use this API.

For more information on the IRE, see [Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Identification and Reconciliation - POST /now/identifyreconcile

Inserts or updates configuration items \(CIs\) in the CMDB by applying identification and reconciliation rules to the specified payload \(request body\). Use this API instead of updating the CMDB directly.

Use the [Identification and Reconciliation - POST /now/identifyreconcile/query](c_IdentifyReconcileAPI.md#) endpoint to simulate submission of a payload to this endpoint without committing changes to the database.

Use the [Identification and Reconciliation - POST /now/identifyreconcile/enhanced](c_IdentifyReconcileAPI.md#) endpoint instead if you need to specify Enhanced IRE options. For more on Enhanced IRE options, see [Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

### URL format

Versioned URL: `/api/now/{api_version}/identifyreconcile`

Default URL: `/api/now/identifyreconcile`

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

sysparm\_data\_source

</td><td>

Source of the CI information. This must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.Data type: String

Default: Insert the API payload into the incomplete payloads table.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

List of CIs to create or update.Data type: Array of Objects

```
"items": [
  {
    "className": "String",
    "internal_id": "String",
    "lookup": [Array],
    "related": [Array],
    "settings": {Object},
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.className

</td><td>

Required. The sys\_class\_name \(class/table name\) of the CI to create or update. This value can be any CMDB table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.Data type: String

</td></tr><tr><td>

items.internal\_id

</td><td>

Unique identifier for this item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup

</td><td>

Array of objects in which each object describes a lookup-based identification record. These records are used to identify the top-level configuration item based on a lookup table that has a reference back to the Configuration Item \[cmdb\_ci\] table.Data type: Array off Objects

```
"lookup": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.lookup.className

</td><td>

Required. The sys\_class\_name or class/table name of the CI to create or update. This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter, or a non-CMDB hierarchy class.Data type: String

</td></tr><tr><td>

items.lookup.internal\_id

</td><td>

Unique identifier for this lookup record in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.lookup.values

</td><td>

Object describing fields for this lookup item as name/value pairs, where the name is the field name.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "ip_address": "String",
  "mac_address": "String",
  "serial_number": "String",
  "serial_number_type": "String",
  "valid": "String"
}
```

</td></tr><tr><td>

items.related

</td><td>

Array of objects in which each object describes an item record to create or update, based on a related table that has a reference to the top-level CI that is being identified. Rules in the Related Entry \[cmdb\_related\_entry\] table define what type of records can be in this array.The related table may or may not extend the Configuration Item \[cmdb\_ci\] table. These records are not used to identify the configuration item.

Data type: Array of Objects

```
"related": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.related.className

</td><td>

Required. The sys\_class\_name or class/table name of the related item to create or update.Data type: String

</td></tr><tr><td>

items.related.internal\_id

</td><td>

Unique identifier for this related item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this related item. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_name

</td><td>

Data source for the related item information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the related item. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the related item was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.related.values

</td><td>

Object describing fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

items.settings

</td><td>

Object containing parameters defining the types of updates that are permitted.Data type: Object

```
"settings": {
  "skipReclassificationRestrictionRules": Boolean,
  "updateWithoutDowngrade": Boolean,
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr><td>

items.settings.skipReclassificationRestrictionRules

</td><td>

Flag that indicates whether IRE should skip running the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr><td>

items.settings.updateWithoutDowngrade

</td><td>

Flag that indicates whether update and downgrade are both permitted for this CI.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutSwitch

</td><td>

Flag that indicates whether this CI can be updated and its class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutUpgrade

</td><td>

Flag that indicates whether update and upgrade are both permitted for this CI.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.values

</td><td>

Object describing fields to create or update for this CI as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

referenceItems

</td><td>

List of reference between two items in the payload.Data type: Array of Objects

```
"referenceItems": [
  {
    "referenced": "String",
    "referencedBy": "String",
    "referenceField": "String"
  }
]
```

</td></tr><tr><td>

referenceItems.referenced

</td><td>

The **internal\_id** defined for the item being referenced by another item.Data type: String

</td></tr><tr><td>

referenceItems.referencedBy

</td><td>

The **internal\_id** defined for the item that references another item.Data type: String

</td></tr><tr><td>

referenceItems.referenceField

</td><td>

Name of the reference field in the class/table for the **referencedBy** item.Data type: String

</td></tr><tr><td>

relations

</td><td>

List of relationships between two items defined in the payload.An object in this array can use either of two formats:

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.
-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

Data type: Array of Objects

```
"relations": [
  {
    "child": Number,
    "parent": Number,
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

 ```
"relations": [
  {
    "child_id": "String",
    "parent_id": "String",
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

</td></tr><tr><td>

relations.child

</td><td>

Integer index of the CI object in the **items** array that represents the child in the relationship.Data type: Number

</td></tr><tr><td>

relations.child\_id

</td><td>

The **internal\_id** of the child item in the relationship.Data type: String

</td></tr><tr><td>

relations.parent

</td><td>

Integer index of the CI object in the **items** array that represents the parent in the relationship.Data type: Number

</td></tr><tr><td>

relations.parent\_id

</td><td>

The **internal\_id** of the parent item in the relationship.Data type: String

</td></tr><tr id="input_rel_sys_rel_source_info-row-IRE"><td>

relations.sys\_rel\_source\_info

</td><td>

Discovery source information for the relationship. For non-dependency relationships, this information is in the Relationship Sources \[sys\_rel\_source\] table. Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr id="input-relations-sys_rel_source_info-source_name-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_name

</td><td>

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr id="input-relations-sys_rel_source_info-source_feed-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_feed

</td><td>

Any string that is a sub-discovery/scan within the discovery source. Default: ‘UNKNOWN’ is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr><td>

relations.type

</td><td>

Type of relationship existing between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr></tbody>
</table>### Headers

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of results produced by the query.Data type: Array

```
"result": [
  "additionalCommittedItems": [Array],
  "additionalCommittedRelations": [Array],
  "items": [Array],
  "relations": [Array]
]
```

</td></tr><tr><td>

result.additionalCommittedItems

</td><td>

List of CIs not included in the request body **items** array to insert or update.Data type: Array of Objects

```
"additionalCommittedItems": [
  {
    "className": "String",
    "errorCount": Number,
    "identificationAttempts": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloads": [Array],
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.className

</td><td>

The sys\_class\_name of this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errorCount

</td><td>

Number of errors encountered while processing this additional CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedItems.errors

</td><td>

List of errors encountered while processing this additional CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.errors.error

</td><td>

Type of error encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errors.message

</td><td>

Error message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts

</td><td>

List of attempts made to identify this additional CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attemptResult

</td><td>

Outcome of this additional CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attributes

</td><td>

Array of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.identifierName

</td><td>

Identifier rule used for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this additional CI.Notable values:

-   Unknown: Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this additional CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedItems.mergedPayloads

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.operation

</td><td>

Operation performed for this additional CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The additional CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the additional CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.sysId

</td><td>

Sys\_id found for this additional CI through identification.Notable values: Unknown - Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings

</td><td>

List of warnings encountered while processing this additional CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.warnings.error

</td><td>

Type of warning encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings.message

</td><td>

Warning message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations

</td><td>

List of dependent relationship CIs not included in the request body **relations** list to insert or update.Data type: Array of Objects

```
"additionalCommittedRelations": [
  {
    "className": "String",
    "operation": "String",
    "markers": [Array],
    "inputIndices": [Array],
    "mergedPayloadIds": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.className

</td><td>

The sys\_class\_name of this additional dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errorCount

</td><td>

Number of errors encountered while processing this additional dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedRelations.errors

</td><td>

List of errors encountered while processing this additional dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.errors.error

</td><td>

Type of error encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errors.message

</td><td>

Error message encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.inputIndices

</td><td>

List of index values for dependent relationship CI objects in the request body **relations** array that correspond to this additional dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedRelations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.operation

</td><td>

Operation performed for this additional dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI is inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and is inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and is inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation is performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table is updated.

Data type: String

</td></tr><tr><td>

result.items

</td><td>

List of CIs included in the request body **items** array.Data type: Array of Objects

```
"items": [
  {
    "additionalRelatedItems": [Array],
    "className": "String",
    "duplicateLookupIndices": {Object},
    "errorCount": Number,
    "errors": [Array],
    "identificationAttempts": [Array],
    "identifierEntrySysId": "String",
    "info": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "relatedItems": [Array],
    "relatedSysIds": [Array],
    "sysId": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems

</td><td>

List of related CIs \(table lookup CI\) from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.Data type: Array of Objects

```
"additionalRelatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.additionalRelatedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this related item.Data type: Array

```
"inputIndices": [
    Number
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.additionalRelatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this related item.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.sysId

</td><td>

Sys\_id of this related CI.Data type: String

</td></tr><tr><td>

result.items.className

</td><td>

Sys\_class\_name of this CI.Data type: String

</td></tr><tr><td>

result.items.duplicateLookupIndices

</td><td>

Object containing arrays of index values for **items.lookup** array elements that reference the same related CI.The array name indicates the first element from the request body **items.lookup** array that references a given related CI. Its values are the set of additional elements from the same array that reference the same related CI.

Data type: Object

This example shows a case where the second element in the **items.lookup** array references the same related CI as a later element from that array:

```
"duplicateLookupIndices": [
  "2": [Array]
]
```

</td></tr><tr><td>

result.items.errorCount

</td><td>

Number of errors encountered while processing this CI.Data type: Number

</td></tr><tr><td>

result.items.errors

</td><td>

List of errors encountered while processing this CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.errors.error

</td><td>

Type of error encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.errors.message

</td><td>

Error message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts

</td><td>

List of attempts made to identify this CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.items.identificationAttempts.attemptResult

</td><td>

Outcome of this CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.attributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

result.items.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.items.identificationAttempts.identifierName

</td><td>

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this CI.Notable values:

-   Unknown: Identification of this CI failed. For details, see **errors**.

Data type: String

</td></tr><tr><td>

result.items.info

</td><td id="items_info-entry-IRE">

List of additional information about the processing of the item.Data type: Array of Objects

```
"info": [
  {
    "code": "String",
    "message": "String",
    "ruleSysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.info.code

</td><td id="items_info_code-entry-IRE">

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_UPGRADE

</td></tr><tr><td>

result.items.info.message

</td><td id="items_info_message-entry-IRE">

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

result.items.info.ruleSysId

</td><td id="items_info_ruleSysId-entry-IRE">

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr><td>

result.items.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.items.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.operation

</td><td>

Operation performed for this CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.items.relatedItems

</td><td>

List of related CIs \(table lookup CI\) from the request body **items.lookup** array.Data type: Array of Objects

```
"relatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.relatedItems.inputIndices

</td><td>

List of index values for CIs and lookup items from the request body **items** and **items.lookup** arrays that correspond to this related item.Data type: Array of Objects

```
"inputIndices": [
  {
    "mainIndex": Number,
    "subIndex": Number
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.inputIndices.mainIndex

</td><td>

Index value from the request body **items** array that corresponds to the CI parent of the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.inputIndices.subIndex

</td><td>

Index value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.relatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for entries in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged into this CI during processing.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.relatedSysIds

</td><td>

List of sys\_id values for related items \(table lookup items\) from the request body **items.lookup** array.Data type: Array

Notable values:

-   null: No sys\_id was identified for this related item.

```
"relatedSysIds": [
    Number,
    Number
]
```

</td></tr><tr><td>

result.items.sysId

</td><td>

Sys\_id found for this CI through identification.Notable values:

-   Unknown: Identification of this CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.items.warnings

</td><td>

List of warnings encountered while processing this CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.warnings.error

</td><td>

Type of warning encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.warnings.message

</td><td>

Warning message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.logContextId

</td><td>

Context ID reported for this payload.Data type: String

</td></tr><tr><td>

result.relations

</td><td>

List of dependent relationship CIs from the request body **relations** array.Data type: Array of Objects

```
"relations": [
  {
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.relations.className

</td><td>

The sys\_class\_name of this dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.relations.errorCount

</td><td>

Number of errors encountered while processing this dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.relations.errors

</td><td>

List of errors encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.errors.error

</td><td>

Type of error encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.errors.message

</td><td>

Error message encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.inputIndices

</td><td>

List of index values for the dependent relationship CI objects in the request body **relations** array that correspond to this dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.relations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.relations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.relations.operation

</td><td>

Operation performed for this dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI was inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and was inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and was inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation was performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table was updated.

 Data type: String

</td></tr><tr><td>

result.relations.warnings

</td><td>

List of warnings encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.warnings.error

</td><td>

Type of warning encountered while processing this dependent relationship CI.Data type: String

</td></tr><tr><td>

result.relations.warnings.message

</td><td>

Warning message encountered while processing this dependent relationship CI.Data type: String

</td></tr></tbody>
</table>### cURL request

Submit a payload containing a Linux server \(with serial number and network adapter related-item lookups\) and an IP switch, with an IP Connection dependent relationship between them.

```
curl "https://instance.servicenow.com/api/now/identifyreconcile" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{ \
  "items": [{ \
    "className": "cmdb_ci_linux_server", \
    "values": { \
      "sys_class_name": "cmdb_ci_linux_server", \
      "name": "lnux101", \
      "host_name": "lnux101.servicenow.com", \
      "ip_address": "10.11.12.173", \
      "os_name": "Linux Red Hat" \
    }, \
    "lookup": [{ \
      "className": "cmdb_serial_number", \
      "values": { \
        "serial_number": "lnux101", \
        "serial_number_type": "uuid", \
        "valid": "true" \
      } \
    }, { \
      "className": "cmdb_ci_network_adapter", \
      "values": { \
        "name": "eth0", \
        "ip_address": "10.11.12.173", \
        "mac_address": "00:55:51:21:26:2f" \
      } \
    }] \
  }, { \
    "className": "cmdb_ci_ip_switch", \
    "values": { \
      "name": "IP-Switch-1", \
      "serial_number": "Switch23587", \
      "serial_number_type": "uuid" \
    } \
  }], \
  "relations": [{ \
    "parent": 0, \
    "child": 1, \
    "type": "IP Connection::IP Connection" \
  }]
}'
```

The Linux server CI is identified via a Hardware Rule search for its name on the Hardware \[cmdb\_ci\_hardware\] table and is processed as an update to an existing CI in the Linux Server \[cmdb\_ci\_linux\_server\] table. The IP switch is similarly identified via a Hardware Rule search for its name on the Hardware table and updates an existing CI in the IP Switch \[cmdb\_ci\_ip\_switch\] table. Finally, the IP Connection dependent relationship between the server and the switch is inserted as a new record in the CI Relationship \[cmdb\_rel\_ci\] table.

```
{
  "result": {
    "items": [{
      "className": "cmdb_ci_linux_server",
      "operation": "UPDATE",
      "sysId": "539747cac0a801640163e60735fbbf6e",
      "relatedSysIds": [null, null],
      "relatedItems": [{
        "markers": [],
        "inputIndices": [{
          "mainIndex": 0,
          "subIndex": 0
        }],
        "mergedPayloadIds": [],
        "className": "cmdb_serial_number"
      }, {
        "markers": [],
        "inputIndices": [{
          "mainIndex": 0,
          "subIndex": 1
        }],
        "mergedPayloadIds": [],
        "className": "cmdb_ci_network_adapter"
      }],
      "additionalRelatedItems": [],
      "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
      "identificationAttempts": [{
        "identifierName": "Hardware Rule",
        "attemptResult": "NO_MATCH",
        "attributes": ["serial_number", "serial_number_type"],
        "searchOnTable": "cmdb_serial_number",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "SKIPPED",
        "attributes": ["serial_number"],
        "searchOnTable": "cmdb_ci_hardware",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "MATCHED",
        "attributes": ["name"],
        "searchOnTable": "cmdb_ci_hardware",
        "hybridEntryCiAttributes": []
      }],
      "markers": [],
      "inputIndices": [0],
      "mergedPayloadIds": [],
      "errorCount": 0
    }, {
      "className": "cmdb_ci_ip_switch",
      "operation": "UPDATE",
      "sysId": "304481257f701200bee45f19befa915b",
      "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
      "identificationAttempts": [{
        "identifierName": "Hardware Rule",
        "attemptResult": "SKIPPED",
        "attributes": ["serial_number", "serial_number_type"],
        "searchOnTable": "cmdb_serial_number",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "NO_MATCH",
        "attributes": ["serial_number"],
        "searchOnTable": "cmdb_ci_hardware",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "MATCHED",
        "attributes": ["name"],
        "searchOnTable": "cmdb_ci_hardware",
        "hybridEntryCiAttributes": []
      }],
      "markers": [],
      "inputIndices": [1],
      "mergedPayloadIds": [],
      "errorCount": 0
    }],
    "additionalCommittedItems": [],
    "relations": [{
      "className": "cmdb_rel_ci",
      "operation": "INSERT",
      "markers": [],
      "inputIndices": [0],
      "mergedPayloadIds": [],
      "errorCount": 0
    }],
    "additionalCommittedRelations": []
  }
}
```

## Identification and Reconciliation - POST /now/identifyreconcile/enhanced

Inserts or updates configuration items \(CIs\) in the CMDB by applying identification and reconciliation rules to the specified payload \(request body\). Use this API instead of updating the CMDB directly.

Use the [Identification and Reconciliation - POST /now/identifyreconcile/queryEnhanced](c_IdentifyReconcileAPI.md#) endpoint to simulate submission of a payload to this endpoint without committing changes to the database.

This method is similar to the [Identification and Reconciliation - POST /now/identifyreconcile](c_IdentifyReconcileAPI.md#) method, but adds the following functionality:

-   Partial payloads
    -   In case of an item having a warning or error, indicates if an item operation is INSERT\_AS\_PARTIAL or INSERT\_INCOMPLETE.
    -   Returns the sys\_ids of partial payloads that were merged with existing partial payloads.
-   Supports payload deduplicate feature.
-   Generates a summary.

### URL format

Versioned URL: `/api/now/{api_version}/identifyreconcile/enhanced`

Default URL: `/api/now/identifyreconcile/enhanced`

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

options

</td><td>

Comma-separated list of name-value pairs representing Enhanced IRE options applied for the request.As an example, to override the default values for the partial payloads, partial commits, deduplicate payloads, and generate summary Enhanced IRE options:

`partial_payloads:false,partial_commits:false,deduplicate_payloads:false,generate_summary:true`

**Note:** By default or if **partial\_payloads** is set to true, both **partial\_commits** and **deduplicate\_payloads** are enabled, even if they are set to false, as those features are essential for partial payloads functionality.

For more on Enhanced IRE options, see [Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Valid values for each name-value pair:

-   true: Enable this Enhanced IRE option.
-   false: Disable this Enhanced IRE option.

Data type: String

</td></tr><tr><td>

sysparm\_data\_source

</td><td>

Source of the CI information. This must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.Data type: String

Default: Insert the API payload into the incomplete payloads table.

</td></tr></tbody>
</table><table id="table_idz_wyn_rlb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

List of CIs to create or update.Data type: Array of Objects

```
"items": [
  {
    "className": "String",
    "internal_id": "String",
    "lookup": [Array],
    "related": [Array],
    "settings": {Object},
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.className

</td><td>

Required. The sys\_class\_name \(class/table name\) of the CI to create or update. This value can be any CMDB table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.Data type: String

</td></tr><tr><td>

items.internal\_id

</td><td>

Unique identifier for this item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup

</td><td>

Array of objects in which each object describes a lookup-based identification record. These records are used to identify the top-level configuration item based on a lookup table that has a reference back to the Configuration Item \[cmdb\_ci\] table.Data type: Array off Objects

```
"lookup": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.lookup.className

</td><td>

Required. The sys\_class\_name or class/table name of the CI to create or update. This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter, or a non-CMDB hierarchy class.Data type: String

</td></tr><tr><td>

items.lookup.internal\_id

</td><td>

Unique identifier for this lookup record in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.lookup.values

</td><td>

Object describing fields for this lookup item as name/value pairs, where the name is the field name.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "ip_address": "String",
  "mac_address": "String",
  "serial_number": "String",
  "serial_number_type": "String",
  "valid": "String"
}
```

</td></tr><tr><td>

items.related

</td><td>

Array of objects in which each object describes an item record to create or update, based on a related table that has a reference to the top-level CI that is being identified. Rules in the Related Entry \[cmdb\_related\_entry\] table define what type of records can be in this array.The related table may or may not extend the Configuration Item \[cmdb\_ci\] table. These records are not used to identify the configuration item.

Data type: Array of Objects

```
"related": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.related.className

</td><td>

Required. The sys\_class\_name or class/table name of the related item to create or update.Data type: String

</td></tr><tr><td>

items.related.internal\_id

</td><td>

Unique identifier for this related item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this related item. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_name

</td><td>

Data source for the related item information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the related item. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the related item was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.related.values

</td><td>

Object describing fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

items.settings

</td><td>

Object containing parameters defining the types of updates that are permitted.Data type: Object

```
"settings": {
  "skipReclassificationRestrictionRules": Boolean,
  "updateWithoutDowngrade": Boolean,
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr><td>

items.settings.skipReclassificationRestrictionRules

</td><td>

Flag that indicates whether IRE should skip running the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr><td>

items.settings.updateWithoutDowngrade

</td><td>

Flag that indicates whether update and downgrade are both permitted for this CI.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutSwitch

</td><td>

Flag that indicates whether this CI can be updated and its class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutUpgrade

</td><td>

Flag that indicates whether update and upgrade are both permitted for this CI.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.values

</td><td>

Object describing fields to create or update for this CI as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

referenceItems

</td><td>

List of reference between two items in the payload.Data type: Array of Objects

```
"referenceItems": [
  {
    "referenced": "String",
    "referencedBy": "String",
    "referenceField": "String"
  }
]
```

</td></tr><tr><td>

referenceItems.referenced

</td><td>

The **internal\_id** defined for the item being referenced by another item.Data type: String

</td></tr><tr><td>

referenceItems.referencedBy

</td><td>

The **internal\_id** defined for the item that references another item.Data type: String

</td></tr><tr><td>

referenceItems.referenceField

</td><td>

Name of the reference field in the class/table for the **referencedBy** item.Data type: String

</td></tr><tr><td>

relations

</td><td>

List of relationships between two items defined in the payload.An object in this array can use either of two formats:

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.
-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

Data type: Array of Objects

```
"relations": [
  {
    "child": Number,
    "parent": Number,
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

 ```
"relations": [
  {
    "child_id": "String",
    "parent_id": "String",
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

</td></tr><tr><td>

relations.child

</td><td>

Integer index of the CI object in the **items** array that represents the child in the relationship.Data type: Number

</td></tr><tr><td>

relations.child\_id

</td><td>

The **internal\_id** of the child item in the relationship.Data type: String

</td></tr><tr><td>

relations.parent

</td><td>

Integer index of the CI object in the **items** array that represents the parent in the relationship.Data type: Number

</td></tr><tr><td>

relations.parent\_id

</td><td>

The **internal\_id** of the parent item in the relationship.Data type: String

</td></tr><tr id="input_rel_sys_rel_source_info-row-IRE"><td>

relations.sys\_rel\_source\_info

</td><td>

Discovery source information for the relationship. For non-dependency relationships, this information is in the Relationship Sources \[sys\_rel\_source\] table. Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr id="input-relations-sys_rel_source_info-source_name-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_name

</td><td>

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr id="input-relations-sys_rel_source_info-source_feed-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_feed

</td><td>

Any string that is a sub-discovery/scan within the discovery source. Default: ‘UNKNOWN’ is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr><td>

relations.type

</td><td>

Type of relationship existing between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr></tbody>
</table>### Headers

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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td>

Internal server error. An unexpected error occurred while processing the request.Error message detail "Chunk \[…\] is not a valid entry" indicates that the **options** query parameter is not in the correct name-value pair format.

For example, specifying an **options** parameter of `partial` produces a 500 status code with "Chunk \[partial\] is not a valid entry" in the message detail.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_mr2_yyn_rlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of results produced by the query.Data type: Array

```
"result": [
  "additionalCommittedItems": [Array],
  "additionalCommittedRelations": [Array],
  "items": [Array],
  "relations": [Array]
]
```

</td></tr><tr><td>

result.additionalCommittedItems

</td><td>

List of CIs not included in the request body **items** array to insert or update.Data type: Array of Objects

```
"additionalCommittedItems": [
  {
    "className": "String",
    "errorCount": Number,
    "identificationAttempts": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloads": [Array],
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.className

</td><td>

The sys\_class\_name of this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errorCount

</td><td>

Number of errors encountered while processing this additional CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedItems.errors

</td><td>

List of errors encountered while processing this additional CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.errors.error

</td><td>

Type of error encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errors.message

</td><td>

Error message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts

</td><td>

List of attempts made to identify this additional CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attemptResult

</td><td>

Outcome of this additional CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attributes

</td><td>

Array of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.identifierName

</td><td>

Identifier rule used for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this additional CI.Notable values:

-   Unknown: Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this additional CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedItems.mergedPayloads

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.operation

</td><td>

Operation performed for this additional CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The additional CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the additional CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.sysId

</td><td>

Sys\_id found for this additional CI through identification.Notable values: Unknown - Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings

</td><td>

List of warnings encountered while processing this additional CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.warnings.error

</td><td>

Type of warning encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings.message

</td><td>

Warning message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations

</td><td>

List of dependent relationship CIs not included in the request body **relations** list to insert or update.Data type: Array of Objects

```
"additionalCommittedRelations": [
  {
    "className": "String",
    "operation": "String",
    "markers": [Array],
    "inputIndices": [Array],
    "mergedPayloadIds": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.className

</td><td>

The sys\_class\_name of this additional dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errorCount

</td><td>

Number of errors encountered while processing this additional dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedRelations.errors

</td><td>

List of errors encountered while processing this additional dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.errors.error

</td><td>

Type of error encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errors.message

</td><td>

Error message encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.inputIndices

</td><td>

List of index values for dependent relationship CI objects in the request body **relations** array that correspond to this additional dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedRelations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.operation

</td><td>

Operation performed for this additional dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI is inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and is inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and is inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation is performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table is updated.

Data type: String

</td></tr><tr><td>

result.items

</td><td>

List of CIs included in the request body **items** array.Data type: Array of Objects

```
"items": [
  {
    "additionalRelatedItems": [Array],
    "className": "String",
    "duplicateLookupIndices": {Object},
    "errorCount": Number,
    "errors": [Array],
    "identificationAttempts": [Array],
    "identifierEntrySysId": "String",
    "info": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "relatedItems": [Array],
    "relatedSysIds": [Array],
    "sysId": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems

</td><td>

List of related CIs \(table lookup CI\) from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.Data type: Array of Objects

```
"additionalRelatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.additionalRelatedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this related item.Data type: Array

```
"inputIndices": [
    Number
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.additionalRelatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this related item.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.sysId

</td><td>

Sys\_id of this related CI.Data type: String

</td></tr><tr><td>

result.items.className

</td><td>

Sys\_class\_name of this CI.Data type: String

</td></tr><tr><td>

result.items.duplicateLookupIndices

</td><td>

Object containing arrays of index values for **items.lookup** array elements that reference the same related CI.The array name indicates the first element from the request body **items.lookup** array that references a given related CI. Its values are the set of additional elements from the same array that reference the same related CI.

Data type: Object

This example shows a case where the second element in the **items.lookup** array references the same related CI as a later element from that array:

```
"duplicateLookupIndices": [
  "2": [Array]
]
```

</td></tr><tr><td>

result.items.errorCount

</td><td>

Number of errors encountered while processing this CI.Data type: Number

</td></tr><tr><td>

result.items.errors

</td><td>

List of errors encountered while processing this CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.errors.error

</td><td>

Type of error encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.errors.message

</td><td>

Error message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts

</td><td>

List of attempts made to identify this CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.items.identificationAttempts.attemptResult

</td><td>

Outcome of this CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.attributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

result.items.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.items.identificationAttempts.identifierName

</td><td>

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this CI.Notable values:

-   Unknown: Identification of this CI failed. For details, see **errors**.

Data type: String

</td></tr><tr><td>

result.items.info

</td><td id="items_info-entry-IRE">

List of additional information about the processing of the item.Data type: Array of Objects

```
"info": [
  {
    "code": "String",
    "message": "String",
    "ruleSysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.info.code

</td><td id="items_info_code-entry-IRE">

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_UPGRADE

</td></tr><tr><td>

result.items.info.message

</td><td id="items_info_message-entry-IRE">

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

result.items.info.ruleSysId

</td><td id="items_info_ruleSysId-entry-IRE">

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr><td>

result.items.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.items.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.operation

</td><td>

Operation performed for this CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.items.relatedItems

</td><td>

List of related CIs \(table lookup CI\) from the request body **items.lookup** array.Data type: Array of Objects

```
"relatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.relatedItems.inputIndices

</td><td>

List of index values for CIs and lookup items from the request body **items** and **items.lookup** arrays that correspond to this related item.Data type: Array of Objects

```
"inputIndices": [
  {
    "mainIndex": Number,
    "subIndex": Number
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.inputIndices.mainIndex

</td><td>

Index value from the request body **items** array that corresponds to the CI parent of the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.inputIndices.subIndex

</td><td>

Index value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.relatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for entries in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged into this CI during processing.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.relatedSysIds

</td><td>

List of sys\_id values for related items \(table lookup items\) from the request body **items.lookup** array.Data type: Array

Notable values:

-   null: No sys\_id was identified for this related item.

```
"relatedSysIds": [
    Number,
    Number
]
```

</td></tr><tr><td>

result.items.sysId

</td><td>

Sys\_id found for this CI through identification.Notable values:

-   Unknown: Identification of this CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.items.warnings

</td><td>

List of warnings encountered while processing this CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.warnings.error

</td><td>

Type of warning encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.warnings.message

</td><td>

Warning message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.logContextId

</td><td>

Context ID reported for this payload.Data type: String

</td></tr><tr><td>

result.relations

</td><td>

List of dependent relationship CIs from the request body **relations** array.Data type: Array of Objects

```
"relations": [
  {
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.relations.className

</td><td>

The sys\_class\_name of this dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.relations.errorCount

</td><td>

Number of errors encountered while processing this dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.relations.errors

</td><td>

List of errors encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.errors.error

</td><td>

Type of error encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.errors.message

</td><td>

Error message encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.inputIndices

</td><td>

List of index values for the dependent relationship CI objects in the request body **relations** array that correspond to this dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.relations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.relations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.relations.operation

</td><td>

Operation performed for this dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI was inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and was inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and was inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation was performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table was updated.

 Data type: String

</td></tr><tr><td>

result.relations.warnings

</td><td>

List of warnings encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.warnings.error

</td><td>

Type of warning encountered while processing this dependent relationship CI.Data type: String

</td></tr><tr><td>

result.relations.warnings.message

</td><td>

Warning message encountered while processing this dependent relationship CI.Data type: String

</td></tr></tbody>
</table>### cURL request

Submit a partial payload for a computer CI.

```
curl "https://instance.servicenow.com/api/now/identifyreconcile/enhanced" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password" \
--data '{ \
  "items" : [ \
    { \
      "className" : "cmdb_ci_computer", \
      "sys_object_source_info" : { \
        "source_name" : "ServiceNow", \
        "source_native_key" : "ncomputer3367" \
      }, \
      "values" : { \
        "cpu_core_count" : "6", \
        "ram" : "8192", \
        "manufacturer" : "DELL", \
        "company" : "My Company" \
      } \
    } \
  ] \
}'
```

The response shows that the payload has been inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.

```
{
  "result": {
    "items": [{
      "className": "cmdb_ci_computer",
      "operation": "INSERT_AS_PARTIAL",
      "sysId": "Unknown",
      "partialSysIds": ["1aec79151bb45010593876a61a4bcb28"],
      "identifierEntrySysId": "Unknown",
      "errors": [],
      "warnings": [{
        "error": "MISSING_MATCHING_ATTRIBUTES",
        "message": "In payload missing minimum set of input values for criterion (matching) attributes from identify rule for table [cmdb_ci_hardware]. Add these input values in payload item '{\"className\":\"cmdb_ci_computer\",\"values\":{\"discovery_source\":\"ServiceNow\",\"company\":\"My Company\",\"cpu_core_count\":\"6\",\"ram\":\"8192\",\"manufacturer\":\"DELL\"},\"sys_object_source_info\":{\"source_name\":\"ServiceNow\",\"source_native_key\":\"ncomputer3367\"},\"settings\":{},\"sys_ire_info\":{\"ire_received_time\":\"2020-05-14 20:14:51\"}}'"
      }],
      "identificationAttempts": [{
        "info": "sys_object_source NO_MATCH",
        "identifierName": "",
        "attemptResult": "NO_MATCH",
        "attributes": [],
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "SKIPPED",
        "attributes": ["serial_number", "serial_number_type"],
        "searchOnTable": "cmdb_serial_number",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "SKIPPED",
        "attributes": ["serial_number"],
        "searchOnTable": "cmdb_ci_hardware",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "SKIPPED",
        "attributes": ["name"],
        "searchOnTable": "cmdb_ci_hardware",
        "hybridEntryCiAttributes": []
      }, {
        "identifierName": "Hardware Rule",
        "attemptResult": "SKIPPED",
        "attributes": ["mac_address", "name"],
        "searchOnTable": "cmdb_ci_network_adapter",
        "hybridEntryCiAttributes": []
      }],
      "errorCount": 0,
      "markers": [],
      "warningCount": 1,
      "mergedPayloadIds": ["7ddcb9551bb45010593876a61a4bcb08"],
      "inputIndices": [0]
    }],
    "additionalCommittedItems": [],
    "relations": [],
    "additionalCommittedRelations": []
  }
}
```

Submit a second partial payload that completes the description of the computer CI, with the summary generation Enhanced IRE option enabled.

```
curl "https://instance.servicenow.com/api/now/identifyreconcile/enhanced?options=generate_summary:true" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password" \
--data '{ \
}'
```

The response shows that the computer CI is inserted, and displays a summary of operations performed.

```
{
  "result": {
    "relations": [],
    "hasError": false,
    "additionalCommittedItems": [],
    "hasWarning": false,
    "items": [
      {
        "relatedSysIds": [
          "735c79151bb45010593876a61a4bcb67"
        ],
        "identifierEntrySysId": "Unknown",
        "sysId": "ff5c79151bb45010593876a61a4bcb64",
        "errorCount": 0,
        "markers": [],
        "className": "cmdb_ci_computer",
        "inputIndices": [
          0
        ],
        "operation": "INSERT",
        "relatedItems": [
          {
            "operation": "INSERT",
            "warningCount": 0,
            "errors": [],
            "sysId": "735c79151bb45010593876a61a4bcb67",
            "className": "cmdb_ci_network_adapter",
            "errorCount": 0,
            "markers": [],
            "inputIndices": [
              {
                "subIndex": 0,
                "mainIndex": 0
              }
            ],
            "mergedPayloadIds": []
          }
        ],
        "mergedPayloadIds": [
          "fe4c39151bb45010593876a61a4bcbd3"
        ],
        "identificationAttempts": [
          {
            "info": "sys_object_source NO_MATCH",
            "attemptResult": "NO_MATCH",
            "identifierName": "",
            "attributes": [],
            "hybridEntryCiAttributes": []
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_serial_number"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "NO_MATCH",
            "identifierName": "Hardware Rule",
            "attributes": [
              "mac_address",
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_network_adapter"
          }
        ],
        "warningCount": 0
      }
    ],
    "additionalCommittedRelations": [],
    "summary": {
      "cmdb_ci_network_adapter": {
        "mergedPartialPayloads": 0,
        "inserted": 1,
        "partial": 0,
        "warnings": 0,
        "incomplete": 0,
        "additionalInserted": 0,
        "unchanged": 0,
        "skipped": 0,
        "updated": 0,
        "errors": 0
      },
      "cmdb_ci_computer": {
        "mergedPartialPayloads": 1,
        "inserted": 1,
        "partial": 0,
        "warnings": 0,
        "incomplete": 0,
        "additionalInserted": 0,
        "unchanged": 0,
        "skipped": 0,
        "updated": 0,
        "errors": 0
      }
    }
  }
}
```

## Identification and Reconciliation - POST /now/identifyreconcile/query

Determines the CMDB operation \(insert/update\) to perform with the specified payload \(request body\), without committing the operations in the database.

Use this endpoint to simulate submission of a payload \(request body\) to the [Identification and Reconciliation - POST /now/identifyreconcile](c_IdentifyReconcileAPI.md#) endpoint.

Use the [Identification and Reconciliation - POST /now/identifyreconcile/enhanced](c_IdentifyReconcileAPI.md#) endpoint instead if you need to specify Enhanced IRE options. For more on Enhanced IRE options, see [Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

### URL format

Versioned URL: `/api/now/{api_version}/identifyreconcile/query`

Default URL: `/api/now/identifyreconcile/query`

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

sysparm\_data\_source

</td><td>

Source of the CI information. This must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.Data type: String

Default: Insert the API payload into the incomplete payloads table.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

List of CIs to create or update.Data type: Array of Objects

```
"items": [
  {
    "className": "String",
    "internal_id": "String",
    "lookup": [Array],
    "related": [Array],
    "settings": {Object},
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.className

</td><td>

Required. The sys\_class\_name \(class/table name\) of the CI to create or update. This value can be any CMDB table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.Data type: String

</td></tr><tr><td>

items.internal\_id

</td><td>

Unique identifier for this item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup

</td><td>

Array of objects in which each object describes a lookup-based identification record. These records are used to identify the top-level configuration item based on a lookup table that has a reference back to the Configuration Item \[cmdb\_ci\] table.Data type: Array off Objects

```
"lookup": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.lookup.className

</td><td>

Required. The sys\_class\_name or class/table name of the CI to create or update. This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter, or a non-CMDB hierarchy class.Data type: String

</td></tr><tr><td>

items.lookup.internal\_id

</td><td>

Unique identifier for this lookup record in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.lookup.values

</td><td>

Object describing fields for this lookup item as name/value pairs, where the name is the field name.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "ip_address": "String",
  "mac_address": "String",
  "serial_number": "String",
  "serial_number_type": "String",
  "valid": "String"
}
```

</td></tr><tr><td>

items.related

</td><td>

Array of objects in which each object describes an item record to create or update, based on a related table that has a reference to the top-level CI that is being identified. Rules in the Related Entry \[cmdb\_related\_entry\] table define what type of records can be in this array.The related table may or may not extend the Configuration Item \[cmdb\_ci\] table. These records are not used to identify the configuration item.

Data type: Array of Objects

```
"related": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.related.className

</td><td>

Required. The sys\_class\_name or class/table name of the related item to create or update.Data type: String

</td></tr><tr><td>

items.related.internal\_id

</td><td>

Unique identifier for this related item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this related item. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_name

</td><td>

Data source for the related item information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the related item. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the related item was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.related.values

</td><td>

Object describing fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

items.settings

</td><td>

Object containing parameters defining the types of updates that are permitted.Data type: Object

```
"settings": {
  "skipReclassificationRestrictionRules": Boolean,
  "updateWithoutDowngrade": Boolean,
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr><td>

items.settings.skipReclassificationRestrictionRules

</td><td>

Flag that indicates whether IRE should skip running the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr><td>

items.settings.updateWithoutDowngrade

</td><td>

Flag that indicates whether update and downgrade are both permitted for this CI.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutSwitch

</td><td>

Flag that indicates whether this CI can be updated and its class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutUpgrade

</td><td>

Flag that indicates whether update and upgrade are both permitted for this CI.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.values

</td><td>

Object describing fields to create or update for this CI as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

referenceItems

</td><td>

List of reference between two items in the payload.Data type: Array of Objects

```
"referenceItems": [
  {
    "referenced": "String",
    "referencedBy": "String",
    "referenceField": "String"
  }
]
```

</td></tr><tr><td>

referenceItems.referenced

</td><td>

The **internal\_id** defined for the item being referenced by another item.Data type: String

</td></tr><tr><td>

referenceItems.referencedBy

</td><td>

The **internal\_id** defined for the item that references another item.Data type: String

</td></tr><tr><td>

referenceItems.referenceField

</td><td>

Name of the reference field in the class/table for the **referencedBy** item.Data type: String

</td></tr><tr><td>

relations

</td><td>

List of relationships between two items defined in the payload.An object in this array can use either of two formats:

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.
-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

Data type: Array of Objects

```
"relations": [
  {
    "child": Number,
    "parent": Number,
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

 ```
"relations": [
  {
    "child_id": "String",
    "parent_id": "String",
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

</td></tr><tr><td>

relations.child

</td><td>

Integer index of the CI object in the **items** array that represents the child in the relationship.Data type: Number

</td></tr><tr><td>

relations.child\_id

</td><td>

The **internal\_id** of the child item in the relationship.Data type: String

</td></tr><tr><td>

relations.parent

</td><td>

Integer index of the CI object in the **items** array that represents the parent in the relationship.Data type: Number

</td></tr><tr><td>

relations.parent\_id

</td><td>

The **internal\_id** of the parent item in the relationship.Data type: String

</td></tr><tr id="input_rel_sys_rel_source_info-row-IRE"><td>

relations.sys\_rel\_source\_info

</td><td>

Discovery source information for the relationship. For non-dependency relationships, this information is in the Relationship Sources \[sys\_rel\_source\] table. Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr id="input-relations-sys_rel_source_info-source_name-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_name

</td><td>

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr id="input-relations-sys_rel_source_info-source_feed-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_feed

</td><td>

Any string that is a sub-discovery/scan within the discovery source. Default: ‘UNKNOWN’ is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr><td>

relations.type

</td><td>

Type of relationship existing between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr></tbody>
</table>### Headers

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of results produced by the query.Data type: Array

```
"result": [
  "additionalCommittedItems": [Array],
  "additionalCommittedRelations": [Array],
  "items": [Array],
  "relations": [Array]
]
```

</td></tr><tr><td>

result.additionalCommittedItems

</td><td>

List of CIs not included in the request body **items** array to insert or update.Data type: Array of Objects

```
"additionalCommittedItems": [
  {
    "className": "String",
    "errorCount": Number,
    "identificationAttempts": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloads": [Array],
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.className

</td><td>

The sys\_class\_name of this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errorCount

</td><td>

Number of errors encountered while processing this additional CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedItems.errors

</td><td>

List of errors encountered while processing this additional CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.errors.error

</td><td>

Type of error encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errors.message

</td><td>

Error message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts

</td><td>

List of attempts made to identify this additional CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attemptResult

</td><td>

Outcome of this additional CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attributes

</td><td>

Array of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.identifierName

</td><td>

Identifier rule used for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this additional CI.Notable values:

-   Unknown: Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this additional CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedItems.mergedPayloads

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.operation

</td><td>

Operation performed for this additional CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The additional CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the additional CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.sysId

</td><td>

Sys\_id found for this additional CI through identification.Notable values: Unknown - Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings

</td><td>

List of warnings encountered while processing this additional CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.warnings.error

</td><td>

Type of warning encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings.message

</td><td>

Warning message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations

</td><td>

List of dependent relationship CIs not included in the request body **relations** list to insert or update.Data type: Array of Objects

```
"additionalCommittedRelations": [
  {
    "className": "String",
    "operation": "String",
    "markers": [Array],
    "inputIndices": [Array],
    "mergedPayloadIds": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.className

</td><td>

The sys\_class\_name of this additional dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errorCount

</td><td>

Number of errors encountered while processing this additional dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedRelations.errors

</td><td>

List of errors encountered while processing this additional dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.errors.error

</td><td>

Type of error encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errors.message

</td><td>

Error message encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.inputIndices

</td><td>

List of index values for dependent relationship CI objects in the request body **relations** array that correspond to this additional dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedRelations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.operation

</td><td>

Operation performed for this additional dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI is inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and is inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and is inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation is performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table is updated.

Data type: String

</td></tr><tr><td>

result.items

</td><td>

List of CIs included in the request body **items** array.Data type: Array of Objects

```
"items": [
  {
    "additionalRelatedItems": [Array],
    "className": "String",
    "duplicateLookupIndices": {Object},
    "errorCount": Number,
    "errors": [Array],
    "identificationAttempts": [Array],
    "identifierEntrySysId": "String",
    "info": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "relatedItems": [Array],
    "relatedSysIds": [Array],
    "sysId": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems

</td><td>

List of related CIs \(table lookup CI\) from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.Data type: Array of Objects

```
"additionalRelatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.additionalRelatedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this related item.Data type: Array

```
"inputIndices": [
    Number
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.additionalRelatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this related item.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.sysId

</td><td>

Sys\_id of this related CI.Data type: String

</td></tr><tr><td>

result.items.className

</td><td>

Sys\_class\_name of this CI.Data type: String

</td></tr><tr><td>

result.items.duplicateLookupIndices

</td><td>

Object containing arrays of index values for **items.lookup** array elements that reference the same related CI.The array name indicates the first element from the request body **items.lookup** array that references a given related CI. Its values are the set of additional elements from the same array that reference the same related CI.

Data type: Object

This example shows a case where the second element in the **items.lookup** array references the same related CI as a later element from that array:

```
"duplicateLookupIndices": [
  "2": [Array]
]
```

</td></tr><tr><td>

result.items.errorCount

</td><td>

Number of errors encountered while processing this CI.Data type: Number

</td></tr><tr><td>

result.items.errors

</td><td>

List of errors encountered while processing this CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.errors.error

</td><td>

Type of error encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.errors.message

</td><td>

Error message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts

</td><td>

List of attempts made to identify this CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.items.identificationAttempts.attemptResult

</td><td>

Outcome of this CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.attributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

result.items.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.items.identificationAttempts.identifierName

</td><td>

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this CI.Notable values:

-   Unknown: Identification of this CI failed. For details, see **errors**.

Data type: String

</td></tr><tr><td>

result.items.info

</td><td id="items_info-entry-IRE">

List of additional information about the processing of the item.Data type: Array of Objects

```
"info": [
  {
    "code": "String",
    "message": "String",
    "ruleSysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.info.code

</td><td id="items_info_code-entry-IRE">

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_UPGRADE

</td></tr><tr><td>

result.items.info.message

</td><td id="items_info_message-entry-IRE">

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

result.items.info.ruleSysId

</td><td id="items_info_ruleSysId-entry-IRE">

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr><td>

result.items.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.items.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.operation

</td><td>

Operation performed for this CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.items.relatedItems

</td><td>

List of related CIs \(table lookup CI\) from the request body **items.lookup** array.Data type: Array of Objects

```
"relatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.relatedItems.inputIndices

</td><td>

List of index values for CIs and lookup items from the request body **items** and **items.lookup** arrays that correspond to this related item.Data type: Array of Objects

```
"inputIndices": [
  {
    "mainIndex": Number,
    "subIndex": Number
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.inputIndices.mainIndex

</td><td>

Index value from the request body **items** array that corresponds to the CI parent of the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.inputIndices.subIndex

</td><td>

Index value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.relatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for entries in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged into this CI during processing.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.relatedSysIds

</td><td>

List of sys\_id values for related items \(table lookup items\) from the request body **items.lookup** array.Data type: Array

Notable values:

-   null: No sys\_id was identified for this related item.

```
"relatedSysIds": [
    Number,
    Number
]
```

</td></tr><tr><td>

result.items.sysId

</td><td>

Sys\_id found for this CI through identification.Notable values:

-   Unknown: Identification of this CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.items.warnings

</td><td>

List of warnings encountered while processing this CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.warnings.error

</td><td>

Type of warning encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.warnings.message

</td><td>

Warning message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.logContextId

</td><td>

Context ID reported for this payload.Data type: String

</td></tr><tr><td>

result.relations

</td><td>

List of dependent relationship CIs from the request body **relations** array.Data type: Array of Objects

```
"relations": [
  {
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.relations.className

</td><td>

The sys\_class\_name of this dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.relations.errorCount

</td><td>

Number of errors encountered while processing this dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.relations.errors

</td><td>

List of errors encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.errors.error

</td><td>

Type of error encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.errors.message

</td><td>

Error message encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.inputIndices

</td><td>

List of index values for the dependent relationship CI objects in the request body **relations** array that correspond to this dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.relations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.relations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.relations.operation

</td><td>

Operation performed for this dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI was inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and was inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and was inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation was performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table was updated.

 Data type: String

</td></tr><tr><td>

result.relations.warnings

</td><td>

List of warnings encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.warnings.error

</td><td>

Type of warning encountered while processing this dependent relationship CI.Data type: String

</td></tr><tr><td>

result.relations.warnings.message

</td><td>

Warning message encountered while processing this dependent relationship CI.Data type: String

</td></tr></tbody>
</table>### cURL request

Simulate submission of a payload containing a Linux server \(with serial number and network adapter related-item lookups\) and an IP switch, with an IP Connection relationship between them.

```
curl "https://instance.servicenow.com/api/now/identifyreconcile/query" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password" \
--data '{ \
  "items": [{ \
    "className": "cmdb_ci_linux_server", \
    "values": { \
      "sys_class_name": "cmdb_ci_linux_server", \
      "name": "lnux101", \
      "host_name": "lnux101.servicenow.com", \
      "ip_address": "10.11.12.173", \
      "os_name": "Linux Red Hat" \
    }, \
    "lookup": [{ \
      "className": "cmdb_serial_number", \
      "values": { \
        "serial_number": "lnux101", \
        "serial_number_type": "uuid", \
        "valid": "true" \
      } \
    }, { \
      "className": "cmdb_ci_network_adapter", \
      "values": { \
        "name": "eth0", \
        "ip_address": "10.11.12.173", \
        "mac_address": "00:55:51:21:26:2f" \
      } \
    }] \
  }, { \
    "className": "cmdb_ci_ip_switch", \
    "values": { \
      "name": "IP-Switch-1", \
      "serial_number": "Switch23587", \
      "serial_number_type": "uuid" \
    } \
  }], \
  "relations": [{ \
    "parent": 0, \
    "child": 1, \
    "type": "IP Connection::IP Connection" \
  }] \
}'
```

The Linux server CI is identified via a Hardware Rule search for its name on the Hardware \[cmdb\_ci\_hardware\] table and is processed as an update to an existing CI in the Linux Server \[cmdb\_ci\_linux\_server\] table. The IP switch is similarly identified via a Hardware Rule search for its name on the Hardware table and updates an existing CI in the IP Switch \[cmdb\_ci\_ip\_switch\] table. Finally, the IP Connection relationship between the server and the switch is inserted as a new record in the CI Relationship \[cmdb\_rel\_ci\] table.

```
{
  "result": {
    "relations": [
      {
        "operation": "INSERT",
        "mergedPayloadIds": [],
        "className": "cmdb_rel_ci",
        "errorCount": 0,
        "markers": [],
        "inputIndices": [
          0
        ]
      }
    ],
    "items": [
      {
        "relatedSysIds": [
          null,
          null
        ],
        "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
        "sysId": "539747cac0a801640163e60735fbbf6e",
        "errorCount": 0,
        "markers": [],
        "identificationAttempts": [
          {
            "attemptResult": "NO_MATCH",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_serial_number"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "MATCHED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          }
        ],
        "inputIndices": [
          0
        ],
        "additionalRelatedItems": [],
        "operation": "UPDATE",
        "relatedItems": [
          {
            "markers": [],
            "mergedPayloadIds": [],
            "inputIndices": [
              {
                "subIndex": 0,
                "mainIndex": 0
              }
            ],
            "className": "cmdb_serial_number"
          },
          {
            "markers": [],
            "mergedPayloadIds": [],
            "inputIndices": [
              {
                "subIndex": 1,
                "mainIndex": 0
              }
            ],
            "className": "cmdb_ci_network_adapter"
          }
        ],
        "mergedPayloadIds": [],
        "className": "cmdb_ci_linux_server"
      },
      {
        "operation": "UPDATE",
        "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
        "mergedPayloadIds": [],
        "sysId": "304481257f701200bee45f19befa915b",
        "identificationAttempts": [
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_serial_number"
          },
          {
            "attemptResult": "NO_MATCH",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "MATCHED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          }
        ],
        "errorCount": 0,
        "markers": [],
        "className": "cmdb_ci_ip_switch",
        "inputIndices": [
          1
        ]
      }
    ],
    "additionalCommittedRelations": [],
    "additionalCommittedItems": []
  }
}
```

## Identification and Reconciliation - POST /now/identifyreconcile/queryEnhanced

Determines the CMDB operation \(insert/update\) to perform with the specified payload \(request body\), without committing the operations in the database.

Use this endpoint to simulate submission of a payload \(request body\) to the [Identification and Reconciliation - POST /now/identifyreconcile/enhanced](c_IdentifyReconcileAPI.md#) endpoint.

This method is similar to the [Identification and Reconciliation - POST /now/identifyreconcile/query](c_IdentifyReconcileAPI.md#) method, but adds the following functionality:

-   Partial payloads
    -   In case of an item having a warning or error, indicates if an item operation is INSERT\_AS\_PARTIAL or INSERT\_INCOMPLETE.
    -   Returns the sys\_ids of partial payloads that were merged with existing partial payloads.
-   Supports payload deduplicate feature.
-   Generates a summary.

### URL format

Versioned URL: `/api/now/{api_version}/identifyreconcile/queryEnhanced`

Default URL: `/api/now/identifyreconcile/queryEnhanced`

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

options

</td><td>

Comma-separated list of name-value pairs representing Enhanced IRE options applied for the request.As an example, to override the default values for the partial payloads, partial commits, deduplicate payloads, and generate summary Enhanced IRE options:

`partial_payloads:false,partial_commits:false,deduplicate_payloads:false,generate_summary:true`

**Note:** By default or if **partial\_payloads** is set to true, both **partial\_commits** and **deduplicate\_payloads** are enabled, even if they are set to false, as those features are essential for partial payloads functionality.

For more on Enhanced IRE options, see [Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Valid values for each name-value pair:

-   true: Enable this Enhanced IRE option.
-   false: Disable this Enhanced IRE option.

Data type: String

</td></tr><tr><td>

sysparm\_data\_source

</td><td>

Source of the CI information. This must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.Data type: String

Default: Insert the API payload into the incomplete payloads table.

</td></tr></tbody>
</table><table id="table_c2c_bzn_rlb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

List of CIs to create or update.Data type: Array of Objects

```
"items": [
  {
    "className": "String",
    "internal_id": "String",
    "lookup": [Array],
    "related": [Array],
    "settings": {Object},
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.className

</td><td>

Required. The sys\_class\_name \(class/table name\) of the CI to create or update. This value can be any CMDB table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.Data type: String

</td></tr><tr><td>

items.internal\_id

</td><td>

Unique identifier for this item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup

</td><td>

Array of objects in which each object describes a lookup-based identification record. These records are used to identify the top-level configuration item based on a lookup table that has a reference back to the Configuration Item \[cmdb\_ci\] table.Data type: Array off Objects

```
"lookup": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.lookup.className

</td><td>

Required. The sys\_class\_name or class/table name of the CI to create or update. This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter, or a non-CMDB hierarchy class.Data type: String

</td></tr><tr><td>

items.lookup.internal\_id

</td><td>

Unique identifier for this lookup record in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.lookup.values

</td><td>

Object describing fields for this lookup item as name/value pairs, where the name is the field name.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "ip_address": "String",
  "mac_address": "String",
  "serial_number": "String",
  "serial_number_type": "String",
  "valid": "String"
}
```

</td></tr><tr><td>

items.related

</td><td>

Array of objects in which each object describes an item record to create or update, based on a related table that has a reference to the top-level CI that is being identified. Rules in the Related Entry \[cmdb\_related\_entry\] table define what type of records can be in this array.The related table may or may not extend the Configuration Item \[cmdb\_ci\] table. These records are not used to identify the configuration item.

Data type: Array of Objects

```
"related": [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

items.related.className

</td><td>

Required. The sys\_class\_name or class/table name of the related item to create or update.Data type: String

</td></tr><tr><td>

items.related.internal\_id

</td><td>

Unique identifier for this related item in this payload. Can be any value, but must be unique within the payload.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this related item. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_name

</td><td>

Data source for the related item information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the related item. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the related item was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.related.values

</td><td>

Object describing fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

items.settings

</td><td>

Object containing parameters defining the types of updates that are permitted.Data type: Object

```
"settings": {
  "skipReclassificationRestrictionRules": Boolean,
  "updateWithoutDowngrade": Boolean,
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr><td>

items.settings.skipReclassificationRestrictionRules

</td><td>

Flag that indicates whether IRE should skip running the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr><td>

items.settings.updateWithoutDowngrade

</td><td>

Flag that indicates whether update and downgrade are both permitted for this CI.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutSwitch

</td><td>

Flag that indicates whether this CI can be updated and its class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.settings.updateWithoutUpgrade

</td><td>

Flag that indicates whether update and upgrade are both permitted for this CI.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Data type: Boolean

Default: false

</td></tr><tr><td>

items.sys\_object\_source\_info

</td><td>

Object describing a unique CI identifier.Data type: Object

```
"sys_object_source_info": {
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
}
```

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_feed

</td><td>

Name that uniquely identifies the feed sending this CI. Use if the source can have multiple feeds.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_name

</td><td>

Data source for the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_native\_key

</td><td>

Unique key/id from the source for the CI. Can be any string that is unique to the item.Data type: String

</td></tr><tr><td>

items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

UTC date and time that the CI was scanned.Data type: String

Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

items.values

</td><td>

Object describing fields to create or update for this CI as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id.Data type: Object

Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr><td>

referenceItems

</td><td>

List of reference between two items in the payload.Data type: Array of Objects

```
"referenceItems": [
  {
    "referenced": "String",
    "referencedBy": "String",
    "referenceField": "String"
  }
]
```

</td></tr><tr><td>

referenceItems.referenced

</td><td>

The **internal\_id** defined for the item being referenced by another item.Data type: String

</td></tr><tr><td>

referenceItems.referencedBy

</td><td>

The **internal\_id** defined for the item that references another item.Data type: String

</td></tr><tr><td>

referenceItems.referenceField

</td><td>

Name of the reference field in the class/table for the **referencedBy** item.Data type: String

</td></tr><tr><td>

relations

</td><td>

List of relationships between two items defined in the payload.An object in this array can use either of two formats:

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.
-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

Data type: Array of Objects

```
"relations": [
  {
    "child": Number,
    "parent": Number,
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

 ```
"relations": [
  {
    "child_id": "String",
    "parent_id": "String",
    "sys_rel_source_info": {Object},
    "type": "String"
  }
]
```

</td></tr><tr><td>

relations.child

</td><td>

Integer index of the CI object in the **items** array that represents the child in the relationship.Data type: Number

</td></tr><tr><td>

relations.child\_id

</td><td>

The **internal\_id** of the child item in the relationship.Data type: String

</td></tr><tr><td>

relations.parent

</td><td>

Integer index of the CI object in the **items** array that represents the parent in the relationship.Data type: Number

</td></tr><tr><td>

relations.parent\_id

</td><td>

The **internal\_id** of the parent item in the relationship.Data type: String

</td></tr><tr id="input_rel_sys_rel_source_info-row-IRE"><td>

relations.sys\_rel\_source\_info

</td><td>

Discovery source information for the relationship. For non-dependency relationships, this information is in the Relationship Sources \[sys\_rel\_source\] table. Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr id="input-relations-sys_rel_source_info-source_name-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_name

</td><td>

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr id="input-relations-sys_rel_source_info-source_feed-row-IRE"><td>

relations.sys\_rel\_source\_info.source\_feed

</td><td>

Any string that is a sub-discovery/scan within the discovery source. Default: ‘UNKNOWN’ is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr><td>

relations.type

</td><td>

Type of relationship existing between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr></tbody>
</table>### Headers

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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td>

Internal server error. An unexpected error occurred while processing the request.Error message detail "Chunk \[…\] is not a valid entry" indicates that the **options** query parameter is not in the correct name-value pair format.

For example, specifying an **options** parameter of `partial` produces a 500 status code with "Chunk \[partial\] is not a valid entry" in the message detail.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_gy4_yyn_rlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List of results produced by the query.Data type: Array

```
"result": [
  "additionalCommittedItems": [Array],
  "additionalCommittedRelations": [Array],
  "items": [Array],
  "relations": [Array]
]
```

</td></tr><tr><td>

result.additionalCommittedItems

</td><td>

List of CIs not included in the request body **items** array to insert or update.Data type: Array of Objects

```
"additionalCommittedItems": [
  {
    "className": "String",
    "errorCount": Number,
    "identificationAttempts": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloads": [Array],
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.className

</td><td>

The sys\_class\_name of this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errorCount

</td><td>

Number of errors encountered while processing this additional CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedItems.errors

</td><td>

List of errors encountered while processing this additional CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.errors.error

</td><td>

Type of error encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.errors.message

</td><td>

Error message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts

</td><td>

List of attempts made to identify this additional CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attemptResult

</td><td>

Outcome of this additional CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.attributes

</td><td>

Array of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.identifierName

</td><td>

Identifier rule used for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this additional CI identification attempt.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this additional CI.Notable values:

-   Unknown: Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this additional CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedItems.mergedPayloads

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedItems.operation

</td><td>

Operation performed for this additional CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The additional CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the additional CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.sysId

</td><td>

Sys\_id found for this additional CI through identification.Notable values: Unknown - Identification of this additional CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings

</td><td>

List of warnings encountered while processing this additional CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedItems.warnings.error

</td><td>

Type of warning encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedItems.warnings.message

</td><td>

Warning message encountered while processing this additional CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations

</td><td>

List of dependent relationship CIs not included in the request body **relations** list to insert or update.Data type: Array of Objects

```
"additionalCommittedRelations": [
  {
    "className": "String",
    "operation": "String",
    "markers": [Array],
    "inputIndices": [Array],
    "mergedPayloadIds": [Array]
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.className

</td><td>

The sys\_class\_name of this additional dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errorCount

</td><td>

Number of errors encountered while processing this additional dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.additionalCommittedRelations.errors

</td><td>

List of errors encountered while processing this additional dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.errors.error

</td><td>

Type of error encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.errors.message

</td><td>

Error message encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr><td>

result.additionalCommittedRelations.inputIndices

</td><td>

List of index values for dependent relationship CI objects in the request body **relations** array that correspond to this additional dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.additionalCommittedRelations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.additionalCommittedRelations.operation

</td><td>

Operation performed for this additional dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI is inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and is inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and is inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation is performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table is updated.

Data type: String

</td></tr><tr><td>

result.items

</td><td>

List of CIs included in the request body **items** array.Data type: Array of Objects

```
"items": [
  {
    "additionalRelatedItems": [Array],
    "className": "String",
    "duplicateLookupIndices": {Object},
    "errorCount": Number,
    "errors": [Array],
    "identificationAttempts": [Array],
    "identifierEntrySysId": "String",
    "info": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "relatedItems": [Array],
    "relatedSysIds": [Array],
    "sysId": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems

</td><td>

List of related CIs \(table lookup CI\) from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.Data type: Array of Objects

```
"additionalRelatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.additionalRelatedItems.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this related item.Data type: Array

```
"inputIndices": [
    Number
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.additionalRelatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this related item.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.additionalRelatedItems.sysId

</td><td>

Sys\_id of this related CI.Data type: String

</td></tr><tr><td>

result.items.className

</td><td>

Sys\_class\_name of this CI.Data type: String

</td></tr><tr><td>

result.items.duplicateLookupIndices

</td><td>

Object containing arrays of index values for **items.lookup** array elements that reference the same related CI.The array name indicates the first element from the request body **items.lookup** array that references a given related CI. Its values are the set of additional elements from the same array that reference the same related CI.

Data type: Object

This example shows a case where the second element in the **items.lookup** array references the same related CI as a later element from that array:

```
"duplicateLookupIndices": [
  "2": [Array]
]
```

</td></tr><tr><td>

result.items.errorCount

</td><td>

Number of errors encountered while processing this CI.Data type: Number

</td></tr><tr><td>

result.items.errors

</td><td>

List of errors encountered while processing this CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.errors.error

</td><td>

Type of error encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.errors.message

</td><td>

Error message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts

</td><td>

List of attempts made to identify this CI.Data type: Array of Objects

```
"identificationAttempts": [
  {
    "attemptResult": "String",
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identiferName": "String",
    "searchOnTable": [Array]
  }
]
```

</td></tr><tr><td>

result.items.identificationAttempts.attemptResult

</td><td>

Outcome of this CI identification attempt.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.attributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

result.items.identificationAttempts.hybridEntryCiAttributes

</td><td>

List of CI identifier entry attributes used during this CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr><td>

result.items.identificationAttempts.identifierName

</td><td>

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identificationAttempts.searchOnTable

</td><td>

Name of the table searched for this CI identification attempt.Data type: String

</td></tr><tr><td>

result.items.identifierEntrySysId

</td><td>

Sys\_id for the identifier rule used to identify this CI.Notable values:

-   Unknown: Identification of this CI failed. For details, see **errors**.

Data type: String

</td></tr><tr><td>

result.items.info

</td><td id="items_info-entry-IRE">

List of additional information about the processing of the item.Data type: Array of Objects

```
"info": [
  {
    "code": "String",
    "message": "String",
    "ruleSysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.info.code

</td><td id="items_info_code-entry-IRE">

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_UPGRADE

</td></tr><tr><td>

result.items.info.message

</td><td id="items_info_message-entry-IRE">

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

result.items.info.ruleSysId

</td><td id="items_info_ruleSysId-entry-IRE">

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr><td>

result.items.inputIndices

</td><td>

List of index values for CIs from the request body **items** array that correspond to this CI.Data type: Array of Objects

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr><td>

result.items.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.operation

</td><td>

Operation performed for this CI.Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

result.items.relatedItems

</td><td>

List of related CIs \(table lookup CI\) from the request body **items.lookup** array.Data type: Array of Objects

```
"relatedItems": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.className

</td><td>

The sys\_class\_name of the related item.Data type: String

</td></tr><tr><td>

result.items.relatedItems.inputIndices

</td><td>

List of index values for CIs and lookup items from the request body **items** and **items.lookup** arrays that correspond to this related item.Data type: Array of Objects

```
"inputIndices": [
  {
    "mainIndex": Number,
    "subIndex": Number
  }
]
```

</td></tr><tr><td>

result.items.relatedItems.inputIndices.mainIndex

</td><td>

Index value from the request body **items** array that corresponds to the CI parent of the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.inputIndices.subIndex

</td><td>

Index value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr><td>

result.items.relatedItems.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.items.relatedItems.mergedPayloadIds

</td><td>

List of sys\_id values for entries in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged into this CI during processing.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.items.relatedSysIds

</td><td>

List of sys\_id values for related items \(table lookup items\) from the request body **items.lookup** array.Data type: Array

Notable values:

-   null: No sys\_id was identified for this related item.

```
"relatedSysIds": [
    Number,
    Number
]
```

</td></tr><tr><td>

result.items.sysId

</td><td>

Sys\_id found for this CI through identification.Notable values:

-   Unknown: Identification of this CI failed. See **errors** for details.

Data type: String

</td></tr><tr><td>

result.items.warnings

</td><td>

List of warnings encountered while processing this CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.items.warnings.error

</td><td>

Type of warning encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.items.warnings.message

</td><td>

Warning message encountered while processing this CI.Data type: String

</td></tr><tr><td>

result.logContextId

</td><td>

Context ID reported for this payload.Data type: String

</td></tr><tr><td>

result.relations

</td><td>

List of dependent relationship CIs from the request body **relations** array.Data type: Array of Objects

```
"relations": [
  {
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String",
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

result.relations.className

</td><td>

The sys\_class\_name of this dependent relationship CI.Only supported value:

-   cmdb\_rel\_ci: The CI Relationship table.

Data type: String

</td></tr><tr><td>

result.relations.errorCount

</td><td>

Number of errors encountered while processing this dependent relationship CI.Data type: Number

</td></tr><tr><td>

result.relations.errors

</td><td>

List of errors encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.errors.error

</td><td>

Type of error encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.errors.message

</td><td>

Error message encountered while processing this dependent relationship CI. Data type: String

</td></tr><tr><td>

result.relations.inputIndices

</td><td>

List of index values for the dependent relationship CI objects in the request body **relations** array that correspond to this dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr><td>

result.relations.markers

</td><td>

List of marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr><td>

result.relations.mergedPayloadIds

</td><td>

List of sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr><td>

result.relations.operation

</td><td>

Operation performed for this dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI was inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and was inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and was inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation was performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table was updated.

 Data type: String

</td></tr><tr><td>

result.relations.warnings

</td><td>

List of warnings encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.relations.warnings.error

</td><td>

Type of warning encountered while processing this dependent relationship CI.Data type: String

</td></tr><tr><td>

result.relations.warnings.message

</td><td>

Warning message encountered while processing this dependent relationship CI.Data type: String

</td></tr></tbody>
</table>### cURL request

Simulate submission of a partial payload for a computer CI.

```
curl "https://instance.servicenow.com/api/now/identifyreconcile/queryEnhanced" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password" \
--data '{ \
  "items" : [ \
    { \
      "className" : "cmdb_ci_computer", \
      "sys_object_source_info" : { \
        "source_name" : "ServiceNow", \
        "source_native_key" : "ncomputer3367" \
      }, \
      "values" : { \
        "cpu_core_count" : "6", \
        "ram" : "8192", \
        "manufacturer" : "DELL", \
        "company" : "My Company" \
      } \
    } \
  ] \
}'
```

The response shows that the payload would be inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.

```
{
  "result": {
    "relations": [],
    "items": [
      {
        "identifierEntrySysId": "Unknown",
        "partialSysIds": [
          "1aec79151bb45010593876a61a4bcb28"
        ],
        "sysId": "Unknown",
        "errorCount": 0,
        "markers": [],
        "className": "cmdb_ci_computer",
        "inputIndices": [
          0
        ],
        "operation": "INSERT_AS_PARTIAL",
        "errors": [],
        "identificationAttempts": [
          {
            "info": "sys_object_source NO_MATCH",
            "attemptResult": "NO_MATCH",
            "identifierName": "",
            "attributes": [],
            "hybridEntryCiAttributes": []
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_serial_number"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "mac_address",
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_network_adapter"
          }
        ],
        "warningCount": 1,
        "warnings": [
          {
            "message": "In payload missing minimum set of input values for criterion (matching) attributes from identify rule for table [cmdb_ci_hardware]. Add these input values in payload item '{\"className\":\"cmdb_ci_computer\",\"values\":{\"discovery_source\":\"ServiceNow\",\"company\":\"My Company\",\"cpu_core_count\":\"6\",\"ram\":\"8192\",\"manufacturer\":\"DELL\"},\"sys_object_source_info\":{\"source_name\":\"ServiceNow\",\"source_native_key\":\"ncomputer3367\"},\"settings\":{},\"sys_ire_info\":{\"ire_received_time\":\"2020-05-14 20:14:51\"}}'",
            "error": "MISSING_MATCHING_ATTRIBUTES"
          }
        ],
        "mergedPayloadIds": [
          "7ddcb9551bb45010593876a61a4bcb08"
        ]
      }
    ],
    "additionalCommittedRelations": [],
    "additionalCommittedItems": []
  }
}
```

Simulate submission of a second partial payload that would complete the description of the computer CI, with the summary generation Enhanced IRE option enabled.

```
curl "https://instance.servicenow.com/api/now/identifyreconcile/queryEnhanced?options=generate_summary:true" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username:password" \
--data '{ \
}'
```

The response shows that the computer CI would be inserted, and displays a summary of operations that would be performed.

```
{
  "result": {
    "relations": [],
    "hasError": false,
    "additionalCommittedItems": [],
    "hasWarning": false,
    "items": [
      {
        "relatedSysIds": [
          "735c79151bb45010593876a61a4bcb67"
        ],
        "identifierEntrySysId": "Unknown",
        "sysId": "ff5c79151bb45010593876a61a4bcb64",
        "errorCount": 0,
        "markers": [],
        "className": "cmdb_ci_computer",
        "inputIndices": [
          0
        ],
        "operation": "INSERT",
        "relatedItems": [
          {
            "operation": "INSERT",
            "warningCount": 0,
            "errors": [],
            "sysId": "735c79151bb45010593876a61a4bcb67",
            "className": "cmdb_ci_network_adapter",
            "errorCount": 0,
            "markers": [],
            "inputIndices": [
              {
                "subIndex": 0,
                "mainIndex": 0
              }
            ],
            "mergedPayloadIds": []
          }
        ],
        "mergedPayloadIds": [
          "fe4c39151bb45010593876a61a4bcbd3"
        ],
        "identificationAttempts": [
          {
            "info": "sys_object_source NO_MATCH",
            "attemptResult": "NO_MATCH",
            "identifierName": "",
            "attributes": [],
            "hybridEntryCiAttributes": []
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number",
              "serial_number_type"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_serial_number"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "serial_number"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "SKIPPED",
            "identifierName": "Hardware Rule",
            "attributes": [
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_hardware"
          },
          {
            "attemptResult": "NO_MATCH",
            "identifierName": "Hardware Rule",
            "attributes": [
              "mac_address",
              "name"
            ],
            "hybridEntryCiAttributes": [],
            "searchOnTable": "cmdb_ci_network_adapter"
          }
        ],
        "warningCount": 0
      }
    ],
    "additionalCommittedRelations": [],
    "summary": {
      "cmdb_ci_network_adapter": {
        "mergedPartialPayloads": 0,
        "inserted": 1,
        "partial": 0,
        "warnings": 0,
        "incomplete": 0,
        "additionalInserted": 0,
        "unchanged": 0,
        "skipped": 0,
        "updated": 0,
        "errors": 0
      },
      "cmdb_ci_computer": {
        "mergedPartialPayloads": 1,
        "inserted": 1,
        "partial": 0,
        "warnings": 0,
        "incomplete": 0,
        "additionalInserted": 0,
        "unchanged": 0,
        "skipped": 0,
        "updated": 0,
        "errors": 0
      }
    }
  }
}
```

