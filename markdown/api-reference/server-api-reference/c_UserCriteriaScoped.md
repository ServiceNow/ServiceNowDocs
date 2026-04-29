---
title: UserCriteria - Scoped
description: The UserCriteria API provides methods to create, modify, and delete user criteria records using scripts.Creates an instance of the UserCriteria class.Creates an instance of the UserCriteria class with the specified sys\_id.Creates a user criteria with specified values in the user\_criteria table. Values specified in columnValues override the values provided via setters.Deletes the current user criteria.Displays the mapping for the attribute and value pairs of the catalog item.Specifies if the user criteria is active.Specifies if the user criteria has an advanced script.Sets the company property for the user criteria.Sets the department property for the user criteria.Sets the group property for the user criteria.Sets the location property for the user criteria.Sets the match\_all property for the user criteria.Sets the name property for the user criteria.Sets the role property for the user criteria.Sets the script for the user criteria.Sets the user property for the user criteria.Updates the current catalog item with the specified values.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# UserCriteria- Scoped

The UserCriteria API provides methods to create, modify, and delete user criteria records using scripts.

To use this class in a scoped application, use the `sn_uc` namespace identifier. The User Criteria Scoped API plugin \(ID: com.glideapp.user\_criteria.scoped.api\) must be enabled to access this API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## UserCriteria - UserCriteria\(\)

Creates an instance of the UserCriteria class.

```
var uc = new sn_uc.UserCriteria();
```

## UserCriteria - UserCriteria\(String sys\_id\)

Creates an instance of the UserCriteria class with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|sys\_id of the user criteria.|

```
var uc = new sn_uc.UserCriteria("31bea3d53790200044e0bfc8bcbe5dec");
```

## UserCriteria - create\(Object columnValues, Boolean standardUpdate\)

Creates a user criteria with specified values in the user\_criteria table. Values specified in columnValues override the values provided via setters.

|Name|Type|Description|
|----|----|-----------|
|columnValues|Object|Key and value pairs for a column and its value.|
|standardUpdate|Boolean|Set to true to enable the running of engines and workflow.|

|Type|Description|
|----|-----------|
|String|sys\_id of the created user criteria.|

```
var uc = new sn_uc.UserCriteria(); 
uc.setCompanies("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89");
uc.setActive(true); 
uc.setUsers("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89");
var UserCriteriaId = uc.create();
gs.info(UserCriteriaId);
```

Output:

```
41bea3d53790200044e0bfc8bcbe5dec
```

## UserCriteria - deleteRecord\(\)

Deletes the current user criteria.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_frq_jlf_vz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

If true, the user criteria is deleted.If false, no user criteria is found to delete.

</td></tr></tbody>
</table>```
var uc = new sn_uc.UserCriteria("31bea3d53790200044e0bfc8bcbe5dec");
uc.deleteRecord();
```

Output:

```
true
```

## UserCriteria - read\(String columns\)

Displays the mapping for the attribute and value pairs of the catalog item.

|Name|Type|Description|
|----|----|-----------|
|columns|String|Array of catalog item attributes.|

|Type|Description|
|----|-----------|
|Object|Mapping for the attribute and value pairs of the catalog item.|

```
var uc = new sn_uc.UserCriteria("7b8a6927ef732100438236caa5c0fb89");
var obj = uc.read(["company","name"]);
gs.info(JSON.stringify(obj));
```

Output:

```
Script: {"name":"All ACME Corporation employees","company":"e7c1f3d53790200044e0bfc8bcbe5deb,227cdfb03710200044e0bfc8bcbe5d6b,86c1f3193790200044e0bfc8bcbe5d95,98c37b193790200044e0bfc8bcbe5dbe,81f95197ac1d55eb35432fd1e068385e,df7d53303710200044e0bfc8bcbe5dac,81fdf9ebac1d55eb4cb89f136a082555,4b7d13f03710200044e0bfc8bcbe5db6,81f87336ac1d55eb06002def816d139f,81fbfe03ac1d55eb286d832de58ae1fd,81fca4cbac1d55eb355b4b6db0e3c80f,187d13f03710200044e0bfc8bcbe5df2,81fd65ecac1d55eb42a426568fc87a63,31bea3d53790200044e0bfc8bcbe5dec,81f75fcaac1d55eb2b0781d6f2c3c260"}
```

## UserCriteria - setActive\(Boolean active\)

Specifies if the user criteria is active.

<table id="table_lc1_x3f_vz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Boolean

</td><td>

If true, the user criteria is active. If false, the user criteria is inactive.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setActive(true); 

```

## UserCriteria - setAdvanced\(boolean advanced\)

Specifies if the user criteria has an advanced script.

<table id="table_eps_xff_vz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

advanced

</td><td>

Boolean

</td><td>

If true, the user criteria has an advanced script.If false, the user criteria does not have an advanced script.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setAdvanced(true); 

```

## UserCriteria - setCompanies\(String companies\)

Sets the company property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|companies|String|Comma-separated list of the company sys\_ids to be set for the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setCompanies("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89"); 

```

## UserCriteria - setDepartments\(String departments\)

Sets the department property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|departments|String|Comma-separated list of the department sys\_ids to be set for the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setDepartments("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89"); 

```

## UserCriteria - setGroups\(String groups\)

Sets the group property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|groups|String|Comma-separated list of the group sys\_ids to be set for the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setGroups("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89"); 

```

## UserCriteria - setLocations\(String locations\)

Sets the location property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|locations|String|Comma-separated list of the location sys\_ids to be set for the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setLocations("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89"); 

```

## UserCriteria - setMatchAll\(Boolean match\_all\)

Sets the match\_all property for the user criteria.

<table id="table_wvg_gkf_vz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

match\_all

</td><td>

If true, all conditions set as properties for the user criteria should be fulfilled. If false, at least one condition set as a property for the user criteria should be fulfilled.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setMatchAll(true); 

```

## UserCriteria - setName\(String name\)

Sets the name property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setName("Property1"); 

```

## UserCriteria - setRoles\(String roles\)

Sets the role property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|roles|String|Comma-separated list of the role sys\_ids to be set for the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setRoles("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89"); 

```

## UserCriteria - setScript\(String script\)

Sets the script for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|script|String|Script to be set for the advanced user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setScript("function scriptTest() {
  var retVal;
  if (gs.getUser().getRecord().getDisplayValue('department') == 'Product Management') {
      retVal = true;
  } else {
      retVal = false;
  }
  return retVal;
}"); 

```

## UserCriteria - setUsers\(String users\)

Sets the user property for the user criteria.

|Name|Type|Description|
|----|----|-----------|
|users|String|Comma-separated list of the user sys\_ids to be set for the user criteria.|

|Type|Description|
|----|-----------|
|void| |

```
var uc = new sn_uc.UserCriteria();
uc.setUsers("31bea3d53790200044e0bfc8bcbe5dec,0c441abbc6112275000025157c651c89"); 

```

## UserCriteria - update\(Object columnValues, String reason\)

Updates the current catalog item with the specified values.

|Name|Type|Description|
|----|----|-----------|
|columnValues|Object|Mapping for the column name and the value pairs.|
|reason|String|Reason for updating the catalog item.|

|Type|Description|
|----|-----------|
|String|Returns the sys\_id of the created user criteria.|

```
var uc = new sn_uc.UserCriteria();
uc.update("name": "Updated name", "The existing name is not relevant. Setting a relevant name"); 

```

Output:

```
31bea3d53790200044e0bfc8bcbe5dec
```

