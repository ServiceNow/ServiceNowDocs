---
title: IdentificationEngine - Scoped
description: The IdentificationEngine API uses the Identification and Reconciliation framework to minimize the creation of duplicate configuration items \(CIs\) and to reconcile CI attributes by only accepting information from authorized data sources when updating the Configuration Management Database \(CMDB\).Inserts or updates configuration items \(CI\) and non-Configuration Management Database \(CMDB\) CIs \(classes not extending from cmdb\_ci\) in the CMDB based on identification and reconciliation rules. Use this API instead of updating the CMDB directly.Inserts or updates configuration items \(CI\) and non-Configuration Management Database \(CMDB\) CIs \(classes not extending from cmdb\_ci\) in the CMDB based on identification and reconciliation rules. Use this API instead of updating the CMDB directly.Determines the operation \(insert/update\) to perform with the specified payload without committing the operation in the database.Determines the Configuration Management Database \(CMDB\) operation \(insert/update\) to perform with the specified payload \(request body\), without committing the operations in the database.Runs an identification audit against the specified configuration item \(CI\) to detect duplicates.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 70
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IdentificationEngine- Scoped

The IdentificationEngine API uses the Identification and Reconciliation framework to minimize the creation of duplicate configuration items \(CIs\) and to reconcile CI attributes by only accepting information from authorized data sources when updating the Configuration Management Database \(CMDB\).

When using this class in a scoped application, use the `sn_cmdb` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IdentificationEngine - createOrUpdateCI\(String source, String input\)

Inserts or updates configuration items \(CI\) and non-Configuration Management Database \(CMDB\) CIs \(classes not extending from cmdb\_ci\) in the CMDB based on identification and reconciliation rules. Use this API instead of updating the CMDB directly.

For additional information on non-CMDB table ingestion, see IRE support for non-CMDB tables.

<table class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input

</td><td>

String

</td><td id="entry_input">

Required. Input payload. A JSON formatted string of configuration items to add or update. ```
"input" { 
 "items": [Array],
 "referenceItems": [Array],
 "relations": [Array]
}
```

</td></tr><tr><td>

input.items

</td><td>

Array of Objects

</td><td id="entry_items">

Items to add or update.```
"items": [
  { 
    "className": "String",
    "display_values": {Object},
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

input.items.className

</td><td>

String

</td><td id="entry_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.

</td></tr><tr><td>

input.items.display\_values

</td><td id="entry-display_values-ire">

Object

</td><td>

Reference fields to create or update for this related item as name-value pairs, where the name is the field name and the value is the referenced display value. If you want to use the sys\_id instead of the display value for reference fields, pass the information in the **input.items.lookup.values** parameter instead of in this parameter.Reference field names depend on the fields selected by the user, such as:

 ```
"display_values": {
  "model_id": "String",
  "location": "String"
}
```

</td></tr><tr><td>

input.items.internal\_id

</td><td>

String

</td><td id="entry_internal_id">

Unique item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.lookup

</td><td>

Array of Objects

</td><td id="entry_lookup">

Identifies the top-level item containing the lookup \(lookup-based identification\). These records are used to identify the configuration item based on a lookup table that has a reference back to cmdb\_ci.For example:

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

input.items.lookup.className

</td><td>

String

</td><td>

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter.

</td></tr><tr><td>

input.items.lookup.internal\_id

</td><td>

String

</td><td>

Unique item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info

</td><td>

Object

</td><td>

Unique CI identifier for a specific source.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key/id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date and time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

input.items.lookup.values

</td><td>

Object

</td><td>

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

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

input.items.related

</td><td>

Array

</td><td>

Reference to the top-level item that contains the related list. Rules in the Related Entry \[cmdb\_related\_entry\] define what type of records can be in this array. These records are used to add items based on a related table that has a reference to the CI that is being identified. The related table may or may not extend cmdb\_ci. These records are not used to identify the configuration item.

```
"related" [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

input.items.related.className

</td><td>

String

</td><td>

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_software\_instance or cmdb\_key\_value.

</td></tr><tr><td>

input.items.related.internal\_id

</td><td>

String

</td><td>

Unique item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info

</td><td>

Object

</td><td>

Unique CI identifier for a specific source.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key/id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date and time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

input.items.related.values

</td><td>

Object

</td><td>

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr id="row_items_settings"><td>

input.items.settings

</td><td>

Object

</td><td>

Parameters that define the types of updates that are permitted.```
"settings": { 
  "skipReclassificationRestrictionRules": Boolean, 
  "updateWithoutDowngrade": Boolean, 
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr><td>

input.items.settings.skipReclassificationRestrictionRules

</td><td>

Boolean

</td><td id="items_set_skipReclassRestrictRules-entry-IRE">

Flag that indicates whether IRE should not run the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutDowngrade"><td>

input.items.settings.updateWithoutDowngrade

</td><td>

Boolean

</td><td>

Flag that indicates whether update and downgrade are both permitted for this item.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutUpgrade"><td>

input.items.settings.updateWithoutUpgrade

</td><td>

Boolean

</td><td>

Flag that indicates whether update and upgrade are both permitted for this item.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutSwitch"><td>

input.items.settings.updateWithoutSwitch

</td><td>

Boolean

</td><td>

Flag that indicates whether the item can be updated and the class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Default: false

</td></tr><tr><td>

input.items.sys\_object\_source\_info

</td><td>

Object

</td><td>

Unique CI identifier for a specific source.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key/id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date and time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

input.items.values

</td><td>

Object

</td><td id="entry_values">

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

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

input.referenceItems

</td><td>

Array of Objects

</td><td id="entry_referenceItems">

List that define references between items in the input payload. The values of each reference item are populated before identifying a CI using the IRE rules defined on a class.```
"referenceItems": [
  { 
    "referenced": "String", 
    "referencedBy": "String", 
    "referenceField": "String" 
  }
]
```

</td></tr><tr><td>

input.referenceItems.referenced

</td><td>

String

</td><td id="entry_referenceItems_referenced">

The **internal\_id** defined for the item being referenced by another item.

</td></tr><tr><td>

input.referenceItems.referencedBy

</td><td>

String

</td><td id="entry_referenceItems_referencedBy">

The **internal\_id** defined for the item that references another item.

</td></tr><tr><td>

input.referenceItems.referenceField

</td><td>

String

</td><td id="entry_referenceItems_referenceField">

Name of the reference field in the class/table for the **referencedBy** item.

</td></tr><tr><td>

input.relations

</td><td>

Array of Objects

</td><td id="entry_relations">

List that specifies relationships between items in the input payload. An object in this array can use either of two formats.

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.

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

-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

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

input.relations.child

</td><td>

Number

</td><td id="entry_relations_child">

Integer index of the CI object in the **items** array that represents the child in the relationship \(items, items.related, or items.lookup.\)

</td></tr><tr><td>

input.relations.child\_id

</td><td>

String

</td><td id="entry_relations_child_id">

The **internal\_id** of the child item in the relation \(items, items.related, or items.lookup.\)

</td></tr><tr><td>

input.relations.parent

</td><td>

Number

</td><td id="entry_relations_parent">

Integer index of the parent item in the **items** array \(items, items.related, or items.lookup.\)

</td></tr><tr><td>

input.relations.parent\_id

</td><td>

String

</td><td id="entry_relations_parent_id">

The **internal\_id** of the parent item in the relation \(items, items.related, or items.lookup.\)

</td></tr><tr><td>

input.relations.sys\_rel\_source\_info

</td><td>

Object

</td><td id="sys_rel_source_info-entry-IRE">

Discovery source information for the relationship. For non-dependency relationships, this information is saved in the Relationship Sources \[sys\_rel\_source\] table \(not persisted for identifyCIEnhanced\(\) or identifyCI\(\) methods.\)Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr><td>

input.relations.sys\_rel\_source\_info.source\_name

</td><td>

String

</td><td id="sys_rel_source_info-source_name-entry-ire">

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr><td>

input.relations.sys\_rel\_source\_info.source\_feed

</td><td>

String

</td><td id="sys_rel_source_into-source_feed-entry-ire">

Any string that is a sub-discovery/scan within the discovery source. Default: 'UNKNOWN' is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr><td>

input.relations.type

</td><td>

String

</td><td id="entry_relations_type">

Type of relationship that exists between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.

</td></tr><tr><td>

source

</td><td>

String

</td><td>

Identifies the data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the cmdb\_ci table.

</td></tr></tbody>
</table><table id="table_yyd_zxn_ylb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;String&gt;

</td><td>

JSON formatted string that is a list of results for the configuration items in the input string. Each result string is in the format  'items: \[\{\}\], relations:\[\{\}\]', where each item within the items and relations lists contains name-value pairs. Data type: String

</td></tr><tr><td>

&lt;String&gt;.additionalCommittedItems

</td><td>

No values are currently returned.

</td></tr><tr><td>

&lt;String&gt;.additionalCommittedRelations

</td><td>

No values are currently returned.

</td></tr><tr><td>

&lt;String&gt;.items

</td><td>

Description of the created or updated CIs.Data type: Object

```
"items": { 
  "additionalRelatedItems": [Array],
  "className": "String",
  "duplicateIndices": [Array],
  "errorCount": Number,
  "errors": [Array],
  "identificationAttempts": [Array],
  "identifierEntrySysId": "String",
  "info": [Array],
  "inputIndices": [Array],
  "maskedAttributes": [Array],
  "operation": "String",
  "relatedItems": [Array],
  "relatedSysIds": [Array],
  "sysId": "String"
}
```

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems

</td><td>

List of information about additional lookup and related items that were processed but not provided as part of the input payload. These items are from partial payloads.This information is not currently returned.

Data type: Array of Objects

```
"additionalRelatedItems": [ 
  {
    "className": "String", 
    "inputIndices": [Array], 
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.className

</td><td>

Class/table name \(sys\_class\_name\) of the CI that was created or updated.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.inputIndices

</td><td>

Index of the corresponding input item. For top-level items, it is a list of integers. For related or lookup items, it is list of JSON objects.Data type: Array of Numbers or Array of Objects

```
"inputIndices": [
  { 
   "mainIndex": Number, 
   "subIndex": Number 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.inputIndices.mainIndex

</td><td>

Index value from the request body **items** array that corresponds to the CI parent of the additional related item. Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.inputIndices.subIndex

</td><td>

Index value from the request body **items.lookup** array that corresponds to the additional related item.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.operation

</td><td>

Type of operation.Possible values:

-   INSERT: New CI was inserted into the database.
-   NO\_CHANGE: No CI changes were made.
-   UPDATE: Existing CI was updated.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.sysId

</td><td>

Sys\_id of the additional related items.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.className

</td><td id="entry_return_item_className">

Class/table name \(sys\_class\_name\) of the CI that was created or updated.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.duplicateIndices

</td><td id="entry_return_items_duplicateIndices">

List of indexes of CIs that are duplicates of the current item.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.errorCount

</td><td>

Number of errors.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.errors

</td><td id="entry_return_item_error">

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

&lt;String&gt;.items.errors.error

</td><td id="items_errors_errors-entry-IRE">

Type of error encountered while processing the CI.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.errors.message

</td><td id="items_errors_msg-entry-IRE">

Error message associated with the error.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts

</td><td id="entry_return_item_identificationAttempts">

List of attempts that were made to identify the CIs.Data type: Array of Objects

```
"identificationAttempts": [
  { 
    "attemptResult": "String", 
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identifierName": "String",
    "searchOnTable": "String" 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.attemptResult

</td><td id="entry_return_item_identificationAttempts_attemptResult">

Results of the attempt to identify the CI.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.attributes

</td><td id="entry_return_item_identificationAttempts_attributes">

List of CI identifier entry attributes that were used during the identification process.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.hybridEntryCiAttributes

</td><td>

No values are currently returned.

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.identifierName

</td><td id="entry_return_item_identificationAttempts_identifierName">

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.searchOnTable

</td><td id="entry_return_item_identificationAttempts_searchOnTable">

Name of the table searched during the identification process.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identifierEntrySysId

</td><td id="entry_return_item_identifierEntrySysId">

Sys\_id for the identifier rule used to identify the CI.Data type: String

Table: Identifier Entry \[cmdb\_identifier\_entry\]

</td></tr><tr><td>

&lt;String&gt;.items.info

</td><td id="items_info-entry-IREE">

List that contain additional information about the processing of the item.Data type: Array of Objects

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

&lt;String&gt;.items.info.code

</td><td>

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_UPGRADE

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info.message

</td><td>

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info.ruleSysId

</td><td>

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.inputIndices

</td><td>

Index values for CIs from the request body **items** array that correspond to this CI.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.maskedAttributes

</td><td id="entry_return_item_maskedAttributes">

List of attributes whose update by a non-authoritative data source was skipped as defined by the Reconciliation Rules.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems

</td><td>

List that provides information about the processed related items.Data type: Array of Objects

```
"relatedItems": [
  { 
    "className": "String",
    "errors": [Array],
    "errorCount": Number, 
    "inputIndices": [Array],
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.className

</td><td>

Class/table name \(sys\_class\_name\) of the related item.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.errors

</td><td>

List of errors that occurred during processing.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.errorCount

</td><td>

Number of errors detected during processing.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.inputIndices

</td><td>

Indexes of the corresponding related items.Data type: Array or Numbers

```
"inputIndices": [
  { 
   "mainIndex": Number, 
   "subIndex": Number 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.inputIndices.mainIndex

</td><td>

Integer value from the request body **items** array that corresponds to the CI parent of the related item.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.inputIndices.subIndex

</td><td>

Integer value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.operation

</td><td>

Type of operation.Possible values:

-   INSERT: New CI was inserted into the database.
-   NO\_CHANGE: No CI changes were made.
-   UPDATE: Existing CI was updated.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedSysIds

</td><td>

List of the sys\_id values for related items \(table lookup items\) from the request body **items.lookup** array.Notable values - null: No sys\_id was identified for this related item.

Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.sys\_id

</td><td id="entry_return_item_sys_id">

Sys\_id of the CI that was updated or created.Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations

</td><td>

Information about the processed relations.Data type: Array of Objects

```
"relations":[
  { 
    "className": "String",
    "errorCount": Number,
    "inputIndices": [Array],
    "operation": "String",
    "sysId": "String" 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.relations.className

</td><td id="entry_return_relations_className">

Sys\_class\_name of this dependent relationship CI.Only supported value: cmdb\_rel\_ci: CI Relationship table.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations.errorCount

</td><td>

Number of errors.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.relations.inputIndices

</td><td>

Indexes of the corresponding input relations.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.relations.operation

</td><td>

Type of operation performed.Possible values:

-   INSERT
-   UPDATE
-   NO\_CHANGE

Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations.sysId

</td><td id="entry_return_relations_sys_id">

Sys\_id of the dependent relationship CI.Data type: String

</td></tr></tbody>
</table>The following shows how to reclassify a configuration item.

```
var payload = {
  "items": [
    {
      "className": "cmdb_ci_win_server",
      "values": {
        "short_description": "Linux server description",
        "name": "Linux Server 1"
      }
    }
  ]
};

var input = JSON.stringify(payload);
var output = sn_cmdb.IdentificationEngine.createOrUpdateCI('ServiceNow', input);

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{
  "items": [
    {
      "className": "cmdb_ci_linux_server",
      "operation": "NO_CHANGE",
      "sysId": "440577800f321010150efc91ff767e94",
      "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
      "identificationAttempts": [
        {
          "attributes": [],
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "serial_number",
            "serial_number_type"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "searchOnTable": "cmdb_serial_number",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "serial_number"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "name"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "MATCHED",
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        }
      ],
      "info": [
        {
          "message": "CI Reclassification not allowed from class: [cmdb_ci_linux_server] to [cmdb_ci_win_server] by a reclassification restriction rule",
          "code": "SKIPPED_CLASS_SWITCH",
          "ruleSysId": "b3d4b3800f321010150efc91ff767eab"
        }
      ],
      "errorCount": 0,
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ],
      "mergedPayloadIds": []
    }
  ],
  "additionalCommittedItems": [],
  "relations": [],
  "additionalCommittedRelations": []
}
```

The following shows how to update a configuration item.

```
var payload = {
"items": [
{
 "className": "cmdb_ci_win_server", 
 "values": {
   "chassis_type": "Desktop",
   "os": "Windows 2012 R2 Datacenter",
   "name": "Windows2012Server1",
   "serial_number": "0000-0011-1690-8730-8636-5722-52",
   "cpu_count": "1"
  },
  "lookup": [
  {
     "values": {
       "valid": "true",
       "serial_number": "0000-0011-1690-8730-8636-5722-52",
       "serial_number_type": "bios"
      },
     "className": "cmdb_serial_number"
   },
   {
     "values": {
       "valid": "true",
       "serial_number": "3311-9736-4988-9744-1749-4183-41",
       "serial_number_type": "chassis"
      },
     "className": "cmdb_serial_number"
   }],

    "internal_id": "16777219",
    "sys_object_source_info": {
      "source_feed": "SN Discovery Feed 1",
      "source_name": "ServiceNow",
      "source_native_key": "16777219",
      "source_recency_timestamp": "2019-10-18 08:31:23"
   }},
   {  
   "className": "cmdb_ci_spkg",
   "values": {
     "name": "Windows 2012 R2 Datacenter",
     "key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL"
     },

  "related": [
    {
      "internal_id": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219",
      "values": {
        "name": "Windows 2012 R2 Datacenter-SAMLABVM52"
      },
      "className": "cmdb_software_instance",
      "sys_object_source_info": {
        "source_feed": "SN Discovery Feed 1",
        "source_name": "ServiceNow",
        "source_native_key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219"
  }}]}, 
  {
  "className": "cmdb_ci_app_server_tomcat",
  "values": {
    "running_process_key_parameters": "/opt/OV/nonOV/tomcat/b/temp org.apache.catalina.startup.Bootstrap start",
    "install_directory": "/opt/OV/nonOV/tomcat/b",
    "name": "Tomcat@hpom9:3443",
    "server_port": "8006",
    "sys_class_name": "cmdb_ci_app_server_tomcat"
  },

  "internal_id": "tomcat_id"
  }],

"relations": [
  {
    "parent_id": "tomcat_id",
    "child_id": "16777219",
    "type": "Runs on::Runs"
  }],

"referenceItems": [
  {
    "referenceField": "installed_on",
    "referenced": "16777219",
    "referencedBy": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219"
  }]};

var input = JSON.stringify(payload);
var output = sn_cmdb.IdentificationEngine.createOrUpdateCI('ServiceNow', input);

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{
  "items": [
    {
      "className": "cmdb_ci_win_server",
      "operation": "INSERT",
      "sysId": "d56ab6eadbd510102f67dfea5e96194e",
      "relatedSysIds": [
        "dd6af62adb1910102f67dfea5e96197f",
        "996af62adb1910102f67dfea5e961980"
      ],
      "relatedItems": [
        {
          "errors": [],
          "operation": "INSERT",
          "errorCount": 0,
          "mergedPayloadIds": [],
          "warningCount": 0,
          "sysId": "dd6af62adb1910102f67dfea5e96197f",
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 0,
              "subIndex": 0
            }
          ],
          "className": "cmdb_serial_number"
        },
        {
          "errors": [],
          "operation": "INSERT",
          "errorCount": 0,
          "mergedPayloadIds": [],
          "warningCount": 0,
          "sysId": "996af62adb1910102f67dfea5e961980",
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 0,
              "subIndex": 1
            }
          ],
          "className": "cmdb_serial_number"
        }
      ],
      "identifierEntrySysId": "Unknown",
      "identificationAttempts": [
        {
          "info": "sys_object_source NO_MATCH",
          "identifierName": "",
          "attemptResult": "NO_MATCH",
          "attributes": [],
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "serial_number",
            "serial_number_type"
          ],
          "searchOnTable": "cmdb_serial_number",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "serial_number"
          ],
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "name"
          ],
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "attributes": [
            "mac_address",
            "name"
          ],
          "searchOnTable": "cmdb_ci_network_adapter",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ]
    },
    {
      "className": "cmdb_ci_spkg",
      "operation": "INSERT",
      "sysId": "116af62adb1910102f67dfea5e961981",
      "relatedSysIds": [
        "6d6af62adb1910102f67dfea5e961984"
      ],
      "relatedItems": [
        {
          "errors": [],
          "operation": "INSERT",
          "errorCount": 0,
          "mergedPayloadIds": [],
          "warningCount": 0,
          "sysId": "6d6af62adb1910102f67dfea5e961984",
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 1,
              "subIndex": 0
            }
          ],
          "className": "cmdb_software_instance"
        }
      ],
      "identifierEntrySysId": "Unknown",
      "identificationAttempts": [
        {
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "attributes": [],
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Software",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "key"
          ],
          "searchOnTable": "cmdb_ci_spkg",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        1
      ]
    },
    {
      "className": "cmdb_ci_app_server_tomcat",
      "operation": "INSERT",
      "sysId": "e96af62adb1910102f67dfea5e961985",
      "identifierEntrySysId": "Unknown",
      "identificationAttempts": [
        {
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "attributes": [],
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        2
      ]
    }
  ],
  "additionalCommittedItems": [],
  "relations": [
    {
      "className": "cmdb_rel_ci",
      "operation": "INSERT",
      "sysId": "e96af62adb1910102f67dfea5e961989",
      "identifierEntrySysId": "Unknown",
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ]
    }
  ],
  "additionalCommittedRelations": []
}
```

Identify a dependent CI.

```
var payload = 
              {items: [ 
                    {className:'cmdb_ci_web_server', 
                     values: {name:'apache linux den 200', 
                              running_process_command: 'xyz',  
                              running_process_key_parameters: 'abc', 
                              tcp_port:'3452'}}, 
                    {className:'cmdb_ci_linux_server', 
                     values: {name:'lnux100', ram:'2048'}}],
               relations:[{parent: 0, child: 1, type: 'Runs on::Runs'}]
              };

var input = JSON.stringify(payload);
var output = sn_cmdb.IdentificationEngine.createOrUpdateCI('ServiceNow', input);

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{
  "items": [
    {
      "className": "cmdb_ci_web_server",
      "operation": "INSERT",
      "sysId": "b9bb766adb1910102f67dfea5e961962",
      "identifierEntrySysId": "Unknown",
      "identificationAttempts": [
        {
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "attributes": [],
          "hybridEntryCiAttributes": []
        },
        {
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "attributes": [],
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ]
    },
    {
      "className": "cmdb_ci_linux_server",
      "operation": "INSERT",
      "sysId": "a5bb766adb1910102f67dfea5e96195b",
      "identifierEntrySysId": "Unknown",
      "identificationAttempts": [
        {
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "attributes": [],
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "attributes": [
            "serial_number",
            "serial_number_type"
          ],
          "searchOnTable": "cmdb_serial_number",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "attributes": [
            "serial_number"
          ],
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "name"
          ],
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "attributes": [
            "mac_address",
            "name"
          ],
          "searchOnTable": "cmdb_ci_network_adapter",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        1
      ]
    }
  ],
  "additionalCommittedItems": [],
  "relations": [
    {
      "className": "cmdb_rel_ci",
      "operation": "INSERT",
      "sysId": "fdbb766adb1910102f67dfea5e961964",
      "identifierEntrySysId": "Unknown",
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ]
    }
  ],
  "additionalCommittedRelations": []
}
```

Identify an independent CI with lookup-based identification.

```
var payload = {items: [
           {className:'cmdb_ci_netgear', 
               values: {name:'ny8500-nbxs08',
                        ports:'1200'}, 
               lookup: [{className:'cmdb_serial_number',
                            values:{serial_number:'1234ABCD', serial_number_type:'uuid',absent:'false',valid:'true'}},
                        {className:'cmdb_serial_number',
                            values:{serial_number:'3456EFGH', serial_number_type:'system',absent:'false',valid:'true'}}]}]};

var input = JSON.stringify(payload);
var output = sn_cmdb.IdentificationEngine.createOrUpdateCI('ServiceNow', input);

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{
  "items": [
    {
      "className": "cmdb_ci_netgear",
      "operation": "INSERT",
      "sysId": "787c7e6adb1910102f67dfea5e96196e",
      "relatedSysIds": [
        "f47c7e6adb1910102f67dfea5e961977",
        "3c7c7e6adb1910102f67dfea5e961977"
      ],
      "relatedItems": [
        {
          "errors": [],
          "operation": "INSERT",
          "errorCount": 0,
          "mergedPayloadIds": [],
          "warningCount": 0,
          "sysId": "f47c7e6adb1910102f67dfea5e961977",
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 0,
              "subIndex": 0
            }
          ],
          "className": "cmdb_serial_number"
        },
        {
          "errors": [],
          "operation": "INSERT",
          "errorCount": 0,
          "mergedPayloadIds": [],
          "warningCount": 0,
          "sysId": "3c7c7e6adb1910102f67dfea5e961977",
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 0,
              "subIndex": 1
            }
          ],
          "className": "cmdb_serial_number"
        }
      ],
      "identifierEntrySysId": "Unknown",
      "identificationAttempts": [
        {
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "attributes": [],
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "serial_number",
            "serial_number_type"
          ],
          "searchOnTable": "cmdb_serial_number",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "attributes": [
            "serial_number"
          ],
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "attributes": [
            "name"
          ],
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "attributes": [
            "mac_address",
            "name"
          ],
          "searchOnTable": "cmdb_ci_network_adapter",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "mergedPayloadIds": [],
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ]
    }
  ],
  "additionalCommittedItems": [],
  "relations": [],
  "additionalCommittedRelations": []
}
```

## IdentificationEngine - createOrUpdateCIEnhanced\(String source, String input, Object options\)

Inserts or updates configuration items \(CI\) and non-Configuration Management Database \(CMDB\) CIs \(classes not extending from cmdb\_ci\) in the CMDB based on identification and reconciliation rules. Use this API instead of updating the CMDB directly.

In addition to providing the functionality of the createOrUpdateCI\(\) method, this method also supports:

-   Handling partial payloads
-   Handling partial commits
-   Removing duplicate items within a payload
-   Generating output summaries

For additional information on IRE and more detailed explanations of the data used by this method, see Identification and Reconciliation \(IRE\).

For additional information on non-CMDB table ingestion, see IRE support for non-CMDB tables.

<table id="table_vyh_fvh_sjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="row_input"><td>

input

</td><td>

String

</td><td id="entry_input">

Required. Input payload. A JSON formatted string of configuration items to add or update. ```
"input" { 
 "items": [Array],
 "referenceItems": [Array],
 "relations": [Array]
}
```

</td></tr><tr id="row_items"><td>

input.items

</td><td>

Array of Objects

</td><td id="entry_items">

Items to add or update.```
"items": [
  { 
    "className": "String",
    "display_values": {Object},
    "internal_id": "String",
    "lookup": [Array],
    "related": [Array],
    "settings": {Object},
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr id="row_className"><td>

input.items.className

</td><td>

String

</td><td id="entry_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.

</td></tr><tr id="row-display_values-ire"><td>

input.items.display\_values

</td><td id="entry-display_values-ire">

Object

</td><td>

Reference fields to create or update for this related item as name-value pairs, where the name is the field name and the value is the referenced display value. If you want to use the sys\_id instead of the display value for reference fields, pass the information in the **input.items.lookup.values** parameter instead of in this parameter.Reference field names depend on the fields selected by the user, such as:

 ```
"display_values": {
  "model_id": "String",
  "location": "String"
}
```

</td></tr><tr id="row_internal_id"><td>

input.items.internal\_id

</td><td>

String

</td><td id="entry_internal_id">

Unique item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr id="row_lookup"><td>

input.items.lookup

</td><td>

Array of Objects

</td><td id="entry_lookup">

Identifies the top-level item containing the lookup \(lookup-based identification\). These records are used to identify the configuration item based on a lookup table that has a reference back to cmdb\_ci.For example:

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

</td></tr><tr id="row-input_items_lookup_className"><td>

input.items.lookup.className

</td><td>

String

</td><td id="entry-input_items_lookup_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter.

</td></tr><tr><td>

input.items.lookup.internal\_id

</td><td>

String

</td><td>

Unique lookup item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info

</td><td>

Object

</td><td>

Defines a unique CI identifier for a specific data source. Different sources may have different name-value pairs for the same CI.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key-id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date/time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

input.items.lookup.values

</td><td>

Object

</td><td>

Field information for the CI as name-value pairs, where the name is the field name. When updating reference fields, the value must be the referenced sys\_id.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "serial_number": "String",
  "serial_number_type": "String",
  "valid": "String",
  "ip_address": "String",
  "mac_address": "String"
}
```

</td></tr><tr id="row_related"><td>

input.items.related

</td><td>

Array of Objects

</td><td id="entry_related">

Reference to the top-level item that contains the related list. Rules in the Related Entry \[cmdb\_related\_entry\] define what type of records can be in this array. These records are used to add items based on a related table that has a reference to the CI that is being identified. The related table may or may not extend cmdb\_ci. These records are not used to identify the configuration item.

```
"related" [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

input.items.related.className

</td><td>

String

</td><td id="entry-input_items_related_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_software\_instance or cmdb\_key\_value.

</td></tr><tr><td>

input.items.related.internal\_id

</td><td>

String

</td><td>

Unique identifier for this related item in this payload. Can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info

</td><td>

Object

</td><td>

Object that makes up a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Identifies the data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key/ID from the source for the related item. The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date and time that the item was scanned.Format: `YYYY-MM-DD hh:mm:ss`

</td></tr><tr><td>

input.items.related.values

</td><td>

Object

</td><td>

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr id="row_items_settings"><td>

input.items.settings

</td><td>

Object

</td><td id="entry_items_settings">

Parameters that define the types of updates that are permitted.```
"settings": { 
  "skipReclassificationRestrictionRules": Boolean, 
  "updateWithoutDowngrade": Boolean, 
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr id="items_set_skipReclassRestrictRules-row-IRE"><td>

input.items.settings.skipReclassificationRestrictionRules

</td><td>

Boolean

</td><td id="items_set_skipReclassRestrictRules-entry-IRE">

Flag that indicates whether IRE should not run the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutDowngrade"><td>

input.items.settings.updateWithoutDowngrade

</td><td>

Boolean

</td><td id="entry_items_settings_updateWithoutDowngrade">

Flag that indicates whether update and downgrade are both permitted for this item.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutSwitch"><td>

input.items.settings.updateWithoutSwitch

</td><td>

Boolean

</td><td id="entry_items_settings_updateWithoutSwitch">

Flag that indicates whether the item can be updated and the class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutUpgrade"><td>

input.items.settings.updateWithoutUpgrade

</td><td>

Boolean

</td><td id="entry_items_settings_updateWithoutUpgrade">

Flag that indicates whether update and upgrade are both permitted for this item.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Default: false

</td></tr><tr id="row_items_sys_object_source_info"><td>

input.items.sys\_object\_source\_info

</td><td>

Object

</td><td id="entry_items_sys_object_source_info">

Unique CI identifier for a specific source.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr id="row_items_sys_object_source_info_source_feed"><td>

input.items.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_feed">

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr id="row_items_sys_object_source_info_source_name"><td>

input.items.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_name">

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr id="row_items_sys_object_source_info_source_native_key"><td>

input.items.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_native_key">

Unique key/id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr id="row_items_sys_object_source_info_source_recency_timestamp"><td>

input.items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_recency_timestamp">

UTC date and time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr id="row_values"><td>

input.items.values

</td><td>

Object

</td><td id="entry_values">

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr id="row_referenceItems"><td>

input.referenceItems

</td><td>

Array of Objects

</td><td id="entry_referenceItems">

List that define references between items in the input payload. The values of each reference item are populated before identifying a CI using the IRE rules defined on a class.```
"referenceItems": [
  { 
    "referenced": "String", 
    "referencedBy": "String", 
    "referenceField": "String" 
  }
]
```

</td></tr><tr id="row_referenceItems_referenced"><td>

input.referenceItems.referenced

</td><td>

String

</td><td id="entry_referenceItems_referenced">

The **internal\_id** defined for the item being referenced by another item.

</td></tr><tr id="row_referenceItems_referencedBy"><td>

input.referenceItems.referencedBy

</td><td>

String

</td><td id="entry_referenceItems_referencedBy">

The **internal\_id** defined for the item that references another item.

</td></tr><tr id="row_referenceItems_referenceField"><td>

input.referenceItems.referenceField

</td><td>

String

</td><td id="entry_referenceItems_referenceField">

Name of the reference field in the class/table for the **referencedBy** item.

</td></tr><tr id="row_relations"><td>

input.relations

</td><td>

Array of Objects

</td><td id="entry_relations">

List that specifies relationships between items in the input payload. An object in this array can use either of two formats.

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.

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

-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

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


</td></tr><tr id="row_relations_child"><td>

input.relations.child

</td><td>

Number

</td><td id="entry_relations_child">

Integer index of the CI object in the **items** array that represents the child in the relationship \(items, items.related, or items.lookup.\)

</td></tr><tr id="row_relations_child_id"><td>

input.relations.child\_id

</td><td>

String

</td><td id="entry_relations_child_id">

The **internal\_id** of the child item in the relation \(items, items.related, or items.lookup.\)

</td></tr><tr id="row_relations_parent"><td>

input.relations.parent

</td><td>

Number

</td><td id="entry_relations_parent">

Integer index of the parent item in the **items** array \(items, items.related, or items.lookup.\)

</td></tr><tr id="row_relations_parent_id"><td>

input.relations.parent\_id

</td><td>

String

</td><td id="entry_relations_parent_id">

The **internal\_id** of the parent item in the relation \(items, items.related, or items.lookup.\)

</td></tr><tr id="input_rel_sys_rel_source_info-row-IRE"><td>

input.relations.sys\_rel\_source\_info

</td><td>

Object

</td><td id="sys_rel_source_info-entry-IRE">

Discovery source information for the relationship. For non-dependency relationships, this information is saved in the Relationship Sources \[sys\_rel\_source\] table \(not persisted for identifyCIEnhanced\(\) or identifyCI\(\) methods.\)Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr id="input-relations-sys_rel_source_info-source_name-row-IRE"><td>

input.relations.sys\_rel\_source\_info.source\_name

</td><td>

String

</td><td id="sys_rel_source_info-source_name-entry-ire">

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr id="input-relations-sys_rel_source_info-source_feed-row-IRE"><td>

input.relations.sys\_rel\_source\_info.source\_feed

</td><td>

String

</td><td id="sys_rel_source_into-source_feed-entry-ire">

Any string that is a sub-discovery/scan within the discovery source. Default: 'UNKNOWN' is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr id="row_relations_type"><td>

input.relations.type

</td><td>

String

</td><td id="entry_relations_type">

Type of relationship that exists between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.

</td></tr><tr id="row_options"><td>

options

</td><td>

Object

</td><td id="entry_options">

Optional, but \{\} or null must be passed-in. Options to enable or disable features.**Note:** By default or if **partial\_payloads** is set to true, both **partial\_commits** and **deduplicate\_payloads** are enabled, even if they are set to false, as those features are essential for partial payloads functionality.

```
"options": { 
 "deduplicate_payloads": Boolean,
 "generate_summary": Boolean, 
 "partial_commits": Boolean, 
 "partial_payloads": Boolean,
 "skip_updating_last_scan_to_now": Boolean,
 "skip_updating_source_last_discovered_to_now": Boolean
}
```

</td></tr><tr id="row_options_deduplicate_payloads"><td>

options.deduplicate\_payloads

</td><td>

Boolean

</td><td id="entry_options_deduplicate_payloads">

Flag that indicates whether duplicate items are merged or considered errors.Valid values:

-   true: Merge duplicate items.
-   false: Consider duplicate items as errors.

Default: true

</td></tr><tr id="row_options_generate_summary"><td>

options.generate\_summary

</td><td>

Boolean

</td><td id="entry_options_generate_summary">

Flag that indicates whether the returned results contain summary information. For the details of the returned summary information, see **&lt;String&gt;.summary** in the return results table.Valid values:

-   true: Include summary information.
-   false: Don't include summary information.

Default: false

</td></tr><tr id="row_options_partial_commits"><td>

options.partial\_commits

</td><td>

Boolean

</td><td id="entry_options_partial_commits">

Flag that indicates whether partial commit support is enabled. For additional information on partial commits, see Enhanced IRE features.Valid values:

-   true: Partial commit enabled.
-   false: Partial commit disabled.

Default: true

</td></tr><tr id="row_options_partial_payloads"><td>

options.partial\_payloads

</td><td>

Boolean

</td><td id="entry_options_partial_payloads">

Flag that indicates whether partial payload support is enabled. For additional information on partial payloads, see Enhanced IRE features and Create an IRE data source rule.Valid values:

-   true: Partial payload enabled.
-   false: Partial payload disabled.

Default: true

</td></tr><tr><td>

options.skip\_updating\_last\_scan\_to\_now

</td><td>

Boolean

</td><td>

Flag that indicates whether to skip updating the sys\_object\_source's last\_scan time field.Valid values:

-   true: If the **source\_recency\_timestamp** parameter is not passed in**sys\_object\_source\_info**, do not update the sys\_object\_source's last\_scan time field.
-   false: Update the sys\_object\_source's last\_scan time field.

Default: Uses the value in the glide.identification\_engine.skip\_updating\_last\_scan\_to\_now system property.

</td></tr><tr><td>

options.skip\_updating\_source\_last\_discovered\_to\_now

</td><td>

Boolean

</td><td>

Flag that indicates whether to skip updating the discovery\_source and last\_discovered fields in the Configuration Item \[cmdb\_ci\] table.Valid values:

-   true: If last\_discovered is not provided in the payload item values, do not update the discovery\_source and last\_discovered fields.
-   false: Update the discovery\_source and last\_discovered fields.

Default: Uses the value in the glide.identification\_engine.skip\_updating\_source\_last\_discovered\_to\_now system property.

</td></tr><tr id="row_source"><td>

source

</td><td>

String

</td><td id="entry_source">

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr></tbody>
</table><table id="table_q4n_dvx_3lb" class="returns"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr id="row-string-enhanced"><td>

&lt;String&gt;

</td><td>

JSON formatted string that is a list of results for the configuration items in the input string.Data type: String

```
{ 
  "additionalCommittedItems": [Array],  
  "additionalCommittedRelations": [Array], 
  "hasError": Boolean, 
  "hasWarning": Boolean,
  "items": [Array],  
  "relations": [Array], 
  "summary": {Object} 
}
```

</td></tr><tr id="row_return_additionalCommittedItems"><td>

&lt;String&gt;.additionalCommittedItems

</td><td>

List of CIs that were committed during the IRE processing of the current payload, but were not present in the current input payload.Data type: Array of Objects

```
"additionalCommittedItems": [
  {
    "className": "String",
    "errorCount": Number,
    "operation": "String",
    "identificationAttempts": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloads": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr id="row-return-additionalCommittedItems-className"><td>

&lt;String&gt;.additionalCommittedItems.className

</td><td>

Sys\_class\_name of this additional CI.Data type: String

</td></tr><tr id="row-return-additionalCommittedItems-errorCount"><td>

&lt;String&gt;.additionalCommittedItems.errorCount

</td><td>

Number of errors encountered while processing this additional CI.Data type: Number

</td></tr><tr id="row-return-additionalCommittedItems-errors"><td>

&lt;String&gt;.additionalCommittedItems.errors

</td><td id="entry-errors">

Array of objects that describes errors encountered while processing this additional CI.Data type: Array

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr id="row-return-additionalCommittedItems-errors-error"><td>

&lt;String&gt;.additionalCommittedItems.errors.error

</td><td id="entry-errors-error">

Type of error encountered while processing the additional CI.Data type: String

</td></tr><tr id="row-return-additionalCommittedItems-errors-message"><td>

&lt;String&gt;.additionalCommittedItems.errors.message

</td><td id="entry-errors-message">

Error message encountered while processing the additional CI.Data type: String

</td></tr><tr id="row-return-additionalCommittedItems-identificationAttempts"><td>

&lt;String&gt;.additionalCommittedItems.identificationAttempts

</td><td id="addCommItems_identificationAttempts-entry-IRE">

Array of objects in which each object describes an attempt made to identify this additional CI.Data type: Array of Objects

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

</td></tr><tr id="row-return-additionalCommittedItems-identificationAttempts-attemptResult"><td>

&lt;String&gt;.additionalCommittedItems.identificationAttempts.attemptResult

</td><td id="addCommItems_idAtt_attemptResult-entry-IRE">

Outcome of this additional CI identification attempt.Data type: String

Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

</td></tr><tr id="row-return-additionalCommittedItems-identificationAttempts-attributes"><td>

&lt;String&gt;.additionalCommittedItems.identificationAttempts.attributes

</td><td id="addCommItems_idAtt_attributes-entry-IRE">

CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr id="row-return-additionalCommittedItems-identificationAttempts-hybrid"><td>

&lt;String&gt;.additionalCommittedItems.identificationAttempts.hybridEntryCiAttributes

</td><td id="addCommItems_idAtt_hybridEntryCIAtt-entry-IRE">

Array of CI identifier entry attributes used during this additional CI identification attempt.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr id="row-return-additionalCommittedItems-identificationAttempts-identifierName"><td>

&lt;String&gt;.additionalCommittedItems.identificationAttempts.identifierName

</td><td id="addCommItems_idAtt_identifierName-entry-IRE">

Identifier rule used for this additional CI identification attempt.Data type: String

</td></tr><tr id="row-return-additionalCommittedItems-identificationAttempts-searchOnTable"><td>

&lt;String&gt;.additionalCommittedItems.identificationAttempts.searchOnTable

</td><td id="addCommItems_identifierEntrySysId-entry-IRE">

Name of the table searched for this additional CI identification attempt.Data type: String

</td></tr><tr id="row-return-additionalCommittedItems-identifierEntrySysId"><td>

&lt;String&gt;.additionalCommittedItems.identifierEntrySysId

</td><td id="addCommItems_identifierEntrySysId2-entry-IRE">

Sys\_id for the identifier rule used to identify this additional CI.Notable values - Unknown: Identification of this additional CI failed. See **errors** for details.

</td></tr><tr id="row-return-additionalCommittedItems-inputIndices"><td>

&lt;String&gt;.additionalCommittedItems.inputIndices

</td><td id="addCommItems_inputIndices-entry-IRE">

Index values for CIs from the request body **items** array that correspond to this additional CI.Data type: Array of Numbers

```
"inputIndices": [
  {
    Number
  }
]
```

</td></tr><tr id="row-return-additionalCommittedItems-markers"><td>

&lt;String&gt;.additionalCommittedItems.markers

</td><td id="addCommItems_markers-entry-IRE">

Marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr id="row-return-additionalCommittedItems-mergedPayloads"><td>

&lt;String&gt;.additionalCommittedItems.mergedPayloads

</td><td id="addCommItems_mergedPayloads-entry-IRE">

Sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged during processing of this additional CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr id="row-return-additionalCommittedItems-operation"><td>

&lt;String&gt;.additionalCommittedItems.operation

</td><td id="addCommItems_operation-entry-IRE">

Operation performed for this additional CI.Data type: String

Possible values:

-   DELETE: An existing CI is removed from the target table.
-   INSERT: The additional CI is inserted into the target table as a new record.
-   NO\_CHANGE: No operation is performed for the additional CI.
-   UPDATE: An existing CI in the target table is updated.
-   UPDATE\_WITH\_DOWNGRADE: An existing CI in the target table is updated and its class is changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: An existing CI in the target table is updated and its class is changed to another class which is not an ancestor or descendent class.
-   UPDATE\_WITH\_UPGRADE: An existing CI in the target table is updated and its class is changed to a more specialized class \(descendent class\).

</td></tr><tr id="row-return-additionalCommittedItems-sysId"><td>

&lt;String&gt;.additionalCommittedItems.sysId

</td><td id="addCommItems_sysId-entry-IRE">

Sys\_id found for this additional CI through identification.Data type: String

Notable values - Unknown: Identification of this additional CI failed. See **errors** for details.

</td></tr><tr id="row-return-additionalCommittedItems-warnings"><td>

&lt;String&gt;.additionalCommittedItems.warnings

</td><td id="addCommItems_warnings-entry-IRE">

Description of warnings encountered while processing this additional CI.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr id="row-return-additionalCommittedItems-warnings-error"><td>

&lt;String&gt;.additionalCommittedItems.warnings.error

</td><td id="addCommItems_warnings_error-entry-IRE">

Type of warning encountered while processing this additional CI.Data type: String

</td></tr><tr id="row-return-additionalCommittedItems-warnings-message"><td>

&lt;String&gt;.additionalCommittedItems.warnings.message

</td><td id="addCommItems_warnings_message-entry-IRE">

Warning message encountered while processing this additional CI.Data type: String

</td></tr><tr id="row_return_additionalCommittedRelations"><td>

&lt;String&gt;.additionalCommittedRelations

</td><td id="entry_return_additionalCommittedRelations">

Description of a dependent relationship CI that was not included in the request body **relations** list to insert or update.Data type: Array of Objects

```
"additionalCommittedRelations": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String"
  }
]
```

</td></tr><tr id="row_return_additionalCommittedRelations-className"><td>

&lt;String&gt;.additionalCommittedRelations.className

</td><td id="addCommRel_className-entry-IRE">

The sys\_class\_name of this additional dependent relationship CI.Data type: String

Only supported value: cmdb\_rel\_ci: The CI Relationship table.

</td></tr><tr id="row_return_additionalCommittedRelations-errorCount"><td>

&lt;String&gt;.additionalCommittedRelations.errorCount

</td><td id="addCommRel_errorCount-entry-IRE">

Number of errors encountered while processing this additional dependent relationship CI.Data type: Number

</td></tr><tr id="row_return_additionalCommittedRelations-errors"><td>

&lt;String&gt;.additionalCommittedRelations.errors

</td><td id="addCommRel_errors-entry-IRE">

Description of the errors encountered while processing this additional dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr id="row_return_additionalCommittedRelations-errors-error"><td>

&lt;String&gt;.additionalCommittedRelations.errors.error

</td><td id="addCommRel_errors_error-entry-IRE">

Type of error encountered while processing the additional dependent relationship CI.Data type: String

</td></tr><tr id="row_return_additionalCommittedRelations-errors-message"><td>

&lt;String&gt;.additionalCommittedRelations.errors.message

</td><td id="addCommRel_errors_message-entry-IRE">

Error message encountered while processing this additional dependent relationship CI.Data type: String

</td></tr><tr id="row_return_additionalCommittedRelations-inputIndices"><td>

&lt;String&gt;.additionalCommittedRelations.inputIndices

</td><td id="addCommRel_inputIndices-entry-IRE">

Index values for dependent relationship CI objects in the request body **relations** array that correspond to this additional dependent relationship CI.Data type: Array

```
"inputIndices": [
  Number
]
```

</td></tr><tr id="row_return_additionalCommittedRelations-markers"><td>

&lt;String&gt;.additionalCommittedRelations.markers

</td><td id="addCommRel_markers-entry-IRE">

Marker values for internal use.Data type: Array

```
"markers": []
```

</td></tr><tr id="row_return_additionalCommittedRelations-mergedPayloadIds"><td>

&lt;String&gt;.additionalCommittedRelations.mergedPayloadIds

</td><td id="addCommRel_mergedPayloadIds-IRE">

Sys\_id values for partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table that were merged for this CI.that were merged during processing of this additional dependent relationship CI.Data type: Array

```
"mergedPayloadIds": [
  "String"
]
```

</td></tr><tr id="row_return_additionalCommittedRelations-operation"><td>

&lt;String&gt;.additionalCommittedRelations.operation

</td><td id="addCommRel_operations-entry-IRE">

Operation that was performed for the additional dependent relationship CI.Possible values:

-   INSERT: The dependent relationship CI is inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and is inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and is inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation is performed for the dependent relationship CI.
-   UPDATE: An existing dependent relationship CI in the target table is updated.

Data type: String

</td></tr><tr id="row_return_hasError"><td>

&lt;String&gt;.hasError

</td><td id="entry_return_summary_class_name_hasError">

Flag that indicates whether any item or relation has errors.Data type: Boolean

</td></tr><tr id="row_return_hasWarning"><td>

&lt;String&gt;.hasWarning

</td><td id="entry_return_summary_class_name_hasWarning">

Flag that indicates whether any item or relation has warnings.Data type: Boolean

</td></tr><tr id="row_items_IEES"><td>

&lt;String&gt;.items

</td><td id="items-entry-IRE">

Description of the created or updated CIs.Data type: Array of Objects

```
"items": [
  {  
    "additionalRelatedItems": [Array],
    "className": "String",
    "duplicateIndices": [Array],
    "errorCount": Number, 
    "errors": [Array], 
    "identificationAttempts": [Array], 
    "identifierEntrySysId": "String",  
    "incompleteSysIds": "String",
    "info": [Array],
    "inputIndices": [Array], 
    "maskedAttributes": [Array],
    "operation": "String", 
    "partialSysIds": "String", 
    "relatedItems": [Array], 
    "relatedSysIds": [Array], 
    "sysId": "String" 
  }
]
```

</td></tr><tr id="row_return_item_additionalRelatedItems"><td>

&lt;String&gt;.items.additionalRelatedItems

</td><td id="entry_return_item_additionalRelatedItems">

Information about additional lookup and related items that were processed but not provided as part of the input payload. These items are from partial payloads.Data type: Array of Objects

```
"additionalRelatedItems": [ 
  {
    "className": "String", 
    "inputIndices": [Array],
    "mergedPayloadIds": [Array], 
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr id="row_return_item_additionalRelatedItems_className"><td>

&lt;String&gt;.items.additionalRelatedItems.className

</td><td id="items_addRelItems_className-entry-IRE">

Class/table name \(sys\_class\_name\) of the CI that was created or updated.Data type: String

</td></tr><tr id="row_return_item_additionalRelatedItems_inputIndices"><td>

&lt;String&gt;.items.additionalRelatedItems.inputIndices

</td><td id="items_addRelItems_inputIndices-entry-IRE">

Index values for CIs from the request body **items** array that correspond to this related item.Data type: Array of Numbers

</td></tr><tr id="row_return_item_additionalRelatedItems_mergedPayloadIds"><td>

&lt;String&gt;.items.additionalRelatedItems.mergedPayloadIds

</td><td id="entry_return_item_additionalRelatedItems_mergedPayloadIds">

List of sys\_ids of the partial payloads that were merged into the related item.Data type: Array

Table: CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\]

</td></tr><tr id="row_return_item_additionalRelatedItems_operations"><td>

&lt;String&gt;.items.additionalRelatedItems.operation

</td><td id="entry_return_item_additionalRelatedItems_operations">

Type of operation.Possible values:

-   INSERT: New CI was inserted into the database.
-   NO\_CHANGE: No CI changes were made.
-   UPDATE: Existing CI was updated.

Data type: String

</td></tr><tr id="row_return_item_additionalRelatedItems_sysId"><td>

&lt;String&gt;.items.additionalRelatedItems.sysId

</td><td id="items_addRelItems_sysId-entry-IRE">

Sys\_id of the CI that was updated or created.Data type: String

</td></tr><tr id="row_return_item_className"><td>

&lt;String&gt;.items.className

</td><td id="entry_return_item_className">

Class/table name \(sys\_class\_name\) of the CI that was created or updated.Data type: String

</td></tr><tr id="row_return_items_duplicateIndices"><td>

&lt;String&gt;.items.duplicateIndices

</td><td id="entry_return_items_duplicateIndices">

List of indexes of CIs that are duplicates of the current item.Data type: Array

</td></tr><tr id="row_return_item_errorCount"><td>

&lt;String&gt;.items.errorCount

</td><td id="entry_return_item_errorCount">

Number of errors encountered while processing the item.Data type: Number

</td></tr><tr id="row_return_item_error"><td>

&lt;String&gt;.items.errors

</td><td id="entry_return_item_error">

List of errors encountered while processing this CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr id="row_return_item_errors-error"><td>

&lt;String&gt;.items.errors.error

</td><td id="items_errors_errors-entry-IRE">

Type of error encountered while processing the CI.Data type: String

</td></tr><tr id="row_return_item_errors-message"><td>

&lt;String&gt;.items.errors.message

</td><td id="items_errors_msg-entry-IRE">

Error message associated with the error.Data type: String

</td></tr><tr id="row_return_item_identificationAttempts"><td>

&lt;String&gt;.items.identificationAttempts

</td><td id="entry_return_item_identificationAttempts">

List of attempts that were made to identify the CIs.Data type: Array of Objects

```
"identificationAttempts": [
  { 
    "attemptResult": "String", 
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identifierName": "String",
    "searchOnTable": "String" 
  }
]
```

</td></tr><tr id="row_return_item_identificationAttempts_attemptResult"><td>

&lt;String&gt;.items.identificationAttempts.attemptResult

</td><td id="entry_return_item_identificationAttempts_attemptResult">

Results of the attempt to identify the CI.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr id="row_return_item_identificationAttempts_attributes"><td>

&lt;String&gt;.items.identificationAttempts.attributes

</td><td id="entry_return_item_identificationAttempts_attributes">

List of CI identifier entry attributes that were used during the identification process.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

&lt;String&gt;items.identificationAttempts.hybridEntryCiAttributes

</td><td id="items_identAtt_hyEntCiAtt-IRE">

List of CI identifier entry attributes that were used during the identification process.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"hybridEntryCiAttributes": [
  "name": "String",
  "serial_number": "String"
]
```

</td></tr><tr id="row_return_item_identificationAttempts_identifierName"><td>

&lt;String&gt;.items.identificationAttempts.identifierName

</td><td id="entry_return_item_identificationAttempts_identifierName">

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr id="row_return_item_identificationAttempts_searchOnTable"><td>

&lt;String&gt;.items.identificationAttempts.searchOnTable

</td><td id="entry_return_item_identificationAttempts_searchOnTable">

Name of the table searched during the identification process.Data type: String

</td></tr><tr id="row_return_item_identifierEntrySysId"><td>

&lt;String&gt;.items.identifierEntrySysId

</td><td id="entry_return_item_identifierEntrySysId">

Sys\_id for the identifier rule used to identify the CI.Data type: String

Table: Identifier Entry \[cmdb\_identifier\_entry\]

</td></tr><tr id="row_return_item_incompleteSysId"><td>

&lt;String&gt;.items.incompleteSysIds

</td><td id="entry_return_item_incompleteSysId">

If the item had errors and was saved as an incomplete payload, this parameter contains the sys\_id of the record in the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info

</td><td id="items_info-entry-IRE">

Additional information about the processing of the item.Data type: Array of Objects

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

&lt;String&gt;.items.info.code

</td><td id="items_info_code-entry-IRE">

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_UPGRADE

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info.message

</td><td id="items_info_message-entry-IRE">

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info.ruleSysId

</td><td id="items_info_ruleSysId-entry-IRE">

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr id="row_return_items_inputIndices"><td>

&lt;String&gt;.items.inputIndices

</td><td id="entry_return_items_inputIndices">

Indexes of the corresponding input CI. For top-level items, it is a list of integers. For related or lookup CIs, it is list of JSON objects.Data type: Array of Numbers

</td></tr><tr id="row_return_item_maskedAttributes"><td>

&lt;String&gt;.items.maskedAttributes

</td><td id="entry_return_item_maskedAttributes">

List of attributes whose update by a non-authoritative data source was skipped as defined by the Reconciliation Rules.Data type: Array

</td></tr><tr id="row_return_item_operation"><td>

&lt;String&gt;.items.operation

</td><td id="entry_return_item_operation">

Operation that took place.Possible values:

-   INSERT: New CI was inserted into the database.
-   INSERT\_AS\_INCOMPLETE: Item was saved in cmdb\_ire\_incomplete\_payloads table.
-   INSERT\_AS\_PARTIAL: Item was saved in cmdb\_ire\_partial\_payloads table.
-   UPDATE: Existing CI was updated.
-   UPDATE\_WITH\_DOWNGRADE: CI was updated and the class changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: CI was updated and the class changed to a class that is not ancestor or descendent.
-   UPDATE\_WITH\_UPDRADE: CI was updated and the class changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr id="row_return_item_partialSysId"><td>

&lt;String&gt;.items.partialSysIds

</td><td id="entry_return_item_partialSysId">

If the item had errors and was saved as a partial payload, this parameter contains the sys\_id of the partial payload record. Data type: String

</td></tr><tr id="row_return_item_relatedItems"><td>

&lt;String&gt;.items.relatedItems

</td><td id="entry_return_item_relatedItems">

List of JSON objects that describe a related CI \(table lookup CI\) from the request body **items.lookup** array.Data type: Array of Objects

```
"relatedItems": [
  { 
    "className": "String",
    "errors": [Array],
    "errorCount": Number, 
    "incompleteSysIds": [Array],
    "inputIndices": [Array],
    "mergePayloadIds": [Array],
    "operation": "String",
    "partialSysIds": [Array], 
    "sysId": "String",
    "warningCount": Number,
    "warnings": [Array]
  }
]
```

</td></tr><tr id="row_return_item_relatedItems_className"><td>

&lt;String&gt;.items.relatedItems.className

</td><td>

Class/table name \(sys\_class\_name\) of the related item.Data type: String

</td></tr><tr id="row_return_item_relatedItems_errors"><td>

&lt;String&gt;.items.relatedItems.errors

</td><td id="entry_return_item_relatedItems_errors">

List of errors that occurred during processing of the related item.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr id="row_return_item_relatedItems_errors_error"><td>

&lt;String&gt;.items.relatedItems.errors.error

</td><td>

Type of error encountered while processing the related item.Data type: String

</td></tr><tr id="row_return_item_relatedItems_errors-message"><td>

&lt;String&gt;.items.relatedItems.errors.message

</td><td>

Error message associated with the error.Data type: String

</td></tr><tr id="row_return_item_relatedItems_errorCount"><td>

&lt;String&gt;.items.relatedItems.errorCount

</td><td id="entry_return_item_relatedItems_errorCount">

Number of errors detected while processing the related items.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.incompleteSysIds

</td><td>

If the relation had errors and was saved as an incomplete payload, this value is the sys\_id of the record in the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.Data type: String

</td></tr><tr id="row_return_item_relatedItems_inputIndices"><td>

&lt;String&gt;.items.relatedItems.inputIndices

</td><td id="entry_return_item_relatedItems_inputIndices">

Index of the corresponding input item. For top-level items, it is a list of integers. For related or lookup items, it is list of JSON objects.Data type: Array of Numbers or Array of Objects

```
"inputIndices": [
  { 
   "mainIndex": Number, 
   "subIndex": Number 
  }
]
```

</td></tr><tr id="row_return_item_relatedItems_inputIndices_mainIndex"><td>

&lt;String&gt;.items.relatedItems.inputIndices.mainIndex

</td><td id="entry_return_item_relatedItems_inputIndices.mainIndex">

Index value from the request body **items** array that corresponds to the CI parent of the related item. Data type: Number

</td></tr><tr id="row_return_item_relatedItems_inputIndices_subIndex"><td>

&lt;String&gt;.items.relatedItems.inputIndices.subIndex

</td><td id="entry_return_item_relatedItems_inputIndices.subIndex">

Index value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr id="row_return_item_relatedItems_mergedPayloadIds"><td>

&lt;String&gt;.items.relatedItems.mergedPayloadIds

</td><td>

List of sys\_ids of the partial payloads that were merged into the CI during processing.Data type: Array

</td></tr><tr id="row_return_item_relatedItems_operation"><td>

&lt;String&gt;.items.relatedItems.operation

</td><td>

Operation that took place.Possible values:

-   INSERT: New related CI was inserted into the database.
-   INSERT\_AS\_INCOMPLETE: Item was saved in cmdb\_ire\_incomplete\_payloads table.
-   INSERT\_AS\_PARTIAL: Item was saved in cmdb\_ire\_partial\_payloads table.
-   NO\_CHANGE: No related CI changes were made.
-   UPDATE: Existing related CI was updated.
-   UPDATE\_WITH\_DOWNGRADE: Related CI was updated and the class changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: Related CI was updated and the class changed to a class that is not ancestor or descendent.
-   UPDATE\_WITH\_UPDRADE: Related CI was updated and the class changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.partialSysIds

</td><td>

If the related item had errors and was saved as a partial payload, this contains a list of the sys\_ids of the associated records in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.Data type: Array

</td></tr><tr id="row_return_item_relatedItems_sysId"><td>

&lt;String&gt;.items.relatedItems.sysId

</td><td>

Sys\_id of the related item.Data type: String

</td></tr><tr id="row_return_item_relatedItems_warningCount"><td>

&lt;String&gt;.items.relatedItems.warningCount

</td><td>

Number of warnings encountered when processing the related items.Data type: Number

</td></tr><tr id="row_return_item_relatedItems_wrnings"><td>

&lt;String&gt;.items.relatedItems.warnings

</td><td>

Description of warnings encountered while processing the related items.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.warnings.error

</td><td>

Type of warning encountered while processing the related item.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.warnings.message

</td><td>

Message associated with the warning.Data type: String

</td></tr><tr id="row_return_item_relatedSysIds"><td>

&lt;String&gt;.items.relatedSysIds

</td><td id="entry_return_item_relatedSysIds">

List of the sys\_id values of the CIs used during lookup-based identification of related items.Data type: String

</td></tr><tr id="row_return_item_sys_id"><td>

&lt;String&gt;.items.sys\_id

</td><td id="entry_return_item_sys_id">

Sys\_id of the CI that was updated or created.Data type: String

</td></tr><tr id="row_return_relations"><td>

&lt;String&gt;.relations

</td><td id="entry_return_relations">

Description of a dependent relationship CI from the request body **relations** array.Data type: Array of Objects

```
"relations": [ 
  { 
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "incompleteSysIds": "String",
    "inputIndices": [Array],
    "operation": "String",
    "partialSysIds": "String",
    "sysId": "String" 
  }
]
```

</td></tr><tr id="row_return_relations_className"><td>

&lt;String&gt;.relations.className

</td><td id="entry_return_relations_className">

Sys\_class\_name of this dependent relationship CI.Only supported value: cmdb\_rel\_ci: CI Relationship table.

Data type: String

</td></tr><tr id="row_return_relations_errorsCount"><td>

&lt;String&gt;.relations.errorCount

</td><td id="entry_return_relations_errorsCount">

Number of errors encountered when processing the dependent relationship CI.Data type: Number

</td></tr><tr id="row_return_relations_errors"><td>

&lt;String&gt;.relations.errors

</td><td id="entry_return_relations_errors">

List that describes errors that were encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.relations.errors.error

</td><td>

Type of error encountered while processing the dependent relationship CI.Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations.errors.message

</td><td>

Error message encountered while processing this dependent relationship CI.Data type: String

</td></tr><tr id="row_return_relations_incompleteSysId"><td>

&lt;String&gt;.relations.incompleteSysIds

</td><td id="entry_return_relations_incompleteSysId">

If the relation had errors and was saved as an incomplete payload, this value is the sys\_id of the record in the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.Data type: String

</td></tr><tr id="row_return_relations_inputIndices"><td>

&lt;String&gt;.relations.inputIndices

</td><td id="entry_return_relations_inputIndices">

Indexes for the dependent relationship CI objects in the request body **relations** array that correspond to this dependent relationship CI.Data type: Array

</td></tr><tr id="row_return_relations_operation"><td>

&lt;String&gt;.relations.operation

</td><td id="entry_return_relations_operation">

Type of operation performed.Possible values:

-   INSERT: The dependent relationship CI was inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and was inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and was inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation was performed.
-   UPDATE: An existing dependent relationship CI in the target table was updated.

Data type: String

</td></tr><tr id="row_return_relations_partialSysId"><td>

&lt;String&gt;.relations.partialSysIds

</td><td id="entry_return_relations_partialSysId">

If the relation had errors and was saved as a partial payload, this value is the sys\_id of the record in the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.Data type: String

</td></tr><tr id="row_return_relations_sys_id"><td>

&lt;String&gt;.relations.sysId

</td><td id="entry_return_relations_sys_id">

Sys\_id of the dependent relationship CI.Data type: String

</td></tr><tr id="row_return_summary"><td>

&lt;String&gt;.summary

</td><td id="entry_return_summary">

List of JSON properties that provide statistics on how many items were inserted, updated, and such, per class.Data type: Array

</td></tr><tr id="row_return_summary_class_name"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;

</td><td id="entry_return_summary_class_name">

Statistics for a specific class.Data type: Object

```
<class_name>: {
 "additionalInsertedItemCount": Number, 
 "errorCount": Number,
 "incompleteItemCount": Number,
 "insertedItemCount": Number,
 "partialItemCount": Number,
 "skippedItemCount": Number,
 "unchangedItemCount": Number,
 "updatedItemCount": Number,
 "warningCount": Number 
}
```

</td></tr><tr id="row_return_summary_class_name_additionalInsertedItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.additionalInsertedItemCount

</td><td id="entry_return_summary_class_name_additionalInsertedItemCount">

Number of items inserted due to processing of partial payloads.Data type: Number

</td></tr><tr id="row_return_summary_class_name_errorCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.errorCount

</td><td id="entry_return_summary_class_name_errorCount">

Number of errors encounter when processing items.Data type: Number

</td></tr><tr id="row_return_summary_class_name_incompleteItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.incompleteItemCount

</td><td id="entry_return_summary_class_name_incompleteItemCount">

Number of items inserted in the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.Data type: Number

</td></tr><tr id="row_return_summary_class_name_insertedItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.insertedItemCount

</td><td id="entry_return_summary_class_name_insertedItemCount">

Number of items created.Data type: Number

</td></tr><tr id="row_return_summary_class_name_partialItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.partialItemCount

</td><td id="entry_return_summary_class_name_partialItemCount">

Number of items saved in the Partial Payload table \[cmdb\_ire\_partial\_payloads\].Data type: Number

</td></tr><tr id="row_return_summary_class_name_skippedItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.skippedItemCount

</td><td>

Number of items that were skipped.Data type: Number

</td></tr><tr id="row_return_summary_class_name_unchangedItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.unchangedItemCount

</td><td id="entry_return_summary_class_name_unchangedItemCount">

Number of items that had entries but were not modified.Data type: Number

</td></tr><tr id="row_return_summary_class_name_updatedItemCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.updatedItemCount

</td><td id="entry_return_summary_class_name_updatedItemCount">

Number of items updated.Data type: Number

</td></tr><tr id="row_return_summary_class_name_warningCount"><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.warningCount

</td><td id="entry_return_summary_class_name_warningCount">

Number of items that generated a warning when processed.Data type: Number

</td></tr></tbody>
</table>This example shows how to import multiple CI entries.

```
var payload = {
"items": [
{
 "className": "cmdb_ci_win_server", 
 "values": {
   "chassis_type": "Desktop",
   "os": "Windows 2012 R2 Datacenter",
   "name": "Windows2012Server1",
   "serial_number": "0000-0011-1690-8730-8636-5722-52",
   "cpu_count": "1"
  },
  "lookup": [
  {
     "values": {
       "valid": "true",
       "serial_number": "0000-0011-1690-8730-8636-5722-52",
       "serial_number_type": "bios"
      },
     "className": "cmdb_serial_number"
   },
   {
     "values": {
       "valid": "true",
       "serial_number": "3311-9736-4988-9744-1749-4183-41",
       "serial_number_type": "chassis"
      },
     "className": "cmdb_serial_number"
   }],

    "internal_id": "16777219",
    "sys_object_source_info": {
      "source_feed": "SN Discovery Feed 1",
      "source_name": "ServiceNow",
      "source_native_key": "16777219",
      "source_recency_timestamp": "2019-10-18 08:31:23"
   }},
   {  
   "className": "cmdb_ci_spkg",
   "values": {
     "name": "Windows 2012 R2 Datacenter",
     "key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL"
     },

  "related": [
    {
      "internal_id": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219",
      "values": {
        "name": "Windows 2012 R2 Datacenter-SAMLABVM52"
      },
      "className": "cmdb_software_instance",
      "sys_object_source_info": {
        "source_feed": "SN Discovery Feed 1",
        "source_name": "ServiceNow",
        "source_native_key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219"
  }}], 
  "settings" : {
        "skipReclassificationRestrictionRules" : "false",
        "updateWithoutDowngrade" : "true",
        "updateWithoutUpgrade" : "true",
        "updateWithoutSwitch" : "true"
      }}, 
  {
  "className": "cmdb_ci_app_server_tomcat",
  "values": {
    "running_process_key_parameters": "/opt/OV/nonOV/tomcat/b/temp org.apache.catalina.startup.Bootstrap start",
    "install_directory": "/opt/OV/nonOV/tomcat/b",
    "name": "Tomcat@hpom9:3443",
    "server_port": "8006",
    "sys_class_name": "cmdb_ci_app_server_tomcat"
  },

  "internal_id": "tomcat_id"
  }],

"relations": [
  {
    "parent_id": "tomcat_id",
    "child_id": "16777219",
    "type": "Runs on::Runs"
  }],

"referenceItems": [
  {
    "referenceField": "installed_on",
    "referenced": "16777219",
    "referencedBy": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219"
  }]};

var input = JSON.stringify((payload));
var output = sn_cmdb.IdentificationEngine.createOrUpdateCIEnhanced('ServiceNow', input, {});

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{

"items": [
{
  "className": "cmdb_ci_win_server",
  "operation": "NO_CHANGE",
  "sysId": "65d873d2b3a0001028f6eae2c6a8dc2a",
  "relatedSysIds": [
    "a1d873d2b3a0001028f6eae2c6a8dc32",
    "a1d873d2b3a0001028f6eae2c6a8dc33"
],

"relatedItems": [
{
  "className": "cmdb_serial_number",
  "sysId": "a1d873d2b3a0001028f6eae2c6a8dc32",
  "markers": [],
  "inputIndices": [
  {
    "mainIndex": 0,
    "subIndex": 0
  }]
},
  "className": "cmdb_serial_number",
  "sysId": "a1d873d2b3a0001028f6eae2c6a8dc33",
  "markers": [],
  "inputIndices": [
  {
    "mainIndex": 0,
    "subIndex": 1
  }]
}],

"additionalRelatedItems": [],
"identificationAttempts": [],
"errorCount": 0,
"inputIndices": [0]
},
{
"className": "cmdb_ci_spkg",
"operation": "NO_CHANGE",
"sysId": "c764e971b320001028f6eae2c6a8dc44",

"relatedSysIds": [
  "8b64e971b320001028f6eae2c6a8dc47"
],
"relatedItems": [
  {
  "className": "cmdb_software_instance",
  "sysId": "8b64e971b320001028f6eae2c6a8dc47",
  "markers": [],
  "inputIndices": [
    {
      "mainIndex": 1,
      "subIndex": 0
    }]
  }],

"additionalRelatedItems": [],
"identifierEntrySysId": "a52a87c03746220006b216a543990e8c",
"identificationAttempts": [
  {
    "attributes": [
      "key"
     ],
    "identifierName": "Software",
    "attemptResult": "MATCHED",
    "searchOnTable": "cmdb_ci_spkg",
    "hybridEntryCiAttributes": []
  }],

"errorCount": 0,
"inputIndices": [1]
},

{
"className": "cmdb_ci_app_server_tomcat",
"operation": "INSERT",
"sysId": "6f29f3d2b3a0001028f6eae2c6a8dcc6",
"identifierEntrySysId": "Unknown",
"identificationAttempts": [
{
  "attributes": [
    "install_directory",
    "running_process_key_parameters",
    "sys_class_name"
  ],
"identifierName": "Tomcat",
"attemptResult": "NO_MATCH",
"searchOnTable": "cmdb_ci_app_server_tomcat",
"hybridEntryCiAttributes": []
},
{
"attributes": [
  "cl_port",
  "sys_class_name"
],
"identifierName": "Application Rule",
"attemptResult": "SKIPPED",
"searchOnTable": "cmdb_ci_appl",
"hybridEntryCiAttributes": []
},
{
"attributes": [
  "running_process_command",
  "running_process_key_parameters",
  "sys_class_name"
],
"identifierName": "Application Rule",
"attemptResult": "NO_MATCH",
"searchOnTable": "cmdb_ci_appl",
"hybridEntryCiAttributes": []
}
],

"errorCount": 0,
"inputIndices": [2]
}
],
"additionalCommittedItems": [],
"relations": [
{
  "className": "cmdb_rel_ci",
  "operation": "INSERT",
  "sysId": "6729f3d2b3a0001028f6eae2c6a8dcc9",
  "errorCount": 0,
  "inputIndices": [0]
}],
"additionalCommittedRelations": []
}
```

## IdentificationEngine - identifyCI\(String jsonString\)

Determines the operation \(insert/update\) to perform with the specified payload without committing the operation in the database.

This works just like createOrUpdateCI\(\), but does not commit the result.

<table id="id_mqd_n1t_pyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

jsonString

</td><td>

String

</td><td>

A JSON formatted string of configuration items to be added or updated. Each input string is in the format  'items: \[\{\}\], relations:\[\{\}\]', where each item within the items and relations lists contains name-value pairs. The possible name-value pairs within the items list are:

-   className: Sys\_class\_name of the CI to be created or updated.
-   lookup:\[\{\}\]: List of records with each item having name-value pairs like the items list.
-   values:\{\}: Field information for the CI as name-value pairs, where the name is the field name.

Possible name-value pairs within the relations list are:

-   child: Index of the child item in the dependency relation
-   parent: Index of the parent item in the dependency relation
-   type: Relationship type. This is one of the name field values from the cmdb\_rel\_type table.

</td></tr></tbody>
</table><table id="id_vn1_51t_pyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formatted string that is a list of results. Each result string is in the format  'items: \[\{\}\], relations:\[\{\}\]', where each item within the items and relations lists contains name-value pairs. The possible name-value pairs within the items list are:

-   className: Sys\_class\_name for the CI that was updated or created.
-   duplicateIndices: List of indexes of items that are duplicates of the current item.
-   errors: List of errors in the format of \(error, message string\)
-   identificationAttempts: List of attempts.
    -   attemptResult: One of SKIPPED, NO\_MATCH, MATCHED, MULTI\_MATCH.
    -   attributes: Attributes of identifier entry used during identification.
    -   identiferName: CI identifier to which this identifier entry belongs.
    -   searchOnTable: Table searched during the identification process.
-   identifierEntrySysId: Sys\_id of identifier entry used during matching.
-   operation: Operation to perform, which is one of the following:
    -   DELETE
    -   INSERT
    -   UPDATE
    -   UPDATE\_WITH\_DOWNGRADE
    -   UPDATE\_WITH\_SWITCH
    -   UPDATE\_WITH\_UPGRADE
-   relatedSysIds: List of sys\_id values of CIs used during lookup based identification.
-   sysId: Sys\_id of the CI that was updated or created.

Possible name-value pairs within the relations list are:

-   className: Relationship CI's class name and is always cmdb\_rel\_ci
-   operation: Type of operation: INSERT, UPDATE, NO\_CHANGE
-   sysId: Sys\_id of the relationship CI inserted or updated

</td></tr></tbody>
</table>The following shows how to reclassify a configuration item.

```
var payload = {
  "items": [
    {
      "className": "cmdb_ci_win_server",
      "values": {
        "short_description": "Linux server description",
        "name": "Linux Server 1"
      }
    }
  ]
};

var input = JSON.stringify(payload);
var output = sn_cmdb.IdentificationEngine.identifyCI(input);

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{
  "items": [
    {
      "className": "cmdb_ci_linux_server",
      "operation": "NO_CHANGE",
      "sysId": "440577800f321010150efc91ff767e94",
      "identifierEntrySysId": "556eb250c3400200d8d4bea192d3ae92",
      "identificationAttempts": [
        {
          "attributes": [],
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "serial_number",
            "serial_number_type"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "searchOnTable": "cmdb_serial_number",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "serial_number"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "name"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "MATCHED",
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        }
      ],
      "info": [
        {
          "message": "CI Reclassification not allowed from class: [cmdb_ci_linux_server] to [cmdb_ci_win_server] by a reclassification restriction rule",
          "code": "SKIPPED_CLASS_SWITCH",
          "ruleSysId": "b3d4b3800f321010150efc91ff767eab"
        }
      ],
      "errorCount": 0,
      "warningCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ],
      "mergedPayloadIds": []
    }
  ],
  "additionalCommittedItems": [],
  "relations": [],
  "additionalCommittedRelations": []
}
```

## IdentificationEngine - identifyCIEnhanced\(String source, String input, Object options\)

Determines the Configuration Management Database \(CMDB\) operation \(insert/update\) to perform with the specified payload \(request body\), without committing the operations in the database.

Use this method to simulate submission of a payload.

This method is similar to the [IdentificationEngine - identifyCI\(String jsonString\)](IdentificationEngineScopedAPI.md#) method, however it also supports the following functionality:

-   Partial payloads
    -   In case of an item having a warning or error, indicates if an item operation is INSERT\_AS\_PARTIAL or INSERT\_INCOMPLETE.
    -   Returns the sys\_ids of partial payloads that were merged with existing partial payloads.
-   Supports payload deduplicate feature.
-   Generates a summary.

<table id="table_lqf_msb_jlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="row_input"><td>

input

</td><td>

String

</td><td id="entry_input">

Required. Input payload. A JSON formatted string of configuration items to add or update. ```
"input" { 
 "items": [Array],
 "referenceItems": [Array],
 "relations": [Array]
}
```

</td></tr><tr id="row_items"><td>

input.items

</td><td>

Array of Objects

</td><td id="entry_items">

Items to add or update.```
"items": [
  { 
    "className": "String",
    "display_values": {Object},
    "internal_id": "String",
    "lookup": [Array],
    "related": [Array],
    "settings": {Object},
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr id="row_className"><td>

input.items.className

</td><td>

String

</td><td id="entry_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_ci\_linux\_server or cmdb\_ci\_win\_server.

</td></tr><tr id="row-display_values-ire"><td>

input.items.display\_values

</td><td id="entry-display_values-ire">

Object

</td><td>

Reference fields to create or update for this related item as name-value pairs, where the name is the field name and the value is the referenced display value. If you want to use the sys\_id instead of the display value for reference fields, pass the information in the **input.items.lookup.values** parameter instead of in this parameter.Reference field names depend on the fields selected by the user, such as:

 ```
"display_values": {
  "model_id": "String",
  "location": "String"
}
```

</td></tr><tr id="row_internal_id"><td>

input.items.internal\_id

</td><td>

String

</td><td id="entry_internal_id">

Unique item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr id="row_lookup"><td>

input.items.lookup

</td><td>

Array of Objects

</td><td id="entry_lookup">

Identifies the top-level item containing the lookup \(lookup-based identification\). These records are used to identify the configuration item based on a lookup table that has a reference back to cmdb\_ci.For example:

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

</td></tr><tr id="row-input_items_lookup_className"><td>

input.items.lookup.className

</td><td>

String

</td><td id="entry-input_items_lookup_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_serial\_number or cmdb\_ci\_network\_adapter.

</td></tr><tr><td>

input.items.lookup.internal\_id

</td><td>

String

</td><td>

Unique lookup item identifier for the associated payload.This can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info

</td><td>

Object

</td><td>

Defines a unique CI identifier for a specific data source. Different sources may have different name-value pairs for the same CI.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key-id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.lookup.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date/time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr><td>

input.items.lookup.values

</td><td>

Object

</td><td>

Field information for the CI as name-value pairs, where the name is the field name. When updating reference fields, the value must be the referenced sys\_id.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "serial_number": "String",
  "serial_number_type": "String",
  "valid": "String",
  "ip_address": "String",
  "mac_address": "String"
}
```

</td></tr><tr id="row_related"><td>

input.items.related

</td><td>

Array of Objects

</td><td id="entry_related">

Reference to the top-level item that contains the related list. Rules in the Related Entry \[cmdb\_related\_entry\] define what type of records can be in this array. These records are used to add items based on a related table that has a reference to the CI that is being identified. The related table may or may not extend cmdb\_ci. These records are not used to identify the configuration item.

```
"related" [
  {
    "className": "String",
    "internal_id": "String",
    "sys_object_source_info": {Object},
    "values": {Object}
  }
]
```

</td></tr><tr><td>

input.items.related.className

</td><td>

String

</td><td id="entry-input_items_related_className">

Required. Class/table name, sys\_class\_name, of the configuration item \(CI\) to create or update.This value can be any CMDB class/table, such as cmdb\_software\_instance or cmdb\_key\_value.

</td></tr><tr><td>

input.items.related.internal\_id

</td><td>

String

</td><td>

Unique identifier for this related item in this payload. Can be any value, but must be unique within the payload.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info

</td><td>

Object

</td><td>

Object that makes up a unique CI identifier for a specified data source. Different sources may have different name-value pairs for the same CI.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td>

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td>

Identifies the data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td>

Unique key/ID from the source for the related item. The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr><td>

input.items.related.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td>

UTC date and time that the item was scanned.Format: `YYYY-MM-DD hh:mm:ss`

</td></tr><tr><td>

input.items.related.values

</td><td>

Object

</td><td>

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr id="row_items_settings"><td>

input.items.settings

</td><td>

Object

</td><td id="entry_items_settings">

Parameters that define the types of updates that are permitted.```
"settings": { 
  "skipReclassificationRestrictionRules": Boolean, 
  "updateWithoutDowngrade": Boolean, 
  "updateWithoutSwitch": Boolean,
  "updateWithoutUpgrade": Boolean
}
```

</td></tr><tr id="items_set_skipReclassRestrictRules-row-IRE"><td>

input.items.settings.skipReclassificationRestrictionRules

</td><td>

Boolean

</td><td id="items_set_skipReclassRestrictRules-entry-IRE">

Flag that indicates whether IRE should not run the Reclassification Restriction rule that matches the class for the payload item.Valid values:

-   true: Skip running the rule.
-   false: Run the rule.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutDowngrade"><td>

input.items.settings.updateWithoutDowngrade

</td><td>

Boolean

</td><td id="entry_items_settings_updateWithoutDowngrade">

Flag that indicates whether update and downgrade are both permitted for this item.Valid values:

-   true: Update the item but downgrade is not permitted.
-   false: Both item update and downgrade are permitted.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutSwitch"><td>

input.items.settings.updateWithoutSwitch

</td><td>

Boolean

</td><td id="entry_items_settings_updateWithoutSwitch">

Flag that indicates whether the item can be updated and the class switched.Valid values:

-   true: Update the item but class switching is not permitted.
-   false: Both item update and class switching are permitted.

Default: false

</td></tr><tr id="row_items_settings_updateWithoutUpgrade"><td>

input.items.settings.updateWithoutUpgrade

</td><td>

Boolean

</td><td id="entry_items_settings_updateWithoutUpgrade">

Flag that indicates whether update and upgrade are both permitted for this item.Valid values:

-   true: Update the item but upgrade is not permitted.
-   false: Both item update and upgrade are permitted.

Default: false

</td></tr><tr id="row_items_sys_object_source_info"><td>

input.items.sys\_object\_source\_info

</td><td>

Object

</td><td id="entry_items_sys_object_source_info">

Unique CI identifier for a specific source.```
"sys_object_source_info": { 
  "source_feed": "String",
  "source_name": "String",  
  "source_native_key": "String",
  "source_recency_timestamp": "String"
} 
```

</td></tr><tr id="row_items_sys_object_source_info_source_feed"><td>

input.items.sys\_object\_source\_info.source\_feed

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_feed">

If the source can have multiple feeds, use this field to provide the name of the feed sending this item.The data source generates this feed name. It can be any string that uniquely identifies the source feed.

</td></tr><tr id="row_items_sys_object_source_info_source_name"><td>

input.items.sys\_object\_source\_info.source\_name

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_name">

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr><tr id="row_items_sys_object_source_info_source_native_key"><td>

input.items.sys\_object\_source\_info.source\_native\_key

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_native_key">

Unique key/id for the item from the source.The data source generates this key. It can be any string that is unique to the item.

</td></tr><tr id="row_items_sys_object_source_info_source_recency_timestamp"><td>

input.items.sys\_object\_source\_info.source\_recency\_timestamp

</td><td>

String

</td><td id="entry_items_sys_object_source_info_source_recency_timestamp">

UTC date and time that the item was scanned.Format: YYYY-MM-DD hh:mm:ss

</td></tr><tr id="row_values"><td>

input.items.values

</td><td>

Object

</td><td id="entry_values">

Fields to create or update for this related item as name/value pairs, where the name is the field name. For a reference field, the value must be the referenced sys\_id. If you want to use the display value instead of the sys\_id for reference fields, pass this information in a **display\_values** object instead of in the **values** object.Field names and types depend on the fields selected by the user, such as:

```
"values": {
  "host_name": "String",
  "ip_address": "String",
  "name": "String",
  "os_name": "String",
  "sys_class_name": "String"
}
```

</td></tr><tr id="row_referenceItems"><td>

input.referenceItems

</td><td>

Array of Objects

</td><td id="entry_referenceItems">

List that define references between items in the input payload. The values of each reference item are populated before identifying a CI using the IRE rules defined on a class.```
"referenceItems": [
  { 
    "referenced": "String", 
    "referencedBy": "String", 
    "referenceField": "String" 
  }
]
```

</td></tr><tr id="row_referenceItems_referenced"><td>

input.referenceItems.referenced

</td><td>

String

</td><td id="entry_referenceItems_referenced">

The **internal\_id** defined for the item being referenced by another item.

</td></tr><tr id="row_referenceItems_referencedBy"><td>

input.referenceItems.referencedBy

</td><td>

String

</td><td id="entry_referenceItems_referencedBy">

The **internal\_id** defined for the item that references another item.

</td></tr><tr id="row_referenceItems_referenceField"><td>

input.referenceItems.referenceField

</td><td>

String

</td><td id="entry_referenceItems_referenceField">

Name of the reference field in the class/table for the **referencedBy** item.

</td></tr><tr id="row_relations"><td>

input.relations

</td><td>

Array of Objects

</td><td id="entry_relations">

List that specifies relationships between items in the input payload. An object in this array can use either of two formats.

-   The object can define a relationship between two top-level items \(only\) using **parent** and **child** name-value pairs, with values representing item indexes from the payload **items** array.

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

-   The object can define a relationship between any two items, including top-level, related, or lookup items, using **parent\_id** and **child\_id** key/value pairs, with values representing **internal\_id** values defined for those items.

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


</td></tr><tr id="row_relations_child"><td>

input.relations.child

</td><td>

Number

</td><td id="entry_relations_child">

Integer index of the CI object in the **items** array that represents the child in the relationship \(items, items.related, or items.lookup.\)

</td></tr><tr id="row_relations_child_id"><td>

input.relations.child\_id

</td><td>

String

</td><td id="entry_relations_child_id">

The **internal\_id** of the child item in the relation \(items, items.related, or items.lookup.\)

</td></tr><tr id="row_relations_parent"><td>

input.relations.parent

</td><td>

Number

</td><td id="entry_relations_parent">

Integer index of the parent item in the **items** array \(items, items.related, or items.lookup.\)

</td></tr><tr id="row_relations_parent_id"><td>

input.relations.parent\_id

</td><td>

String

</td><td id="entry_relations_parent_id">

The **internal\_id** of the parent item in the relation \(items, items.related, or items.lookup.\)

</td></tr><tr id="input_rel_sys_rel_source_info-row-IRE"><td>

input.relations.sys\_rel\_source\_info

</td><td>

Object

</td><td id="sys_rel_source_info-entry-IRE">

Discovery source information for the relationship. For non-dependency relationships, this information is saved in the Relationship Sources \[sys\_rel\_source\] table \(not persisted for identifyCIEnhanced\(\) or identifyCI\(\) methods.\)Data type: Object

```
"sys_rel_source_info": { 
  "source_name": "String", 
  "source_feed": "String" 
} 
```

</td></tr><tr id="input-relations-sys_rel_source_info-source_name-row-IRE"><td>

input.relations.sys\_rel\_source\_info.source\_name

</td><td>

String

</td><td id="sys_rel_source_info-source_name-entry-ire">

Discovery source name. Default: Discovery source passed in the API method parameter.

</td></tr><tr id="input-relations-sys_rel_source_info-source_feed-row-IRE"><td>

input.relations.sys\_rel\_source\_info.source\_feed

</td><td>

String

</td><td id="sys_rel_source_into-source_feed-entry-ire">

Any string that is a sub-discovery/scan within the discovery source. Default: 'UNKNOWN' is stored in the source\_feed column when creating a record in sys\_rel\_source table.

</td></tr><tr id="row_relations_type"><td>

input.relations.type

</td><td>

String

</td><td id="entry_relations_type">

Type of relationship that exists between the parent and child items. This must be a name field value from the CI Relationship Type \[cmdb\_rel\_type\] table.

</td></tr><tr id="row_options"><td>

options

</td><td>

Object

</td><td id="entry_options">

Optional, but \{\} or null must be passed-in. Options to enable or disable features.**Note:** By default or if **partial\_payloads** is set to true, both **partial\_commits** and **deduplicate\_payloads** are enabled, even if they are set to false, as those features are essential for partial payloads functionality.

```
"options": { 
 "deduplicate_payloads": Boolean,
 "generate_summary": Boolean, 
 "partial_commits": Boolean, 
 "partial_payloads": Boolean,
 "skip_updating_last_scan_to_now": Boolean,
 "skip_updating_source_last_discovered_to_now": Boolean
}
```

</td></tr><tr id="row_options_deduplicate_payloads"><td>

options.deduplicate\_payloads

</td><td>

Boolean

</td><td id="entry_options_deduplicate_payloads">

Flag that indicates whether duplicate items are merged or considered errors.Valid values:

-   true: Merge duplicate items.
-   false: Consider duplicate items as errors.

Default: true

</td></tr><tr id="row_options_generate_summary"><td>

options.generate\_summary

</td><td>

Boolean

</td><td id="entry_options_generate_summary">

Flag that indicates whether the returned results contain summary information. For the details of the returned summary information, see **&lt;String&gt;.summary** in the return results table.Valid values:

-   true: Include summary information.
-   false: Don't include summary information.

Default: false

</td></tr><tr id="row_options_partial_commits"><td>

options.partial\_commits

</td><td>

Boolean

</td><td id="entry_options_partial_commits">

Flag that indicates whether partial commit support is enabled. For additional information on partial commits, see Enhanced IRE features.Valid values:

-   true: Partial commit enabled.
-   false: Partial commit disabled.

Default: true

</td></tr><tr id="row_options_partial_payloads"><td>

options.partial\_payloads

</td><td>

Boolean

</td><td id="entry_options_partial_payloads">

Flag that indicates whether partial payload support is enabled. For additional information on partial payloads, see Enhanced IRE features and Create an IRE data source rule.Valid values:

-   true: Partial payload enabled.
-   false: Partial payload disabled.

Default: true

</td></tr><tr><td>

options.skip\_updating\_last\_scan\_to\_now

</td><td>

Boolean

</td><td>

Flag that indicates whether to skip updating the sys\_object\_source's last\_scan time field.Valid values:

-   true: If the **source\_recency\_timestamp** parameter is not passed in**sys\_object\_source\_info**, do not update the sys\_object\_source's last\_scan time field.
-   false: Update the sys\_object\_source's last\_scan time field.

Default: Uses the value in the glide.identification\_engine.skip\_updating\_last\_scan\_to\_now system property.

</td></tr><tr><td>

options.skip\_updating\_source\_last\_discovered\_to\_now

</td><td>

Boolean

</td><td>

Flag that indicates whether to skip updating the discovery\_source and last\_discovered fields in the Configuration Item \[cmdb\_ci\] table.Valid values:

-   true: If last\_discovered is not provided in the payload item values, do not update the discovery\_source and last\_discovered fields.
-   false: Update the discovery\_source and last\_discovered fields.

Default: Uses the value in the glide.identification\_engine.skip\_updating\_source\_last\_discovered\_to\_now system property.

</td></tr><tr id="row_source"><td>

source

</td><td>

String

</td><td id="entry_source">

Data source of the CI information. This value must be one of the choice values defined for the discovery\_source field of the Configuration Item \[cmdb\_ci\] table.

</td></tr></tbody>
</table><table class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;String&gt;

</td><td>

JSON formatted string that is a list of results for the configuration items in the input string.Data type: String

```
{ 
  "additionalCommittedItems": [Array],  
  "additionalCommittedRelations": [Array], 
  "hasError": Boolean, 
  "hasWarning": Boolean,
  "items": [Array],  
  "relations": [Array], 
  "summary": {Object} 
}
```

</td></tr><tr><td>

&lt;String&gt;.additionalCommittedItems

</td><td>

List of CIs that were committed during the IRE processing of the current payload, but were not present in the current input payload.Data type: Array of Objects

```
"additionalCommittedItems": [
  {
    "className": "String",
    "errorCount": Number,
    "operation": "String",
    "identificationAttempts": [Array],
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloads": [Array],
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.additionalCommittedRelations

</td><td id="entry_return_additionalCommittedRelations">

Description of a dependent relationship CI that was not included in the request body **relations** list to insert or update.Data type: Array of Objects

```
"additionalCommittedRelations": [
  {
    "className": "String",
    "inputIndices": [Array],
    "markers": [Array],
    "mergedPayloadIds": [Array],
    "operation": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.hasError

</td><td id="entry_return_summary_class_name_hasError">

Flag that indicates whether any item or relation has errors.Data type: Boolean

</td></tr><tr><td>

&lt;String&gt;.hasWarning

</td><td id="entry_return_summary_class_name_hasWarning">

Flag that indicates whether any item or relation has warnings.Data type: Boolean

</td></tr><tr><td>

&lt;String&gt;.items

</td><td>

Description of the created or updated CIs.Data type: Array of Objects

```
"items": [ 
  {  
    "additionalRelatedItems": [Array],
    "className": "String",
    "duplicateIndices": [Array],
    "errorCount": Number, 
    "errors": [Array], 
    "identificationAttempts": [Array], 
    "identifierEntrySysId": "String",
    "info": [Array], 
    "inputIndices": [Array], 
    "maskedAttributes": [Array],
    "operation": "String",
    "relatedSysIds": [Array], 
    "sysId": "String" 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems

</td><td id="entry_return_item_additionalRelatedItems">

Information about additional lookup and related items that were processed but not provided as part of the input payload. These items are from partial payloads.Data type: Array of Objects

```
"additionalRelatedItems": [ 
  {
    "className": "String", 
    "inputIndices": [Array],
    "mergedPayloadIds": [Array], 
    "operation": "String",
    "sysId": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.className

</td><td id="items_addRelItems_className-entry-IRE">

Class/table name \(sys\_class\_name\) of the CI that was created or updated.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.inputIndices

</td><td id="items_addRelItems_inputIndices-entry-IRE">

Index values for CIs from the request body **items** array that correspond to this related item.Data type: Array of Numbers

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.mergedPayloadIds

</td><td id="entry_return_item_additionalRelatedItems_mergedPayloadIds">

List of sys\_ids of the partial payloads that were merged into the related item.Data type: Array

Table: CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\]

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.operation

</td><td id="entry_return_item_additionalRelatedItems_operations">

Type of operation.Possible values:

-   INSERT: New CI was inserted into the database.
-   NO\_CHANGE: No CI changes were made.
-   UPDATE: Existing CI was updated.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.additionalRelatedItems.sysId

</td><td id="items_addRelItems_sysId-entry-IRE">

Sys\_id of the CI that was updated or created.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.className

</td><td id="entry_return_item_className">

Class/table name \(sys\_class\_name\) of the CI that was created or updated.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.duplicateIndices

</td><td id="entry_return_items_duplicateIndices">

List of indexes of CIs that are duplicates of the current item.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.errorCount

</td><td id="entry_return_item_errorCount">

Number of errors encountered while processing the item.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.errors

</td><td id="entry_return_item_error">

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

&lt;String&gt;.items.errors.error

</td><td>

Type of error encountered while processing the CI.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.errors.message

</td><td>

Error message encountered while processing the CI.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts

</td><td id="entry_return_item_identificationAttempts">

List of attempts that were made to identify the CIs.Data type: Array of Objects

```
"identificationAttempts": [
  { 
    "attemptResult": "String", 
    "attributes": [Array],
    "hybridEntryCiAttributes": [Array],
    "identifierName": "String",
    "searchOnTable": "String" 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.attemptResult

</td><td id="entry_return_item_identificationAttempts_attemptResult">

Results of the attempt to identify the CI.Possible values:

-   MATCHED: Identification succeeded. A unique CI was found in the identifier rule table which exactly matched the specified attributes.
-   MULTI\_MATCH: Identification failed with an error. Duplicate CIs were found in the identifier rule table when matching against the specified attributes.
-   NO\_MATCH: Identification failed. No CI was found in the identifier rule table which matched the specified attributes.
-   SKIPPED: Identification not attempted. The attributes required for this identifier rule table search were not provided, so the rule was not applied.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.attributes

</td><td id="entry_return_item_identificationAttempts_attributes">

List of CI identifier entry attributes that were used during the identification process.Data type: Array

Attribute names and types depend on the request body data and the identifier in use, such as:

```
"attributes": [
  "serial_number": "String",
  "serial_number_type": "String",
]
```

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.identifierName

</td><td id="entry_return_item_identificationAttempts_identifierName">

Identifier rule used for this CI identification attempt.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identificationAttempts.searchOnTable

</td><td id="entry_return_item_identificationAttempts_searchOnTable">

Name of the table searched during the identification process.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.identifierEntrySysId

</td><td id="entry_return_item_identifierEntrySysId">

Sys\_id for the identifier rule used to identify the CI.Data type: String

Table: Identifier Entry \[cmdb\_identifier\_entry\]

</td></tr><tr><td>

&lt;String&gt;.items.info

</td><td>

Additional information about the processing of the item.Data type: Array of Objects

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

&lt;String&gt;.items.info.code

</td><td>

Reclassification type that was skipped.Possible values:

-   SKIPPED\_CLASS\_SWITCH
-   SKIPPED\_CLASS\_DOWNGRADE
-   SKIPPED\_CLASS\_UPGRADE

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info.message

</td><td>

Message that provides additional insights into the reason for skipping the reclassification.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.info.ruleSysId

</td><td>

Sys\_id of the reclassification restriction rule that was matched. Applicable only when IRE skips reclassification due to reclassification restriction rule. This value is empty if the reclassification is skipped due to a payload or global flag.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.inputIndices

</td><td id="entry_return_items_inputIndices">

Indexes of the corresponding input CI. For top-level items, it is a list of integers. For related or lookup CIs, it is list of JSON objects.Data type: Array of Numbers

</td></tr><tr><td>

&lt;String&gt;.items.maskedAttributes

</td><td id="entry_return_item_maskedAttributes">

List of attributes whose update by a non-authoritative data source was skipped as defined by the Reconciliation Rules.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.operation

</td><td id="entry_return_item_operation">

Operation that took place.Possible values:

-   INSERT: New CI was inserted into the database.
-   INSERT\_AS\_INCOMPLETE: Item was saved in cmdb\_ire\_incomplete\_payloads table.
-   INSERT\_AS\_PARTIAL: Item was saved in cmdb\_ire\_partial\_payloads table.
-   UPDATE: Existing CI was updated.
-   UPDATE\_WITH\_DOWNGRADE: CI was updated and the class changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: CI was updated and the class changed to a class that is not ancestor or descendent.
-   UPDATE\_WITH\_UPDRADE: CI was updated and the class changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems

</td><td id="entry_return_item_relatedItems_identifyCI">

Information about the processed related items.Data type: Array of Objects

```
"relatedItems": [
  { 
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "inputIndices": [Array],
    "mergePayloadIds": [Array],
    "operation": "String",
    "sysId": "String",
    "warningCount": Number,
    "warnings": [Array]
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.className

</td><td>

Class/table name \(sys\_class\_name\) of the related item.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.errorCount

</td><td id="entry_return_item_relatedItems_errorCount">

Number of errors detected while processing the related items.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.errors

</td><td id="entry_return_item_relatedItems_errors">

List of errors that occurred during processing of the related item.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.errors.error

</td><td>

Type of error encountered while processing the related item.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.errors.message

</td><td>

Error message encountered while processing the related item.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.inputIndices

</td><td id="entry_return_item_relatedItems_inputIndices">

Index of the corresponding input item. For top-level items, it is a list of integers. For related or lookup items, it is list of JSON objects.Data type: Array of Numbers or Array of Objects

```
"inputIndices": [
  { 
   "mainIndex": Number, 
   "subIndex": Number 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.inputIndices.mainIndex

</td><td id="entry_return_item_relatedItems_inputIndices.mainIndex">

Index value from the request body **items** array that corresponds to the CI parent of the related item. Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.inputIndices.subIndex

</td><td id="entry_return_item_relatedItems_inputIndices.subIndex">

Index value from the request body **items.lookup** array that corresponds to the related item.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.mergedPayloadIds

</td><td>

List of sys\_ids of the partial payloads that were merged into the CI during processing.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.operation

</td><td>

Operation that took place.Possible values:

-   INSERT: New related CI was inserted into the database.
-   INSERT\_AS\_INCOMPLETE: Item was saved in cmdb\_ire\_incomplete\_payloads table.
-   INSERT\_AS\_PARTIAL: Item was saved in cmdb\_ire\_partial\_payloads table.
-   NO\_CHANGE: No related CI changes were made.
-   UPDATE: Existing related CI was updated.
-   UPDATE\_WITH\_DOWNGRADE: Related CI was updated and the class changed to a more generic class \(ancestor class\).
-   UPDATE\_WITH\_SWITCH: Related CI was updated and the class changed to a class that is not ancestor or descendent.
-   UPDATE\_WITH\_UPDRADE: Related CI was updated and the class changed to a more specialized class \(descendent class\).

Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.sysId

</td><td>

Sys\_id of the related item.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.warningCount

</td><td>

Number of warnings encountered when processing the related items.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.items.relatedItems.warnings

</td><td>

Description of warnings encountered while processing the related items.Data type: Array of Objects

```
"warnings": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.items.relatedSysIds

</td><td id="entry_return_item_relatedSysIds">

List of the sys\_id values of the CIs used during lookup-based identification of related items.Data type: String

</td></tr><tr><td>

&lt;String&gt;.items.sys\_id

</td><td id="entry_return_item_sys_id">

Sys\_id of the CI that was updated or created.Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations

</td><td id="_identifyCI">

Information about the processed relations.Data type: Array of Objects

```
"relations": [ 
  { 
    "className": "String",
    "errorCount": Number,
    "errors": [Array],
    "inputIndices": [Array],
    "operation": "String",
    "sysId": "String" 
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.relations.className

</td><td id="entry_return_relations_className">

Sys\_class\_name of this dependent relationship CI.Only supported value: cmdb\_rel\_ci: CI Relationship table.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations.errorCount

</td><td id="entry_return_relations_errorsCount">

Number of errors encountered when processing the dependent relationship CI.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.relations.errors

</td><td id="entry_return_relations_errors">

List that describes errors that were encountered while processing this dependent relationship CI.Data type: Array of Objects

```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

&lt;String&gt;.relations.inputIndices

</td><td id="entry_return_relations_inputIndices">

Indexes for the dependent relationship CI objects in the request body **relations** array that correspond to this dependent relationship CI.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.relations.operation

</td><td id="entry_return_relations_operation">

Type of operation performed.Possible values:

-   INSERT: The dependent relationship CI was inserted into the target table as a new record.
-   INSERT\_AS\_INCOMPLETE: The dependent relationship CI had errors and was inserted into the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.
-   INSERT\_AS\_PARTIAL: The dependent relationship CI had errors and was inserted into the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table.
-   NO\_CHANGE: No operation was performed.
-   UPDATE: An existing dependent relationship CI in the target table was updated.

Data type: String

</td></tr><tr><td>

&lt;String&gt;.relations.sysId

</td><td id="entry_return_relations_sys_id">

Sys\_id of the dependent relationship CI.Data type: String

</td></tr><tr><td>

&lt;String&gt;.summary

</td><td id="entry_return_summary">

List of JSON properties that provide statistics on how many items were inserted, updated, and such, per class.Data type: Array

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;

</td><td id="entry_return_summary_class_name">

Statistics for a specific class.Data type: Object

```
<class_name>: {
 "additionalInsertedItemCount": Number, 
 "errorCount": Number,
 "incompleteItemCount": Number,
 "insertedItemCount": Number,
 "partialItemCount": Number,
 "skippedItemCount": Number,
 "unchangedItemCount": Number,
 "updatedItemCount": Number,
 "warningCount": Number 
}
```

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.additionalInsertedItemCount

</td><td id="entry_return_summary_class_name_additionalInsertedItemCount">

Number of items inserted due to processing of partial payloads.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.errorCount

</td><td id="entry_return_summary_class_name_errorCount">

Number of errors encounter when processing items.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.incompleteItemCount

</td><td id="entry_return_summary_class_name_incompleteItemCount">

Number of items inserted in the CMDB IRE Incomplete Payloads \[cmdb\_ire\_incomplete\_payloads\] table.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.insertedItemCount

</td><td id="entry_return_summary_class_name_insertedItemCount">

Number of items created.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.partialItemCount

</td><td id="entry_return_summary_class_name_partialItemCount">

Number of items saved in the Partial Payload table \[cmdb\_ire\_partial\_payloads\].Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.skippedItemCount

</td><td>

Number of items that were skipped.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.unchangedItemCount

</td><td id="entry_return_summary_class_name_unchangedItemCount">

Number of items that had entries but were not modified.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.updatedItemCount

</td><td id="entry_return_summary_class_name_updatedItemCount">

Number of items updated.Data type: Number

</td></tr><tr><td>

&lt;String&gt;.summary.&lt;class\_name&gt;.warningCount

</td><td id="entry_return_summary_class_name_warningCount">

Number of items that generated a warning when processed.Data type: Number

</td></tr></tbody>
</table>```
var payload = {
"items": [
{
"className": "cmdb_ci_win_server",
"values": {
   "chassis_type": "Desktop",
   "os": "Windows 2012 R2 Datacenter",
   "name": "Windows2012Server1",
   "serial_number": "0000-0011-1690-8730-8636-5722-52",
   "cpu_count": "1"
  },
  "lookup": [
  {
     "values": {
       "valid": "true",
       "serial_number": "0000-0011-1690-8730-8636-5722-52",
       "serial_number_type": "bios"
      },
     "className": "cmdb_serial_number"
   },
   {
     "values": {
       "valid": "true",
       "serial_number": "3311-9736-4988-9744-1749-4183-41",
       "serial_number_type": "chassis"
      },
     "className": "cmdb_serial_number"
   }],
 
    "internal_id": "16777219",
    "sys_object_source_info": {
      "source_feed": "SN Discovery Feed 1",
      "source_name": "ServiceNow",
      "source_native_key": "16777219",
      "source_recency_timestamp": "2019-10-18 08:31:23"
   }},
   {
   "className": "cmdb_ci_spkg",
   "values": {
     "name": "Windows 2012 R2 Datacenter",
     "key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL"
     },
 
  "related": [
    {
     "internal_id": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219",
      "values": {
        "name": "Windows 2012 R2 Datacenter-SAMLABVM52"
      },
      "className": "cmdb_software_instance",
      "sys_object_source_info": {
        "source_feed": "SN Discovery Feed 1",
        "source_name": "ServiceNow",
        "source_native_key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219"
  }},
  {
    "internal_id": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777229",
      "values": {
        "name": "Windows 2012 R2 Datacenter-SAMLABVM52"
      },
    "className": "cmdb_software_instance",
    "sys_object_source_info": {
      "source_feed": "SN Discovery Feed 1",
      "source_name": "ServiceNow",
      "source_native_key": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777229"
  }}
],
  "settings" : {
        "skipReclassificationRestrictionRules" : "false",
        "updateWithoutDowngrade" : "true",
        "updateWithoutUpgrade" : "true",
        "updateWithoutSwitch" : "true"
      }},
  {
  "className": "cmdb_ci_app_server_tomcat",
  "values": {
    "running_process_key_parameters": "/opt/OV/nonOV/tomcat/b/temp org.apache.catalina.startup.Bootstrap start",
    "install_directory": "/opt/OV/nonOV/tomcat/b",
    "name": "Tomcat@hpom9:3443",
    "server_port": "8006",
    "sys_class_name": "cmdb_ci_app_server_tomcat"
  },
 
  "internal_id": "tomcat_id"
  }],
 
"relations": [
  {
    "parent_id": "tomcat_id",
    "child_id": "16777219",
    "type": "Runs on::Runs"
  }],
 
"referenceItems": [
  {
    "referenceField": "installed_on",
    "referenced": "16777219",
    "referencedBy": "Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777219"
  }]};
 
var input = JSON.stringify(payload);
var output = sn_cmdb.IdentificationEngine.identifyCIEnhanced('ServiceNow', input, {});

gs.info(JSON.stringify(JSON.parse(output), null, 2));
```

Output:

```
{
  "items": [
    {
      "className": "cmdb_ci_win_server",
      "operation": "INSERT",
      "relatedSysIds": [
        null,
        null
      ],
      "relatedItems": [
        {
          "errors": [],
          "operation": "INSERT",
          "className": "cmdb_serial_number",
          "errorCount": 0,
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 0,
              "subIndex": 0
            }
          ],
          "mergedPayloadIds": [],
          "warningCount": 0
        },
        {
          "errors": [],
          "operation": "INSERT",
          "className": "cmdb_serial_number",
          "errorCount": 0,
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 0,
              "subIndex": 1
            }
          ],
          "mergedPayloadIds": [],
          "warningCount": 0
        }
      ],
      "identificationAttempts": [
        {
          "attributes": [],
          "info": "sys_object_source NO_MATCH",
          "identifierName": "",
          "attemptResult": "NO_MATCH",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "serial_number",
            "serial_number_type"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "searchOnTable": "cmdb_serial_number",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "serial_number"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "name"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "NO_MATCH",
          "searchOnTable": "cmdb_ci_hardware",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "mac_address",
            "name"
          ],
          "identifierName": "Hardware Rule",
          "attemptResult": "SKIPPED",
          "searchOnTable": "cmdb_ci_network_adapter",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ],
      "mergedPayloadIds": [],
      "warningCount": 0
    },
    {
      "className": "cmdb_ci_spkg",
      "operation": "INSERT",
      "relatedSysIds": [
        null
      ],
      "relatedItems": [
        {
          "errors": [],
          "operation": "INSERT",
          "className": "cmdb_software_instance",
          "errorCount": 0,
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 1,
              "subIndex": 0
            }
          ],
          "mergedPayloadIds": [],
          "warningCount": 0
        },
        {
          "errors": [],
          "warnings": [
            {
              "error": "MISSING_MATCHING_ATTRIBUTES",
              "message": "In payload missing minimum set of input values for criterion (matching) attributes from identify rule for table [cmdb_software_instance]. Add these input values in payload item '{\"className\":\"cmdb_software_instance\",\"values\":{},\"internal_id\":\"f7273cccec30101056cd4bb46eb4db5d\",\"sys_object_source_info\":{\"source_feed\":\"SN Discovery Feed 1\",\"source_name\":\"ServiceNow\",\"source_native_key\":\"Microsoft Windows Server 2012 R2 Datacenter_:::_NULL|16777229\"},\"settings\":{},\"sys_ire_info\":{\"ire_received_time\":\"2020-05-10 17:57:48\"}}'"
            }
          ],
          "operation": "INSERT_AS_PARTIAL",
          "className": "cmdb_software_instance",
          "errorCount": 0,
          "sysId": "Unknown",
          "markers": [],
          "inputIndices": [
            {
              "mainIndex": 1,
              "subIndex": 1
            }
          ],
          "mergedPayloadIds": [],
          "warningCount": 1
        }
      ],
      "identificationAttempts": [
        {
          "attributes": [],
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "hybridEntryCiAttributes": []
        },
        {
          "attributes": [
            "key"
          ],
          "identifierName": "Software",
          "attemptResult": "NO_MATCH",
          "searchOnTable": "cmdb_ci_spkg",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "markers": [],
      "inputIndices": [
        1
      ],
      "mergedPayloadIds": [],
      "warningCount": 0
    },
    {
      "className": "cmdb_ci_app_server_tomcat",
      "operation": "INSERT",
      "identificationAttempts": [
        {
          "attributes": [],
          "info": "sys_object_source SKIPPED",
          "identifierName": "",
          "attemptResult": "SKIPPED",
          "hybridEntryCiAttributes": []
        }
      ],
      "errorCount": 0,
      "markers": [],
      "inputIndices": [
        2
      ],
      "mergedPayloadIds": [],
      "warningCount": 0
    }
  ],
  "additionalCommittedItems": [],
  "relations": [
    {
      "className": "cmdb_rel_ci",
      "operation": "INSERT",
      "errorCount": 0,
      "markers": [],
      "inputIndices": [
        0
      ],
      "mergedPayloadIds": [],
      "warningCount": 0
    }
  ],
  "additionalCommittedRelations": []
}  
```

## IdentificationEngine - runIdentificationAudit\(GlideRecord now\_GR\)

Runs an identification audit against the specified configuration item \(CI\) to detect duplicates.

If duplicates are found, duplication tasks are created. Only use this method on CI types with independent identification rules.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|CI on which to run the audit to detect duplicates. The CI must have independent identification rules.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to check a record in the Linux Servers \[cmdb\_ci\_linux\_server\] table for duplicates.

```
var sysId = '<cbdb_ci_sys_id>';
var gr = new GlideRecord('cmdb_ci_linux_server');
gr.get(sysId);
sn_cmdb.IdentificationEngine.runIdentificationAudit(gr);
```

