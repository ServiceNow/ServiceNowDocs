---
title: PreferenceDestination - Scoped, Global
description: The PreferenceDestination API updates user notification preferences.Returns the channel that is used to send notifications to the destination.Returns the identifier for the destination.Returns the type of destination, such as personal email or work email.Checks if the destination has permission to receive a notification.Checks if a notification overrides a user's preferences for the destination.Sets the user preference for a destination to receive or not receive notifications.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PreferenceDestination - Scoped, Global

The PreferenceDestination API updates user notification preferences.

A notification destination is somewhere that a notification can be delivered to, such as a specific email address or phone number. This API is based on notifications from the Notification \[sys\_notification\] table. Notifications are sent through channels such as email or Workspace. A channel can be used to send notifications to multiple types of destinations. For example, an email channel could send notifications to both personal email and work email destinations. Destination types are listed in the Notification Destination Type \[sys\_notif\_destination\_type\] table.

A user can update their own notification preferences, and an admin can update notification preferences for any user. User notification preferences control which destinations will receive which notifications.

Use this API with the [Preferences](../../Preferences/concept/PreferencesBothAPI.md#) API. Before calling any methods in this class, you must call the Preferences.getDestinations\(\) or Preferences.getDestinationsByChannel\(\) methods to instantiate a PreferenceDestination object.

This class uses the `sn_notification` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PreferenceDestination - getChannel\(\)

Returns the channel that is used to send notifications to the destination.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord from the Notification Channel \[sys\_notification\_channel\] table for the channel that is used to send notifications to the destination.|

This example prints the channel that is used to send notifications for each of Abel Tuter's destinations.

```
var recipient = new GlideRecord('sys_user');
recipient.get('last_name', 'Tuter');
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
for (var i=0; i<dests.length; i++) {
     gs.print('Channel for destination '+(i+1)+' is '+dests[i].getChannel().name); 
}
```

Output:

```
Channel for destination 1 is Workspace
```

## PreferenceDestination - getDeliverTo\(\)

Returns the identifier for the destination.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Identifier for the destination. For example, an email address, push application install token, or sys\_id.|

This example prints the identifier for each of Abel Tuter's destinations. The output shows that the identifier for Abel's Workspace destination is the user sys\_id.

```
var recipient = new GlideRecord('sys_user');
recipient.get('last_name', 'Tuter');
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
for (var i=0; i<dests.length; i++) {
     gs.print('The identifier for '+recipient.first_name+'\'s '+dests[i].getDestinationType().name+' destination is '+dests[i].getDeliverTo());
}
```

Output:

```
The identifier for Abel's Workspace destination is 62826bf03710200044e0bfc8bcbe5df1
```

## PreferenceDestination - getDestinationType\(\)

Returns the type of destination, such as personal email or work email.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord from the Notification Destination Type \[sys\_notif\_destination\_type\] table for the destination type.|

This example prints the identifier for each of Abel Tuter's destinations. The output shows that the identifier for Abel's Workspace destination is the user sys\_id.

```
var recipient = new GlideRecord('sys_user');
recipient.get('last_name', 'Tuter');
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
for (var i=0; i<dests.length; i++) {
     gs.print('The identifier for '+recipient.first_name+'\'s '+dests[i].getDestinationType().name+' destination is '+dests[i].getDeliverTo());
}
```

Output:

```
The identifier for Abel's Workspace destination is 62826bf03710200044e0bfc8bcbe5df1
```

## PreferenceDestination - isActive\(GlideRecord notification\)

Checks if the destination has permission to receive a notification.

|Name|Type|Description|
|----|----|-----------|
|notification|GlideRecord|Optional. Notification to check if the destination has permission to receive that notification. An exception is thrown if the notification doesn't exist or if the notification isn't readable by the destination's user. If no notification is specified, this method checks if the destination has permission to receive any notifications.|

<table id="table_k4d_bw3_wnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the destination has permission to receive a notification.Possible values:

-   true: The destination has permission receive a notification.
-   false: The destination doesn't have permission to receive a notification.

</td></tr></tbody>
</table>This example checks if each of Abel Tuter's destinations has permission to receive the Approval Request notification.

```
var recipient = new GlideRecord('sys_user');
recipient.get('last_name', 'Tuter');
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
var notif = new GlideRecord('sys_notification'); 
notif.get('name', 'Approval Request'); 
for (var i=0; i<dests.length; i++) {
   var active = dests[i].isActive(notif) ? 'active' : 'inactive'; 
   gs.print(dests[i].getDestinationType().name + ' ' + dests[i].getDeliverTo() + ' is ' + active + ' for this notification');
}
```

Output:

```
Workspace 62826bf03710200044e0bfc8bcbe5df1 is active for this notification
```

## PreferenceDestination - isOverriden\(GlideRecord notification\)

Checks if a notification overrides a user's preferences for the destination.

|Name|Type|Description|
|----|----|-----------|
|notification|GlideRecord|Specify a notification to check if it overrides user preferences for the destination. The notification should be a GlideRecord from the Notification \[sys\_notification\] table.|

<table id="table_t1c_5v3_wnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the notification overrides user preferences for the destination.

 Valid values:

-   true: User preferences for the destination are ignored for this notification.
-   false: The destination receives or doesn't receive the notification according to the user preference.

</td></tr></tbody>
</table>This example checks if the Approval Request notification overrides user preferences for one of Abel Tuter's destinations. If the notification doesn't override user preferences, the destination is given permission to receive the notification. Otherwise, no preference is set because the notification overrides the preference.

```
var recipient = new GlideRecord('sys_user');
recipient.get('last_name', 'Tuter');
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
var notif = new GlideRecord('sys_notification'); 
notif.get('name', 'Approval Request'); 
var firstDest = dests[0]; 
if (!firstDest.isOverridden(notif)) { 
     dests[0].setActive(notif, true); 
} else { 
     gs.print('This notification overrides user preference, so don't bother to set a preference.'); 
} 
```

## PreferenceDestination - setActive\(GlideRecord notification, Boolean active\)

Sets the user preference for a destination to receive or not receive notifications.

The isOverriden\(\) method can be called first to check if the user preference will be ignored, but it is not required.

<table id="table_h3k_kw3_wnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notification

</td><td>

GlideRecord

</td><td>

Optional. If a notification is specified, the user preference is set for the destination to receive or not receive that notification. The notification should be a GlideRecord from the Notification \[sys\_notification\] table. If no notification is specified, the user preference is set for the destination to receive or not receive all notifications.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the destination has permission to receive a notification.

 Valid values:

-   true: The destination has permission receive a notification.
-   false: The destination doesn't have permission to receive a notification.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example checks if the Approval Request notification overrides user preferences for one of Abel Tuter's destinations. If the notification doesn't override user preferences, the destination is given permission to receive the notification. Otherwise, no preference is set because the notification overrides the preference.

```
var recipient = new GlideRecord('sys_user');
recipient.get('last_name', 'Tuter');
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
var notif = new GlideRecord('sys_notification'); 
notif.get('name', 'Approval Request'); 
var firstDest = dests[0]; 
if (!firstDest.isOverridden(notif)) { 
     dests[0].setActive(notif, true); 
} else { 
     gs.print('This notification overrides user preference, so don't bother to set a preference.'); 
} 
```

