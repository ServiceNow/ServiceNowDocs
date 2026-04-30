---
title: GlideUser - Global
description: The GlideUser API provides methods to access information about the current user and current user roles.Returns the current user's company sys\_id.Returns the current user's display name.Returns the display value of the user's session domain.Returns the identifier of the user's current session domain.Returns the user's email address.Returns the user's first name.Returns the sys\_id of the current user.Returns the user's last name.Returns an iterator containing the list of all groups to which the user belongs. Only active groups are returned.Returns the user ID, or login name, of the current user.Returns a list of roles associated with the user. Includes explicitly granted roles, inherited roles, and roles acquired by group membership.Returns the user object associated with the passed-in user ID \(sys\_id in sys\_user\) or user\_name.Returns the list of roles explicitly granted to the user.Returns true if the user has the specified role.Returns true if the user has the specified role or the admin role.Determines if the current user is an explicit member of the specified group. Only active groups are evaluated by this method.Determines if the current user is a member of the specified group. Only active groups are evaluated by this method.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideUser- Global

The GlideUser API provides methods to access information about the current user and current user roles.

Using the GlideUser API avoids the need to use the slower GlideRecord queries to obtain user information.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideUser - getCompanyID\(\)

Returns the current user's company sys\_id.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Company sys\_id|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getCompanyID());
```

### Scoped equivalent

To use the getCompanyID\(\) method in a scoped application, use the corresponding scoped method: [getCompanyID\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getDisplayName\(\)

Returns the current user's display name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's display name|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getDisplayName());
```

### Scoped equivalent

To use the getDisplayName\(\) method in a scoped application, use the corresponding scoped method: [getDisplayName\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getDomainDisplayValue\(\)

Returns the display value of the user's session domain.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The display value of the user's session domain.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getDomainDisplayValue());
```

### Scoped equivalent

There is no workaround for scoped applications.

## GlideUser - getDomainID\(\)

Returns the identifier of the user's current session domain.

The identifier that is returned depends on the domain type and the instantiation of that domain.

-   If the user is configured in the global domain, and does not use the domain picker to switch domains, the method returns null.
-   If the user uses the domain picker to switch to the global domain, the method returns the string "global".
-   For all other domains, the method returns the sys\_id of that domain.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Domain identifier.|

```
var domain = new GlideRecord('domain');
domain.get(gs.getUser().getDomainID());
gs.info(domain.name);
```

## GlideUser - getEmail\(\)

Returns the user's email address.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's email address|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getEmail());
```

### Scoped equivalent

To use the getEmail\(\) method in a scoped application, use the corresponding scoped method: [getEmail\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getFirstName\(\)

Returns the user's first name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_njs_zb3_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object/String

</td><td>

User's first name.**Note:** The data type for the returned value is object, however, the information is returned as a string.

</td></tr></tbody>
</table>```
var currentUser = gs.getUser(); 
var userName = currentUser.getFirstName();
gs.info('User First Name: + userName);
gs.info('Data type: ' + typeof userName);
```

```
*** Script: User First Name: John
*** Script: Data type: object
```

### Scoped equivalent

To use the getFirstName\(\) method in a scoped application, use the corresponding scoped method: [getFirstName\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getID

Returns the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's sys\_id|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getID());
```

### Scoped equivalent

To use the getID\(\) method in a scoped application, use the corresponding scoped method: [getID\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getLastName\(\)

Returns the user's last name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bgq_1g3_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object/String

</td><td>

User's last name.**Note:** The data type for the returned value is object, however, the information is returned as a string.

</td></tr></tbody>
</table>```
var currentUser = gs.getUser(); 
var userName = currentUser.getLastName();
gs.info('User Last Name: + userName);
gs.info('Data type: ' + typeof userName);
```

```
*** Script: User Last Name: Smith
*** Script: Data type: object
```

### Scoped equivalent

To use the getLastName\(\) method in a scoped application, use the corresponding scoped method: [getLastName\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getMyGroups\(\)

Returns an iterator containing the list of all groups to which the user belongs. Only active groups are returned.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|iterator|A list of sys\_ids for the active groups to which the user belongs.|

The following example shows how to return a list of groups the user belongs to.

```
var groupsArray = gs.getUser().getMyGroups().toArray();
gs.info(groupsArray[0]);
```

Output:

```
cfcbad03d711110050f5edcb9e61038f
```

### Scoped equivalent

There is no scoped equivalent for this method.

## GlideUser - getName\(\)

Returns the user ID, or login name, of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User ID|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getName());
```

### Scoped equivalent

To use the getName\(\) method in a scoped application, use the corresponding scoped method: [getName\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getRoles\(\)

Returns a list of roles associated with the user. Includes explicitly granted roles, inherited roles, and roles acquired by group membership.

**Note:** Use hasRole\(\) instead of getRoles\(\) if any session-related role changes occur, like role masking or role delegation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Comma-separated list of user roles.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getRoles());
```

Output:

```
admin,hr_fulfiller,itsa_fulfiller,security_admin
```

### Scoped equivalent

To use the getRoles\(\) method in a scoped application, use the corresponding scoped method: [getRoles\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - getUserByID \(String id\)

Returns the user object associated with the passed-in user ID \(sys\_id in sys\_user\) or user\_name.

|Name|Type|Description|
|----|----|-----------|
|id|String|Unique ID \(sys\_id\) or user\_name of the desired user record.|

|Type|Description|
|----|-----------|
|Object|User object associated with the specified sys\_id or user\_name.|

Example using user name \(user\_name\).

```
var currentUser = gs.getUser();
gs.info(currentUser.getFirstName()); // print the first name of the logged in user
var newUser = currentUser.getUserByID('abel.tuter'); // fetch a different user using the user_name field
gs.info(newUser.getFirstName()); // print the first name of the Abel Tuter user 

```

Example using user ID \(sys\_id\).

```
var currentUser = gs.getUser();
gs.info(currentUser.getFirstName()); // print the first name of the logged in user
var newUser = currentUser.getUserByID('62826bf03710200044e0bfc8bcbe5df1'); // fetch Abel Tuter user using sys_id from sys_user record
gs.info(newUser.getFirstName()); // print the first name of the Abel Tuter user 

```

## GlideUser - getUserRoles\(\)

Returns the list of roles explicitly granted to the user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qkf_xnm_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object/String

</td><td>

List of comma-separated roles explicitly assigned to the user.**Note:** The data type for the returned value is object, however, the information is returned as a string.

</td></tr></tbody>
</table>```
var currentUser = gs.getUser(); 
var userRoles = currentUser.getUserRoles();
gs.info('User Roles: ' + userRoles);
gs.info('Data type: ' + typeof userRoles);
```

```
*** Script: User Roles: ,admin,security_admin
*** Script: Data type: object
```

### Scoped equivalent

To use the getUserRoles\(\) method in a scoped application, use the corresponding scoped method: [getUserRoles\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - hasAssignedRole\(String roleName\)

Returns true if the user has the specified role.

<table id="table_gjw_pcp_ldc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

roleName

</td><td>

String

</td><td>

Checks if the user has this role.**Note:** For the current user, this method checks for the role in their [elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) only if they elevated to that role in the current session. For non current users, this method checks for the role in all of their elevated privilege roles.

</td></tr></tbody>
</table><table id="table_hjw_pcp_ldc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user has the specified role.

 Valid values:

-   true: The user has the specified role.
-   false: The user doesn't have the specified role.

</td></tr></tbody>
</table>This example checks if the current user has the admin role.

```
var currentUser = gs.getUser();
gs.info(currentUser.hasAssignedRole('admin'));
```

Output:

```
true
```

### Scoped equivalent

To use the hasAssignedRole\(\) method in a scoped application, use the corresponding scoped method: [hasAssignedRole\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - hasRole\(String role\)

Returns true if the user has the specified role or the admin role.

**Note:** Use hasRole\(\) instead of getRoles\(\) if any session-related role changes occur, like role masking or role delegation.

|Name|Type|Description|
|----|----|-----------|
|role|String|Checks if the user has this role.|

<table id="table_ymz_mmm_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user has the specified role or the admin role.

 Valid values:

-   true: The user has the specified role or the admin role.
-   false: The user doesn't have the specified role or the admin role.

</td></tr></tbody>
</table>This example checks if the current user has the admin role.

```
var currentUser = gs.getUser(); 
gs.info(currentUser.hasRole('admin'));
```

Output:

```
true
```

### Scoped equivalent

To use the hasRole\(\) method in a scoped application, use the corresponding scoped method: [hasRole\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

## GlideUser - isExplicitMemberOf\(String group\)

Determines if the current user is an explicit member of the specified group. Only active groups are evaluated by this method.

The isMemberOf\(\) method returns true for a parent group if the user is a member of the child group. Use this method if you only want to return true for parent groups.

|Name|Type|Description|
|----|----|-----------|
|group|String|Sys\_id of the user group to check.|

<table id="table_m1q_4lm_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user is an explicit member of the specified group.

 Valid values:

-   true: The current user is an explicit member of the specified group.
-   false: The current user is not an explicit member of the specified group.

</td></tr></tbody>
</table>The following example shows how to check if the current user is an explicit member of the specified group.

```
var isExplMem = gs.getUser().isExplicitMemberOf('b8ef24616fc331003b3c498f5d3ee434');
gs.info(isExplMem);
```

Output:

```
false
```

### Scoped equivalent

There is no scoped equivalent for this method.

## GlideUser - isMemberOf\(String group\)

Determines if the current user is a member of the specified group. Only active groups are evaluated by this method.

This method returns true for a parent group if the user is a member of the child group. Use the isExplicitMemberOf\(\) if you only want to return true for parent groups.

|Name|Type|Description|
|----|----|-----------|
|group|String|Sys\_id of the user group to check.|

<table id="table_m1q_4lm_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user is a member of the specified group.

 Valid values:

-   true: The current user is a member of the specified group.
-   false: The current user is not a member of the specified group.

</td></tr></tbody>
</table>The following example shows how to check if the current user is a member of the specified group.

```
var currentUser = gs.getUser(); 
gs.info(currentUser.isMemberOf(­'Capacity Mgmt'));
```

### Scoped equivalent

To use the isMemberOf\(\) method in a scoped application, use the corresponding scoped method: [isMemberOf\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

