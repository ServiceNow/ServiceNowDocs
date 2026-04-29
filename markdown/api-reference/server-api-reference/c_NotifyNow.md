---
title: NotifyNow \(Legacy\) - Global
description: The legacy NotifyNow API provides functionality for sending emails, sending SMS messages, and setting up conference calls.Adds ad-hoc users to an ongoing conference call.Converts a local phone number to an E.164-compliant phone number based on a user's location.Returns all participants for a conference call.Returns a number of frequently-called users, up to the limit parameter, in alphabetical order.Returns a user's preferred E.164-compliant phone number for SMS messages.Returns a user's preferred E.164-compliant phone number for voice calls.Returns a user's preferred email addressIndicates whether Notify is set up correctly or not.Returns the current status of Notify configuration.Initiate a new conference call.Initiate a new conference call.Determines whether a user is callable or not.Checks if the telephone number associated with the Twilio account is capable of sending SMS messages.Checks if a user is able to send SMS messages.Checks if the telephone number associated with the Twilio account is capable of setting up phone calls.Checks if a user is able to make voice calls.Removes a participant from a conference call.Mutes a participant on a conference call.Send an email question to an email address.Sends an SMS message to an E.164-compliant mobile phone number.Sends an SMS message to an E.164-compliant mobile phone number.Sends an SMS question.Unmutes a participant on a conference call.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyNow \(Legacy\)- Global

The legacy NotifyNow API provides functionality for sending emails, sending SMS messages, and setting up conference calls.

Use this when you want to use Notify functionality with applications on your system.

**Note:** This API is included with the legacy Notify functionality. For APIs included in the current Notify feature, see the Notify, NotifyAction, NotifyPhoneNumber, and NotifyClient APIs.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyNow - addConferenceCallParticipant\(String conferenceCall, String participant\)

Adds ad-hoc users to an ongoing conference call.

When the method is called with a phone number for the participant parameter and there is exactly one sys\_user record that matches the phone number, that sys\_user record will be related to the participant. The participant's phone number field will be left blank because the phone number is in the sys\_user record. If there are several sys\_user records that match the phone number, or if there are no results, the participant's phone number field will be filled in, and there will be no stored reference to sys\_user because the user is not known.

|Name|Type|Description|
|----|----|-----------|
|conferenceCall|String or GlideRecord|The sys\_id or GlideRecord of an active conference call.|
|participant|String or GlideRecord|The sys\_id or GlideRecord of a user with an E.164-compliant phone number, or an E.164-compliant phone number.|

|Type|Description|
|----|-----------|
|GlideRecord|The participant record of the new participant that was added to the conference call.|

```
// add a new participant by conference call sys_id (string) and phone number (string) 
var nn = new SNC.NotifyNow();
gs.log(nn.addConferenceCallParticipant('d193b242eb020100a04d4910f206fe39', '+31612345678'));
```

```
// add a new participant by conference call sys_id (string) and user record (GlideRecord)
var user = new GlideRecord('sys_user');
user.query('user_name', 'myUserName');
if (user.hasNext() && user.next()) {
    var nn = new SNC.NotifyNow();
    gs.log(nn.addConferenceCallParticipant('d193b242eb020100a04d4910f206fe39', user));
 
    // you could have added the user by sys_id as well:
    // nn.addConferenceCallParticipant('d193b242eb020100a04d4910f206fe39', user.getValue('sys_id'));
} else {
    gs.log('no such user');
}
```

```
// add a new participant by conference call record (GlideRecord) and phone number (string)
var conferenceCall = new GlideRecord('notifynow_conference_call');
conferenceCall.query('title', 'IA0001001');
if (conferenceCall.hasNext() && conferenceCall.next()) {
    var nn = new SNC.NotifyNow();
    gs.log(nn.addConferenceCallParticipant(conferenceCall, '+31612345678'));
} else {
    gs.log('no such conference call');
}
```

## NotifyNow - convertLocalPhoneNumberToE164\(String userID, String phoneNumber\)

Converts a local phone number to an E.164-compliant phone number based on a user's location.

|Name|Type|Description|
|----|----|-----------|
|userID|String|The sys\_id of a sys\_user record to get location information from.|
|phoneNumber|String|The phone number.|

|Type|Description|
|----|-----------|
|String|The E.164-compliant phone number.|

```
var localPhoneNumber = '01784 221600';
var userName = 'Heath Vanalphen';
 
var user = new GlideRecord('sys_user');
user.get('name',userName);
var E164Number = new SNC.NotifyNow().convertLocalPhoneNumberToE164(user.getUniqueValue(), localPhoneNumber);
gs.log('converted: ' + localPhoneNumber + ' to ' + E164Number + ' based on ' + user.getValue('name') + 
     '\'s location (' + user.getValue('location') + ')');
```

## NotifyNow - getConferenceCallParticipants\(String conferenceCallId, Boolean isCallable\)

Returns all participants for a conference call.

|Name|Type|Description|
|----|----|-----------|
|conferenceCallId|String|The ID of the conference call.|
|isCallable|Boolean|An optional flag to return either only the users you can call \(true\) or those you cannot call \(false\).|

|Type|Description|
|----|-----------|
|GlideRecord|The participants|

```
var nn = new SNC.NotifyNow();
var user = nn.getConferenceCallParticipants('c2e91710eb120100f34087b9d106fe37');
 
while (user.hasNext() && user.next()) {
    if (user.getValue('participant')) {
        gs.log('user: ' + user.getValue('sys_id'));
    } else {
        gs.log('phone number: ' + user.getValue('phone_number'));
    }
}
```

```
var nn = new SNC.NotifyNow();
var user = nn.getConferenceCallParticipants('c2e91710eb120100f34087b9d106fe37', true);
 
while (user.hasNext() && user.next()) {
    if (user.getValue('participant')) {
        gs.log('user: ' + user.getValue('sys_id'));
    } else {
        gs.log('phone number: ' + user.getValue('phone_number'));
    }
}
```

```
var conferenceCallId = '32b11430eb1201003cf587b9d106feb8';
 
// get all participants
gs.log('all conference call participants:');
var nn = new SNC.NotifyNow();
var user = nn.getConferenceCallParticipants(conferenceCallId);
gs.log(user);
 
// get all callable participants
gs.log('all conference call participants we can call:');
user = nn.getConferenceCallParticipants(conferenceCallId, true);
gs.log(user);
 
// get all un callable participants
gs.log('all conference call participants that are already in an active session and whom we cannot call:');
user = nn.getConferenceCallParticipants(conferenceCallId, false);
gs.log(user);
```

## NotifyNow - getFrequentlyCalledUsers\(Number limit\)

Returns a number of frequently-called users, up to the limit parameter, in alphabetical order.

|Name|Type|Description|
|----|----|-----------|
|limit|Number|The maximum number of results.|

|Type|Description|
|----|-----------|
|GlideRecord|The frequently called users in alphabetical order.|

```
var nn = new SNC.NotifyNow();
var fc = nn.getFrequentlyCalledUsers(10);
 
while (fc.hasNext() && fc.next()) {
    gs.log("got user " + fc.getValue('name') + ' - ' + fc.getValue('sys_id'));
}
```

## NotifyNow - getPreferredE164SMSNumber\(GlideRecord user\)

Returns a user's preferred E.164-compliant phone number for SMS messages.

|Name|Type|Description|
|----|----|-----------|
|user|GlideRecord or String|The user record or the sys\_id of a user to get the E.164-compliant phone number from.|

|Type|Description|
|----|-----------|
|String|The E.164-compliant phone number or null.|

```
var userID = "<user sys_id>";
var E164Number = new SNC.NotifyNow().getPreferredE164SMSNumber(userID);
gs.log('the preferred phone number for sending SMS notifications is ' + E164Number + ' for user with id: ' + userID);
```

## NotifyNow - getPreferredE164VoiceNumber\(GlideRecord user\)

Returns a user's preferred E.164-compliant phone number for voice calls.

|Name|Type|Description|
|----|----|-----------|
|user|GlideRecord or String|The user record or the sys\_id of a user to get the E.164-compliant phone number from.|

|Type|Description|
|----|-----------|
|String|The E.164-compliant phone number or null.|

```
var userID = "<user sys_id>";
var E164Number = new SNC.NotifyNow().getPreferredE164VoiceNumber(userID);
gs.log('the preferred phone number for setting up voice calls is ' + E164Number + ' for user with id: ' + userID);
```

## NotifyNow - getPreferredEmailAddress\(GlideRecord user\)

Returns a user's preferred email address

|Name|Type|Description|
|----|----|-----------|
|user|GlideRecord or String|The user record or the sys\_id of a user to get the email address from.|

|Type|Description|
|----|-----------|
|String|The email address or null.|

```
var userID = "some user sys id";
var email = new SNC.NotifyNow().getPreferredEmailAddress(userID);
gs.log('the preferred email address for sending email notifications is ' + email + ' for user with id: ' + userID);
```

## NotifyNow - getReadyState\(\)

Indicates whether Notify is set up correctly or not.

This method can only be accessed by administrators or users with the notifynow\_admin role. Users with all other roles get the message False when trying to run the function in a script.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if Notify is set up correctly, otherwise false.|

```
var nn = new SNC.NotifyNow();
gs.log(((nn.getReadyState()) ? "OK" :  "NOT OK"));
```

## NotifyNow - getStatus\(\)

Returns the current status of Notify configuration.

This method can only be accessed by administrators or users with the notifynow\_admin role. Users with all other roles get the message Unauthorized when trying to run the function in a script.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_uxg_fc2_vt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

One of the possible status messages.<table id="table_gdb_jc2_vt"><tbody><tr><td>

Status

</td><td>

Description

</td></tr><tr><td>

NO\_NUMBER\_MESSAGE

</td><td>

The account does not have a telephone number set up. Ensure that you set up the telephone number for the account.

</td></tr><tr><td>

NO\_ENDPOINTS\_MESSAGE

</td><td>

The account does not have its endpoints set up correctly. Ensure that you set up the endpoints for the account.

</td></tr><tr><td>

ACCOUNT\_OK\_MESSAGE

</td><td>

The account is active and ready for use.

</td></tr><tr><td>

ACCOUNT\_NO\_AUTH

</td><td>

The Twilio AuthToken is not valid.

</td></tr><tr><td>

ACCOUNT\_NOT\_CONFIGURED

</td><td>

The Twilio AccountSID or AuthToken is not valid.

</td></tr></tbody>
</table>

</td></tr></tbody>
</table>```
var nn = new SNC.NotifyNow();
gs.log(nn.getStatus());
```

## NotifyNow - initiateConferenceCall\(String\[\] conferenceCallParticipants, String conferenceCallTitle\)

Initiate a new conference call.

|Name|Type|Description|
|----|----|-----------|
|conferenceCallParticipants|String|One or more users, conference call participants, identified by the sys\_ids from the sys\_user table or E.164-compliant phone numbers.|
|conferenceCallTitle|String|Title of the conference call. This parameter has a maximum length of 40 characters.|

|Type|Description|
|----|-----------|
|GlideRecord|The conference call record, or null if there was an error.|

This initiates a conference call with E.164-compliant phone numbers for participants, without the optional source record parameter and and does not send any conference call details via SMS or email.

```
var participants = ['+31205655548', '+31205655552', '+31652825393'];
// set up conference call
var nn = new SNC.NotifyNow();
var conferenceCall = nn.initiateConferenceCall(participants, "testing12");
gs.log('started conference call: ' + conferenceCall.getUniqueValue());
```

## NotifyNow - initiateConferenceCall\(String\[\] conferenceCallParticipants, String conferenceCallTitle, GlideRecord sourceRecord, Boolean private\)

Initiate a new conference call.

|Name|Type|Description|
|----|----|-----------|
|conferenceCallParticipants|String|One or more users, conference call participants, identified by the sys\_ids from the sys\_user table or E.164-compliant phone numbers.|
|conferenceCallTitle|String|Title of the conference call. This parameter has a maximum length of 40 characters.|
|sourceRecord|GlideRecord|Source record to associate to the conference call such as an incident or problem number.|
|private|Boolean|Value to control if a conference call is private. This value defaults to false.|

|Type|Description|
|----|-----------|
|GlideRecord|The conference call record, or null if there was an error.|

This initiates a conference call with participants that have a E.164-compliant phone number and participants from the sys\_user table and sends conference call details via SMS and email to all participants.

```
// define phone number participants
var participants = ['+31205655548', '+31205655552', '+31652825393'];
 
// we also want to add two Dutch sys_user participants
var user = new GlideRecord('sys_user');
user.addNotNullQuery('mobile_phone');
user.addQuery('mobile_phone', 'STARTSWITH', '+316');
user.setLimit(2);
user.query();
 
// add users to the participant array
while (user.hasNext() && user.next()) {
	gs.log('adding user ' + user.getValue('name') + ' with phone number ' + 
             user.getValue('mobile_phone') + ' to the participant array');
	participants.push(user.getUniqueValue());
}
 
// define a source record to associate with the conference call
var source = new GlideRecord("cmdb_ci");
source.query("asset_tag", "P1000167");
if (source.hasNext() && source.next()) {
	// set up conference call
	var nn = new SNC.NotifyNow();
	var conferenceCall = nn.initiateConferenceCall(participants, "testing 1 2", source);
 
	// check if the conference call was successfully created
	if (conferenceCall != null) {
		gs.log('started conference call: ' + conferenceCall.getUniqueValue());
	} else {
		gs.log('could not start the conference call :(');
	}
}
```

## NotifyNow - isCallable\(String participant\)

Determines whether a user is callable or not.

A user must have a valid phone number to be callable. A user who is already in an active session is not callable.

|Name|Type|Description|
|----|----|-----------|
|participant|String or GlideRecord|A sys\_user or notifynow\_participant record, or an E.164-compliant phone number.|

|Type|Description|
|----|-----------|
|boolean|Whether this participant can be called or not.|

```
var nn = new SNC.NotifyNow();
gs.log('by number: ' + nn.isCallable('+31612345678'));
 
var user = GlideRecord('sys_user');
user.query('sys_id', '13d39544eb5201003cf587b9d106fea9');
if (user.hasNext() && user.next())
  gs.log('by user: ' + nn.isCallable(user));
 
var participant = GlideRecord('notifynow_participant');
participant.query('sys_id', '33b11430eb1201003cf587b9d106feb9');
if (participant.hasNext() && participant.next())
  gs.log('by participant: ' + nn.isCallable(participant));
```

## NotifyNow - isSMSCapable\(\)

Checks if the telephone number associated with the Twilio account is capable of sending SMS messages.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Whether the telephone number associated with the Twilio account is capable of sending SMS messages.|

```
gs.log('The twilio number is SMS capable: ' + ((new SNC.NotifyNow().isSMSCapable()) ? 'yes' : 'no'));
```

## NotifyNow - isSMSCapable\(String userID\)

Checks if a user is able to send SMS messages.

|Name|Type|Description|
|----|----|-----------|
|userID|String|The sys\_id of the user you want to check for an SMS-capable phone number.|

|Type|Description|
|----|-----------|
|Boolean|If the user can send SMS messages.|

```
gs.log('the user is able to send SMS messages (e.g. has a SMS device): ' + ((new SNC.NotifyNow().isSMSCapable('<user sys_id>')) ? 
     'yes' : 'no'));
```

## NotifyNow - isVoiceCapable\(\)

Checks if the telephone number associated with the Twilio account is capable of setting up phone calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Whether the telephone number associated with the Twilio account is capable of setting up phone calls.|

```
gs.log('the Twilio number is Voice capable: ' + ((new SNC.NotifyNow().isVoiceCapable()) ? 'yes' : 'no'));
```

## NotifyNow - isVoiceCapable\(String userID\)

Checks if a user is able to make voice calls.

|Name|Type|Description|
|----|----|-----------|
|userID|String|The sys\_id of the user you want to check for a voice-call capable phone number.|

|Type|Description|
|----|-----------|
|boolean|Whether the user has a voice-call capable phone number.|

```
gs.log('the user is able to send SMS messages (e.g. has a SMS device): ' + 
     ((new SNC.NotifyNow().isVoiceCapable('someuserid')) ? 'yes' : 'no'));
```

## NotifyNow - kick\(GlideRecord participant\)

Removes a participant from a conference call.

|Name|Type|Description|
|----|----|-----------|
|participant|GlideRecord|The conference call participant to remove from the call.|

|Type|Description|
|----|-----------|
|Boolean|True if the participant was removed, otherwise false.|

```
var participantId = "<participant sys_id>";
var participant = new GlideRecord('notifynow_participant');
participant.get(participantId);
if (participant.isValid()) {
     // kick participant
     result = new SNC.NotifyNow().kick(participant);
     gs.log('participant kicked: ' + result);
}
```

## NotifyNow - mute\(GlideRecord participant\)

Mutes a participant on a conference call.

|Name|Type|Description|
|----|----|-----------|
|participant|GlideRecord|The conference call participant to mute.|

|Type|Description|
|----|-----------|
|Boolean|True if the participant was muted, otherwise false.|

```
var participantId = "<participant sys_id>";
var participant = new GlideRecord('notifynow_participant');
participant.get(participantId);
if (participant.isValid()) {
     // mute participant
     result = new SNC.NotifyNow().mute(participant);
     gs.log('participant muted: ' + result);
}
```

## NotifyNow - sendEmailQuestion\(String emailAddress, String question, GlideRecord sourceRecord, String emailSubject\)

Send an email question to an email address.

The sendEmailQuestion method produces a question body and requires users to click a link to indicate their choice.

|Name|Type|Description|
|----|----|-----------|
|emailAddress|String|Email address to send the question to.|
|question|String or GlideRecord|The question record to send or the sys\_id of a question record.|
|sourceRecord|GlideRecord|An optional source record to associate to the SMS question, such as an incident.|
|emailSubject|String|Optional text to override the default email subject.|

|Type|Description|
|----|-----------|
|String|The conversation sys\_id.|

This example demonstrates using the default email subject.

```
var user = GlideRecord("sys_user");
user.get("email", "someone@somedomain.com");
 
new SNC.NotifyNow().sendEmailQuestion(user.getValue('email'), "b6b34500bf3111003cf585ce2c0739ce", user);
```

This example uses dot-walking and specifies a source record and email subject.

```
new SNC.NotifyNow().sendEmailQuestion("someone@somedomain.com", "b6071733bf1111003cf585ce2c07390f", current, 
        "Please answer this question");
```

This example uses dot-walking and specifies an email subject but no source record.

```
new SNC.NotifyNow().sendEmailQuestion("someone@somedomain.com", "b6071733bf1111003cf585ce2c07390f", 
        "Please answer this question");
```

## NotifyNow - sendSMS\(String phoneNumber, String smsBody\)

Sends an SMS message to an E.164-compliant mobile phone number.

Notify supports international numbers. Using this method with a number that does not support sending SMS messages results in an error being logged.

|Name|Type|Description|
|----|----|-----------|
|phoneNumber|String|The E.164-compliant phone number to send the message to.|
|smsBody|String|The message to send, maximum 1600 characters.|

|Type|Description|
|----|-----------|
|void| |

```
new SNC.NotifyNow().sendSMS("+31612345678", "This is a message without source record");
```

## NotifyNow - sendSMS\(String phoneNumber, String smsBody, GlideRecord source\)

Sends an SMS message to an E.164-compliant mobile phone number.

Notify supports international numbers. Using this method with a number that does not support sending SMS messages results in an error being logged.

See also: [Advanced configuration for SMS](https://www.servicenow.com/docs/access?context=t_ConfigureNotifyforVoiceandSMS&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|phoneNumber|String|The E.164-compliant phone number to send the message to.|
|smsBody|String|The message to send, maximum 1600 characters.|
|source|GlideRecord|The source record to associate with this SMS message.|

|Type|Description|
|----|-----------|
|void| |

```
var source = new GlideRecord("my_table");
source.query("my_field", "my_value");

if (source.hasNext() && source.next()) {
    // send a text message
    var nn = new SNC.NotifyNow();
    var message = "this is just a test";
    var number = "+31612345678";
    nn.sendSMS(number, message, source);
}
```

This example uses dot-walking and the current record as the source record.

```
new SNC.NotifyNow().sendSMS("+31612345678", "this is a test", current);
```

## NotifyNow - sendSMSQuestion\(String phoneNumber, String question, GlideRecord sourceRecord\)

Sends an SMS question.

|Name|Type|Description|
|----|----|-----------|
|phoneNumber| |An E.164-compliant phone number to send the message to.|
|question|String or GlideRecord|The question record to send or the sys\_id of a question record.|
|sourceRecord| |An optional source record to associate to the SMS question, such as an incident.|

|Type|Description|
|----|-----------|
|String|The conversation sys\_id, or null if the SMS was not sent successfully.|

```
var question = new GlideRecord("notifynow_question");
question.query();
 
// get the first question
if (question.hasNext() && question.next()) {
	// send the sms question
        var number = "+31612345678";
	var nn = new SNC.NotifyNow();
	nn.sendSMSQuestion(number, question.getUniqueValue(), current);
}
```

## NotifyNow - umute\(GlideRecord participant\)

Unmutes a participant on a conference call.

|Name|Type|Description|
|----|----|-----------|
|participant|GlideRecord|The muted conference call participant to unmute.|

|Type|Description|
|----|-----------|
|Boolean|True if the participant was unmuted, otherwise false.|

```
var participantId = "<participant sys_id>";
var participant = new GlideRecord('notifynow_participant');
participant.get(participantId);
if (participant.isValid()) {
     // unmute participant
     result = new SNC.NotifyNow().unmute(participant);
     gs.log('participant unmuted: ' + result);
}
```

