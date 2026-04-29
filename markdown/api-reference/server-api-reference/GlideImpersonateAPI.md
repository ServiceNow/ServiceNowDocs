---
title: GlideImpersonate - Global
description: The GlideImpersonate API enables administrators to pose as another authenticated user for testing purposes.Verifies whether the specified user can perform debugging on scripts.Verifies whether the current user can impersonate the specified user.Sets the user ID for the current administrator to the passed-in user ID, enabling the administrator to act as that user.Determines whether the current user is impersonating another user.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideImpersonate- Global

The GlideImpersonate API enables administrators to pose as another authenticated user for testing purposes.

Use this API when you need to act as another user so to test functionality within your application. When impersonating another user, the administrator has access to exactly what the impersonated user would have access to in the system, including the same menus and modules.

**Note:** The system records anything the administrator does while impersonating another user as having been done by that user.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideImpersonate - canDebug\(String userSysId\)

Verifies whether the specified user can perform debugging on scripts.

In order for a user to be able to debug scripts, they must be on a developer instance. Debugging is not allowed on production instances.

|Name|Type|Description|
|----|----|-----------|
|userSysId|String|sys\_Id of the user to verify for debugging capability.|

<table id="table_wlb_std_t1b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

True: User is able to debug the application. False: User is not able to debug the application.

</td></tr></tbody>
</table>```
userDebug: function(userId) {
  var impUser = new GlideImpersonate();
  impUser.canDebug(userId);
 }
```

## GlideImpersonate - canImpersonate\(String userSysId\)

Verifies whether the current user can impersonate the specified user.

If the current user is not assigned the admin role, the user to impersonate is inactive, or there are other issues with impersonating the specified user, the method returns "false" and the user cannot be impersonated.

|Name|Type|Description|
|----|----|-----------|
|userSysId|String|sys\_Id of the user to impersonate|

<table id="table_g2t_w4d_t1b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user can impersonate the specified user.Possible values:

-   true: Current user can impersonate the specified user.
-   false: Current user cannot impersonate the specified user.

</td></tr></tbody>
</table>```
function onlineImpersonate(userSysId) {
  if (!GlideImpersonate().canImpersonate(userSysId)){
    gs.addInfoMessage("No access to impersonate " + userSysId);
  } else {
    GlideImpersonate().impersonate(userSysId);
  }
  return;
}
```

## GlideImpersonate - impersonate\(String userSysId\)

Sets the user ID for the current administrator to the passed-in user ID, enabling the administrator to act as that user.

When impersonating another user, the administrator has access to exactly what the impersonated user would have access to in the system, including the same menus and modules. Only use this method when testing functionality in an application. Ensure that once you are finished impersonating a user that you call the method again with the administrator sys\_Id to stop the impersonation.

|Name|Type|Description|
|----|----|-----------|
|userSysId|String|Sys\_id of the user to impersonate.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the user that was logged in prior to the impersonation request.|

The following example shows how to get the current user object.

```
var user = gs.getUserDisplayName();
gs.print ("The current user display name is: " + user);

var impUser = new GlideImpersonate();
impUser.impersonate("62826bf03710200044e0bfc8bcbe5df1");
var user = gs.getUserDisplayName();
gs.print ("The impersonated user display name is: " + user);
```

Output:

```
The current user display name is: System Administrator
The impersonated user display name is: Abel Tuter
```

## GlideImpersonate - isImpersonating\(\)

Determines whether the current user is impersonating another user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_mrd_nwd_t1b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

True: User is currently impersonating another user.False: User is not currently impersonating another user.

</td></tr></tbody>
</table>```
function abortOnImpersonate() {
    if (GlideImpersonate().isImpersonating()){
  current.setAbortAction(true);
  gs.addInfoMessage("Transaction canceled due to Impersonation");
    }
    return;
}
```

