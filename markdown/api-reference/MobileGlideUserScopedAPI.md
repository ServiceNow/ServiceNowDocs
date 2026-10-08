---
title: MobileGlideUser - Scoped
description: The MobileGlideUser API provides a read-only view of the currently logged-in user. An instance is returned by the getUser\(\) method of MobileGlideSystem.Gets the sys\_id of the user's company.Gets the user's display name, as shown throughout the UI.Gets the user's email address.Gets the user's first name.Gets the sys\_id of the currently logged-in user.Gets the user's last name.Gets the sys\_ids of the groups the user is a member of.Gets the user's login name \(username\).Gets the roles the user has been explicitly assigned, not including inherited roles.Gets all roles the user has, including inherited roles.Determines whether the current user has the specified role.Determines whether the current user is a member of the specified group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/MobileGlideUserScopedAPI.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideUser - Scoped

The MobileGlideUser API provides a read-only view of the currently logged-in user. An instance is returned by the getUser\(\) method of MobileGlideSystem.

MobileGlideUser provides a read-only view of the currently logged-in user, returned by the `getUser()` method of [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideSystemScopedAPI.md). It provides access to identity fields such as the sys\_id, user name, and email address, to display information, and to role and group membership checks. It provides a subset of the methods available in the GlideUser API.

A button condition or a write-back action script can use these methods to control behavior based on who the user is. For example, a script can allow an action only for members of a specific group, or hide a field from users who don't have a required role.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getUser()` method of [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideSystemScopedAPI.md).

## MobileGlideUser - getCompanyId\(\)

Gets the sys\_id of the user's company.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the user's company, referencing the core\_company table. Maximum length: 32.|

This example calls getCompanyId.

```
var companyId = mgs.getUser().getCompanyId();
mgs.info(companyId);
```

Output:

```
"31bea3d53790200044e0bfc8bcbe5c3"
```

## MobileGlideUser - getDisplayName\(\)

Gets the user's display name, as shown throughout the UI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's display name, sourced from the sys\_user table's user\_display\_name field. Maximum length: 255.|

This example calls getDisplayName.

```
var displayName = mgs.getUser().getDisplayName();
mgs.info(displayName);
```

Output:

```
"Jordan Alvarez"
```

## MobileGlideUser - getEmail\(\)

Gets the user's email address.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's email address, sourced from the sys\_user table's email field \(maximum length 100\).|

This example calls getEmail.

```
var email = mgs.getUser().getEmail();
mgs.info(email);
```

Output:

```
"jordan.alvarez@example.com"
```

## MobileGlideUser - getFirstName\(\)

Gets the user's first name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's first name, sourced from the sys\_user table's first\_name field. Maximum length: 50.|

This example calls getFirstName.

```
var firstName = mgs.getUser().getFirstName();
mgs.info(firstName);
```

Output:

```
"Jordan"
```

## MobileGlideUser - getID\(\)

Gets the sys\_id of the currently logged-in user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current user. Maximum length: 32.|

This example calls getID.

```
var userId = mgs.getUser().getID();
mgs.info(userId);
```

Output:

```
"62826bf03710200044e0bfc8bcbe5dec"
```

## MobileGlideUser - getLastName\(\)

Gets the user's last name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's last name, sourced from the sys\_user table's last\_name field. Maximum length: 50.|

This example calls getLastName.

```
var lastName = mgs.getUser().getLastName();
mgs.info(lastName);
```

Output:

```
"Alvarez"
```

## MobileGlideUser - getMyGroups\(\)

Gets the sys\_ids of the groups the user is a member of.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of String|List of sys\_user\_group sys\_ids the user belongs to.|

This example calls getMyGroups.

```
var groups = mgs.getUser().getMyGroups();
var inTargetGroup = groups.indexOf('a1b2c3d4e5f6') !== -1;
mgs.info(inTargetGroup);
```

Output:

```
false
```

## MobileGlideUser - getName\(\)

Gets the user's login name \(username\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The user's login name, sourced from the sys\_user table's user\_name field. Maximum length: 40.|

This example calls getName.

```
var loginName = mgs.getUser().getName();
mgs.info(loginName);
```

Output:

```
"employee.smith"
```

## MobileGlideUser - getRoles\(\)

Gets the roles the user has been explicitly assigned, not including inherited roles.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of String|List of role names explicitly assigned to the user. Does not include roles inherited through group membership or role hierarchy.|

This example calls getRoles.

```
var roles = mgs.getUser().getRoles();
mgs.info(roles.join(', '));
```

Output:

```
"itil, catalog_admin"
```

## MobileGlideUser - getUserRoles\(\)

Gets all roles the user has, including inherited roles.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of String|List of all effective role names for the user, including roles inherited through group membership or role hierarchy.|

This example calls getUserRoles.

```
var allRoles = mgs.getUser().getUserRoles();
var isItil = allRoles.includes('itil');
mgs.info(isItil);
```

Output:

```
true
```

## MobileGlideUser - hasRole\(String role\)

Determines whether the current user has the specified role.

|Name|Type|Description|
|----|----|-----------|
|role|String|Name of the role to check, for example, 'itil'.|

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the current user has the specified role. Possible values: true, user has the role; false, user does not have the role.|

This example calls hasRole\_S.

```
var isItil = mgs.getUser().hasRole('itil');
mgs.info(isItil);
```

Output:

```
true
```

## MobileGlideUser - isMemberOf\(String group\)

Determines whether the current user is a member of the specified group.

|Name|Type|Description|
|----|----|-----------|
|group|String|Identifier of the group to check membership against — accepts either the group's sys\_id or its unique name.|

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the current user is a member of the specified group. Possible values: true, user is a member of the group; false, user is not a member of the group.|

This example calls isMemberOf\_S.

```
var inServiceDesk = mgs.getUser().isMemberOf('service_desk');
if (inServiceDesk) {
  mgs.info('User belongs to the Service Desk group');
}
```

Output:

```
"User belongs to the Service Desk group"
```

