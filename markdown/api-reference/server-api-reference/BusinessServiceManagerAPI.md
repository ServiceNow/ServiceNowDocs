---
title: BusinessServiceManager - Global
description: The BusinessServiceManager API provides methods that unify service management by converting manually-created services to application services, populating application services, and adding/removing configuration items and connections.Instantiates a BusinessServiceManager object.Adds a CI to a manually-created application service.Adds an entry point to the application service and starts discovery on the entry point.Adds a new entry point without starting discovery.Adds a manually created connection to an application service.Checks the roles of a specified user and the permissions data configured for a specified service/service group and returns a Boolean value that indicates whether the user can view the service/service group.Converts a manual service to an application service.Populates an application service with relations and CIs from the designated entry point.Removes a manually created CI from an application service.Removes an existing entry point from the application service.Removes a manually created connection and the connected CI from an application service.Updates an existing entry point in the application service.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# BusinessServiceManager- Global

The BusinessServiceManager API provides methods that unify service management by converting manually-created services to application services, populating application services, and adding/removing configuration items and connections.

Use BusinessServiceManager methods in global server scripts. You must have the Application Service administrator \[app\_service\_admin\] role to call this API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## BusinessServiceManager - BusinessServiceManager\(\)

Instantiates a BusinessServiceManager object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var bsManager = new SNC.BusinessServiceManager();
```

## BusinessServiceManager - addCI\(String service\_id, String source\_id, String target\_id\)

Adds a CI to a manually-created application service.

|Name|Type|Description|
|----|----|-----------|
|service\_id|String|Sys\_id of the application service to add a CI to. Must be of type cmdb\_ci\_service\_discovered.|
|source\_id|String|Sys\_id of the CI whose outgoing connection joins the target CI.|
|target\_id|String|Sys\_id of the CI to add to the service. Cannot be an excluded item. Excluded items are CIs configured in the Manual CI Inclusions/Exclusions \[svc\_manual\_ci\_exclusions\_inclusions.list\] table.|

|Type|Description|
|----|-----------|
|void| |

```
//Application service is 'PeopleSoft Portals'
//Source CI is windows server 'PS Apache01'
//Target CI is 'SAP WEB01'

var bsManager = new SNC.BusinessServiceManager();
var appService = bsManager.addCI('2fce42d80a0a0bb4004af34d7e3984c8','3a27d4370a0a0bb4006316812bf45439', '3a6cadc1c0a8ce01001f1e5d0d7d68fa');
```

### Add a new entry point

Use the addCI\(\) method to add a new entry point to a service by providing the following parameter values in your request:

-   Provide the service\_ID as normal.
-   Leave the source\_ID value empty. For example, use `''`.
-   For target\_ID, enter the Sys ID of the CI under which to add the new entry point.

As a result, the addCI\(\) method creates a new entry point with a connection to the specified target CI. The following is an example of how to add a new entry point:

```
//Application service sys_id is '49de2b3187cd9d50d5c8a6880cbb35ea' 
//Source CI is passed as an empty string as '' 
//Target CI sys id is '15ca5fb187129910d5c8a6880cbb3537'   

var bsManager = new SNC.BusinessServiceManager(); 
var appService = bsManager.addCI('49de2b3187cd9d50d5c8a6880cbb35ea','', '15ca5fb187129910d5c8a6880cbb3537');
```

## BusinessServiceManager - addEntryPoint\(serviceId, endpointGr\)

Adds an entry point to the application service and starts discovery on the entry point.

|Name|Type|Description|
|----|----|-----------|
|serviceId|Sting|Sys\_id of the application service to add the connection to.|
|endpointGr|String|Glide Record object in the CI Endpoint \[cmdb\_ci\_endpoint\] table or its child table to add to the application service.|

<table id="table_dlj_sw2_zwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating the entry point was successfully added to the application service.

 Possible values:

-   true: the addition was successful.
-   false: the addition was not successful.

</td></tr></tbody>
</table>The following addEntryPoint\(\) method shows how to add a new entry point to the application service.

```
var now_GR = new GlideRecord("cmdb_ci_endpoint_tcp");
now_GR.initialize(); 
now_GR.setValue("host", "10.196.39.251");
now_GR.setValue("port", "8080");
now_GR.insert();
var bsManager = new SNC.BusinessServiceManager();
var serviceId = "5bf65ebeedb91300964f6fa662989533";
bsManager.addEntryPoint(serviceId,now_GR);

```

Output:

```
true
```

## BusinessServiceManager - addEntryPointWithoutStartDiscovery\(serviceId, endpointGr\)

Adds a new entry point without starting discovery.

|Name|Type|Description|
|----|----|-----------|
|serviceId|String|Sys\_id of the application service to add the connection to.|
|endpointGr|String|Glide Record object in the CI Endpoint \[cmdb\_ci\_endpoint\] table or its child table to add to the application service.|

<table id="table_bt2_252_zwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating the entry point was successfully added to the application service.

 Possible values:

-   true: the addition was successful.
-   false: the addition was not successful.

</td></tr></tbody>
</table>The following example shows how to use the addEntryPointWithoutStartDiscovery\(\) method to add a new entry point to the application service without initiating discovery.

```
var now_GR = new GlideRecord("cmdb_ci_endpoint_tcp");
now_GR.initialize(); 
now_GR.setValue("host", "10.196.39.251");
now_GR.setValue("port", "8080");
now_GR.insert();
var bsManager = new SNC.BusinessServiceManager();
var serviceId = "5bf65ebeedb91300964f6fa662989533";
bsManager.addEntryPointWithoutStartDiscovery(serviceId,now_GR);

```

Output:

```
true
```

## BusinessServiceManager - addManualConnection\(String source\_id, Object manual\_endpoint, String service\_id\)

Adds a manually created connection to an application service.

|Name|Type|Description|
|----|----|-----------|
|source\_id|String|Sys ID of the CI to add to the connection.|
|manual\_endpoint|Object|GlideRecord object in the cmdb\_ci\_endpoint\_manual table to add to the application service.|
|service\_id|String|Sys ID of the application service to add the connection to.|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord("cmdb_ci_endpoint_manual");
now_GR.initialize(); 
now_GR.name='myEndpoint'; 
now_GR.insert();

var bsManager = new SNC.BusinessServiceManager();
var appService = bsManager.addManualConnection("3a307c930a0a0bb400353965d0b8861f", now_GR, "2fce42d80a0a0bb4004af34d7e3984c8");
```

## BusinessServiceManager - isReadingPermitted\(Object gr, String userSysID\)

Checks the roles of a specified user and the permissions data configured for a specified service/service group and returns a Boolean value that indicates whether the user can view the service/service group.

The following defines the process flow that the method uses to determine whether the user can view the service/service group:

1.  If the specified record is a service group, checks the user roles and group policy. For more information on assigned roles for service groups, see [Assign a role to a service group](https://www.servicenow.com/docs/access?context=t_EMAssignRoleSvcGroup&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
2.  If the roles list contains “itil” but doesn’t contain “app\_service\_admin” and “sam\_core\_user”, return true.
3.  If the roles list contains “maint”, return true.
4.  If the roles list contains “app\_serivce\_user” but doesn’t contain “app\_service\_admin” and “sm\_app\_owner”, and the service isn’t operational, return false.
5.  Check the group of the service.
    1.  If the service belongs to a single group, and the group is “all”, return true.
    2.  For any non “all” group, checks the policy for user roles and group based on the rules specified in [Assign a role to a service group](https://www.servicenow.com/docs/access?context=t_EMAssignRoleSvcGroup&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US). If any of them returns true, return true.

<table id="table_snj_253_kyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

gr

</td><td>

GlideRecord

</td><td>

GlideRecord of the service/service group. This GlideRecord can be from one of the following tables:-   Application Service \[cmdb\_ci\_service\_auto\]
-   Application Service Group \[cmdb\_ci\_service\_group\]
-   Dynamic CI Group \[cmdb\_ci\_query\_based\_service\]
-   Manual Services \[cmdb\_ci\_service\_manual\]
-   Mapped Application Service \[cmdb\_ci\_service\_discovered\]
-   Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

userSysId

</td><td>

String

</td><td>

Sys\_id of the user record. Located in the User \[sys\_user\] table.

</td></tr></tbody>
</table><table id="table_tnj_253_kyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user has permission to view the specified service/service group.Possible values:

-   true: User can view the specified service/service group.
-   false: User can't view the specified service/service group.

</td></tr></tbody>
</table>The following code example shows how to call this method to check the specified user's ability to access the specified service group.

```
var cmdbServGr = new GlideRecord('cmdb_ci_service_discovered');
cmdbServGr.addQuery('sys_id', "123123123123123123123123");
cmdbServGr.query();
var userId = gs.getUserID();

var bsManager = new SNC.BusinessServiceManager();
while (cmdbServGr.next()) {
  var answer = bsManager.isReadingPermitted(cmdbServGr, userId);

  //do something with / according to the answer

}
```

## BusinessServiceManager - migrateManualToApplicationService\(String service\_id\)

Converts a manual service to an application service.

|Name|Type|Description|
|----|----|-----------|
|service\_id|String|Sys ID of the manual service to convert.|

|Type|Description|
|----|-----------|
|Boolean|True if the migration to an application service succeeds.|

```
var bsManager = new SNC.BusinessServiceManager();
var appService = bsManager.migrateManualToApplicationService("451047c6c0a8016400de0ae6df9b9d76");
```

## BusinessServiceManager - populateApplicationService\(String service\_id, Number levels, String black\_listed\_relation\_types\)

Populates an application service with relations and CIs from the designated entry point.

|Name|Type|Description|
|----|----|-----------|
|service\_id|String|Sys ID of the application service to populate.|
|levels|Number|Number of levels of CIs to add from the CMDB.|
|black\_listed\_relation\_types|String|Relation types to exclude when populating the application service.|

|Type|Description|
|----|-----------|
|Boolean|True if the operation is successful.|

```
var bsManager = new SNC.BusinessServiceManager();
var appService = bsManager.populateApplicationService("5bf65ebeedb91300964f6fa662989533", 10, "Depends on::Used by");
```

## BusinessServiceManager - removeCI\(String service\_id, String target\_id\)

Removes a manually created CI from an application service.

<table id="table_bcz_py1_sdb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

service\_id

</td><td>

String

</td><td>

Sys ID of the application service to remove a CI from.

 **Note:** Passing a GlideRecord object is also supported.

</td></tr><tr><td>

target\_id

</td><td>

String

</td><td>

Sys ID of the CI to remove from the application service.

 **Note:** Passing a GlideRecord object is also supported.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var bsManager = new SNC.BusinessServiceManager();
var appService = bsManager.removeCI("2fce42d80a0a0bb4004af34d7e3984c8", "3a290cc60a0a0bb400000bdb386af1cf");
```

## BusinessServiceManager - removeEntryPoint\(serviceId, endpointSysId\)

Removes an existing entry point from the application service.

|Name|Type|Description|
|----|----|-----------|
|serviceId|String|Sys\_id of the application service to add the connection to.|
|endpointSysId|String|Sys\_id of the entry point endpoint to remove.|

<table id="table_yj2_n32_zwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating that the entry point was successfully removed from the application service.

 Possible values:

-   true: the update was successful.
-   false: the update was not successful.

</td></tr></tbody>
</table>The following example removes the entry point associated with Sys\_id “aa65ebeedb91300964f6fa6629895ss” from the given application service.

```
var bsManager = new SNC.BusinessServiceManager();
var serviceId = "5bf65ebeedb91300964f6fa662989533";
var entrypointId = “aa65ebeedb91300964f6fa6629895ss”;
bsManager.removeEntryPoint(serviceId, entrypointId);

```

Output:

```
true
```

## BusinessServiceManager - removeManualConnection\(String source\_id, String endpoint\_id, String service\_id\)

Removes a manually created connection and the connected CI from an application service.

|Name|Type|Description|
|----|----|-----------|
|source\_id|String|Sys ID of the CI connected to the endpoint.|
|endpoint\_id|String|Sys ID of the manually created connection to remove from the application service|
|service\_id|String|Sys ID of the application service to remove the connection from.|

|Type|Description|
|----|-----------|
|void| |

```
var bsManager = new SNC.BusinessServiceManager();
var appService = bsManager.removeManualConnection("3a307c930a0a0bb400353965d0b8861f", "60ce3176edb91300964f6fa6629895d1", "2fce42d80a0a0bb4004af34d7e3984c8");
```

## BusinessServiceManager - updateEntryPoint\(serviceId, endpointGr\)

Updates an existing entry point in the application service.

|Name|Type|Description|
|----|----|-----------|
|serviceId|String|Sys\_id of the application service to add the connection to.|
|endpointGr|Object|Glide Record object in the CI Endpoint \[cmdb\_ci\_endpoint\] table or its child table to add to the application service.|

<table id="table_pht_422_zwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag indicating the update was successfully applied to the entry point.

 Possible values:

-   true: the update was successful.
-   false: the update was not successful.

</td></tr></tbody>
</table>The following updateEntryPoint\(\) example shows how to update the connection with a new entry point.

```
var now_GR = new GlideRecord("cmdb_ci_endpoint_http");
now_GR.get(“11f65ebeedb91300964f6fa66298951”);
now_GR.setValue(“protocol”, “https”);
var bsManager = new SNC.BusinessServiceManager();
var serviceId = "5bf65ebeedb91300964f6fa662989533";
bsManager.updateEntryPoint(serviceId,now_GR);

```

Output:

```
true
```

