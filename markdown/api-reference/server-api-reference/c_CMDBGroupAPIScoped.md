---
title: CMDBGroupAPI - Scoped
description: The CMDBGroupAPI provides methods for performing actions on Configuration Management Database \(CMDB\) groups.Returns all configuration items \(CIs\) for the specified group. The results include all manual CIs and the list of CIs from the query builder's saved query.Returns all configuration items \(CIs\) returned from all saved query builders' query IDs for the specified group.Returns the CMDB group's manual CI list.Returns the query builder's query IDs for the specified CMDB group.Sets the manual CI list for the specified group. The existing manual CI list is overwritten. CI sysIds not found in the cmdb\_ci table are ignored.Sets the saved query ID list for the specified group. The existing query ID list is overwritten. Query sysIds not found in the qb\_saved\_query table are ignored.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CMDBGroupAPI- Scoped

The CMDBGroupAPI provides methods for performing actions on Configuration Management Database \(CMDB\) groups.

This API is a scoped static class. To use this class you must include the `sn_cmdbgroup` namespace identifier before the CMDBGroupAPI object. For example:

```
var response = sn_cmdbgroup.CMDBGroupAPI.getManualCIList(groupSysId, false);
```

To access this API you must have the itil or asset role.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CMDBGroupAPI - getAllCI\(String groupId, Boolean requireCompleteSet, Boolean requireAllQueryNodesCis\)

Returns all configuration items \(CIs\) for the specified group. The results include all manual CIs and the list of CIs from the query builder's saved query.

<table id="table_nyt_5lz_kx" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupId

</td><td>

String

</td><td id="entry-groupId-CMDB">

Sys\_id of the Configuration Management Database \(CMDB\) group.

</td></tr><tr><td>

requireCompleteSet

</td><td>

Boolean

</td><td id="entry-requireCompleteSet-CMDB">

Optional, but must be passed if **requireAllQueryNodesCis** is passed. Flag that indicates whether an empty string is returned if any CIs are filtered out by access control list \(ACL\) restrictions.

 Valid values:

-   true: Return empty string.
-   false: Don't return value.

 Default: false

</td></tr><tr><td>

requireAllQueryNodesCis

</td><td>

Boolean

</td><td id="entry-requireAllQueryNodesCis-CMDB">

Optional. Flag that indicates whether to return CIs from all CMDB classes of the query. Valid values:

-   true: Return CIs from all columns.
-   false: Only return CIs from the starting node of the query builder query.

 Default: false

</td></tr></tbody>
</table><table id="table_rm2_322_vlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td>

List of errors for a failed operation.Data type: Array

 ```
"errors": [ 
  {
    "message": "String",
    "error": "String"
  } 
]
```

</td></tr><tr><td>

errors.error

</td><td>

Error name.Possible values:

-   GROUP\_SYS\_ID\_IS\_NOT\_FOUND
-   GROUP\_SYS\_ID\_IS\_EMPTY
-   FAIL\_TO\_INSERT\_GROUP\_CI\_PAIR
-   FAIL\_TO\_INSERT\_GROUP\_QUERY\_ID\_PAIR
-   CI\_CAN\_NOT\_FOUND
-   SAVED\_QUERY\_ID\_NOT\_FOUND
-   ERROR\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   TIMEOUT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   NOT\_COMPLETE\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   MAX\_LIMIT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   GROUP\_API\_TIMEOUT
-   EXCEPTION\_FROM\_EXECUTE\_QUERY
-   SOME\_CI\_NOT\_VISIBLE\_DUE\_TO\_SECURITY\_CONSTRAINT

 Data type: String

</td></tr><tr><td>

errors.message

</td><td>

Brief description of the error message.Data type: String

</td></tr><tr><td>

idList

</td><td>

List of CMDB CI sys\_ids.Data type: Array

</td></tr><tr><td>

partialCIListDueToACLFlag

</td><td>

Flag that indicates if the list of returned CIs is incomplete due to ACL restrictions.**Note:** This is not considered an error condition, and no corresponding error information is returned.

 Data type: Boolean

 Valid values:

-   true: **idList** is incomplete.
-   false: **idList** is complete.

</td></tr><tr><td>

result

</td><td>

Flag that indicates whether the method completed successfully.Possible values:

-   true: Success
-   false: Error

</td></tr></tbody>
</table>```
// Script example: 
var getAllCIFunc = function(groupSysId) {
  var parser = new JSONParser();
  var response = sn_cmdbgroup.CMDBGroupAPI.getAllCI(groupSysId, false);
  var parsed = parser.parse(response);
  if (parsed.result) {
    gs.info("succeed to retrieve ci list: " + parsed.idList);
  } else {
    gs.info("fail to retrieve list, errors: " + JSON.stringify(parsed.errors));
  }
}
var groupExists = "d0d2d25113152200eef2dd828144b0e4";
var groupContainsInvalidSavedQuery = "e685a2c3d7012200de92a5f75e610387";
getAllCIFunc(groupExists);
getAllCIFunc(groupContainsInvalidSavedQuery);
```

Output:

```
// Successful response
{
  'result':true, 
  'partialCIListDueToACLFlag': false,
  'idList':[
    '3a5dd3dbc0a8ce0100655f1ec66ed42c',
    '6b43105c37301000deeabfc8bcbe5db2'
  ] 
}

// Error response
{ 
  'result':false, 
  'errors':[ 
    {
      'message':'Group does not exist',
      'error':'GROUP_SYS_ID_IS_NOT_FOUND'
    } 
  ], 
  'partialCIListDueToACLFlag':false,
  'idList':[] 
}
```

## CMDBGroupAPI - getAllCIFromQueryBuilder\(String groupId, Boolean requireCompleteSet, Boolean requireAllQueryNodesCis\)

Returns all configuration items \(CIs\) returned from all saved query builders' query IDs for the specified group.

<table id="table_kcy_mjz_kx" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupId

</td><td>

String

</td><td id="entry-groupId-CMDB">

Sys\_id of the Configuration Management Database \(CMDB\) group.

</td></tr><tr><td>

requireCompleteSet

</td><td>

Boolean

</td><td id="entry-requireCompleteSet-CMDB">

Optional, but must be passed if **requireAllQueryNodesCis** is passed. Flag that indicates whether an empty string is returned if any CIs are filtered out by access control list \(ACL\) restrictions.

 Valid values:

-   true: Return empty string.
-   false: Don't return value.

 Default: false

</td></tr><tr><td>

requireAllQueryNodesCis

</td><td>

Boolean

</td><td id="entry-requireAllQueryNodesCis-CMDB">

Optional. Flag that indicates whether to return CIs from all CMDB classes of the query. Valid values:

-   true: Return CIs from all columns.
-   false: Only return CIs from the starting node of the query builder query.

 Default: false

</td></tr></tbody>
</table><table id="table_lfb_k22_vlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td>

List of errors for a failed operation.Data type: Array

 ```
"errors": [ 
  {
    "message": "String",
    "error": "String"
  } 
]
```

</td></tr><tr><td>

errors.error

</td><td>

Error name.Possible values:

-   GROUP\_SYS\_ID\_IS\_NOT\_FOUND
-   GROUP\_SYS\_ID\_IS\_EMPTY
-   FAIL\_TO\_INSERT\_GROUP\_CI\_PAIR
-   FAIL\_TO\_INSERT\_GROUP\_QUERY\_ID\_PAIR
-   CI\_CAN\_NOT\_FOUND
-   SAVED\_QUERY\_ID\_NOT\_FOUND
-   ERROR\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   TIMEOUT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   NOT\_COMPLETE\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   MAX\_LIMIT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY
-   GROUP\_API\_TIMEOUT
-   EXCEPTION\_FROM\_EXECUTE\_QUERY
-   SOME\_CI\_NOT\_VISIBLE\_DUE\_TO\_SECURITY\_CONSTRAINT

 Data type: String

</td></tr><tr><td>

errors.message

</td><td>

Brief description of the error message.Data type: String

</td></tr><tr><td>

idList

</td><td>

List of CMDB CI sys\_ids.Data type: Array

</td></tr><tr><td>

partialCIListDueToACLFlag

</td><td>

Flag that indicates if the list of returned CIs is incomplete due to ACL restrictions.**Note:** This is not considered an error condition, and no corresponding error information is returned.

 Data type: Boolean

 Valid values:

-   true: **idList** is incomplete.
-   false: **idList** is complete.

</td></tr><tr><td>

result

</td><td>

Flag that indicates whether the method completed successfully.Possible values:

-   true: Success
-   false: Error

</td></tr></tbody>
</table>```
// Script example:
var getAllCIFromQueryBuilderFunc = function(groupSysId) {
  var parser = new JSONParser();
  var response = sn_cmdbgroup.CMDBGroupAPI.getAllCIFromQueryBuilder(groupSysId, false);
  var parsed = parser.parse(response);
  if (parsed.result) {
    gs.info("succeed to retrieve ci list: " + parsed.idList);
  } else {
    gs.info("fail to retrieve list, errors: " + JSON.stringify(parsed.errors));
  }
}
var groupExists = "d0d2d25113152200eef2dd828144b0e4";
var groupContainsInvalidSavedQuery = "e685a2c3d7012200de92a5f75e610387";
getAllCIFromQueryBuilderFunc(groupExists);
getAllCIFromQueryBuilderFunc(groupContainsInvalidSavedQuery);
```

Output:

```
// Successful response
{
  'result':true, 
  'partialCIListDueToACLFlag': false,
  'idList':[
    '3a5dd3dbc0a8ce0100655f1ec66ed42c',
    '6b43105c37301000deeabfc8bcbe5db2'
  ] 
}

// Error response
{ 
  'result':false, 
  'errors':[ 
    {'message':'Group does not exist',
    'error':'GROUP_SYS_ID_IS_NOT_FOUND'} 
  ], 
  'partialCIListDueToACLFlag':false,
  'idList':[] 
}
```

## CMDBGroupAPI - getManualCIList\(String groupId, Boolean requireCompleteSet\)

Returns the CMDB group's manual CI list.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The sysId of the CMDB group.|
|requireCompleteSet|Boolean|When true, returns an error string if any CIs are filtered out by ACL restrictions.|

<table id="table_ffx_szx_kx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formated string in the format ```
{ 'result':false, 
'errors':[ {'message':'Group does not exist',
            'error':'GROUP_SYS_ID_IS_NOT_FOUND'},
 { } // another error if it exists 
 ], 
'partialCIListDueToACLFlag':false,
'idList':['sys_id_1', 'sys_id2'] }
```

Where -   result - a boolean flag. When true the method was successful.
-   errors - a list of errors with a message and error code.
-   partialCIListDueToACLFlag -  a Boolean flag. When true, the idList is incomplete due to an ACL restriction. When false, the idList is complete.
-   idList - an array of cmdb\_ci sys\_ids

 When not successful, returns one of the errors GROUP\_SYS\_ID\_IS\_NOT\_FOUND, GROUP\_SYS\_ID\_IS\_EMPTY, FAIL\_TO\_INSERT\_GROUP\_CI\_PAIR, FAIL\_TO\_INSERT\_GROUP\_QUERY\_ID\_PAIR, CI\_CAN\_NOT\_FOUND, SAVED\_QUERY\_ID\_NOT\_FOUND, ERROR\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, TIMEOUT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, NOT\_COMPLETE\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, MAX\_LIMIT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, GROUP\_API\_TIMEOUT, EXCEPTION\_FROM\_EXECUTE\_QUERY, SOME\_CI\_NOT\_VISIBLE\_DUE\_TO\_SECURITY\_CONSTRAINT

</td></tr></tbody>
</table>```
// Script example for requireCompleteSet being false:
    var getManualCIList = function(groupSysId) {
    var parser = new JSONParser();
    var response = sn_cmdbgroup.CMDBGroupAPI.getManualCIList(groupSysId, false);
    var parsed = parser.parse(response);
    if (parsed.result) {
        gs.info("succeed to retrieve ci list: " + parsed.idList);
    } else {
        gs.info("fail to retrieve list, errors: " + JSON.stringify(parsed.errors));
    }
}
// create a group in cmdb_group, and add CIs to this group in Edit Manual CI form
var groupExists = "d0d2d25113152200eef2dd828144b0e4";
// use a non-exist group
var groupDoesNotExists = "d0d2d25113152200eef2dd828144b0e4111";
getManualCIList(groupExists);
getManualCIList(groupDoesNotExists);
 
```

Output: \(Line breaks added for formatting.\)

```
succeed to retrieve ci 
list: 6b43105c37301000deeabfc8bcbe5db2,2dfd7c8437201000deeabfc8bcbe5d56
fail to retrieve list, errors: 
[{"message":"Group does not exist","error":"GROUP_SYS_ID_IS_NOT_FOUND"}]
```

```
// Script example for requireCompleteSet being true
    var getManualCIList = function(groupSysId) {
    var parser = new JSONParser();
    var response = sn_cmdbgroup.CMDBGroupAPI.getManualCIList(groupSysId, true);
    var parsed = parser.parse(response);
    if (parsed.result) {
        gs.info("succeed to retrieve ci list: " + parsed.idList);
    } else {
        gs.info("fail to retrieve list, errors: " + JSON.stringify(parsed.errors));
    }
}
// create a group in cmdb_group, and add CIs to this group in Edit Manual CI form
var groupExists = "d0d2d25113152200eef2dd828144b0e4";
getManualCIList(groupExists);
```

Output: \(Line breaks added for formatting.\)

```
fail to retrieve list, errors: 
[{"message":"Some CI(s) not visible due to security constraint",
"error":"SOME_CI_NOT_VISIBLE_DUE_TO_SECURITY_CONSTRAINT"}]
```

## CMDBGroupAPI - getSavedQueryIdList\(String groupId, Boolean requireCompleteSet\)

Returns the query builder's query IDs for the specified CMDB group.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The sysId of the CMDB group.|
|requireCompleteSet|Boolean|When true, returns an empty string if any CIs are filtered out by ACL restrictions.|

<table id="table_fwk_lfy_kx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formated string in the format ```
{ 'result':false, 
'errors':[ {'message':'Group does not exist',
            'error':'GROUP_SYS_ID_IS_NOT_FOUND'},
 { } // another error if it exists 
 ], 
'partialCIListDueToACLFlag':false,
'idList':['sys_id_1', 'sys_id2'] }
```

Where -   result - a boolean flag. When true the method was successful.
-   errors - a list of errors with a message and error code.
-   partialCIListDueToACLFlag -  a Boolean flag. When true, the idList is incomplete due to an ACL restriction. When false, the idList is complete.
-   idList - an array of cmdb\_ci sys\_ids

 When not successful, returns one of the errors GROUP\_SYS\_ID\_IS\_NOT\_FOUND, GROUP\_SYS\_ID\_IS\_EMPTY, FAIL\_TO\_INSERT\_GROUP\_CI\_PAIR, FAIL\_TO\_INSERT\_GROUP\_QUERY\_ID\_PAIR, CI\_CAN\_NOT\_FOUND, SAVED\_QUERY\_ID\_NOT\_FOUND, ERROR\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, TIMEOUT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, NOT\_COMPLETE\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, MAX\_LIMIT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, GROUP\_API\_TIMEOUT, EXCEPTION\_FROM\_EXECUTE\_QUERY, SOME\_CI\_NOT\_VISIBLE\_DUE\_TO\_SECURITY\_CONSTRAINT

</td></tr></tbody>
</table>```
// Script example:
var getSavedQueryIdList = function(groupSysId) {
    var parser = new JSONParser();
    var response = sn_cmdbgroup.CMDBGroupAPI.getSavedQueryIdList(groupSysId, false);
    var parsed = parser.parse(response);
    if (parsed.result) {
        gs.info("succeed to retrieve saved query id list: " + parsed.idList);
    } else {
        gs.info("fail to retrieve list, errors: " + JSON.stringify(parsed.errors));
    }
}
var groupExists = "d0d2d25113152200eef2dd828144b0e4";
var groupDoesNotExists = "d0d2d25113152200eef2dd828144b0e4111";
getSavedQueryIdList(groupExists);
getSavedQueryIdList(groupDoesNotExists);
```

Output: \(Line breaks added for formatting.\)

```
succeed to retrieve saved query id list: 5d498532d7c12200de92a5f75e6103ce
fail to retrieve list, errors:
 [{"message":"Group does not exist","error":"GROUP_SYS_ID_IS_NOT_FOUND"}]
```

## CMDBGroupAPI - setManualCIList\(String groupId, String ciSysIds\)

Sets the manual CI list for the specified group. The existing manual CI list is overwritten. CI sysIds not found in the cmdb\_ci table are ignored.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The sysId of the CMDB group.|
|ciSysIds|String|Comma separated list of CI sysIds.|

<table id="table_a53_cnz_kx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td id="CMDBGroupAPI_JSON_output">

A JSON formated string in the format ```
{ 'result':false, 
'errors':[ {'message':'Group does not exist',
            'error':'GROUP_SYS_ID_IS_NOT_FOUND'},
 { } // another error if it exists 
 ], 
'partialCIListDueToACLFlag':false,
'idList':['sys_id_1', 'sys_id2'] }
```

Where -   result - a boolean flag. When true the method was successful.
-   errors - a list of errors with a message and error code.
-   partialCIListDueToACLFlag -  a Boolean flag. When true, the idList is incomplete due to an ACL restriction. When false, the idList is complete.
-   idList - an array of cmdb\_ci sys\_ids

 When not successful, returns one of the errors GROUP\_SYS\_ID\_IS\_NOT\_FOUND, GROUP\_SYS\_ID\_IS\_EMPTY, FAIL\_TO\_INSERT\_GROUP\_CI\_PAIR, FAIL\_TO\_INSERT\_GROUP\_QUERY\_ID\_PAIR, CI\_CAN\_NOT\_FOUND, SAVED\_QUERY\_ID\_NOT\_FOUND, ERROR\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, TIMEOUT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, NOT\_COMPLETE\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, MAX\_LIMIT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, GROUP\_API\_TIMEOUT, EXCEPTION\_FROM\_EXECUTE\_QUERY, SOME\_CI\_NOT\_VISIBLE\_DUE\_TO\_SECURITY\_CONSTRAINT

</td></tr></tbody>
</table>```
// Script example:
var setManualCIListFunc = function(groupSysId, manualCIList) {
    var parser = new JSONParser();
    var response = sn_cmdbgroup.CMDBGroupAPI.setManualCIList(groupSysId, manualCIList);
    var parsed = parser.parse(response);
    if (parsed.result) {
        gs.info("succeed to set manual ci list");
    } else {
        gs.info("fail to set manual ci list, errors: " + JSON.stringify(parsed.errors));
    }
}
var group = "d0d2d25113152200eef2dd828144b0e4";
var groupDoesNotExist = "1234";
var manualCIList = "b4fd7c8437201000deeabfc8bcbe5dc1, affd3c8437201000deeabfc8bcbe5dc3";
setManualCIListFunc(group, manualCIList);
setManualCIListFunc(groupDoesNotExist, manualCIList);
```

Output: \(Line breaks added for formatting.\)

```
succeed to set manual ci list
fail to set manual ci list, errors: [{"message":"Group does not exist","error":
"GROUP_SYS_ID_IS_NOT_FOUND"}]
```

## CMDBGroupAPI - setSavedQueryIdList\(String groupId, String queryIds\)

Sets the saved query ID list for the specified group. The existing query ID list is overwritten. Query sysIds not found in the qb\_saved\_query table are ignored.

|Name|Type|Description|
|----|----|-----------|
|groupId|String|The sysId of the CMDB group.|
|queryIds|String|Comma separated list of saved query sysIds.|

<table id="table_i3d_1qz_kx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

A JSON formated string in the format ```
{ 'result':false, 
'errors':[ {'message':'Group does not exist',
            'error':'GROUP_SYS_ID_IS_NOT_FOUND'},
 { } // another error if it exists 
 ], 
'partialCIListDueToACLFlag':false,
'idList':['sys_id_1', 'sys_id2'] }
```

Where -   result - a boolean flag. When true the method was successful.
-   errors - a list of errors with a message and error code.
-   partialCIListDueToACLFlag -  a Boolean flag. When true, the idList is incomplete due to an ACL restriction. When false, the idList is complete.
-   idList - an array of cmdb\_ci sys\_ids

 When not successful, returns one of the errors GROUP\_SYS\_ID\_IS\_NOT\_FOUND, GROUP\_SYS\_ID\_IS\_EMPTY, FAIL\_TO\_INSERT\_GROUP\_CI\_PAIR, FAIL\_TO\_INSERT\_GROUP\_QUERY\_ID\_PAIR, CI\_CAN\_NOT\_FOUND, SAVED\_QUERY\_ID\_NOT\_FOUND, ERROR\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, TIMEOUT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, NOT\_COMPLETE\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, MAX\_LIMIT\_DURING\_QUERY\_BUILDER\_PROCESS\_QUERY, GROUP\_API\_TIMEOUT, EXCEPTION\_FROM\_EXECUTE\_QUERY, SOME\_CI\_NOT\_VISIBLE\_DUE\_TO\_SECURITY\_CONSTRAINT

</td></tr></tbody>
</table>```
// Script example:
var setSavedQueryIdListFunc = function(groupSysId, queryIdList) {
    var parser = new JSONParser();
    var response = sn_cmdbgroup.CMDBGroupAPI.setSavedQueryIdList(groupSysId, queryIdList);
    var parsed = parser.parse(response);
    if (parsed.result) {
        gs.info("succeed to set saved query id list");
    } else {
        gs.info("fail to set saved query id list, errors: " + JSON.stringify(parsed.errors));
    }
}
var group = "d0d2d25113152200eef2dd828144b0e4";
var savedQueryBuilderIdList = "394585fed7812200de92a5f75e6103e8";
var savedQueryBuilderIdNotExistList = "b4fd7c8437201000deeabfc8bcbe5dc1,
   affd3c8437201000deeabfc8bcbe5dc3";
 
setSavedQueryIdListFunc(group, savedQueryBuilderIdList);
setSavedQueryIdListFunc(group, savedQueryBuilderIdNotExistList);

```

Output: \(Line breaks added for formatting.\)

```
succeed to set saved query id list
fail to set saved query id list, errors: [{"message":
"Saved query id(b4fd7c8437201000deeabfc8bcbe5dc1) is not found for 
group(d0d2d25113152200eef2dd828144b0e4)","error":
"SAVED_QUERY_ID_NOT_FOUND"},{"message":
"Saved query id(affd3c8437201000deeabfc8bcbe5dc3) is not found for 
group(d0d2d25113152200eef2dd828144b0e4)","error":"SAVED_QUERY_ID_NOT_FOUND"}]
```

