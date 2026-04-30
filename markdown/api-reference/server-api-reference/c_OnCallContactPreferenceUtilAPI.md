---
title: OnCallContactPreferenceUtil - Global
description: The OnCallContactPreferenceUtil script include provides methods for handling contact preferences.Creates an instance of the OnCallContactPreferenceUtil class.Gets a list of contacts with the escalatee object. Each returned contact contains a list of user contact preferences.Gets the list of contact preferences at the time at which the user has opted for communication. If no time is specified, then current time is used. This method is applicable to single and overlapping shifts.Gets a list of catch-all contacts and preferences.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OnCallContactPreferenceUtil- Global

The OnCallContactPreferenceUtil script include provides methods for handling contact preferences.

For contact preference configuration, see [Configure contact preferences](https://www.servicenow.com/docs/access?context=config-my-contact-prefs-oncall&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

This script include supports the [OnCallRotation](../../OnCallRotation/concept/c_OnCallRotationAPI.md#) script include.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OnCallContactPreferenceUtil - OnCallContactPreferenceUtil\(\)

Creates an instance of the OnCallContactPreferenceUtil class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## OnCallContactPreferenceUtil - getContactsAtByEscalatee\(Object escalatee, Number contactAttempt, GlideDateTime gdt, String rotaSysIds\)

Gets a list of contacts with the escalatee object. Each returned contact contains a list of user contact preferences.

<table id="table_o1s_x5j_3gb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

escalatee

</td><td>

Object

</td><td>

Mandatory. Escalatee object returned by the [getEscalationPlan\(\)](../../OnCallRotation/concept/c_OnCallRotationAPI.md#) method.

</td></tr><tr><td>

contactAttempt

</td><td>

Number

</td><td>

Optional. The attempt you are trying to contact \[ default value = 1 \].-   `1`: First attempt
-   `2`: First reminder
-   `3 or more`: Subsequent reminders

</td></tr><tr><td>

gdt

</td><td>

GlideDateTime

</td><td>

Optional. yyyy-MM-dd HH:mm:ss format in the UTC timezone. Default is now.admin

</td></tr><tr><td>

rotaSysIds

</td><td>

String

</td><td>

Optional. Comma-separated string of Sys IDs of shifts from the \[cmn\_rota\] table. Default value returns Sys IDs of the shifts at current time.

</td></tr></tbody>
</table><table id="table_nmd_wvj_3gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array object

</td><td>

Array of escalatees \(either a user, group, or device records depending on the notification rules\) at a specific time and position.-   type: String. Type of contact, e.g., user.
-   sys\_id: String. Sys ID of the user from the \[sys\_user\] table.
-   rota\_id: String. Sys ID of the shift from the \[cmn\_rota\] table.
-   roster\_id: String. Sys ID of the roster from the \[cmn\_rota\_roster\] table.
-   escalation\_step\_id: String. If an escalation path has been defined, Sys ID of the escalation step from the \[cmn\_rota\_esc\_step\_def\] table.
-   forced\_communication\_channel: String. If specified in the preferences, mandatory communication channel. Supported values include SMS, voice or email.
-   override\_user\_contact\_preference: Boolean. True if there are contact overrides, false otherwise.
-   preference\_source: String. Source of preference, such as contact or group.
-   contact\_attempt: Number. Contact attempts: 1 = first attempt, 2 = first reminder, and so on.
-   user\_preferences: Array Object.
    -   type: String. User's preferred contact format, e.g. sms, email, or number.
    -   &lt;name of preferred format, e.g., email or number&gt;: String. Content of preferred contact type, e.g., email address or phone number.
-   contact\_preferences, Array Object.
    -   type: String. User's preferred contact format, e.g., email or number.
    -   &lt;name of preferred format, e.g., email or number&gt;: String. Content of preferred contact type, e.g., email address or phone number.

</td></tr></tbody>
</table>```
var serviceDeskSysId = '<Sys_ID>';
var ocRotation = new OnCallRotation();
var escalationPlan = ocRotation.getEscalationPlan(serviceDeskSysId);
var escalatee = escalationPlan[0];

var onContactPrefUtil = new OnCallContactPreferenceUtil();
var contactAttempt = 1;
var gdt = new GlideDateTime();
var contacts = onContactPrefUtil.getContactsAtByEscalatee(escalatee, contactAttempt, gdt);
gs.log(JSON.stringify(contacts));
```

Output:

```
[{
    "type": "user",
    "sys_id": "<Sys_ID>",
    "rota_id": "<Rotation_ID>",
    "roster_id": "",
    "escalation_step_id": "<Escalation_Step_ID>",
    "forced_communication_channel": "",
    "override_user_contact_preference": true,
    "preference_source": "contact",
    "contact_attempt": 1,
    "user_preferences": [{
        "type": "sms",
        "number": "8587200477"
    }],
    "contact_preferences": [{
        "type": "voice",
        "number": "5555555555"
    }]
}]
```

## OnCallContactPreferenceUtil - getUserPreferences\(String userSysId, Number contactAttempt, GlideDateTime gdt, String communicationTypes\)

Gets the list of contact preferences at the time at which the user has opted for communication. If no time is specified, then current time is used. This method is applicable to single and overlapping shifts.

<table id="table_ixr_4jk_3gb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userSysId

</td><td>

String

</td><td>

Sys ID of the user from the \[sys\_user\] table.

</td></tr><tr><td>

contactAttempt

</td><td>

Number

</td><td>

Optional. The attempt you are trying to contact \[ default value = 1 \].-   `1`: First attempt
-   `2`: First reminder
-   `3 or more`: Subsequent reminders

</td></tr><tr><td>

gdt

</td><td>

GlideDateTime

</td><td>

Optional. yyyy-MM-dd HH:mm:ss format in the UTC timezone. Default is now.

</td></tr><tr><td>

communicationTypes

</td><td>

String

</td><td>

Optional. Comma-separated string containing one or more of the following values:-   email
-   sms
-   voice

Default includes all available communication types.

</td></tr></tbody>
</table><table id="table_ubq_ykk_3gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array Object

</td><td>

On-call user contact preference. -   type: String. User's preferred contact format, e.g. sms, email, or number.
-   &lt;name of preferred format, e.g., email or number&gt;: String. Content of preferred contact type, e.g., email address or phone number.

</td></tr></tbody>
</table>```
var onContactPrefUtil = new OnCallContactPreferenceUtil();
var contactAttempt = 1;
var gdt = new GlideDateTime();
var itilUserSysId = '<itilUserSysId>;
var userPreferences = onContactPrefUtil.getUserPreferences(itilUserSysId, contactAttempt, gdt);
gs.log(JSON.stringify(userPreferences));
```

Output:

```
[{
    "type": "sms",
    "number": "5555555555"
}, {
    "type": "voice",
    "number": "5555555555"
}]
```

## OnCallContactPreferenceUtil - getCatchAllContacts\(String rotaId, GlideDateTime gdt\)

Gets a list of catch-all contacts and preferences.

|Name|Type|Description|
|----|----|-----------|
|rotaId|String|Sys ID of the shift from the \[cmn\_rota\] table.|
|gdt|GlideDateTime|Optional. yyyy-MM-dd HH:mm:ss format in the UTC timezone. Default is now.|

<table id="table_ygb_ypj_3gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array object

</td><td>

List of catch-all contacts with preferences.-   type: String. Type of contact, e.g., user.
-   sys\_id: String. Sys ID of the user from the \[sys\_user\] table.
-   rota\_id: String. Sys ID of the shift from the \[cmn\_rota\] table.
-   roster\_id: String. Sys ID of the roster from the \[cmn\_rota\_roster\] table.
-   escalation\_step\_id: String. If an escalation path has been defined, Sys ID of the escalation step from the \[cmn\_rota\_esc\_step\_def\] table.
-   forced\_communication\_channel: String. If specified in the preferences, mandatory communication channel. Supported values include SMS, voice or email.
-   override\_user\_contact\_preference: Boolean. True if there are contact overrides, false otherwise.
-   preference\_source: String. Source of preference, such as contact or group.
-   contact\_attempt: Number. Contact attempts: 1 = first attempt, 2 = first reminder, and so on.
-   user\_preferences: Array Object.
    -   type: String. User's preferred contact format, e.g. sms, email, or number.
    -   &lt;name of preferred format, e.g., email or number&gt;: String. Content of preferred contact type, e.g., email address or phone number.
-   contact\_preferences, Array Object.
    -   type: String. User's preferred contact format, e.g., email or number.
    -   &lt;name of preferred format, e.g., email or number&gt;: String. Content of preferred contact type, e.g., email address or phone number.

</td></tr></tbody>
</table>Example:

```

var onContactPrefUtil = new OnCallContactPreferenceUtil();
var contactAttempt = 1;
var gdt = new GlideDateTime();
var rotaSysId = '<Rotation_Sys_ID>';
var catchAllContacts = onContactPrefUtil.getCatchAllContacts(rotaSysId, gdt);
gs.log(JSON.stringify(catchAllContacts));
```

Output:

```
[{
    "type": "user",
    "sys_id": "<Sys_ID>",
    "rota_id": "<Rotation_ID>",
    "roster_id": "",
    "escalation_step_id": "<Escalation_Step_ID>",
    "forced_communication_channel": "",
    "override_user_contact_preference": true,
    "preference_source": "contact",
    "contact_attempt": 1,
    "user_preferences": [{
        "type": "sms",
        "number": "8587200477"
    }],
    "contact_preferences": [{
        "type": "voice",
        "number": "5555555555"
    }]
}]
```

