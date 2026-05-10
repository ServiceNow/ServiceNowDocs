---
title: GlideUser - Global
description: The GlideUser API provides methods to access information about the current user and current user roles.Returns the current user's company sys\_id.Returns the current user's display name.Returns the display value of the user's session domain.Returns the identifier of the user's current session domain.Returns the user's email address.Returns the user's first name.Returns the sys\_id of the current user.Returns the user's last name.Returns an iterator containing the list of all groups to which the user belongs. Only active groups are returned.Returns the user ID, or login name, of the current user.Returns a list of roles associated with the user. Includes explicitly granted roles, inherited roles, and roles acquired by group membership.Returns the current user's time zone label in the current user's preferred language.Returns the current user's time zone label in the specified language.Returns the user object associated with the passed-in user ID \(sys\_id in sys\_user\) or user\_name.Returns the list of roles explicitly granted to the user.Determines if the current user has the specified role.Determines if the current user is an explicit member of the specified group. Only active groups are evaluated by this method.Determines if the current user is a member of the specified group. Only active groups are evaluated by this method.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
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

## GlideUser - getTimeZoneLabel\(\)

Returns the current user's time zone label in the current user's preferred language.

For more information about setting a user's preferred language, see [User specific language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_UserSpecificLanguage.md).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current user's time zone label.|

This example shows how to return the current user's time zone label in their preferred language.

```
gs.info(gs.getUser().getTimeZoneLabel());
```

Output:

```
Europe/Dublin
```

## GlideUser - getTimeZoneLabelLang\(String language\)

Returns the current user's time zone label in the specified language.

<table id="table_bkc_4w2_bdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

language

</td><td>

String

</td><td>

Language to use for the time zone label. Located in the ID column of the Language \[sys\_language\] table. If a valid language isn't provided, the time zone label is returned in English.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The current user's time zone label.|

This example shows how to return the current user's time zone label in a specified language.

```
gs.info(gs.getUser().getTimeZoneLabelLang("es")); //Spanish
gs.info(gs.getUser().getTimeZoneLabelLang("ja")); //Japanese
gs.info(gs.getUser().getTimeZoneLabelLang("jksjsjks")); //invalid
```

Output:

```
Europa/Dublín
ヨーロッパ/ダブリン
Europe/Dublin
```

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

## GlideUser - hasRole\(String role\)

Determines if the current user has the specified role.

**Note:** Use hasRole\(\) instead of getRoles\(\) if any session-related role changes occur, like role masking or role delegation.

|Name|Type|Description|
|----|----|-----------|
|role|String|Role to check|

|Type|Description|
|----|-----------|
|Boolean|True if the user has the role.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.hasRole('admin'));
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
|group|String|Sys\_id or name of the group to check.|

<table id="table_m1q_4lm_xz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user is a member of the specified group.Possible values:

-   true: User is a member of the group.
-   false: User isn't a member of the group.

</td></tr></tbody>
</table>The following example checks if the current user is a member of the Capacity Mgmt group.

```
var currentUser = gs.getUser(); 
gs.info(currentUser.isMemberOf('Capacity Mgmt'));
```

Output:

```
false
```

### Scoped equivalent

To use the isMemberOf\(\) method in a scoped application, use the corresponding scoped method: [isMemberOf\(\)](../../glideUserScoped/concept/c_GlideUserScopedAPI.md#).

