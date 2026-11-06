---
title: MobileGlideUser - Scoped
description: The MobileGlideUser API provides a read-only view of the currently logged-in user. An instance is returned by the getUser\(\) method of MobileGlideSystem.Gets the sys\_id of the company that the current user belongs to.Gets the display name of the current user, as shown on records and in the app.Gets the email address of the current user.Gets the first name of the current user.Gets the sys\_id of the current user.Gets the last name of the current user.Gets the sys\_ids of the groups that the current user is a member of.Gets the user's login name \(username\).Gets the roles that are directly assigned to the current user. The list does not include inherited roles. To get all roles, use getUserRoles\(\).Gets all roles that the current user has, including roles inherited through group membership or the role hierarchy.Determines whether the current user has a specific role.Determines whether the current user is a member of the specific group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/MobileGlideUserScopedAPI.html
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [Mobile Scripting API reference, API reference, API implementation and reference]
---

# MobileGlideUser - Scoped

The MobileGlideUser API provides a read-only view of the currently logged-in user. An instance is returned by the getUser\(\) method of MobileGlideSystem.

MobileGlideUser provides a read-only view of the currently logged-in user, returned by the `getUser()` method of [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md). It provides access to identity fields such as the sys\_id, user name, and email address, to display information, and to role and group membership checks. It provides a subset of the methods available in the GlideUser API.

A button condition or a write-back action script can use these methods to control behavior based on who the user is. For example, a script can allow an action only for members of a specific group.

Whether a script that calls this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The methods in this class are available in both cases: the mobile client provides its own implementation of the same API surface, so the same script returns the same result in either context. Typical calling contexts include a condition script on a mobile button \(`sys_sg_button`\) and an execution script on a write-back action item or step.

This API contains the following capabilities:

-   Getting user details: [MobileGlideUser - getID\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getDisplayName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getFirstName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getLastName\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getEmail\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getCompanyId\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md)
-   Checking roles: [MobileGlideUser - getRoles\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - getUserRoles\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - hasRole\(String role\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md)
-   Checking group membership: [MobileGlideUser - getMyGroups\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md), [MobileGlideUser - isMemberOf\(String group\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideUserScopedAPI.md)

## API access

This API is registered in the `sn_mobile_scripting` application scope and requires the `mobile_admin` role. It requires the `com.glide.sg.mobile_scripting` plugin, which is enabled by default. The class has no public constructor. Obtain an instance from the `getUser()` method of [mgs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/MobileGlideSystemScopedAPI.md).

## MobileGlideUser - getCompanyId\(\)

Gets the sys\_id of the company that the current user belongs to.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the user's company, from the Companies \[core\_company\] table.|

This example gets the sys\_id of the current user's company and logs it.

```
var companyId = mgs.getUser().getCompanyId();
        mgs.info(companyId);
```

Output:

```
31bea3d53790200044e0bfc8bcbe5c3a
```

This example checks whether a task belongs to the same company as the current user. A button condition can use this check to show a Request transfer button only for tasks from the user's own company.

```
var userCompany = mgs.getUser().getCompanyId();
        var sameCompany = current.getValue('company') === userCompany;
        mgs.info('Show Request transfer button: ' + sameCompany);
```

Output:

```
Show Request transfer button: true
```

## MobileGlideUser - getDisplayName\(\)

Gets the display name of the current user, as shown on records and in the app.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Display name of the current user, from the `user_display_name` field of the User \[sys\_user\] table. Maximum length: 255.|

This example gets the display name of the current user and logs it.

```
var displayName = mgs.getUser().getDisplayName();
        mgs.info(displayName);
```

Output:

```
Jordan Alvarez
```

This example builds a sign-off line that shows both the display name and the login name of the user who completed a job. The display name is for people to read, and the login name identifies the account.

```
var user = mgs.getUser();
        var signoff = 'Completed by ' + user.getDisplayName() + ' (' + user.getName() + ')';
        mgs.info(signoff);
```

Output:

```
Completed by Jordan Alvarez (jordan.alvarez)
```

## MobileGlideUser - getEmail\(\)

Gets the email address of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Email address of the current user, from the `email` field of the User \[sys\_user\] table. Maximum length: 100.|

This example gets the email address of the current user and logs it.

```
var email = mgs.getUser().getEmail();
        mgs.info(email);
```

Output:

```
jordan.alvarez@example.com
```

This example tells the user where a confirmation will be sent, or shows an error if the user has no email address. The nil\(\) check covers both an empty value and a null value.

```
var email = mgs.getUser().getEmail();
        if (mgs.nil(email)) {
        mgs.addErrorMessage('Add an email address to your profile to receive a confirmation.');
        } else {
        mgs.addInfoMessage('A confirmation will be sent to ' + email + '.');
        }
```

Message shown to the user:

```
A confirmation will be sent to jordan.alvarez@example.com.
```

## MobileGlideUser - getFirstName\(\)

Gets the first name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|First name of the current user, from the `first_name` field of the User \[sys\_user\] table. Maximum length: 50.|

This example gets the first name of the current user and logs it.

```
var firstName = mgs.getUser().getFirstName();
        mgs.info(firstName);
```

Output:

```
Jordan
```

This example greets the user by first name, with a greeting that depends on the local time of day.

```
var hour = mgs.nowGlideDateTime().getLocalTime().getHourOfDayLocalTime();
        var greeting = 'Good evening';
        if (hour < 12) {
        greeting = 'Good morning';
        } else if (hour < 18) {
        greeting = 'Good afternoon';
        }
        mgs.addInfoMessage(greeting + ', ' + mgs.getUser().getFirstName() + '.');
```

Message shown to the user:

```
Good afternoon, Jordan.
```

## MobileGlideUser - getID\(\)

Gets the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current user. Maximum length: 32.|

This example gets the sys\_id of the current user and logs it.

```
var userId = mgs.getUser().getID();
        mgs.info(userId);
```

Output:

```
62826bf03710200044e0bfc8bcbe5dec
```

This example assigns a task to the current user and logs the saved value. A write-back action can use this pattern for an Assign to me button.

```
var gr = new MobileGlideRecord('wm_task');
        if (gr.get(current.getValue('sys_id'))) {
        gr.setValue('assigned_to', mgs.getUser().getID());
        gr.update();
        mgs.info('Assigned to: ' + gr.getValue('assigned_to'));
        }
```

Output:

```
Assigned to: 62826bf03710200044e0bfc8bcbe5dec
```

## MobileGlideUser - getLastName\(\)

Gets the last name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Last name of the current user, from the `last_name` field of the User \[sys\_user\] table. Maximum length: 50.|

This example gets the last name of the current user and logs it.

```
var lastName = mgs.getUser().getLastName();
        mgs.info(lastName);
```

Output:

```
Alvarez
```

This example builds a name in last-name-first order, such as for a list that is sorted alphabetically by last name.

```
var user = mgs.getUser();
        var listName = user.getLastName() + ', ' + user.getFirstName();
        mgs.info(listName);
```

Output:

```
Alvarez, Jordan
```

## MobileGlideUser - getMyGroups\(\)

Gets the sys\_ids of the groups that the current user is a member of.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of String|Sys\_ids of the groups, from the Group \[sys\_user\_group\] table, that the current user belongs to.|

This example checks whether the current user belongs to a specific group by the group's sys\_id and logs the result.

```
var groups = mgs.getUser().getMyGroups();
        var inTargetGroup = groups.indexOf('a1b2c3d4e5f60718293a4b5c6d7e8f90') !== -1;
        mgs.info(inTargetGroup);
```

Output:

```
false
```

This example counts the active tasks that are assigned to any of the current user's groups, such as for a My team's tasks list.

```
var groups = mgs.getUser().getMyGroups();
        var gr = new MobileGlideRecord('wm_task');
        gr.addEncodedQuery('active=true^assignment_groupIN' + groups.join(','));
        gr.query();
        var count = 0;
        while (gr.next()) {
        count++;
        }
        mgs.info('Tasks assigned to my groups: ' + count);
```

Output:

```
Tasks assigned to my groups: 5
```

## MobileGlideUser - getName\(\)

Gets the user's login name \(username\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Login name of the current user, from the `user_name` field of the User \[sys\_user\] table. Maximum length: 40.|

This example gets the login name of the current user and logs it.

```
var loginName = mgs.getUser().getName();
        mgs.info(loginName);
```

Output:

```
jordan.alvarez
```

This example builds a file name for an inspection report from the login name and today's date. The login name has no spaces, so it is safe to use in a file name.

```
var fileName = 'inspection_' + mgs.getUser().getName() + '_' + mgs.nowNoTZ().substring(0, 10) + '.txt';
        mgs.info(fileName);
```

Output:

```
inspection_jordan.alvarez_2026-08-26.txt
```

## MobileGlideUser - getRoles\(\)

Gets the roles that are directly assigned to the current user. The list does not include inherited roles. To get all roles, use getUserRoles\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of String|Names of the roles that are directly assigned to the user. The list does not include roles that the user inherits through group membership or the role hierarchy.|

This example gets the roles that are directly assigned to the current user and logs them as a list.

```
var roles = mgs.getUser().getRoles();
        mgs.info(roles.join(', '));
```

Output:

```
itil, catalog_admin
```

This example checks whether a role is directly assigned to the user, as opposed to inherited, such as to diagnose why a user has access.

```
var roles = mgs.getUser().getRoles();
        var isDirect = roles.indexOf('catalog_admin') !== -1;
        mgs.info('catalog_admin assigned directly: ' + isDirect);
```

Output:

```
catalog_admin assigned directly: true
```

## MobileGlideUser - getUserRoles\(\)

Gets all roles that the current user has, including roles inherited through group membership or the role hierarchy.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array of String|Names of all roles that apply to the user, including inherited roles.|

This example gets all roles that the current user has and checks whether the list includes the itil role.

```
var allRoles = mgs.getUser().getUserRoles();
        var isItil = allRoles.indexOf('itil') !== -1;
        mgs.info(isItil);
```

Output:

```
true
```

This example lists the roles that the user inherits, by comparing all roles with the roles that are directly assigned. A script can use this to explain why a user has access to a feature.

```
var user = mgs.getUser();
        var directRoles = user.getRoles();
        var allRoles = user.getUserRoles();
        var inherited = [];
        for (var i = 0; i < allRoles.length; i++) {
        if (directRoles.indexOf(allRoles[i]) === -1) {
        inherited.push(allRoles[i]);
        }
        }
        mgs.info('Inherited roles: ' + inherited.join(', '));
```

Output:

```
Inherited roles: cmdb_read
```

## MobileGlideUser - hasRole\(String role\)

Determines whether the current user has a specific role.

|Name|Type|Description|
|----|----|-----------|
|role|String|Name of the role to check, such as `itil`.|

<table id="table_MGU-hasRole_S_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user has the specified role.Possible values:

-   true: User has the role
-   false: User does not have the role.

</td></tr></tbody>
</table>This example checks whether the current user has the itil role and logs the result.

```
var isItil = mgs.getUser().hasRole('itil');
        mgs.info(isItil);
```

Output:

```
true
```

This example stops a reassignment and shows an error message unless the user is a dispatcher. A write-back action can use this check to limit who can reassign tasks.

```
var user = mgs.getUser();
        if (!user.hasRole('wm_dispatcher')) {
        mgs.addErrorMessage('Only dispatchers can reassign tasks.');
        }
```

Message shown to a user without the role:

```
Only dispatchers can reassign tasks.
```

## MobileGlideUser - isMemberOf\(String group\)

Determines whether the current user is a member of the specific group.

|Name|Type|Description|
|----|----|-----------|
|group|String|Sys\_id or unique name of the group to check.|

<table id="table_MGU-isMemberOf_S_r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user is a member of the specified group.Possible values:

-   true: User is a member of the group.
-   false: User is not a member of the group.

</td></tr></tbody>
</table>This example checks whether the current user is a member of the Service Desk group, by the group's name, and logs a message if so.

```
var inServiceDesk = mgs.getUser().isMemberOf('service_desk');
        if (inServiceDesk) {
        mgs.info('User belongs to the Service Desk group');
        }
```

Output:

```
User belongs to the Service Desk group
```

This example checks group membership by the group's sys\_id. A button condition can use this check to show a Dispatch button only to members of the dispatch group. Using the sys\_id keeps the check working if the group is renamed.

```
var dispatchGroupId = 'b2c3d4e5f60718293a4b5c6d7e8f90a1';
        var canDispatch = mgs.getUser().isMemberOf(dispatchGroupId);
        mgs.info('Show Dispatch button: ' + canDispatch);
```

Output:

```
Show Dispatch button: true
```

