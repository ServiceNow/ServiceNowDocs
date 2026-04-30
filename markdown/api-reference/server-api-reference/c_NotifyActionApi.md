---
title: NotifyAction - Global
description: The NotifyAction API allows you to define actions to send to a telephony provider.Adds a conference action to move the current call into the current conference call.Defines whether the conference call should end when a specified caller exits the conference call.Defines whether the conference call should end when a participant presses the star \(\*\) key.Defines whether the specified caller should be muted in the current conference call.Sets the name of the current conference call to the specified name.Defines whether the associated conference call should be recorded.Defines whether the conference call should start when the specified caller joins the conference call.Forwards a call to a specified phone number or Notify Client.Defines the caller ID for the outgoing call.Sets the current caller to a Notify caller by specifying the table in which to find the Notify caller record and the caller's unique identifier.Defines the DTMF tones to play when the call connects.Defines whether the call should end when the star \(\*\) key is pressed.Defines the phone number to call.Defines whether the outgoing call should be recorded.Sets the number of seconds after which the outgoing call times out.Presents a specified interactive phone menu to the caller.Plays an audio file on the call.Defines the text-to-speech to read on the call.Defines the key that the caller inputs to denote the end of their input.Defines the number of digits to collect.Defines the amount of time after which gathering of input will timeout.Ends an active phone call.Queues the call, which puts the call on hold.Removes the call from the current call queue \(takes it off of "hold"\).Defines the name associated with a queue.Plays an audio file on the call.Defines the number of times to play \(loop through\) the audio file.Defines the URL where to obtain the audio file to play.Adds an action to record the call to the current NotifyAction object.Defines the key that terminates the recording.Defines the maximum length of the recording.Sets the number of seconds of silence, after which, the recording ends.Rejects an incoming call.Defines the reason why the call was rejected.Defines the text-to-speech to read on the call.Defines the language in which to speak the text.Defines the text to be read within the current call.Sends an SMS message.Defines the text of the SMS message to send.Sets the phone number to which to sent the SMS message.Appends the specified NotifyAction object to the current client's NotifyAction object.Deserialize a NotifyAction object from a JSON string.Defines the Notify call record in which to add subsequent actions.Serialize the NotifyAction object to a JSON string.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 23
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyAction- Global

The NotifyAction API allows you to define actions to send to a telephony provider.

You add actions to a NotifyAction object by calling the respective add function for each type of action. Each add function returns an Action object, such as a SayAction object for the addSay\(\) method. Refer to each method example for information about returned objects.

**Note:** The NotifyAction API is only valid within global applications. To utilize this type of functionality within scoped applications, you must create custom Notify workflow activities. For additional information on creating these activities, see [Notify workflow activities](https://www.servicenow.com/docs/access?context=c_NotifyActivities&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyAction - addConference\(\)

Adds a conference action to move the current call into the current conference call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ConferenceAction|Action added to the NotifyAction object. Use the ConferenceAction object to define the conference call name, and the behavior of the conference call when a participant joins or leaves.|

This example demonstrates how to add a conference action and set the name of the conference.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set its name
var conference = notifyAction.addConference();
conference.setName('Brown Bag: Week 3');
```

## NotifyAction - addConference.setEndOnExit\(Boolean endOnExit\)

Defines whether the conference call should end when a specified caller exits the conference call.

<table id="table_j33_tmc_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

endOnExit

</td><td>

Boolean

</td><td>

Flag that indicates whether the conference call should end when the specified caller exits the current conference call.-   true: end the conference call when the specified caller exits the conference call
-   false: Default. End the conference call once all participants exit

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to add a conference call action and then set it so the conference call ends when the specified caller exits.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set the caller that starts the meeting
var conference = notifyAction.addConference();

// retrieve the participant for which the conference call should exit when they leave
var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
conference.setEndOnExit(true);
}
```

## NotifyAction - addConference.setHangupOnStar\(Boolean hangupOnStar\)

Defines whether the conference call should end when a participant presses the star \(\*\) key.

<table id="table_kjb_jkc_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hangupOnStar

</td><td>

Boolean

</td><td>

Flag that indicates whether the conference call should end when a participant presses the star \(\*\) key.Valid values:

 -   true: end the conference call
-   false: Default. Don't end the conference call

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to add a conference action and then record the conference call.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set the hang up action
var conference = notifyAction.addConference();
conference.setHangupOnStar(true);
```

## NotifyAction - addConference.setMuted\(Boolean muted\)

Defines whether the specified caller should be muted in the current conference call.

If you do not call this method, the caller is not muted by default.

<table id="table_zws_qgc_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

muted

</td><td>

Boolean

</td><td>

Flag that indicates whether the specified caller should be muted in the current conference call.-   true: caller should be muted
-   false: Default. Caller should not be muted

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to add a conference action and then mute a specified caller.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set it to mute the specified participant
var conference = notifyAction.addConference();

var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
conference.setMuted(true);
}
```

## NotifyAction - addConference.setName\(String name\)

Sets the name of the current conference call to the specified name.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name to associate with the current conference call.|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to add a conference action and set the name of the conference call.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set its name
var conference = notifyAction.addConference();

conference.setName('Brown Bag: Week 3');
```

## NotifyAction - addConference.setRecord\(Boolean record\)

Defines whether the associated conference call should be recorded.

If you do not call this method, the conference call is not recorded by default.

<table id="table_bz2_ffc_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record

</td><td>

Boolean

</td><td>

Flag that indicates whether the current conference call should be recorded.-   true: start recording the conference call
-   false: Default. Conference call is not recorded. Recording is stopped if it is currently being recorded.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to add a conference action and then record the conference call.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set it to be recorded
var conference = notifyAction.addConference();
conference.setRecord(true);
```

## NotifyAction - addConference.setStartOnEnter\(Boolean startOnEnter\)

Defines whether the conference call should start when the specified caller joins the conference call.

By default, whenever there are two or more callers, the conference call starts. To make it so the conference call only starts when a specific caller joins, you must call this method for each of the other callers and set the value to "false". By doing this, the conference call will not start until the desired person joins the conference call.

<table id="table_dps_43c_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

startOnEnter

</td><td>

Boolean

</td><td>

Flag that indicates whether the conference call should start when the selected caller joins the current conference call.-   true: Default. Start the conference call when the specified caller joins the conference call.
-   false: start the conference call once it is added

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to add a conference action and then set it so the conference call does not start until the specified caller joins.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a conference call action and set the caller that starts the meeting
var conference = notifyAction.addConference();

// retrieve the participant for which the conference call should start when they arrive
var notifyParticipantGr = new GlideRecord('notify_participant');
notifyParticipantGr.get('active participant sys id');
 
if (notifyParticipantGr.isValid) {
conference.setStartOnEnter(true);
}
```

## NotifyAction - addDial\(\)

Forwards a call to a specified phone number or Notify Client.

Once the addDial action is created, the associated phone number \(setPhoneNumber\(\)\) or Notify Client \(setClientRecord\(\)\) must also be set.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|DialAction|Action added to the NotifyAction object.|

This example shows how to make an outbound call and record the call.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party – this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');
 
// Invoke setRecord(Boolean record) to record the call to this new number +919765xxxxxxx
dialAction.setRecord(true);
```

## NotifyAction - addDial.setCallerID\(String callerID\)

Defines the caller ID for the outgoing call.

|Name|Type|Description|
|----|----|-----------|
|callerID|String|Caller identifier to set for the outgoing call.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to make an outbound call and set a call timeout.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party – this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');
 
// Set the caller ID
dialAction.setCallerID('Planning Conf Call');
```

## NotifyAction - addDial.setClientRecord\(String tableName, String sysID\)

Sets the current caller to a Notify caller by specifying the table in which to find the Notify caller record and the caller's unique identifier.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table that contains the desired caller's information.|
|sysID|String|Unique identifier \(sys\_id\) of the desired Notify caller.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to set the current caller to a Notify caller using setClientRecord\(\).

```
// set up a dial action to forward the
// call to the specified client
var action = new SNC.NotifyAction();
var dial = action.addDial();
dial.setClientRecord(notifyClientRecord.getTableName(), notifyClientRecord.getUniqueValue());
dial.setTimeout(activity.vars.timeout);
dial.setRecord(activity.vars.record);
```

## NotifyAction - addDial.setDTMF\(String value\)

Defines the DTMF tones to play when the call connects.

|Name|Type|Description|
|----|----|-----------|
|value|String|Valid DTMF digits to play when the call connects.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to make an outbound call and defines the DTMF tones to play when the call connects.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party - this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');
 
// DTMF tones to play when call connects
dialAction.setDTMF("1246AF");
```

## NotifyAction - addDial.setHangupOnStar\(Boolean hangupOnStar\)

Defines whether the call should end when the star \(\*\) key is pressed.

<table id="table_uns_2gd_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hangupOnStar

</td><td>

Boolean

</td><td>

Flag that indicates whether the call should end when the star \(\*\) key is pressed.-   true: end the call
-   false: don't end the call

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to make an outbound call and set the hang up key to star.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party – this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');
 
// End call by pressing star
dialAction.setHangupOnStar(true);
```

## NotifyAction - addDial.setPhoneNumber\(String phoneNumber\)

Defines the phone number to call.

|Name|Type|Description|
|----|----|-----------|
|phoneNumber|String|E.164-compliant phone number to call.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to make an outbound call and set a call timeout.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party – this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');

```

## NotifyAction - addDial.setRecord\(Boolean record\)

Defines whether the outgoing call should be recorded.

<table id="table_hbp_sdd_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record

</td><td>

 

</td><td>

Flag that indicates whether the outgoing call should be recorded.Valid values:

 -   true: record the outgoing call
-   false: do not record the outgoing call

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to make an outbound call and record the call.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party – this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');
 
// Record the call
dialAction.setRecord(true);
```

## NotifyAction - addDial.setTimeout\(Integer timeout\)

Sets the number of seconds after which the outgoing call times out.

|Name|Type|Description|
|----|----|-----------|
|timeout|Integer|Number of seconds after which the outgoing call times out. Default: 30|

|Type|Description|
|----|-----------|
|void| |

This example shows how to make an outbound call and set a call timeout.

```
// Initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addDial() to connect to another party – this returns an object of type DialAction
var dialAction = notifyAction.addDial();
 
// Call setPhoneNumber(String phoneNumber)in DialAction.java to specify the phone number to dial
dialAction.setPhoneNumber('+919765xxxxxxx');
 
// Set the number of seconds to wait before timing out
dialAction.setTimeout(45);
```

## NotifyAction - addGather\(\)

Presents a specified interactive phone menu to the caller.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GatherAction|Action added to the NotifyAction object. Use the GatherAction object to define the menu settings and options to present to the user.|

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// present the user with a menu
var gather = notifyAction.addGather();
gather.setNumberOfDigits(1);    // the user can type 1 digit
gather.setFinishKey('#');       // # or *, useful for > 1 digit
gather.setTimeout(10);          // time to enter answer, in seconds

// add first menu item
var usSay = gather.addSay();
usSay.setText('Press 1 for english');
usSay.setLanguage('en-US');

// add second menu item
var nlSay = gather.addSay();
nlSay.setText('Kies 2 voor Nederlands');
nlSay.setLanguage('nl-NL');

// add third menu item
var frSay = gather.addSay();
frSay.setText('Choisissez 3 pour le français.');
frSay.setLanguage('fr-FR');

// and finish off with an applause
var play = gather.addPlay();
play.setURL('http://www.wavsource.com/snds_2015-04-12_5971820382841326/sfx/applause_y.wav');
```

## NotifyAction - addGather.addPlay\(\)

Plays an audio file on the call.

Refer to the NotifyAction addPlay\(\) method for a description of the supported child methods.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|PlayAction|Action added to the NotifyAction object. Use the PlayAction object to define the audio file URL and the number of times to loop the audio.|

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// Create the gather action object
var gather = notifyAction.addGather();

// Play an audio file
var play = gather.addPlay();
play.setURL('http://www.wavsource.com/snds_2015-04-12_5971820382841326/sfx/applause_y.wav');
```

## NotifyAction - addGather.addSay\(\)

Defines the text-to-speech to read on the call.

Refer to the NotifyAction addSay\(\) method for a description of the supported child methods.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|SayAction|Action added to the NotifyAction object. Use the SayAction object to define the text and language to read.|

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// present the user with a menu
var gather = notifyAction.addGather();
gather.setNumberOfDigits(1);    // the user can type 1 digit
gather.setTimeout(20);          // time to enter answer, in seconds

// add first menu item
var gatherSay = gather.addSay();
gatherSay.setText('Press 1 for english');
gatherSay.setLanguage('en-US');

```

## NotifyAction - addGather.setFinishKey\(String finishKey\)

Defines the key that the caller inputs to denote the end of their input.

<table id="table_pk1_hmd_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

finishKey

</td><td>

String

</td><td>

Key that denotes the end of caller input.Valid values:

 -   0-9
-   \# \(default\)
-   \*

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to add a gather action and define the key that denotes the end of the caller input.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

var gather = notifyAction.addGather();
gather.setNumberOfDigits(4);    // the user can type four digit
gather.setFinishKey('#');       // # or *, useful for > 1 digit
```

## NotifyAction - addGather.setNumberOfDigits\(Integer numberOfDigits\)

Defines the number of digits to collect.

|Name|Type|Description|
|----|----|-----------|
|numberOfDigits|Integer|Number of digits to collect. Zero is an invalid value.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to add a gather action and define the number of key strokes to collect.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// present the user with a menu
var gather = notifyAction.addGather();
gather.setNumberOfDigits(4);    // the user can type four digit
gather.setFinishKey('#');       // # or *, useful for > 1 digits
gather.setTimeout(20);          // time to enter answer, in seconds

```

## NotifyAction - addGather.setTimeout\(Integer timeout\)

Defines the amount of time after which gathering of input will timeout.

|Name|Type|Description|
|----|----|-----------|
|timeout|Integer|Number of seconds to wait for caller input before timing out. Default: 10|

|Type|Description|
|----|-----------|
|void| |

This example shows how to add a gather action and define the input timeout value.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// present the user with a menu
var gather = notifyAction.addGather();
gather.setNumberOfDigits(4);    // the user can type 1 digit
gather.setFinishKey('#');       // # or *, useful for > 1 digits
gather.setTimeout(20);          // time to enter answer, in seconds

```

## NotifyAction - addHangUp\(\)

Ends an active phone call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|HangUpAction|Action added to the NotifyAction object.|

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// hang up
notifyAction.addHangUp();
```

## NotifyAction - addQueue\(\)

Queues the call, which puts the call on hold.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|QueueAction|Action added to the NotifyAction object. Use the QueueAction object to define the queue name, and queueing or dequeueing behavior.|

This example shows how to add the call to the specified queue.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// queue the call
var queue = notifyAction.addQueue();
queue.setName('my queue');
```

This example shows how to remove the call from the queue.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// dequeue the call
var queue = notifyAction.addQueue();
queue.setDequeue(true);
```

## NotifyAction - addQueue.setDequeue\(Boolean dequeue\)

Removes the call from the current call queue \(takes it off of "hold"\).

<table id="table_enw_wwd_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dequeue

</td><td>

Boolean

</td><td>

Flag that indicates whether to remove the current call from the queue.-   true: remove the call from the queue
-   false: call is put in the queue

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to remove the call from the queue.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// dequeue the call
var queue = notifyAction.addQueue();
queue.setDequeue(true);
```

## NotifyAction - addQueue.setName\(String name\)

Defines the name associated with a queue.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name to associate with the queue.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to define the name of a queue.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// queue the call
var queue = notifyAction.addQueue();
queue.setName('my queue');
```

## NotifyAction - addPlay\(\)

Plays an audio file on the call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|PlayAction|Action added to the NotifyAction object. Use the PlayAction object to define the audio file URL and number of times to loop the audio.|

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a play action
var play = notifyAction.addPlay();
play.setURL('http://www.moviesounds.com/2001/imsorry.wav');
play.setLoop(1);
```

## NotifyAction - addPlay.setLoop\(Integer loop\)

Defines the number of times to play \(loop through\) the audio file.

|Name|Type|Description|
|----|----|-----------|
|loop|Integer|Number of times to play the audio file.|

|Type|Description|
|----|-----------|
|void| |

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a play action
var play = notifyAction.addPlay();
play.setURL('http://www.moviesounds.com/2001/imsorry.wav');
play.setLoop(2);
```

## NotifyAction - addPlay.setURL\(String url\)

Defines the URL where to obtain the audio file to play.

|Name|Type|Description|
|----|----|-----------|
|url|String|URL of the audio file to play.|

|Type|Description|
|----|-----------|
|void| |

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a play action
var play = notifyAction.addPlay();
play.setURL('http://www.moviesounds.com/2001/imsorry.wav');
play.setLoop(1);
```

## NotifyAction - addRecord\(\)

Adds an action to record the call to the current NotifyAction object.

The recording automatically ends when the call is completed or when a specified terminate is pressed \(setFinishKey\(\)\). The recording is then placed in the notify\_record table for the associated call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to record a call.

```
// First we initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Call addRecord() of NotifyAction – This returns an object of type RecordAction
var recordAction = notifyAction.addRecord();
 
// Optional. Define the key that callers use to stop the recording
recordAction.setFinishKey('#'); // Stop the call recording when caller presses the '#' key.
```

## NotifyAction - addRecord.setFinishKey\(String finishKey\)

Defines the key that terminates the recording.

<table id="table_t1r_fhd_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

finishKey

</td><td>

String

</td><td>

Key that terminates the recording.Valid values:

 -   0-9
-   \# \(default\)
-   \*

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to record a call and set the call termination key.

```
// First we initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Then we call addRecord() of NotifyAction 
var recordAction = notifyAction.addRecord();
 
// Set the key that terminates the recording
recordAction.setFinishKey('#'); // This means that we stop the call recording when user presses the '#' key.
```

## NotifyAction - addRecord.setMaxDuration\(Integer seconds\)

Defines the maximum length of the recording.

|Name|Type|Description|
|----|----|-----------|
|seconds|Integer|Maximum length of the recording in seconds. Default: 3600|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to record a call and set the call termination key.

```
// First we initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Then we call addRecord() of NotifyAction 
var recordAction = notifyAction.addRecord();
 
// Set the maximum length of the recording
recordAction.setMaxDuration(4800); 
```

## NotifyAction - addRecord.setTimeout\(Integer timeout\)

Sets the number of seconds of silence, after which, the recording ends.

|Name|Type|Description|
|----|----|-----------|
|timeout|Integer|Number of seconds of silence on the call, after which the recording ends. Default: 10|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates how to record a call and set the recording timeout value.

```
// First we initialize NotifyAction
var notifyAction = new SNC.NotifyAction();
 
// Then we call addRecord() of NotifyAction 
var recordAction = notifyAction.addRecord();
 
// Set the recoding timeout value
recordAction.setTimeout(360); 
```

## NotifyAction - addReject\(\)

Rejects an incoming call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|RejectAction|Action added to the NotifyAction object. Use the RejectAction object to define the reason for rejecting the call.|

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// reject the call
var rejectAction = notifyAction.addReject();
rejectAction.setReason('busy'); // 'busy' or 'rejected'
```

## NotifyActon - addReject.setReason\(String reason\)

Defines the reason why the call was rejected.

<table id="table_fdf_bzd_cgb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

reason

</td><td>

String

</td><td>

Reason why the call was rejected.Valid values:

 -   busy
-   rejected

All other values are ignored.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// reject the call
var rejectAction = notifyAction.addReject();
rejectAction.setReason('busy'); // 'busy' or 'rejected'
```

## NotifyAction - addSay\(\)

Defines the text-to-speech to read on the call.

Multiple languages are supported with text-to-speech. Available languages depend on the telephony provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|SayAction|Action added to the NotifyAction object. Use the SayAction object to define the text and language to read.|

This example demonstrates reading text in several languages.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a say action to say something in US English
var usSay = notifyAction.addSay();
usSay.setText('Welcome. I can speak english');
usSay.setLanguage('en-US');

// add a say action to say something in Dutch
var nlSay = notifyAction.addSay();
nlSay.setText('Ik spreek ook vloeiend nederlands');
nlSay.setLanguage('nl-NL');

// and german
var deSay = notifyAction.addSay();
deSay.setText('Und ich kan auch deutsch sprechen');
deSay.setLanguage('de-DE');
```

## NotifyAction - addSay.setLanguage\(String language\)

Defines the language in which to speak the text.

Use this method in conjunction with the setText\(\) method to define the verbiage to speak.

|Name|Type|Description|
|----|----|-----------|
|language|String|ISO 3166 language code that defines the language in which to speak the associated text. For example, "en-US" or "nl-NL".|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates reading text in several languages.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a say action to say something in US English
var usSay = notifyAction.addSay();
usSay.setText('Welcome. I can speak english');
usSay.setLanguage('en-US');

// add a say action to say something in Dutch
var nlSay = notifyAction.addSay();
nlSay.setText('Ik spreek ook vloeiend nederlands');
nlSay.setLanguage('nl-NL');

// and german
var deSay = notifyAction.addSay();
deSay.setText('Und ich kan auch deutsch sprechen');
deSay.setLanguage('de-DE');
```

## NotifyAction - addSay.setText\(String text\)

Defines the text to be read within the current call.

Use this method in conjunction with the setLanguage\(\) method to define the language in which to speak the provided text.

|Name|Type|Description|
|----|----|-----------|
|text|String|Text to read aloud within the current call.|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates reading text in several languages.

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// add a say action to say something in US English
var usSay = notifyAction.addSay();
usSay.setText('Welcome. I can speak english');
usSay.setLanguage('en-US');

// add a say action to say something in Dutch
var nlSay = notifyAction.addSay();
nlSay.setText('Ik spreek ook vloeiend nederlands');
nlSay.setLanguage('nl-NL');

// and german
var deSay = notifyAction.addSay();
deSay.setText('Und ich kan auch deutsch sprechen');
deSay.setLanguage('de-DE');
```

## NotifyAction - addSMS\(\)

Sends an SMS message.

**Note:** When using this function with an active call, you do not need to call the setTo function on the returned SMSAction object. The SMS is automatically sent to the caller.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|SMSAction|Action added to the NotifyAction object. Use the SMSAction object to define the message text and the phone number to which to send the message.|

```
// Instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// Define where to send the SMS to
var number = new GlideElementPhoneNumber();
number.setPhoneNumber('+31612345678', true);

// Add an SMS action
var sms = notifyAction.addSMS();
sms.setMessage('Lorem ipsum dolor sit amet, consectetur adipiscing elit.');
sms.setTo(number);
```

## NotifyAction - addSMS.setMessage\(String message\)

Defines the text of the SMS message to send.

|Name|Type|Description|
|----|----|-----------|
|message|String|Text of the SMS message to send.|

|Type|Description|
|----|-----------|
|void| |

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// define where to send the sms to
var number = new GlideElementPhoneNumber();
number.setPhoneNumber('+31612345678', true);

// add a SMS action
var sms = notifyAction.addSMS();
sms.setMessage('Lorem ipsum dolor sit amet, consectetur adipiscing elit.');
sms.setTo(number);
```

## NotifyAction - addSMS.setTo\(String to\)

Sets the phone number to which to sent the SMS message.

|Name|Type|Description|
|----|----|-----------|
|to|String|E.164-compliant phone number to which to send the SMS message.|

|Type|Description|
|----|-----------|
|void| |

```
// instantiate NotifyAction
var notifyAction = new SNC.NotifyAction();

// define where to send the sms to
var number = new GlideElementPhoneNumber();
number.setPhoneNumber('+31612345678', true);

// add a SMS action
var sms = notifyAction.addSMS();
sms.setMessage('Lorem ipsum dolor sit amet, consectetur adipiscing elit.');
sms.setTo(number);
```

## NotifyAction - append\(NotifyAction action\)

Appends the specified NotifyAction object to the current client's NotifyAction object.

There are two types of NotifyActions: terminal and non-terminal. Once you append a terminal action to a client's NotifyAction object, you cannot append any additional actions. Non-terminal actions include:

-   PlayAction
-   RecordAction
-   SayAction
-   SMSAction

All others NotifyActions are terminal. If you try to add another NotifyAction after a terminal action, the call will fail.

|Name|Type|Description|
|----|----|-----------|
|action|NotifyAction|NotifyAction object to append to the NotifyAction object of the current caller.|

|Type|Description|
|----|-----------|
|void| |

## NotifyAction - fromJson\(String json\)

Deserialize a NotifyAction object from a JSON string.

|Name|Type|Description|
|----|----|-----------|
|json|String|A JSON string representation of a NotifyAction object.|

|Type|Description|
|----|-----------|
|void| |

This example demonstrates deserializing a NotifyAction object.

```
var json = ".... some json obtained from toJson ....";

// instantiate notify action
var notifyAction = new SNC.NotifyAction();

// deserialize and reconstruct the notify action instance
notifyAction.fromJson(json);
```

This example demonstrates both serializing and deserializing a NotifyAction object.

```
// instantiate notify action
var notifyAction = new SNC.NotifyAction();

// add a queue
var queue = notifyAction.addQueue();
queue.setName('myQueueName');
queue.setDequeue(false);

// serialize to json
var json = notifyAction.toJson();
gs.log('serialization result: ' + json);

// instantiate a new notify action
var newAction = new SNC.NotifyAction();

// deserialize the json generated above
newAction.fromJson(json);

// serialize the new object and log the result
newJson = newAction.toJson();
gs.log('new serialization result: ' + newJson);
gs.log('the same: ' + (json == newJson));
```

Output: \*\*\* Script: serialization result: \{"fClassName":"NotifyAction","fActions":\[\{"fClassName":"QueueAction","fDequeue":true,"fQueueName":"myQueueName"\}\]\} \*\*\* Script: new serialization result: \{"fClassName":"NotifyAction","fActions":\[\{"fClassName":"QueueAction","fDequeue":true,"fQueueName":"myQueueName"\}\]\} \*\*\* Script: the same: true

## NotifyAction - setCallRecord\(GlideRecord callRecord\)

Defines the Notify call record in which to add subsequent actions.

|Name|Type|Description|
|----|----|-----------|
|callRecord|GlideRecord|GlideRecord containing the record of the caller \(within the notify\_call table\) for which to add actions. This caller stays in affect until this method is called again with a different caller.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to set the caller to which you want to add actions.

```
public NotifyAction runIncomingCallWorkflow(NotifyPhoneNumber notifyPhoneNumber, GlideRecord callRecord) throws NoWorkflowConfiguredException, NoSuchNotifyGroupRecordException {
   NotifyAction notifyAction = runWorkflow(notifyPhoneNumber, COL_INCOMING_CALL_WF, callRecord);
   notifyAction.setCallRecord(callRecord);
   return notifyAction;
}
```

## NotifyAction - toJson\(\)

Serialize the NotifyAction object to a JSON string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|JSON representation of this NotifyAction object.|

This example demonstrates serializing a NotifyAction object.

```
// instantiate notify action
var notifyAction = new SNC.NotifyAction();

// add one or more notify actions
// ...

// and serialize to json
var json = notifyAction.toJson();
```

This example demonstrates both serializing and deserializing a NotifyAction object.

```
// instantiate notify action
var notifyAction = new SNC.NotifyAction();

// add a queue
var queue = notifyAction.addQueue();
queue.setName('myQueueName');
queue.setDequeue(false);

// serialize to json
var json = notifyAction.toJson();
gs.log('serialization result: ' + json);

// instantiate a new notify action
var newAction = new SNC.NotifyAction();

// deserialize the json generated above
newAction.fromJson(json);

// serialize the new object and log the result
newJson = newAction.toJson();
gs.log('new serialization result: ' + newJson);
gs.log('the same: ' + (json == newJson));
```

Output: \*\*\* Script: serialization result: \{"fClassName":"NotifyAction","fActions":\[\{"fClassName":"QueueAction","fDequeue":true,"fQueueName":"myQueueName"\}\]\} \*\*\* Script: new serialization result: \{"fClassName":"NotifyAction","fActions":\[\{"fClassName":"QueueAction","fDequeue":true,"fQueueName":"myQueueName"\}\]\} \*\*\* Script: the same: true

