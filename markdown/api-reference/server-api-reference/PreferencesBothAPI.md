---
title: Preferences - Scoped, Global
description: The Preferences API gets notification destinations for a user.Instantiates a Preferences object for a specified user.Returns a user's notification destinations.Returns a user's notification destinations that use a specified channel.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Preferences - Scoped, Global

The Preferences API gets notification destinations for a user.

A notification destination is somewhere that a notification can be delivered to, such as a specific email address or phone number. This API is based on notifications from the Notification \[sys\_notification\] table. Notifications are sent through channels such as email or Workspace. A channel can be used to send notifications to multiple types of destinations. For example, an email channel could send notifications to both personal email and work email destinations. Destination types are listed in the Notification Destination Type \[sys\_notif\_destination\_type\] table.

Use this API with the [PreferenceDestination](../../PreferenceDestination/concept/PreferenceDestinationBothAPI.md#) API to update user notification preferences.

This class uses the `sn_notification` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Preferences - Preferences\(GlideRecord recipient\)

Instantiates a Preferences object for a specified user.

|Name|Type|Description|
|----|----|-----------|
|recipient|GlideRecord|GlideRecord from the User \[sys\_user\] table for the user that you want to get notification destinations for.|

This example instantiates a Preferences object for the user Abel Tuter.

```
var recipient = new GlideRecord('sys_user'); 
recipient.get('last_name', 'Tuter'); 
var prefs = new sn_notification.Preferences(recipient);
```

## Preferences - getDestinations\(\)

Returns a user's notification destinations.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of [PreferenceDestination](../../PreferenceDestination/concept/PreferenceDestinationBothAPI.md#) objects. If the user doesn't have any destinations, the array is empty.|

This example gets all of Abel Tuter's notification destinations. The output shows that Abel has one destination.

```
var recipient = new GlideRecord('sys_user'); 
recipient.get('last_name', 'Tuter'); 
var prefs = new sn_notification.Preferences(recipient);
var dests = prefs.getDestinations();
gs.print(dests);
```

Output:

```
[object PreferenceDestination]
```

## Preferences - getDestinationsByChannel\(GlideRecord channel\)

Returns a user's notification destinations that use a specified channel.

|Name|Type|Description|
|----|----|-----------|
|channel|GlideRecord|GlideRecord from the Notification Channel \[sys\_notification\_channel\] table for the channel you want to filter on.|

|Type|Description|
|----|-----------|
|Array|Array of [PreferenceDestination](../../PreferenceDestination/concept/PreferenceDestinationBothAPI.md#) objects. If the user doesn't have any notification destinations that use the channel or if the channel doesn't exist, the array is empty.|

This example gets all of Abel Tuter's destinations that use the Workspace channel. The output shows that Abel has one destination that uses the Workspace channel.

```
var recipient = new GlideRecord('sys_user'); 
recipient.get('last_name', 'Tuter'); 
var prefs = new sn_notification.Preferences(recipient);
var channel = new GlideRecord('sys_notification_channel');
channel.get('name', 'Workspace'); 
var dests = prefs.getDestinationsByChannel(channel);
gs.print(dests);
```

Output:

```
[object PreferenceDestination]
```

