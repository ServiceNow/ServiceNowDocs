---
title: Notify - Global
description: The Notify API allows you to interact with Notify calls and SMS messages using scripts.Calls the specified E.164-compliant telephone number.Creates a new conference call GlideRecord.Resumes a call after it was put in a queue \(on hold\).Forwards the specified call to a different call recipient.Returns a list of client sessions that are available to receive calls.Returns the sys\_id of a specified call's parent call.Returns all phone numbers and short codes available to Notify.Returns client tokens for any active telephony drivers for use in WebRTC or mobile clients.Returns the maximum amount of time that a client session stays active for a specified telephony driver before automatically timing out.Determines whether the specified phone number has the specified capability.Removes the specified caller from the current Notify conference call.Performs one or more actions on an active Notify phone call.Mutes the specified conference call participant.Puts the specified call into a queue \(on hold\).Sends a specified SMS message to the specified list of Notify clients \(phone numbers\).Sends an SMS text message to an E.164-compliant phone number.Unmutes the specified conference call participant.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Notify- Global

The Notify API allows you to interact with Notify calls and SMS messages using scripts.

Access the global Notify class and its associated methods in the `SNC` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Notify - call\(String notifyPhoneNumber, String toPhoneNumber, GlideRecord conferenceCall, GlideRecord conferenceCallRecord, String userSysId, String groupSysId, GlideRecord sourceRecord\)

Calls the specified E.164-compliant telephone number.

In addition, this method can automatically add the specified phone number to a specified conference call.

<table id="table_abs_4hn_wr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyPhoneNumber

</td><td>

String or NotifyPhoneNumber

</td><td>

Notify phone number from which to make the call. When you initiate a call, the outgoing call workflow for the number group associated with this number runs. Ensure this workflow includes a **join conference call** activity to connect the user to the conference call.

</td></tr><tr><td>

toPhoneNumber

</td><td>

String

</td><td>

Phone number to call. Called numbers are added to the conference call.

</td></tr><tr><td>

conferenceCall

</td><td>

GlideRecord

</td><td>

Optional. If this parameter is passed in, the callers identified in the **toPhoneNumber** parameter are automatically joined into the conference call identified by this record. GlideRecord for the Notify Call \[notify\_call\] table that identifies the conference call record. This record is automatically added to the outgoing call workflow scratchpad as the workflow.scratchpad.conference\_call variable.

</td></tr><tr><td>

userSysId

</td><td>

String

</td><td>

Optional. Unique identifier \(sys\_id\) of the user associated with the call.

</td></tr><tr><td>

groupSysId

</td><td>

String

</td><td>

Optional. Unique identifier \(sys\_id\) of the group associated with the call.

</td></tr><tr><td>

sourceRecord

</td><td>

GlideRecord

</td><td>

Optional. Source record that prompted this call.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example illustrates how to initiate a call to another phone number.

```
var from = '+14048007337';
var to = '+31646810495';

// set up call
new SNC.Notify().call(from, to);
```

This example illustrates how to initiate a call to list of telephone numbers and automatically join those numbers into a new conference call.

```
var notify = new SNC.Notify();
var from = '+14041234567';
var participants = ['+31612345678', '+31623456789', '+31687654321'];

// set up a conference call
var conferenceCall = notify.conferenceCall();

// set up the outbound calls for all conference call participants
for (var i in participants) {
    var to = participants[i];
    notify.call(from, to, conferenceCall);
}
```

This example illustrates how to initiate a new conference call.

```
SNC.Notify.call('+15413970605', '+91406XXXXXXX', SNC.Notify.conferenceCall(), null, null, null);
```

This example illustrates how to initiate new a conference call using a user record.

```
var sysUserGr = new GlideRecord('sys_user');
sysUserGr.get('active conference sys id');
 
if (conferenceGr.isValid) {
    SNC.Notify.call('+15413970605', '+91406XXXXXXX', SNC.Notify.conferenceCall(), sysUserGr.getUniqueValue(), null, null);
}
```

This example illustrates how to initiate a new conference call with a user, group, and source record.

```
var sysUserGr = new GlideRecord('sys_user');
sysUserGr.get('active sys user sys id');
 
var sysUserGroupGr = new GlideRecord('sys_user_group');
sysUserGroupGr.get('active sys user group sys id');
 
var incidentGr = new GlideRecord('incident');
incidentGr.get('incident sys_id');
 
if (conferenceGr.isValid) {
    SNC.Notify.call('+15413970605', '+91406XXXXXXX',
        SNC.Notify.conferenceCall(),
        sysUserGr.getUniqueValue(),
        sysUserGroupGr.getUniqueValue(),
        incidentGr.getUniqueValue());
}
```

### Scoped equivalent

To use the call\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - call\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - conferenceCall\(GlideRecord sourceRecord\)

Creates a new conference call GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|sourceRecord|GlideRecord|Optional. Record that initiated the request to create the conference call. Used to populate the source and table fields on notify\_conference\_call record.|

|Type|Description|
|----|-----------|
|GlideRecord|New Notify conference call \[notify\_conference\_call\] record.|

```
var notify = new SNC.Notify();
var from = '+14041234567';
var participants = ['+31612345678', '+31623456789', '+31687654321'];

// set up a conference call
var conferenceCall = notify.conferenceCall();

// set up the outbound calls for all conference call participants
for (var i in participants) {
    var to = participants[i];
    notify.call(from, to, conferenceCall);
}
```

### Scoped equivalent

To use the conferenceCall\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - conferenceCall\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

**Related topics**  


[Notify - call\(String notifyPhoneNumber, String toPhoneNumber, GlideRecord conferenceCall, GlideRecord conferenceCallRecord, String userSysId, String groupSysId, GlideRecord sourceRecord\)](c_NotifyAPI.md#)

## Notify - dequeueCall\(GlideRecord callRecord\)

Resumes a call after it was put in a queue \(on hold\).

Use this method to resume calls that were put in a queue with the queueCall\(\) method.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|A GlideRecord object on the Notify Call \[notify\_call\] table with the held call you want to resume.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to reactivate a call that was put on hold.

```
var notifyCallGr = new GlideRecord('notify_call');
notifyCallGr.get('active participant sys id');
 
if (notifyCallGr.isValid) {
    SNC.Notify.dequeueCall(notifyCallGr);
}
```

### Scoped equivalent

To use the dequeueCall\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - dequeueCall\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - forwardCall\(GlideRecord call, String destination, String dtmf\)

Forwards the specified call to a different call recipient.

|Name|Type|Description|
|----|----|-----------|
|call|GlideRecord or String|Notify call record or the telephony provider call ID, of the call to be forwarded.|
|destination|GlideRecord or String|Notify phone number record or an E.164-compliant phone number, of the caller to which to forward the call.|
|dtmf|String|Dual Tone - Multi Frequency \(DTMF\) code to send upon call connection.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to forward a call to another phone number.

```
var callID = 'CA92374b5aa561dab476a7001db6026edc'; // Twilio Call ID
var phoneNumber = '+91406xxxxxxx';
var dtmfTones = null;
 
var notifyCallGr = new GlideRecord('notify_call');
notifyCallGr.get('active participant sys id');
 
if (notifyCallGr.isValid) {
    SNC.Notify.forwardCall(notifyCallGr(or) callID, phoneNumber, dtmfTones)
}
```

### Scoped equivalent

To use the forwardCall\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - forwardCall\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - getAvailableClients\(String notifyNumber\)

Returns a list of client sessions that are available to receive calls.

|Name|Type|Description|
|----|----|-----------|
|notifyNumber|String|Valid Notify phone number.|

<table id="table_jbs_r1n_ms" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideRecord

</td><td>

GlideRecord from the notify\_client\_session table for the specified phone number. Returns "0" if there are no available client sessions.

</td></tr></tbody>
</table>The following example shows how to use the getAvailableClients\(\) method to index into the notify\_client\_session table and then iterate across all available Notify clients.

```
var clientSessionGr = SNC.Notify.getAvailableClients('+185xxxxxxxx'); 
// Here clientSessionGr is of type GlideRecord on 'notify_client_session' table.
 
var isLoggedInUserAvailable = false;
while (clientSessionGr.next()) {
  if (clientSessionGr.user == gs.getUserID())
    isLoggedInUserAvailable = clientSessionGr.available;
}
gs.info('isLoggedInUserAvailable - ' + isLoggedInUserAvailable);
```

### Scoped equivalent

To use the getAvailableClients\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - getAvailableClients\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - getParentCallID\(GlideRecord callRecord\)

Returns the sys\_id of a specified call's parent call.

Any call started by forwarding another call, such as with the Forward workflow activity, is considered a child of the original call. The original call is the parent call.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|Record on the Notify Call \[notify\_call\] table for which to return the call status.|

|Type|Description|
|----|-----------|
|String|Unique sys\_id of the parent call record.|

This example shows how to obtain the parent call of the specified call.

```
var callRecord = new GlideRecord('notify_call');
callRecord.get("0f4f5863ff13310014ecffffffffff28");

var notify = new SNC.Notify();
var parentCallID = notify.getParentCallID(callRecord);
```

## Notify - getPhoneNumbers\(\)

Returns all phone numbers and short codes available to Notify.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|List|List of NotifyPhoneNumber objects, each object representing one phone number available to Notify.|

```
var list = SNC.Notify.getPhoneNumbers();
for (var i = 0; i < list.size(); i++) {
    var num = list.get(i);
    gs.info(num.getNumber())
}
```

### Scoped equivalent

To use the getPhoneNumbers\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - getPhoneNumbers\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - getTokens\(GlideRecord, record\)

Returns client tokens for any active telephony drivers for use in WebRTC or mobile clients.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|GlideRecord to use to identify the Notify client, such as a group record or a user record.|

|Type|Description|
|----|-----------|
|String|Web RTC tokens for the supported drivers, as a JSON string with the following format: \{driverName1: "token1", driverName2: "token2"\}, such as "TwilioDirect":"eyJhxxxx.eyJleHAiOiIxxxx.7fejxxx\_mbLxxx"|

This example shows how to obtain the client tokens for the currently logged in user.

```
// get Notify client Tokens per active Notify driver for the currently logged in user
var json = new SNC.Notify().getTokens();
 
// Parse the JSON that was return into a tokens object
var tokens = JSON.parse(json);

// Log line
gs.log('Notify client tokens for the currently logged in user');

 // iterate over the driver tokens
for (var driver in tokens) {
 	gs.log(driver + ' Driver token: ' + tokens[driver]);
}
```

This example shows how to obtain the client tokens for every Notify group.

```
// instantiate Notify
var notify = new SNC.Notify();
 
// get all Notify Groups
var notifyGroup = new GlideRecord("notify_group");
notifyGroup.query();
 
// iterate over all notify groups
while (notifyGroup.next()) {
  // generate Notify Client tokens per active Notify Driver for this group
  var json = notify.getTokens(notifyGroup);
  var tokens = JSON.parse(json);
 
  for (var driver in tokens) {
    gs.log(gs.getMessage("Notify Client token for {0} driver and Notify Group '{1}': {2}", [driver, notifyGroup.getValue('name'), tokens[driver]]));
  }
}
```

### Scoped equivalent

To use the getTokens\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - getTokens\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - getTokenTTL\(String owner\)

Returns the maximum amount of time that a client session stays active for a specified telephony driver before automatically timing out.

<table id="table_mnj_xqb_zfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

owner

</td><td>

String

</td><td>

Name of the telephony driver for which to retrieve the session length. Valid values:

 -   Twilio: for the old driver
-   TwilioDirect: for the new driver

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Integer|Maximum length of the session \(in seconds\). Default: 1800 seconds|

The following example shows how to properly call this method and the associated response. It also shows what is returned if an invalid driver is passed.

```
var owner = "TwilioDirect";  // Valid driver
var ttl = SNC.Notify.getTokenTTL(owner);
gs.info("Token TTL for " + owner + " --> " + ttl);
 
owner = "Abcxyz";  // Invalid driver
ttl = SNC.Notify.getTokenTTL(owner);
// For an invalid driver, we throw NoSuchNotifyDriverException saying that Abcxyzdriver is not available
// and return the default value of TTL
gs.info("Token TTL for " + owner + " --> " + ttl); 
```

### Scoped equivalent

To use the getTokenTTL\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - getAvailableClients\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - hasCapability\(String notifyPhoneNumber, String capability\)

Determines whether the specified phone number has the specified capability.

The telephony driver associated with the phone number contains a list of all of the capabilities of the phone.

**Note:** In the base system, the Notify JS driver only has 'show\_speakers' as a capability; this can be modified.

|Name|Type|Description|
|----|----|-----------|
|notifyPhoneNumber|String|Phone number for which to check for the specified capability.|
|capability|String|Capability to detect. The string text must be an exact match to what is in the phone.|

<table id="table_wsy_rdg_yfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified phone has the specified capability.-   true: phone has the capability
-   false: phone does not have the capability

</td></tr></tbody>
</table>This example shows how to check if a phone has a specific capability.

```
// Each driver has a defined set of capabilities.

var capability = 'show_speakers';
gs.info(SNC.Notify.hasCapability('+185xxxxxxxx', capability)); // true
 
capability = 'send_sms';
gs.info(SNC.Notify.hasCapability('+185xxxxxxxx', capability)); // false
```

### Scoped equivalent

To use the hasCapability\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - hasCapability\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - kick\(GlideRecord participant\)

Removes the specified caller from the current Notify conference call.

|Name|Type|Description|
|----|----|-----------|
|participant|GlideRecord|GlideRecord object containing the Notify Participant \[notify\_participant\] record of the caller to remove from the conference call.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to remove a participant from a conference call.

```
var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
    SNC.Notify.kick(notifyParticipantGr);
}
```

### Scoped equivalent

To use the kick\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - kick\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - modifyCall\(GlideRecord callRecord, NotifyAction notifyAction\)

Performs one or more actions on an active Notify phone call.

Available actions that you can perform on calls include queuing or dequeueing the call, reading text, playing audio, or forwarding the call. You can also create custom actions Call the modifyCall\(\) method after you have specified all the actions that you want to apply to the specified call. Refer to the [NotifyAction](../../NotifyAction/concept/c_NotifyActionApi.md#) API documentation for more information about available actions.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|Notify Call \[notify\_call\] record of the call for which to apply the actions.|
|notifyAction|NotifyAction|NotifyAction object describing one or more actions to perform on the call. Create this object by calling one or more of the NotifyAction\(\) methods.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to modify a call.

```
// get the most recent call record
var callRecord = new GlideRecord('notify_call');
callRecord.orderByDesc('sys_created_on');
callRecord.query();
 
if (callRecord.next()) {
    // instantiate notify action container class
    var notifyAction = new SNC.NotifyAction();
    // The call is already in progress. Now, we want to modify the call behavior by putting this call in a queue.
    // So, we add a queue action to queue the call
    notifyAction.addQueue('my fancy queue');
   
    // modify the call by passing in the above action, putting the call in a queue
    new SNC.Notify().modifyCall(callRecord, notifyAction);
} else {
    gs.log('no such call record');
}
```

### Scoped equivalent

To use the modifyCall\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - modifyCall\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - mute\(GlideRecord participantRecord\)

Mutes the specified conference call participant.

|Name|Type|Description|
|----|----|-----------|
|participantRecord|GlideRecord|GlideRecord from the notify\_participant table for the participant to mute.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to mute a caller.

```
var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
    SNC.Notify.mute(notifyParticipantGr);
}
```

### Scoped equivalent

To use the mute\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - mute\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - queueCall\(GlideRecord callRecord\)

Puts the specified call into a queue \(on hold\).

Resume a queued call using the dequeueCall\(\) method.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|GlideRecord object of the Notify Call record \(notify\_call table\) to put on hold.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to put a call on hold \(in the queue\).

```
var notifyCallGr = new GlideRecord('notify_call');
notifyCallGr.get('active participant sys id');
 
if (notifyCallGr.isValid) {
    SNC.Notify.queueCall(notifyCallGr);
}
```

### Scoped equivalent

To use the queueCall\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - queueCall\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - sendBulkSMS\(String notifyPhoneNumber, Array toPhoneNumbers, String messageBody, GlideRecord source\)

Sends a specified SMS message to the specified list of Notify clients \(phone numbers\).

<table id="table_n2q_3zf_yfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyPhoneNumber

</td><td>

String

</td><td>

Notify phone number from which the SMS message is being sent.

</td></tr><tr><td>

toPhoneNumbers

</td><td>

Array of Strings

</td><td>

Comma-separated list of phone numbers to which to send the SMS message.Format: E.164

</td></tr><tr><td>

messageBody

</td><td>

String

</td><td>

SMS text to send.

</td></tr><tr><td>

source

</td><td>

GlideRecord

</td><td>

Source record that prompted this SMS message, such as an incident.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Null|

The following example shows how to send a bulk SMS message.

```
var incidentGr = new GlideRecord('incident');
incidentGr.get(active incident sys_id');
if (incidentGr.isValid()) {
    SNC.Notify.sendBulkSMS('+15413970605', ['+919885XXXXXX', '+919775XXXXXX'], 'Test automation message', incidentGr);
}
```

### Scoped equivalent

To use the sendBulkSMS\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - sendBulkSMS\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - sendSMS\(String notifyPhoneNumber, String toPhoneNumber, String messageBody, GlideRecord source\)

Sends an SMS text message to an E.164-compliant phone number.

This method creates a new record on the Notify Message \[notify\_message\] table and associates it with the source record.

|Name|Type|Description|
|----|----|-----------|
|notifyPhoneNumber|String|Notify phone number from which the SMS message is being sent.|
|toPhoneNumber|String|E.164-compliant phone number to which to send the SMS message.|
|messageBody|String|Body of the SMS text message.|
|source|GlideRecord|Source record that prompted this SMS message, such as an incident.|

|Type|Description|
|----|-----------|
|String|Unique message SID; stored in the Notify Message \[notify\_message\] record as message\_id.|

The following example shows how to send an SMS message.

```
var incidentGr = new GlideRecord('incident');
incidentGr.get('active incident sys_id');
if (incidentGr.isValid()) {
    SNC.Notify.sendSMS('+15413970605', '+919885XXXXXX', 'Test automation message', incidentGr);
}
```

### Scoped equivalent

To use the sendSMS\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - sendSMS\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

## Notify - unmute\(GlideRecord participantRecord\)

Unmutes the specified conference call participant.

|Name|Type|Description|
|----|----|-----------|
|participantRecord|GlideRecord|GlideRecord from the notify\_participant table for the participant to unmute.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to unmute a caller.

```
var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
    SNC.Notify.unmute(notifyParticipantGr);
}
```

### Scoped equivalent

To use the unmute\(\) method in a scoped application, use the corresponding scoped method: [NotifyScoped - unmute\(\)](../../NotifyScoped/concept/notifyScopedAPI.md#).

