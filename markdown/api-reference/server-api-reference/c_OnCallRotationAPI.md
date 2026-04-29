---
title: OnCallRotation - Global
description: The OnCallRotation script include provides methods to manage on-call schedules.Creates an instance of the OnCallRotation class.Add the current escalation member to the list of notified users so that the API knows who has been contacted. This API is applicable for a single shift, overlapping shifts, and custom escalation.Cancels any escalations for the GlideRecord that were started with the startEscalations API. This API is applicable for a single shift, overlapping shifts, and custom escalation.Continue the escalations for a document\(incident now\_GR\) and group. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets the sys\_id of the catch all person. Use together with the getCatchAllType\(\) method to determine the source of the returned id. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets the type of \_catch all\_ that lives at the end of the escalation chain. When the escalation chain finishes without assigning an on-call person, if configured, the incident is assigned to the \_catch all\_. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets an item to escalate to, either a user \[sys\_user\], group, or notification device \[cmn\_notif\_device\], for a group's shift at the specified date and time and at a certain position in the escalation lineup. This API is applicable for a single shift.Gets a list of escalatees that are on-call for a given time. If no time is specified, then the current time is used. If no groupSysIds are provided, empty list is returned. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets a list of objects to escalate to, escalation plans that consist of either a user \[sys\_user\] or notification device \[cmn\_notif\_device\], for a group's shift at the specified date and time. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets the type of escalation based on a simple calculation. If there is one active roster in the rota, rotate through members. If there is more than one active roster in the rota, rotate through rosters. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets the escalatees \(either a user, group, or device records depending on the notification rules\) at a specific time and position. This API is applicable for a single shift, overlapping shifts and custom escalation.Gets the sys\_id of the current primary contact when there is a single shift.Gets the sys\_id of the current primary user of the specified shift. This API is applicable for a single shift and overlapping shifts.Gets the name of the current primary contact. This API is applicable for a single shift.Gets the name of the current primary user of the specified shift. This API is applicable for a single shift and overlapping shifts.Gets the list of primary contacts for a shift. This API is applicable for a single shift, overlapping shifts, and custom escalation.Checks if the parent span and child spans overlap.Start the escalations for a document\(incident now\_GR\) and group, and specify the event name for the escalation notifications. In addition, specify the name of the business rule to call when an escalation occurs. This method should be used after a succesful call to who or whoAt methods. This API is applicable for a single shift, overlapping shifts, and custom escalation.Specifies if there is an on-call user, group, or device. This method is applicable for a single shift, overlapping shifts, and custom escalation.Specifies if there is an on-call user, group, or device. This API is applicable for a single shift, overlapping shifts, and custom escalation.Gets the list of users that are on-call at a given time. If no time is specified, then current time is used. This API is applicable for a single shift and overlapping shifts.Escalation business rules determine who in the shift should be contacted next. The escalation record passed to the method tracks the escalation between invocations of the business rule. This API is applicable for a single shift, overlapping shifts, and custom escalation.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OnCallRotation- Global

The OnCallRotation script include provides methods to manage on-call schedules.

For information, see [On-call scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OnCallRotation - OnCallRotation\(\)

Creates an instance of the OnCallRotation class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var oncall = new OnCallRotation();
```

## OnCallRotation - addCurrentToNotified\(\)

Add the current escalation member to the list of notified users so that the API knows who has been contacted. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## OnCallRotation - cancelEscalations\(GlideRecord escalationGr\)

Cancels any escalations for the GlideRecord that were started with the startEscalations API. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|escalationGr|GlideRecord|GlideRecord of Rotation escalation\(cmn\_rota\_escalation|

|Type|Description|
|----|-----------|
|void| |

## OnCallRotation - continueEscalations\(GlideRecord escalationGr\)

Continue the escalations for a document\(incident now\_GR\) and group. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|escalationGr|GlideRecord|GlideRecord of Rotation escalation\(cmn\_rota\_escalation|

|Type|Description|
|----|-----------|
|void| |

## OnCallRotation - getCatchAll\(String rotaID\)

Gets the sys\_id of the catch all person. Use together with the getCatchAllType\(\) method to determine the source of the returned id. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|rotaID|String|The sys\_id of the rota.|

|Type|Description|
|----|-----------|
|String|The sys\_id of a sys\_user, a cmn\_rota\_roster, or null.|

```

var rotaSysId = '349f399173062300e7af6238edf6a75e';
var onCallRotation = new OnCallRotation();
var catchAll = onCallRotation.getCatchAll(rotaSysId);
gs.log(catchAll);

```

Output:

```
46d44a23a9fe19810012d100cca80666
```

## OnCallRotation - getCatchAllType\(String rotaID\)

Gets the type of \_catch all\_ that lives at the end of the escalation chain. When the escalation chain finishes without assigning an on-call person, if configured, the incident is assigned to the \_catch all\_. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|rotaID|String|The sys\_id of the rota.|

<table id="table_hsz_g1g_2w" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

-   Null: invalid rota id or catch all is not available.
-   Group\_manager: the manager of the group linked to the rota is the catch all person.
-   Individual: a configured user is the catch all person.
-   All: all members of the configured roster are the catch all person.

</td></tr></tbody>
</table>```
var rotaSysId = '349f399173062300e7af6238edf6a75e';
var onCallRotation = new OnCallRotation();
var catchAllType = onCallRotation.getCatchAllType(rotaSysId);
gs.log(catchAllType);

```

Output:

```
group_manager
```

## OnCallRotation - getEscalateeAt\(String groupID, GlideDateTime dateTime, Number position\)

Gets an item to escalate to, either a user \[sys\_user\], group, or notification device \[cmn\_notif\_device\], for a group's shift at the specified date and time and at a certain position in the escalation lineup. This API is applicable for a single shift.

The method returns null if an invalid position or group is passed as an argument.

You can use the getTableName\(\) method to check whether the returning GlideRecord comes from the sys\_user or cmn\_notif\_device table.

|Name|Type|Description|
|----|----|-----------|
|groupID|String|The sys\_id for the group from which to get the item to escalate.|
|dateTime|GlideDateTime|The date and time when the escalation lineup should begin.|
|position|Number|The position in the lineup to determine the item to escalate to \(1-based, which means the count starts with 1\).|

|Type|Description|
|----|-----------|
|GlideRecord|The item to escalate to,that is, escalatees \(either a user, group, or device records depending on the notification rules\) at a specific time and position. Returns null if nothing is found.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var escalatee = onCallRotation.getEscalateeAt(groupSysId, currentTime, 1);
gs.log(escalatee.name);

```

Output:

```
Abel Tuter
```

## OnCallRotation - getEscalatees\(String groupSysIds, String rotaSysIds, String rosterSysIds, GlideDateTime gdt, GlideRecord taskGr\)

Gets a list of escalatees that are on-call for a given time. If no time is specified, then the current time is used. If no groupSysIds are provided, empty list is returned. This API is applicable for a single shift, overlapping shifts, and custom escalation.

**Note:** Set the taskGR parameter to enable escalation plan evaluation.

|Name|Type|Description|
|----|----|-----------|
|groupSysIds|String|Comma-separated list of sys\_ids of the sys\_user\_group, to filter the records by.|
|rotaSysIds|String|Comma-separated list of cmn\_rota sys\_ids to filter the records by.|
|rosterSysIds|String|Comma-separated list of cmn\_rota\_roster sys\_ids to filter the records by.|
|gdt|GlideDateTime|Date in the UTC timezone|
|taskGr|GlideRecord|Optional. Current task record. If taskGr is empty, this method returns the default escalation plan. If taskGr is passed, escalation policies are evaluated in order and this method returns the corresponding escalation plan.|

|Type|Description|
|----|-----------|
|Object|Escalatee information such as userIds, deviceIds, and escalationGroups.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.getEscalatees(groupSysId, "", "", currentTime);
gs.log(JSON.stringify(result));

```

Output:

For single shift:

```
[
  {
    "memberId": "119f399173062300e7af6238edf6a7e7",
    "memberIds": [],
    "userId": "62826bf03710200044e0bfc8bcbe5df1",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "9d9f399173062300e7af6238edf6a7ec"
  },
  {
    "memberId": "1d9f399173062300e7af6238edf6a7e8",
    "memberIds": [],
    "userId": "a8f98bb0eb32010045e1a5115206fe3a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "d99f399173062300e7af6238edf6a7ef"
  },
  {
    "memberId": "dd9f399173062300e7af6238edf6a7e9",
    "memberIds": [],
    "userId": "0a826bf03710200044e0bfc8bcbe5d7a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 3,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "519f399173062300e7af6238edf6a7f2"
  }
]

```

For overlapping shift:

```
[
  {
    "memberId": "119f399173062300e7af6238edf6a7e7",
    "memberIds": [],
    "userId": "62826bf03710200044e0bfc8bcbe5df1",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "9d9f399173062300e7af6238edf6a7ec"
  },
  {
    "memberId": "7daf799173062300e7af6238edf6a7a2",
    "memberIds": [],
    "userId": "d2826bf03710200044e0bfc8bcbe5dc9",
    "userIds": [],
    "roster": "b5af799173062300e7af6238edf6a7a2",
    "rota": "35af799173062300e7af6238edf6a79e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "3daf799173062300e7af6238edf6a79e",
    "memberScheduleId": "06af799173062300e7af6238edf6a7cd"
  },
  {
    "memberId": "1d9f399173062300e7af6238edf6a7e8",
    "memberIds": [],
    "userId": "a8f98bb0eb32010045e1a5115206fe3a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "d99f399173062300e7af6238edf6a7ef"
  },
  {
    "memberId": "f5af799173062300e7af6238edf6a7c9",
    "memberIds": [],
    "userId": "ee826bf03710200044e0bfc8bcbe5def",
    "userIds": [],
    "roster": "b5af799173062300e7af6238edf6a7a2",
    "rota": "35af799173062300e7af6238edf6a79e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "3daf799173062300e7af6238edf6a79e",
    "memberScheduleId": "8aaf799173062300e7af6238edf6a7cf"
  },
  {
    "memberId": "dd9f399173062300e7af6238edf6a7e9",
    "memberIds": [],
    "userId": "0a826bf03710200044e0bfc8bcbe5d7a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 3,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "519f399173062300e7af6238edf6a7f2"
  },
  {
    "memberId": "8aaf799173062300e7af6238edf6a7ca",
    "memberIds": [],
    "userId": "e2826bf03710200044e0bfc8bcbe5de0",
    "userIds": [],
    "roster": "b5af799173062300e7af6238edf6a7a2",
    "rota": "35af799173062300e7af6238edf6a79e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 3,
    "isOverride": false,
    "rotationScheduleId": "3daf799173062300e7af6238edf6a79e",
    "memberScheduleId": "02af799173062300e7af6238edf6a7d2"
  }
]

```

For custom escalation

```
[
  {
    "memberId": "",
    "memberIds": [],
    "userId": "",
    "userIds": [
      "62826bf03710200044e0bfc8bcbe5df1",
      "46d44a23a9fe19810012d100cca80666"
    ],
    "roster": "",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [
      "a715cd759f2002002920bde8132e7018"
    ],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": ""
  },
  {
    "memberId": "",
    "memberIds": [
      "119f399173062300e7af6238edf6a7e7"
    ],
    "userId": "",
    "userIds": [
      "62826bf03710200044e0bfc8bcbe5df1"
    ],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": ""
  }
]

```

```
/**
 * create a custom escalation for service desk shift with condition as P1 for Incident
 * taskGr is optional parameter
 * if taskGr is empty then it returns list of escalatees in default escalation plan
 * if taskGr is passed then escalation policies are executed evaluated in order and list of escalatees in corresponding escalation plan is returned
**/
var serviceDeskSysId = 'd625dccec0a8016700a222a0f7900d06';
var taskGr = new GlideRecord('incident');
taskGr.get('ed92e8d173d023002728660c4cf6a7bc');

var ocRotation = new OnCallRotation();
var escalatees = ocRotation.getEscalatees(serviceDeskSysId, null, null, null, null, taskGr);
gs.log(JSON.stringify(escalatees));
```

## OnCallRotation - getEscalationPlan\(String groupSysId, GlideDateTime gdt, String rotaSysIds, GlideRecord taskGr\)

Gets a list of objects to escalate to, escalation plans that consist of either a user \[sys\_user\] or notification device \[cmn\_notif\_device\], for a group's shift at the specified date and time. This API is applicable for a single shift, overlapping shifts, and custom escalation.

The Escalation object contains the following fields:

-   Number order: the escalation order within the lineup
-   String userId: sys\_id of the sys\_user record or null
-   String deviceId: sys\_id of the cmn\_notif\_device record or null
-   Boolean isDevice: true or false depending on whether the item to escalate to is a device or user
-   GlideDuration timeBetweenReminders: the time between reminders being sent
-   Number reminderNum: number of reminders to be sent for each item to escalate to

**Note:** Set the taskGR parameter to enable escalation plan evaluation.

|Name|Type|Description|
|----|----|-----------|
|groupID|String|sys\_id for the group for which you need the escalation plan.|
|gdt|GlideDateTime|Date and time when the escalation lineup should begin. Default is now. yyyy-MM-dd HH:mm:ss is the format in UTC timezone.|
|rotaSysIds|String|Comma-separated list of cmn\_rota sys\_ids to filter the records by.|
|taskGr|GlideRecord|Optional. Current task record. If taskGr is empty, this method returns the default escalation plan. If taskGr is passed, escalation policies are evaluated in order and this method returns the corresponding escalation plan.|

|Type|Description|
|----|-----------|
|Object|A list of escalation objects to escalate to.|

```
var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.getEscalationPlan(groupSysId, currentTime);
gs.log(JSON.stringify(result));

```

Output:

For single shift:

```
[
  {
    "order": 1,
    "userId": "62826bf03710200044e0bfc8bcbe5df1",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeToNextStep": null,
    "cmnRotaEscStepDefId": null,
    "reminderNum": 1,
    "rosterId": "9d9f399173062300e7af6238edf6a7e5",
    "memberId": "119f399173062300e7af6238edf6a7e7",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "9d9f399173062300e7af6238edf6a7ec"
  },
  {
    "order": 2,
    "userId": "a8f98bb0eb32010045e1a5115206fe3a",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeToNextStep": null,
    "cmnRotaEscStepDefId": null,
    "reminderNum": 1,
    "rosterId": "9d9f399173062300e7af6238edf6a7e5",
    "memberId": "1d9f399173062300e7af6238edf6a7e8",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "d99f399173062300e7af6238edf6a7ef"
  },
  {
    "order": 3,
    "userId": "0a826bf03710200044e0bfc8bcbe5d7a",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeToNextStep": null,
    "cmnRotaEscStepDefId": null,
    "reminderNum": 1,
    "rosterId": "9d9f399173062300e7af6238edf6a7e5",
    "memberId": "dd9f399173062300e7af6238edf6a7e9",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "519f399173062300e7af6238edf6a7f2"
  }
]

```

For overlapping shift:

```
[
  {
    "order": 1,
    "userId": "62826bf03710200044e0bfc8bcbe5df1",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeToNextStep": null,
    "cmnRotaEscStepDefId": null,
    "reminderNum": 1,
    "rosterId": "9d9f399173062300e7af6238edf6a7e5",
    "memberId": "119f399173062300e7af6238edf6a7e7",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [
      {
        "order": 1,
        "userId": "d2826bf03710200044e0bfc8bcbe5dc9",
        "userIds": [],
        "deviceId": "",
        "deviceIds": [],
        "escalationGroups": [],
        "isDevice": false,
        "timeToNextStep": null,
        "cmnRotaEscStepDefId": null,
        "reminderNum": 1,
        "rosterId": "b5af799173062300e7af6238edf6a7a2",
        "memberId": "7daf799173062300e7af6238edf6a7a2",
        "memberIds": [],
        "isOverride": false,
        "additionalEscalatees": [],
        "forcedCommunicationChannel": "",
        "rotaId": "35af799173062300e7af6238edf6a79e",
        "groupId": "096fb59173062300e7af6238edf6a783",
        "rotaScheduleId": "3daf799173062300e7af6238edf6a79e",
        "memberScheduleId": "06af799173062300e7af6238edf6a7cd"
      }
    ],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "9d9f399173062300e7af6238edf6a7ec"
  },
  {
    "order": 2,
    "userId": "a8f98bb0eb32010045e1a5115206fe3a",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeToNextStep": null,
    "cmnRotaEscStepDefId": null,
    "reminderNum": 1,
    "rosterId": "9d9f399173062300e7af6238edf6a7e5",
    "memberId": "1d9f399173062300e7af6238edf6a7e8",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [
      {
        "order": 2,
        "userId": "ee826bf03710200044e0bfc8bcbe5def",
        "userIds": [],
        "deviceId": "",
        "deviceIds": [],
        "escalationGroups": [],
        "isDevice": false,
        "timeToNextStep": null,
        "cmnRotaEscStepDefId": null,
        "reminderNum": 1,
        "rosterId": "b5af799173062300e7af6238edf6a7a2",
        "memberId": "f5af799173062300e7af6238edf6a7c9",
        "memberIds": [],
        "isOverride": false,
        "additionalEscalatees": [],
        "forcedCommunicationChannel": "",
        "rotaId": "35af799173062300e7af6238edf6a79e",
        "groupId": "096fb59173062300e7af6238edf6a783",
        "rotaScheduleId": "3daf799173062300e7af6238edf6a79e",
        "memberScheduleId": "8aaf799173062300e7af6238edf6a7cf"
      }
    ],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "d99f399173062300e7af6238edf6a7ef"
  },
  {
    "order": 3,
    "userId": "0a826bf03710200044e0bfc8bcbe5d7a",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeToNextStep": null,
    "cmnRotaEscStepDefId": null,
    "reminderNum": 1,
    "rosterId": "9d9f399173062300e7af6238edf6a7e5",
    "memberId": "dd9f399173062300e7af6238edf6a7e9",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [
      {
        "order": 3,
        "userId": "e2826bf03710200044e0bfc8bcbe5de0",
        "userIds": [],
        "deviceId": "",
        "deviceIds": [],
        "escalationGroups": [],
        "isDevice": false,
        "timeToNextStep": null,
        "cmnRotaEscStepDefId": null,
        "reminderNum": 1,
        "rosterId": "b5af799173062300e7af6238edf6a7a2",
        "memberId": "8aaf799173062300e7af6238edf6a7ca",
        "memberIds": [],
        "isOverride": false,
        "additionalEscalatees": [],
        "forcedCommunicationChannel": "",
        "rotaId": "35af799173062300e7af6238edf6a79e",
        "groupId": "096fb59173062300e7af6238edf6a783",
        "rotaScheduleId": "3daf799173062300e7af6238edf6a79e",
        "memberScheduleId": "02af799173062300e7af6238edf6a7d2"
      }
    ],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "519f399173062300e7af6238edf6a7f2"
  }
]

```

For custom escalation:

```
[
  {
    "order": 1,
    "userId": "",
    "userIds": [
      "62826bf03710200044e0bfc8bcbe5df1",
      "46d44a23a9fe19810012d100cca80666"
    ],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [
      "a715cd759f2002002920bde8132e7018"
    ],
    "isDevice": false,
    "timeBetweenReminders": {},
    "timeToNextStep": {},
    "cmnRotaEscStepDefId": "655042d173062300e7af6238edf6a738",
    "reminderNum": 1,
    "rosterId": "",
    "memberId": "",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": ""
  },
  {
    "order": 2,
    "userId": "",
    "userIds": [],
    "deviceId": "",
    "deviceIds": [],
    "escalationGroups": [],
    "isDevice": false,
    "timeBetweenReminders": {},
    "timeToNextStep": {},
    "cmnRotaEscStepDefId": "8b6042d173062300e7af6238edf6a7f3",
    "reminderNum": 1,
    "rosterId": "",
    "memberId": "",
    "memberIds": [],
    "isOverride": false,
    "additionalEscalatees": [],
    "forcedCommunicationChannel": "",
    "rotaId": "349f399173062300e7af6238edf6a75e",
    "groupId": "096fb59173062300e7af6238edf6a783",
    "rotaScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": ""
  }
]

```

```
/**
* create a custom escalation for service desk shift with condition as P1 for Incident
* taskGr is optional parameter
* if taskGr is empty then it returns default escalation plan
* if taskGr is passed then escalation policies are executed evaluated in order and corresponding escalation plan is returned
**/

var serviceDeskSysId = 'd625dccec0a8016700a222a0f7900d06';
var taskGr = new GlideRecord('incident');
taskGr.get('ed92e8d173d023002728660c4cf6a7bc');

var ocRotation = new OnCallRotation();
var escalationPlan = ocRotation.getEscalationPlan(serviceDeskSysId, null, null, taskGr);
gs.log(JSON.stringify(escalationPlan));
```

## OnCallRotation - getEscalationType\(String rotaID\)

Gets the type of escalation based on a simple calculation. If there is one active roster in the rota, rotate through members. If there is more than one active roster in the rota, rotate through rosters. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|rotaID|String|The sys\_id for the rota to check for rosters.|

<table id="table_bvq_4zf_2w" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

-   Member: if there is one roster in the rota.
-   Roster: if there is more than one roster in the rota.
-   No rosters in this rota: if none of the above.
-   Custom: If the custom escalation is applicable.

</td></tr></tbody>
</table>```
var rotaSysId = '349f399173062300e7af6238edf6a75e';
var onCallRotation = new OnCallRotation();
var escalationType = onCallRotation.getEscalationType(rotaSysId);
gs.log(escalationType);

```

Output:

```
custom
```

## OnCallRotation - getEscalateesAt\(String groupSysId, GlideDateTime gdt, Number position, GlideRecord taskGr\)

Gets the escalatees \(either a user, group, or device records depending on the notification rules\) at a specific time and position. This API is applicable for a single shift, overlapping shifts and custom escalation.

**Note:** Set the taskGR parameter to enable escalation plan evaluation.

|Name|Type|Description|
|----|----|-----------|
|groupSysId|String|ys\_id of the group.|
|gdt|GlideDateTime|yyyy-MM-dd HH:mm:ss format in the UTC timezone. Default is now.|
|position|Number|Position of the escalation step.|
|taskGr|GlideRecord|Optional. Current task record. If taskGr is empty, this method returns the default escalation plan. If taskGr is passed, escalation policies are evaluated in order and this method returns the corresponding escalation plan.|

|Type|Description|
|----|-----------|
|GlideRecord|Array of escalatees \(either a user, group, or device records depending on the notification rules\) at a specific time and position.|

```
var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var escalatees = onCallRotation.getEscalateesAt(groupSysId, currentTime, 1);
for (var i = 0; i < escalatees.length; i++) {
gs.log(escalatees[i].name);
}

```

Output:

For overlapping shifts:

```
Abel Tuter
Barbara Hindley

```

For custom escalation:

```
Abel Tuter
Beth Anglin
Change Management
Barbara Hindley

```

```
// Create a custom escalation for service desk shift with condition as P1 for Incident
var serviceDeskSysId = 'd625dccec0a8016700a222a0f7900d06';
// optional parameter taskGR
var taskGr = new GlideRecord('incident');
taskGr.get('ed92e8d173d023002728660c4cf6a7bc');

var ocRotation = new OnCallRotation();
var position = 1;
var escalatees = ocRotation.getEscalateesAt(serviceDeskSysId, new GlideDateTime(), position, taskGr);

// if taskGr is empty then it returns escalatees at a position in default escalation plan
// if taskGr is passed then escalation policies are executed evaluated in order and escalatees at a position in corresponding escalation plan is returned
for (var i = 0; i < escalatees.length; i++) {
    gs.log(escalatees[i].getDisplayValue());
}
```

## OnCallRotation - getPrimaryUser\(\)

Gets the sys\_id of the current primary contact when there is a single shift.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|sys\_id of the current primary contact.|

Example:

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.who(groupSysId, currentTime);
var primaryUser = onCallRotation.getPrimaryUser();

```

Output:

```
62826bf03710200044e0bfc8bcbe5df1
```

## OnCallRotation - getPrimaryUserByRota\(String rotaId\)

Gets the sys\_id of the current primary user of the specified shift. This API is applicable for a single shift and overlapping shifts.

|Name|Type|Description|
|----|----|-----------|
|rotaId|String|sys\_id of the cmn\_rota.|

|Type|Description|
|----|-----------|
|String|sys\_id of the current primary user of the specified shift.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var rotaId = '349f399173062300e7af6238edf6a75e';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.who(groupSysId, currentTime);
var primaryUser = onCallRotation.getPrimaryUserByRota(rotaId);
gs.log(primaryUser);

```

Output:

```
62826bf03710200044e0bfc8bcbe5df1
```

## OnCallRotation - getPrimaryUserName\(\)

Gets the name of the current primary contact. This API is applicable for a single shift.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the current primary contact.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.who(groupSysId, currentTime);
var primaryUser = onCallRotation.getPrimaryUserName();
gs.log(primaryUser);

```

Output:

```
Abel Tuter
```

## OnCallRotation - getPrimaryUserNameByRota\(String rotaId\)

Gets the name of the current primary user of the specified shift. This API is applicable for a single shift and overlapping shifts.

|Name|Type|Description|
|----|----|-----------|
|rotaId|String|sys\_id of the cmn\_rota.|

|Type|Description|
|----|-----------|
|String|Name of the current primary user of the specified shift.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var rotaId = '349f399173062300e7af6238edf6a75e';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.who(groupSysId, currentTime);
var primaryUser = onCallRotation.getPrimaryUserNameByRota(rotaId);
gs.log(primaryUser);

```

Output:

```
Abel Tuter
```

## OnCallRotation - getPrimaryUsers\(\)

Gets the list of primary contacts for a shift. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|List of primary contacts.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.who(groupSysId, currentTime);
var primaryUser = onCallRotation.getPrimaryUser();
gs.log(JSON.stringify(primaryUser));

```

Output:

```
{
  "349f399173062300e7af6238edf6a75e": {
    "userSysId": "62826bf03710200044e0bfc8bcbe5df1",
    "userName": "Abel Tuter"
  },
  "35af799173062300e7af6238edf6a79e": {
    "userSysId": "d2826bf03710200044e0bfc8bcbe5dc9",
    "userName": "Barbara Hindley"
  }
}

```

## OnCallRotation - spansOverlap\(ArrayList parent, ArrayList child, String timeZone\)

Checks if the parent span and child spans overlap.

|Name|Type|Description|
|----|----|-----------|
|parent|ArrayList|The parent spans to compare.|
|child|ArrayList|The child spans to compare.|
|timeZone|String|The name of the time zone.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the parent and child spans overlap.|

```
var onCall = new OnCallRotation();
 
// get a time range we are interested in
var timeZone = gs.getSession().getTimeZoneName();
var dateStart = new GlideDateTime();
var dateEnd = new GlideDateTime().addMonths(1);
 
// convert glidedatime to scheduledatetime because it is required
// by the function being called below
var scheduleStart = new GlideScheduleDateTime(dateStart);
var scheduleEnd =  new GlideScheduleDateTime(dateEnd);
scheduleStart.setTimeZone(timeZone);
scheduleEnd.setTimeZone(timeZone);
 
// calculate rotation items based on the date and time given
// for all the groups the currently logged in user is a member of
gs.include("OnCallRotationPersonal");
var rotation = new OnCallRotationPersonal();
var myGroups = gs.getUser().getMyGroups();
var groupIter = myGroups.iterator();
 
while(groupIter.hasNext()){
	var rotaItems = rotation.onCallDuringPeriod(groupIter.next(), scheduleStart, scheduleEnd);
 
	// loop through rotation schedules
	for (var i = 0; i < rotaItems.length - 1; i++) {
		var parentItem = rotaItems[i];
		var nextItem = rotaItems[i + 1];
 
		// check if previous and next time spans overlap
		var overlaps = onCall.spansOverlap(parentItem.getTimeSpans(), nextItem.getTimeSpans(), 
			gs.getSession().getTimeZoneName());
	}
}
```

## OnCallRotation - startEscalations\(GlideRecord now\_GR, String eventName, String escalationScriptName\)

Start the escalations for a document\(incident now\_GR\) and group, and specify the event name for the escalation notifications. In addition, specify the name of the business rule to call when an escalation occurs. This method should be used after a succesful call to who or whoAt methods. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|Document glide record. For example, Incident now\_GR.|
|eventName|String|Event name for the escalation notifications.|
|escalationScriptName|String|Business rule to call when escalation occurs|

|Type|Description|
|----|-----------|
|void| |

## OnCallRotation - who\(String groupSysId, GlideDateTime gdt, Boolean nullifyOverrideRoster, String rotaSysIds, Boolean overrideCustomEscalation, GlideRecord taskGR\)

Specifies if there is an on-call user, group, or device. This method is applicable for a single shift, overlapping shifts, and custom escalation.

**Note:** Pass the **taskGR** parameter to enable escalation plan evaluation.

<table id="table_xgb_ypj_3gb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupSysId

</td><td>

String

</td><td>

Sys\_id of the group to check for.

</td></tr><tr><td>

gdt

</td><td>

[GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#)

</td><td>

Date and time.Format: yyyy-MM-dd HH:mm:ss in the UTC time zone

Default: Current date and time

</td></tr><tr><td>

nullifyOverrideRoster

</td><td>

Boolean

</td><td>

Flag that indicates whether the notification list for the group is for a specific roster.Valid values:

-   true: Not for a specific roster.
-   false: For a specific roster.

</td></tr><tr><td>

rotaSysIds

</td><td>

String

</td><td>

Comma-separated list of cmn\_rota sys\_ids to filter the records by.

</td></tr><tr><td>

overrideCustomEscalation

</td><td>

Boolean

</td><td>

Flag that indicates whether to override the default escalation policy with the custom escalation. Valid values:

-   true: Override the default escalation policy.
-   false: Do not override the default escalation policy.

</td></tr><tr><td>

taskGR

</td><td>

[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

Optional. Current task record. If passed, the method populates the escalatees based on the escalation conditions.

</td></tr></tbody>
</table><table id="table_lzh_1rj_3gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether a match was found.Possible values:

-   true: At least one match was found.
-   false: No matches were found.

</td></tr></tbody>
</table>```
var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.who(groupSysId, currentTime);
gs.log(result);
```

Output:

```
true
```

The following example shows how to create a custom escalation for service desk shift with condition P1 for an incident.

```
/**
 * When the who() method is invoked with the optional taskGr parameter, 
 * escalatees are populated based on the conditional escalations
**/

var serviceDeskSysId = 'd625dccec0a8016700a222a0f7900d06';
var taskGr = new GlideRecord('incident');
taskGr.get('ed92e8d173d023002728660c4cf6a7bc');

var ocRotation = new OnCallRotation();
ocRotation.who(serviceDeskSysId, null, null, null, null, taskGr);
while (ocRotation.next()) {
    gs.log(ocRotation.getUserName());
}
```

Output:

```
Beth Anglin
```

## OnCallRotation - whoAt\(String groupSysId, GlideDateTime gdt, String rotaSysIds\)

Specifies if there is an on-call user, group, or device. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|groupSysId|String|Sys ID of the group.|
|gdt|GlideDateTime|yyyy-MM-dd HH:mm:ss format in the UTC timezone. Default is now.|
|rotaSysIds|String|Comma-separated list of cmn\_rota Sys IDs to filter the records by.|

|Type|Description|
|----|-----------|
|Boolean|True if there is at least one on-call user, group, or device; false otherwise.|

```

var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var result = onCallRotation.whoAt(groupSysId, currentTime);
gs.log(result);

```

Output:

```
true
```

## OnCallRotation - whoIsOnCall\(String groupSysIds, String rotaSysIds, String rosterSysIds, GlideDateTime gdt\)

Gets the list of users that are on-call at a given time. If no time is specified, then current time is used. This API is applicable for a single shift and overlapping shifts.

|Name|Type|Description|
|----|----|-----------|
|groupSysIds|String|Comma-separated list of sys\_ids of the sys\_user\_group, to filter the records by.|
|rotaSysIds|String|Comma-separated list of cmn\_rota sys\_ids to filter the records by.|
|rosterSysIds|String|Comma-separated list of cmn\_rota\_roster sys\_ids to filter the records by.|
|gdt|GlideDateTime|Date in the UTC timezone|

|Type|Description|
|----|-----------|
|Object|List of users, groups, or devices that are on-call at a given time. For example, information about userIds, deviceIds, and escalationGroups.|

```
var groupSysId = '096fb59173062300e7af6238edf6a783';
var currentTime = new GlideDateTime();
var onCallRotation = new OnCallRotation();
var escalatees = onCallRotation. whoIsOnCall(groupSysId, "", "", currentTime);
gs.log(JSON.stringify(escalatees));

```

Output:

For single shift:

```
[
  {
    "memberId": "119f399173062300e7af6238edf6a7e7",
    "memberIds": [],
    "userId": "62826bf03710200044e0bfc8bcbe5df1",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "9d9f399173062300e7af6238edf6a7ec"
  },
  {
    "memberId": "1d9f399173062300e7af6238edf6a7e8",
    "memberIds": [],
    "userId": "a8f98bb0eb32010045e1a5115206fe3a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "d99f399173062300e7af6238edf6a7ef"
  },
  {
    "memberId": "dd9f399173062300e7af6238edf6a7e9",
    "memberIds": [],
    "userId": "0a826bf03710200044e0bfc8bcbe5d7a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 3,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "519f399173062300e7af6238edf6a7f2"
  }
]

```

For overlapping shift:

```
[
  {
    "memberId": "119f399173062300e7af6238edf6a7e7",
    "memberIds": [],
    "userId": "62826bf03710200044e0bfc8bcbe5df1",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "9d9f399173062300e7af6238edf6a7ec"
  },
  {
    "memberId": "7daf799173062300e7af6238edf6a7a2",
    "memberIds": [],
    "userId": "d2826bf03710200044e0bfc8bcbe5dc9",
    "userIds": [],
    "roster": "b5af799173062300e7af6238edf6a7a2",
    "rota": "35af799173062300e7af6238edf6a79e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 1,
    "isOverride": false,
    "rotationScheduleId": "3daf799173062300e7af6238edf6a79e",
    "memberScheduleId": "06af799173062300e7af6238edf6a7cd"
  },
  {
    "memberId": "1d9f399173062300e7af6238edf6a7e8",
    "memberIds": [],
    "userId": "a8f98bb0eb32010045e1a5115206fe3a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "d99f399173062300e7af6238edf6a7ef"
  },
  {
    "memberId": "f5af799173062300e7af6238edf6a7c9",
    "memberIds": [],
    "userId": "ee826bf03710200044e0bfc8bcbe5def",
    "userIds": [],
    "roster": "b5af799173062300e7af6238edf6a7a2",
    "rota": "35af799173062300e7af6238edf6a79e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 2,
    "isOverride": false,
    "rotationScheduleId": "3daf799173062300e7af6238edf6a79e",
    "memberScheduleId": "8aaf799173062300e7af6238edf6a7cf"
  },
  {
    "memberId": "dd9f399173062300e7af6238edf6a7e9",
    "memberIds": [],
    "userId": "0a826bf03710200044e0bfc8bcbe5d7a",
    "userIds": [],
    "roster": "9d9f399173062300e7af6238edf6a7e5",
    "rota": "349f399173062300e7af6238edf6a75e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 3,
    "isOverride": false,
    "rotationScheduleId": "119f399173062300e7af6238edf6a7df",
    "memberScheduleId": "519f399173062300e7af6238edf6a7f2"
  },
  {
    "memberId": "8aaf799173062300e7af6238edf6a7ca",
    "memberIds": [],
    "userId": "e2826bf03710200044e0bfc8bcbe5de0",
    "userIds": [],
    "roster": "b5af799173062300e7af6238edf6a7a2",
    "rota": "35af799173062300e7af6238edf6a79e",
    "group": "096fb59173062300e7af6238edf6a783",
    "escalationGroups": [],
    "deviceId": "",
    "deviceIds": [],
    "isDevice": false,
    "order": 3,
    "isOverride": false,
    "rotationScheduleId": "3daf799173062300e7af6238edf6a79e",
    "memberScheduleId": "02af799173062300e7af6238edf6a7d2"
  }
]

```

## OnCallRotation - whoIsNext\(GlideRecord escalationGr\)

Escalation business rules determine who in the shift should be contacted next. The escalation record passed to the method tracks the escalation between invocations of the business rule. This API is applicable for a single shift, overlapping shifts, and custom escalation.

|Name|Type|Description|
|----|----|-----------|
|escalationGr|GlideRecord|GlideRecord of Rotation escalation \[cmn\_rota\_escalation\].|

|Type|Description|
|----|-----------|
|None| |

