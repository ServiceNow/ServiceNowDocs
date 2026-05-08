---
title: NotifyScoped - Scoped
description: The NotifyScoped API allows you to interact with Notify calls and SMS messages using scripts.Calls the specified E.164-compliant telephone number.Creates a new conference call GlideRecord.Resumes a call after it was put in a queue \(on hold\).Forwards the specified call to a different call recipient.Returns a list of client sessions that are available to receive calls.Returns all phone numbers and short codes available to Notify.Returns all short codes available to Notify.Returns client tokens for any active telephony drivers for use in WebRTC or mobile clients.Returns the maximum amount of time that a client session stays active for a specified telephony driver before automatically timing out.Determines whether the specified phone number has the specified capability.Removes the specified caller from the current Notify conference call.Performs one or more activities on an active Notify phone call.Mutes the specified conference call participant.Puts the specified call into a queue \(on hold\).Sends a specified SMS message to the specified list of Notify clients \(phone numbers\).Sends an SMS text message to an E.164-compliant phone number.Unmutes the specified conference call participant.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyScoped- Scoped

The NotifyScoped API allows you to interact with Notify calls and SMS messages using scripts.

Execute the NotifyScoped class and its associated methods from the `sn_notify` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyScoped - call\(String notifyPhoneNumber, String toPhoneNumber, GlideRecord conferenceCall, GlideRecord conferenceCallRecord, String userSysId, String groupSysId, GlideRecord sourceRecord\)

Calls the specified E.164-compliant telephone number.

<table id="table_qk4_txx_zfb" class="parameters"><thead><tr><th>

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

Optional. If this parameter is passed in, the callers identified in the **toPhoneNumber** parameter are automatically joined into the conference call identified by this record. GlideRecord for the Notify Call \[notify\_call\] table which identifies the conference call record. This record is automatically added to the outgoing call workflow scratchpad as the workflow.scratchpad.conference\_call variable.

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
new sn_notify.NotifyScoped().call(from, to);
```

This example illustrates how to initiate a call to a list of telephone numbers and automatically join those numbers into a new conference call.

```
var notify = new sn_notify.NotifyScoped();
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

## NotifyScoped - conferenceCall\(GlideRecord sourceRecord\)

Creates a new conference call GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|sourceRecord|GlideRecord|Optional. Record that initiated the request to create the conference call. Used to populate the source and table fields on notify\_conference\_call record.|

|Type|Description|
|----|-----------|
|GlideRecord|New Notify conference call \[notify\_conference\_call\] record.|

```
var notify = new sn_notify.NotifyScoped();
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

## NotifyScoped - dequeueCall\(GlideRecord callRecord\)

Resumes a call after it was put in a queue \(on hold\).

Use this method to resume calls that were put in a queue with the queueCall\(\) method.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|GlideRecord object on the Notify Call \[notify\_call\] table with the held call you want to resume.|

|Type|Description|
|----|-----------|
|void| |

The following example shows how to reactivate a call that was put on hold.

```
var notifyCallGr = new GlideRecord('notify_call');
notifyCallGr.get('active participant sys id');
 
if (notifyCallGr.isValid) {
    sn_notify.NotifyScoped.dequeueCall(notifyCallGr);
}
```

## NotifyScoped - forwardCall\(GlideRecord call, String destination, String dtmf\)

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
    sn_notify.NotifyScoped.forwardCall(notifyCallGr(or) callID, phoneNumber, dtmfTones)
}
```

## NotifyScoped - getAvailableClients\(String notifyNumber\)

Returns a list of client sessions that are available to receive calls.

|Name|Type|Description|
|----|----|-----------|
|notifyNumber|String|Valid Notify phone number.|

<table id="table_jxd_kk2_1gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

GlideRecord from the notify\_client\_session table for the specified phone number. Returns "0" if there are no available client sessions.

</td></tr></tbody>
</table>The following example shows how to use the getAvailableClients\(\) method to index into the notify\_client\_session table and then iterate across all available Notify clients.

```
var clientSessionGr = sn_notify.NotifyScoped.getAvailableClients('+185xxxxxxxx'); 
// Here clientSessionGr is of type GlideRecord on 'notify_client_session' table.
 
var isLoggedInUserAvailable = false;
while (clientSessionGr.next()) {
  if (clientSessionGr.user == gs.getUserID())
    isLoggedInUserAvailable = clientSessionGr.available;
}
gs.info('isLoggedInUserAvailable - ' + isLoggedInUserAvailable);
```

## NotifyScoped - getPhoneNumbers\(\)

Returns all phone numbers and short codes available to Notify.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List of NotifyPhoneNumber objects, each object representing one phone number available to Notify.|

This example illustrates how to obtain the Notify phone numbers and then iterate over the list.

```
// Instantiate notify
var notify = new sn_notify.NotifyScoped();

// Retrieve all available phone numbers
var phoneNumbers = notify.getPhoneNumbers();

// Iterate over phone numbers
for (var i = 0; i < phoneNumbers.length; i++) {
  var number = phoneNumbers[i];

  // Perform any actions using each phone number

}
```

## NotifyScoped - getShortCodes\(\)

Returns all short codes available to Notify.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example illustrates how to obtain the Notify short codes and then iterate over the list.

```
// Instantiate notify
var notify = new sn_notify.NotifyScoped();

// Retrieve all available shortcodes
var shortCodes = notify.getShortCodes();

// Iterate over phone numbers
for (var i = 0; i < shortCodes.length; i++) {
  var shortCode = shortCodes[i];
  gs.log(shortCode.getNumber());

//perform any actions using each shortcode

}
```

## NotifyScoped - getTokens\(GlideRecord, record\)

Returns client tokens for any active telephony drivers for use in WebRTC or mobile clients.

This method uses the currently logged-in user record as the client.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|GlideRecord to use to identify the Notify client, such as a group record or a user record.|

|Type|Description|
|----|-----------|
|String|Web RTC tokens for the supported drivers, as a JSON string with the following format: \{driverName1: "token1", driverName2: "token2"\}, such as "TwilioDirect":"eyJhxxxx.eyJleHAiOiIxxxx.7fejxxx\_mbLxxx"|

This example shows how to obtain the client tokens for the currently logged in user.

```
// get Notify client Tokens per active Notify driver for the currently logged in user
var json = new sn_notify.NotifyScoped().getTokens();
 
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
var notify = new sn_notify.NotifyScoped.Notify();
 
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

This example illustrates how to obtain the client tokens for the active telephony drivers.

```
var notify = new sn_notify.NotifyScoped();
var now_GR = new GlideRecord('sys_user');
if (now_GR.get(gs.getUserID())) {
  gs.info(notify.getTokens(now_GR));
}
```

Output:

```
{"TwilioDirect":"eyJhxxxx.eyJleHAiOiIxxxx.7fejxxx_mbLxxx"}
```

## NotifyScoped - getTokenTTL\(String owner\)

Returns the maximum amount of time that a client session stays active for a specified telephony driver before automatically timing out.

<table id="table_kym_hl2_1gb" class="parameters"><thead><tr><th>

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
</table><table id="table_lym_hl2_1gb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integer

</td><td>

Maximum length of the session \(in seconds\). Default: 1800 seconds

</td></tr></tbody>
</table>The following example shows how to properly call this method and the associated response. It also shows what is returned if an invalid driver is passed.

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

## NotifyScoped - hasCapability\(String notifyPhoneNumber, String capability\)

Determines whether the specified phone number has the specified capability.

The telephony driver associated with the phone number contains a list of all of the capabilities of the phone.

**Note:** In the base system, the Notify JS driver only has 'show\_speakers' as a capability; this can be modified.

|Name|Type|Description|
|----|----|-----------|
|notifyPhoneNumber|String|Phone number for which to check for the specified capability.|
|capability|String|Capability to detect. The string text must be an exact match to what is in the phone.|

<table id="table_c3l_2n2_1gb" class="returns"><thead><tr><th>

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
gs.info(sn_notify.NotifyScoped.hasCapability('+185xxxxxxxx', capability)); // true
 
capability = 'send_sms';
gs.info(sn_notify.NotifyScoped.hasCapability('+185xxxxxxxx', capability)); // false
```

## NotifyScoped - kick\(GlideRecord participant\)

Removes the specified caller from the current Notify conference call.

|Name|Type|Description|
|----|----|-----------|
|participant|GlideRecord|GlideRecord object containing the Notify Participant \[notify\_participant\] record of the caller to remove from the conference call.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to remove a participant from a call.

```
var participant = new GlideRecord('notify_participant');
participant.get('<sys_id>');
if (participant.isValid()) {
    new sn_notify.NotifyScoped().kick(participant);
}
```

## NotifyScoped - modifyCall\(GlideRecord callRecord, NotifyAction notifyAction\)

Performs one or more activities on an active Notify phone call.

Use this method to change the behavior of a call. For example, transferring a call, playing audio, or forcing a hangup.

**Note:** The scoped implementation of this method only supports custom Notify activities. Unlike the global implementation, it does not provide a NotifyAction API. For details on how to create a custom Notify activity, see Notify workflow activities.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|Notify Call \[notify\_call\] record of the call for which to apply the actions.|
|notifyAction|NotifyAction|NotifyAction object describing one or more activities to perform on the call.|

|Type|Description|
|----|-----------|
|void| |

## NotifyScoped - mute\(GlideRecord participantRecord\)

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
    sn_notify.NotifyScoped.mute(notifyParticipantGr);
}
```

## NotifyScoped - queueCall\(GlideRecord callRecord\)

Puts the specified call into a queue \(on hold\).

Resume a queued call using the dequeueCall\(\) method.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|GlideRecord object of the Notify Call record \(notify\_call table\) to put on hold.|

|Type|Description|
|----|-----------|
|void| |

```
var call = new GlideRecord('notify_call');
call.get('<call record sys_id>');
if (call.isValid()) {
    new sn_notify.NotifyScoped().queueCall(call);
}
```

## NotifyScoped - sendBulkSMS\(NotifyPhoneNumber notifyPhoneNumber, String toPhoneNumbers, String messageBody, GlideRecord source\)

Sends a specified SMS message to the specified list of Notify clients \(phone numbers\).

<table id="table_ss5_g1d_1gb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyPhoneNumber

</td><td>

[NotifyPhoneNumber](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#)

</td><td>

Phone number from which the SMS message is being sent.

</td></tr><tr><td>

toPhoneNumbers

</td><td>

String

</td><td>

Comma separated list phone numbers to which to send the SMS message.Format: E.164-compliant

</td></tr><tr><td>

messageBody

</td><td>

String

</td><td>

SMS text to send.

</td></tr><tr><td>

source

</td><td>

[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)

</td><td>

Source record that prompted this SMS message, such as an incident.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Null|

This example shows how to send an SMS message to multiple phone numbers \(bulk SMS\).

```
var incidentGr = new GlideRecord('incident');
incidentGr.get('active incident sys_id');
if (incidentGr.isValid()) {
    sn_notify.NotifyScoped.sendBulkSMS('+15413970605', ['+919885XXXXXX', '+919775XXXXXX'], 'Test automation message', incidentGr);
}
```

## NotifyScoped - sendSMS\(NotifyPhoneNumber notifyPhoneNumber, String toPhoneNumber, String messageBody, GlideRecord source\)

Sends an SMS text message to an E.164-compliant phone number.

This method creates a new record on the Notify Message \[notify\_message\] table and associates it with the source record.

|Name|Type|Description|
|----|----|-----------|
|notifyPhoneNumber|[NotifyPhoneNumber](../../NotifyPhoneNumberScoped/concept/NPNScopedAPI.md#)|Notify phone number or short code to which to send this SMS message.|
|toPhoneNumber|String|E.164-compliant phone number to which to send the SMS message.|
|messageBody|String|SMS text message.|
|source|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|Source record that prompted this SMS message, such as an incident.|

|Type|Description|
|----|-----------|
|String|Unique message SID; stored in the Notify Message \[notify\_message\] record as message\_id.|

The following example shows how to send an SMS message.

```
var incidentGr = new GlideRecord('incident');
incidentGr.get('active incident sys_id');
if (incidentGr.isValid()) {
    sn_notify.NotifyScoped.sendSMS('+15413970605', '+919885XXXXXX', 'Test automation message', incidentGr);
}
```

## NotifyScoped - unmute\(GlideRecord participantRecord\)

Unmutes the specified conference call participant.

|Name|Type|Description|
|----|----|-----------|
|participantRecord|GlideRecord|GlideRecord from the notify\_participant table for the participant to unmute.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to unmute a specified call participant.

```
var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
    sn_notify.NotifyScoped.unmute(notifyParticipantGr);
}
```

