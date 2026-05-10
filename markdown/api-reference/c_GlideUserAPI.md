---
title: GlideUser - Client
description: The GlideUser API provides methods that access information about the current user and current user roles. Using this API avoids the need to use the slower GlideRecord queries to get user information.The current user's first name.Returns a client value set using setClientData\(\) or GlideSession -- putClientData\(\).Returns the first and last name of the current user.Returns true if the current user has the specified role or the admin role.Determines whether the current user has the specified role.Returns true if the current user has at least one of the specified roles or has the admin role.Returns true if the current user has any role.The current user's last name.Sets a client value that you can retrieve using getClientData\(\).The current user's username, for example gsmith02. It is not the user's name, for example George Smith.Returns the sys\_id of the current user.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideUser - Client

The GlideUser API provides methods that access information about the current user and current user roles. Using this API avoids the need to use the slower GlideRecord queries to get user information.

GlideUser methods and properties are accessed through a global object \(`g_user`\) that is only available in client scripts.

This API:

-   contains name and role information about the current user.
-   is typically used in client scripts and UI policies but is also found in UI actions that run on the client.
-   cannot be used in business rules or UI actions that run on the server.

Session information about the current user and current user roles is contained in the client \(web browser\). All GlideUser methods except getClientData\(\) access the session information that is available by default. The getClientData\(\) method requires setup on the server and use of the putClientData\(\) method to make session information available.

For information on using client-side scripts, see [Introduction to Client-side Scripting](https://developer.servicenow.com/dev.do#!/learn/courses/sandiego/app_store_learnv2_scripting_rome_scripting_in_servicenow/app_store_learnv2_scripting_rome_client_side_scripting/app_store_learnv2_scripting_rome_introduction_to_client_side_scripting).

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideUser - firstName

The current user's first name.

|Name|Type|Description|
|----|----|-----------|
|firstName|String|Current user's first name.|

```
alert('first name = ' + g_user.firstName);
```

## GlideUser - getClientData\(String key\)

Returns a client value set using setClientData\(\) or GlideSession -- putClientData\(\).

Session client data is a set of named strings that may be setup on the server using [GlideSession -- putClientData\(\)](../../GlideSessionScoped/concept/c_GlideSessionScopedAPI.md#). You can use getClientData\(\) during form load time to get information that the client script needs to make decisions about the form. For example, to identify which fields should be visible.

See also [GlideForm](../../GlideForm/concept/c_GlideFormAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the client data to retrieve.|

|Type|Description|
|----|-----------|
|String|Value of the client data.|

```
var loginLanguage = g_user.getClientData("loginlanguage");
```

## GlideUser - getFullName\(\)

Returns the first and last name of the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current user's full name.|

```
var formalName = g_user.getFullName();
```

## GlideUser - hasRole\(String role, Boolean includeDefaults\)

Returns true if the current user has the specified role or the admin role.

<table id="table_p1w_4m3_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

role

</td><td>

String

</td><td>

Role to check.

</td></tr><tr><td>

includeDefaults

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include default roles, such as snc\_internal and snc\_external, in the request. For additional information on roles, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/exploring-user-administration.md). Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Boolean|Returns true if the current user has the specified role or the admin role; otherwise returns false.|

```
var isInternal = g_user.hasRole('snc_internal', true);
```

```
var isItil = g_user.hasRole('itil');
```

## GlideUser - hasRoleExactly\(String role, Boolean includeDefaults\)

Determines whether the current user has the specified role.

<table id="table_r53_hn3_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

includeDefaults

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include default roles, such as snc\_internal and snc\_external, in the request. For additional information on roles, see [Explicit roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/explicit-roles.md).

Default: false

</td></tr><tr><td>

role

</td><td>

String

</td><td>

Role to check.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Boolean|Returns true if the current user has the specified role.|

```
var isInternal = g_user.hasRoleExactly('snc_internal', true);
```

```
var isItil = g_user.hasRoleExactly('itil');
```

## GlideUser - hasRoleFromList\(String roles, Boolean includeDefaults\)

Returns true if the current user has at least one of the specified roles or has the admin role.

<table id="table_oxf_wn3_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

roles

</td><td>

String

</td><td>

Comma-separated list of roles to check

</td></tr><tr><td>

includeDefaults

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include default roles, such as snc\_internal and snc\_external, in the request. For additional information on roles, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/exploring-user-administration.md). Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Boolean|Returns true if the current user has a role in the list or the admin role.|

```
var isOK = g_user.hasRoleFromList("itil, maint");
```

```
var isOK = g_user.hasRoleFromList("itil, maint, snc_internal", true);
```

## GlideUser - hasRoles\(Boolean includeDefaults\)

Returns true if the current user has any role.

<table id="table_ups_k43_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

includeDefaults

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to include default roles, such as snc\_internal and snc\_external, in the request. For additional information on roles, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/exploring-user-administration.md). Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Boolean|Returns true if the current user has at least one role.|

```
var yesRole = g_user.hasRoles();
```

```
var yesRole = g_user.hasRoles(true);
```

## GlideUser - lastName

The current user's last name.

|Name|Type|Description|
|----|----|-----------|
|lastName|String|Current user's last name.|

```
alert('last name = ' + g_user.lastName);
```

## GlideUser - setClientData\(String key, String value\)

Sets a client value that you can retrieve using getClientData\(\).

See also [GlideForm](../../GlideForm/concept/c_GlideFormAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the client data to store as a key.|
|value|Number|Value to assign to the key.|

|Type|Description|
|----|-----------|
|None| |

```
function onSubmit() {
	
	if (!g_user.getClientData('keyName')) {
		var now_GR = new GlideRecord('incident');
		now_GR.addActiveQuery();
		now_GR.setLimit(1);
		now_GR.query(cb);
		return false;
	}
	return true;
}

function cb(now_GR) {
	// <insert glide operation >
	g_user.setClientData('keyName', now_GR.getValue('<number>'));
	g_form.submit();	
}
```

## GlideUser - userName

The current user's username, for example gsmith02. It is not the user's name, for example George Smith.

|Name|Type|Description|
|----|----|-----------|
|userName|String|Current user's username.|

```
var userName = g_user.userName;
   alert('Current user = ' + userName);
```

## GlideUser - userID

Returns the sys\_id of the current user.

|Name|Type|Description|
|----|----|-----------|
|userID|String|Sys\_id of the current user.|

```
var userID = g_user.userID;
   alert('Current user ID = ' + userID);
```

