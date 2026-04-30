---
title: GlideUser - Scoped
description: The GlideUser API provides methods to access information about the current user and current user roles.Returns the current user's company sys\_id.Returns the current user's display name.Returns the user's email address.Returns the user's first name.Gets the sys\_id of the current user.Returns the user's last name.Returns the user ID, or login name, of the current user.Gets the specified user preference value for the current user.Returns a list of roles that includes explicitly granted roles, inherited roles, and roles acquired by group membership.Returns the list of roles explicitly granted to the user.Returns true if the user has the specified role.Returns true if the user has the specified role or the admin role.Determines if the current user is a member of the specified group.Saves a user preference value to the database.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideUser- Scoped

The GlideUser API provides methods to access information about the current user and current user roles.

Using the GlideUser API avoids the need to use the slower GlideRecord queries to get user information.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideUser - getCompanyID\(\)

Returns the current user's company sys\_id.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Company sys\_id.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getCompanyID());
```

## Scoped GlideUser - getDisplayName\(\)

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

## Scoped GlideUser - getEmail\(\)

Returns the user's email address.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's email address.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getEmail());
```

## Scoped GlideUser - getFirstName\(\)

Returns the user's first name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's first name.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getFirstName());
```

## Scoped GlideUser - getID\(\)

Gets the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's sys\_id.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getID());
```

## Scoped GlideUser - getLastName\(\)

Returns the user's last name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User's last name.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getLastName());
```

## Scoped GlideUser - getName\(\)

Returns the user ID, or login name, of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|User ID or login name.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getName());
```

## Scoped GlideUser - getPreference\(String name\)

Gets the specified user preference value for the current user.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the preference.|

|Type|Description|
|----|-----------|
|String|Preference value.|

```
var currentUser = gs.getUser(); 
currentUser.savePreference(­'myPref','red'); 
gs.info(currentUser.getPreference(­'myPref'));
```

## Scoped GlideUser - getRoles\(\)

Returns a list of roles that includes explicitly granted roles, inherited roles, and roles acquired by group membership.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List of all roles available to the user|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getRoles());
```

## Scoped GlideUser - getUserRoles\(\)

Returns the list of roles explicitly granted to the user.

Unlike the getRoles\(\) method, this method does not return roles the user inherits or roles acquired from group membership.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List of roles explicitly assigned to the user.|

```
var currentUser = gs.getUser(); 
gs.info(currentUser.getUserRoles());
```

## Scoped GlideUser - hasAssignedRole\(String roleName\)

Returns true if the user has the specified role.

<table id="table_o2s_mlp_ldc" class="parameters"><thead><tr><th>

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
</table><table id="table_p2s_mlp_ldc" class="returns"><thead><tr><th>

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

## Scoped GlideUser - hasRole\(String role\)

Returns true if the user has the specified role or the admin role.

|Name|Type|Description|
|----|----|-----------|
|role|String|Checks if the user has this role.|

<table id="table_ik4_5k4_1r" class="returns"><thead><tr><th>

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

## Scoped GlideUser - isMemberOf\(String group\)

Determines if the current user is a member of the specified group.

|Name|Type|Description|
|----|----|-----------|
|group|String|Group to check.|

<table id="table_ock_gl4_1r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user is a member of the specified group.Possible values:

-   true: User is a member of the specified group.
-   false: User isn't a member of the specified group.

</td></tr></tbody>
</table>```
var currentUser = gs.getUser(); 
gs.info(currentUser.isMemberOf(­'Capacity Mgmt'));
```

## Scoped GlideUser - savePreference\(String name, String value\)

Saves a user preference value to the database.

|Name|Type|Description|
|----|----|-----------|
|name|String|Preference to save.|
|value|String|Preference value.|

|Type|Description|
|----|-----------|
|None| |

```
var currentUser = gs.getUser(); 
currentUser.savePreference('myPref','red'); 
gs.info(currentUser.getPreference('myPref'));
```

