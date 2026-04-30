---
title: NotifyOnTaskClient - Client
description: The NotifyOnTaskClient API provides methods for sending SMS messages or starting/managing a conference call for various telephony service providers, such as Zoom and Webex.Adds the specified participants to a specified conference call.Performs the specified conference call action, such as starting/ending a conference call or joining, removing, muting, or unmuting participants from a conference call.Terminates the specified conference call.Returns a JSON data template to use with the doConferenceAction\(\) method. Using this template automatically structures the data object so that you don't have to manually create it.Starts a new conference call.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 17
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# NotifyOnTaskClient- Client

The NotifyOnTaskClient API provides methods for sending SMS messages or starting/managing a conference call for various telephony service providers, such as Zoom and Webex.

Any UI can consume the NotifyOnTaskClient API by explicitly including the NotifyOnTaskClient UI script.

Using the NotifyOnTaskClient API you can:

-   Start a conference call
-   End a conference call
-   Add participants
-   Perform actions that are available through the telephony driver such as:
    -   mute/unmute participants
    -   remove participants from a conference call
    -   add participants to a conference call
    -   start a conference call
    -   end a conference call

The Notify \(com.snc.notify\) plugin requires a separate subscription. For additional information on activating the Notify plugin, see [Activate Notify](https://www.servicenow.com/docs/access?context=t_ActivateNotify&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## NotifyOnTaskClient - addParticipants\(Object data\)

Adds the specified participants to a specified conference call.

<table id="dataObject-table-NConf" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Object

</td><td>

Object that describes the conference call.

</td></tr><tr><td>

data.addToWorkNotes

</td><td>

Boolean

</td><td>

Flag that indicates whether to add information about the participants that were included in the conference call in the work notes field of the associated record. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record in which to add the work notes.

 Default: false

</td></tr><tr><td>

data.confId

</td><td>

String

</td><td>

Required. Sys ID of the conference call. The conference Sys ID is located in the Notify Conference Call \[notify\_conference\_call\] table.

</td></tr><tr><td>

data.items

</td><td>

Array

</td><td>

Required. Information for each participant to include in the conference call. Valid array values:

 -   **id**: User Sys ID; located in the User \[sys\_User\] table.
-   **notifyParticipantId**: Participant Sys ID; located in the Notify Participant \[notify\_participant\] table.
-   **phoneNumber**: Phone number of the participant. If this value is passed in conjunction with either the **id** or **notifyParticipantId**, this value supersedes the phone numbers in the user/participant record and is used to place the call.
-   **email**: email address of the participant.

</td></tr><tr><td>

data.message

</td><td>

String

</td><td>

Message that is read aloud when a user answers the call, such as, "P1 incident has been created please login to instance."

</td></tr><tr><td>

data.serviceProvider

</td><td>

String

</td><td>

Required. Name of conference service provider, such as Zoom or Webex.

</td></tr><tr><td>

data.sysId

</td><td>

String

</td><td>

Sys ID of the source record to associate with the conference call. For example, if a conference call is held to discuss a specific incident or problem, put the Sys ID of the incident or problem record in this value. This Sys ID is stored in the Source column of the NotifyConference Call \[notify\_conference\_call\] table and can later be tracked.

 This parameter is used in conjunction with the **data.Table**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

 You should configure this value when the conference call is initially created through a "start" action. If required, you can also set this value through this method.

</td></tr><tr><td>

data.table

</td><td>

String

</td><td>

Table that contains the source record to associate with the conference call. A source record can be any record, such as an "incident" or "problem", that is the topic of discussion in the conference call. This table name is stored in the Table column of the NotifyConference Call \[notify\_conference\_call\] table and can be tracked.

 This parameter is used in conjunction with the **data.sysId**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

 You should configure this value when the conference call is initially created through a "start" action. If required, you can also set this value through this method.

</td></tr></tbody>
</table><table id="table_rpj_1y5_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

 -   Data type: Boolean
-   Valid values:
    -   true: Conference action succeeded
    -   false: Conference action failed

 `<action>.successMessages`: If *status* is true, success message\(s\), else empty.

 -   Data type: Array of Strings

 `<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

 -   Data type: Array of Strings

 `<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

 -   Data type: Array of Strings

</td></tr></tbody>
</table>```
function addToConferenceCall() {
    var data = NotifyOnTaskClient.getNotifyActionTemplate();
    data.serviceProvider = 'Telephony'; // e.g 'Zoom', 'WebEx'
    data.confId = 'Active conference sysId';
    data.items.push({ id: 'userSysId' });
    data.items.push({ phoneNumber: '+917799555331' });
    data.items.push({ email: 'yln99518@gmail.com' });

    NotifyOnTaskClient.addParticipants(data).then(function (result) {
        var joinActionResult = result[0];
        if(joinActionResult.status) {
            joinActionResult.successMessages.forEach(function(msg) {
                console.log(msg);
            });
            return;
        }

        joinActionResult.warnMessages.forEach(function(msg) {
            console.warn(msg);
        });
        joinActionResult.errorMessages.forEach(function(msg) {
            console.error(msg);
        });
    }, function (errMsg) {
        console.log(errMsg);
    });
}
```

## NotifyOnTaskClient - doConferenceAction\(String action, Object data\)

Performs the specified conference call action, such as starting/ending a conference call or joining, removing, muting, or unmuting participants from a conference call.

You can start a new conference call and add participants within a single call to this method or call the method multiple times to start the call and then manage participants separately. In addition, through the passed in data object, you can configure the method to:

-   Save pointers in the conference call record to the specific record \(source record\), such as an incident or problem, that is the topic of discussion for the conference call.
-   Allow/disallow multiple conference calls for a source record.
-   Automatically log the participants that were in the conference call in the **Work notes** field of the source record.
-   Have a message read aloud when a participant answers an outgoing call from the conference.

<table id="table_qqs_vdv_nhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

String

</td><td>

Defines the conference call action to perform.The following are the available conference call actions:

-   start: Starts the conference call identified in **data.confId**
-   end: Terminates the conference call identified in **data.confId**
-   join: Adds the participant specified in the **data.items** array to the conference call identified in **data.confId**
-   multiJoin: Adds the participants specified in the **data.items** array to the conference call identified in **data.confId**
-   selfJoin: Adds the currently logged in user to the conference call \(no entry in **data.items** required.\)
-   kick: Removes the participant specified in the **data.items** array from the conference call identified in **data.confId**
-   multiKick: Removes the participants specified in the **data.items** array from the conference call identified in **data.confId**
-   mute: Mutes the participant specified in the **data.items** array on the conference call identified in **data.confId**
-   multiMute: Mutes the participants specified in the **data.items** array on the conference call identified in **data.confId**
-   unmute: Unmutes the participant specified in the **data.items** array from the conference call identified in **data.confId**
-   multiUnmute: Unmutes the participants specified in the **data.items** array from the conference call identified in **data.confId**

</td></tr><tr><td>

data

</td><td>

Object

</td><td>

Object that describes the conference call.

</td></tr><tr><td>

data.addToWorkNotes

</td><td>

Boolean

</td><td id="data.addToWorkNotes-entry-NConf">

Flag that indicates whether to add information about the participants that were included in the conference call in the work notes field of the associated record. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record in which to add the work notes.

 Default: false

 Actions for which this parameter is valid:

 -   start
-   join
-   multiJoin
-   selfJoin

</td></tr><tr><td>

data.allowMulticonference

</td><td>

Boolean

</td><td id="data.allowMulticonference-entry-NConf">

Flag that indicates whether to allow multiple conference calls for a specific record at one time. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record that is allowed to have multiple conference calls.

 Default: false

 Actions for which this parameter is valid:

 -   start

</td></tr><tr><td>

data.confId

</td><td>

String

</td><td id="data.confId-entry-NConf">

Sys ID of the conference call. The conference Sys ID is located in the Notify Conference Call \[notify\_conference\_call\] table.

 Actions for which this parameter is required:

 -   end
-   join
-   multiJoin
-   selfJoin

 **Note:** Participant actions such as mute, unmute, and kick do not require this parameter to be set as the method obtains this information from the Notify Conference Call Participant \[notify\_participant\] table.

</td></tr><tr><td>

data.fromNumber

</td><td>

String

</td><td id="data.fromNumber-entry-NConf">

Service provider number to call into for the conference call. Locate this value in the Number or Phone number column of the Notify Phone Number \[notify\_number\] table.

 Actions for which this parameter is required:

 -   start

</td></tr><tr><td>

data.isNewConference

</td><td>

Boolean

</td><td id="data.isNewConference-entry-NConf">

Flag that indicates whether this is a new or an existing conference call. Valid values:

 -   true: New conference call
-   false: Existing conference call

 Default: false

 Actions for which this parameter is valid:

 -   start

</td></tr><tr><td>

data.message

</td><td>

String

</td><td id="data.message-entry-NConf">

Message that is read aloud when a user answers the call, such as, "P1 incident has been created please login to instance." Actions for which this parameter is valid:

 -   start
-   join
-   multiJoin

</td></tr><tr><td>

data.items

</td><td>

Array

</td><td id="data.items-entry-NConf">

Information for each participant to include in the conference call. Valid array values:

 -   id: Sys ID of user; located in the User \[sys\_User\] table.

Valid actions: join, multiJoin, start

-   notifyParticipantId: Sys ID of the Notify participant; located in the Notify Participant \[notify\_participant\] table.

Valid actions: join, kick, multiJoin, mute, start, unmute

-   phoneNumber: Phone number of the participant. If this value is passed in conjunction with either the **id** or **notifyParticipantId**, this value supersedes the phone numbers in the user/participant record and is used to place the call.

Valid actions: join, multiJoin, start

-   email: Email address of the participant.

Valid actions: join, multiJoin, start


</td></tr><tr><td>

data.serviceProvider

</td><td>

String

</td><td id="data.serviceProvider-entry-NConf">

Required. Name of conference service provider, such as Zoom or Webex. Actions for which this parameter is required:

 -   all

</td></tr><tr><td>

data.sysId

</td><td>

String

</td><td id="data.sys_id-entry-NConf">

Sys ID of the source record to associate with the conference call. For example, if a conference call is held to discuss a specific incident or problem, put the Sys ID of the incident or problem record in this value. This Sys ID is stored in the Source column of the NotifyConference Call \[notify\_conference\_call\] table and can later be tracked.

 This parameter is used in conjunction with the **data.Table**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

 Actions for which this parameter is valid:

 -   start

</td></tr><tr><td>

data.table

</td><td>

String

</td><td id="data.table-entry-NConf">

Table that contains the source record to associate with the conference call. A source record can be any record, such as an "incident" or "problem", that is the topic of discussion in the conference call. This table name is stored in the Table column of the NotifyConference Call \[notify\_conference\_call\] table and can be tracked.

 This parameter is used in conjunction with the **data.sysId**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

 Actions for which this parameter is valid:

 -   start

</td></tr></tbody>
</table><table id="table_rqs_vdv_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

 -   Data type: Boolean
-   Valid values:
    -   true: Conference action succeeded
    -   false: Conference action failed

 `<action>.successMessages`: If *status* is true, success message\(s\), else empty.

 -   Data type: Array of Strings

 `<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

 -   Data type: Array of Strings

 `<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

 -   Data type: Array of Strings

</td></tr></tbody>
</table>The following example shows how to create a function to call doConferenceAction\(\) to manipulate the participants in a conference call by passing in the action and the participants.

```

/**
 * 
 * @param {string} action - action to perform on the conference object or participant object
 * @param {Array} participants;
 */
function doConferenceAction(action, participants) {
    var data = NotifyOnTaskClient.getNotifyActionTemplate();
    data.serviceProvider = 'Telephony'; // e.g 'Zoom', 'WebEx'
    data.confId = 'Active conference sysId';
    data.items = participants;

    NotifyOnTaskClient.doConferenceAction(action, data).then(function (result) {
        var kickActionResult = result[0];
        if (kickActionResult.status)
            console.log(action + ' succeeded');
        else {
            kickActionResult.warnMessages.forEach(function (msg) {
                console.warn(msg);
            });
            kickActionResult.errorMessages.forEach(function (msg) {
                console.error(msg);
            });
        }
    }, function (errMsg) {
            console.log(errMsg)
    });
}

// kick participants

doConferenceAction('kick', [{notifyParticipantId: 'notifyParticipantSysId'}]);

// kick multiple participants

doConferenceAction('multiKick',
    [{notifyParticipantId: 'notifyParticipantSysId'},
    {notifyParticipantId: 'notifyParticipantSysId'}]);

// Mute participants
doConferenceAction('mute', [{notifyParticipantId: 'notifyParticipantSysId'}]);
doConferenceAction('mute', [{notifyParticipantId: 'notifyParticipantSysId'}]);

doConferenceAction('multiMute',
    [{notifyParticipantId: 'notifyParticipantSysId'},
    {notifyParticipantId: 'notifyParticipantSysId'}]);

// self join to any confernece. 
doConferenceAction('selfJoin', [{id: 'logged in userId'}]);

```

## NotifyOnTaskClient - endConference\(Object data\)

Terminates the specified conference call.

|Name|Type|Description|
|----|----|-----------|
|data|Object|Object that describes the conference call.|
|data.confId|String|Sys ID of the conference call.|
|data.serviceProvider|String|Required. Name of conference service provider, such as Zoom or Webex.|

<table id="table_dqd_qcv_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

 -   Data type: Boolean
-   Valid values:
    -   true: Conference action succeeded
    -   false: Conference action failed

 `<action>.successMessages`: If *status* is true, success message\(s\), else empty.

 -   Data type: Array of Strings

 `<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

 -   Data type: Array of Strings

 `<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

 -   Data type: Array of Strings

</td></tr></tbody>
</table>```
function endConferenceCall() {
    var data = NotifyOnTaskClient.getNotifyActionTemplate();
    data.serviceProvider = 'Telephony'; // e.g 'Zoom', 'WebEx'
    data.confId = 'Active conference sysId';

    NotifyOnTaskClient.endConference(data).then(function (result) {
        var endActionResult = result[0];
        if (endActionResult.status)
            console.log('Conference has been ended');
        else {
            endActionResult.warnMessages.forEach(function (msg) {
                console.warn(msg);
            });
            endActionResult.errorMessages.forEach(function (msg) {
                console.error(msg);
            });
        }
    }, function (errMsg) {
        console.log(errMsg);
    });
}
```

## NotifyOnTaskClient - getNotifyActionTemplate\(\)

Returns a JSON data template to use with the doConferenceAction\(\) method. Using this template automatically structures the data object so that you don't have to manually create it.

Call this method prior to calling the doConferenceAction\(\) method. For the desired conference call action, set the desired parameters within the template, and then pass the template in the doConferenceAction\(\) call. For additional information on the valid parameters for each action, see [doConferenceAction\(\)](NotifyOnTaskClient.md#).

**Note:** This is a helper method. You can also manually construct this object and pass it into the doConferenceAction\(\) method and have the same outcome.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_c2h_cwd_vhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Object that describes the conference call.

</td></tr><tr><td>

data.addToWorkNotes

</td><td>

Flag that indicates whether to add information about the participants that were included in the conference call in the work notes field of the associated record. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record in which to add the work notes.

 Default: false

 Actions for which this parameter is valid:

 -   start
-   join
-   multiJoin
-   selfJoin

</td></tr><tr><td>

data.allowMultconference

</td><td>

Flag that indicates whether to allow multiple conference calls for a specific record at one time. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record that is allowed to have multiple conference calls.

 Default: false

 Actions for which this parameter is valid:

 -   start

</td></tr><tr><td>

data.confId

</td><td>

Sys ID of the conference call. The conference Sys ID is located in the Notify Conference Call \[notify\_conference\_call\] table.

 Actions for which this parameter is required:

 -   end
-   join
-   multiJoin
-   selfJoin

 **Note:** Participant actions such as mute, unmute, and kick do not require this parameter to be set as the method obtains this information from the Notify Conference Call Participant \[notify\_participant\] table.

</td></tr><tr><td>

data.fromNumber

</td><td>

Service provider number to call into for the conference call. Locate this value in the Number or Phone number column of the Notify Phone Number \[notify\_number\] table.

 Actions for which this parameter is required:

 -   start

</td></tr><tr><td>

data.isNewConference

</td><td>

Flag that indicates whether this is a new or an existing conference call. Valid values:

 -   true: New conference call
-   false: Existing conference call

 Default: false

 Actions for which this parameter is valid:

 -   start

</td></tr><tr><td>

data.items

</td><td>

Information for each participant to include in the conference call. Valid array values:

 -   id: Sys ID of user; located in the User \[sys\_User\] table.

Valid actions: join, multiJoin, start

-   notifyParticipantId: Sys ID of the Notify participant; located in the Notify Participant \[notify\_participant\] table.

Valid actions: join, kick, multiJoin, mute, start, unmute

-   phoneNumber: Phone number of the participant. If this value is passed in conjunction with either the **id** or **notifyParticipantId**, this value supersedes the phone numbers in the user/participant record and is used to place the call.

Valid actions: join, multiJoin, start

-   email: Email address of the participant.

Valid actions: join, multiJoin, start


</td></tr><tr><td>

data.message

</td><td>

Message that is read aloud when a user answers the call, such as, "P1 incident has been created please login to instance." Actions for which this parameter is valid:

 -   start
-   join
-   multiJoin

</td></tr><tr><td>

data.serviceProvider

</td><td>

Required. Name of conference service provider, such as Zoom or Webex. Actions for which this parameter is required:

 -   all

</td></tr><tr><td>

data.sysId

</td><td>

Sys ID of the source record to associate with the conference call. For example, if a conference call is held to discuss a specific incident or problem, put the Sys ID of the incident or problem record in this value. This Sys ID is stored in the Source column of the NotifyConference Call \[notify\_conference\_call\] table and can later be tracked.

 This parameter is used in conjunction with the **data.Table**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

 Actions for which this parameter is valid:

 -   start

</td></tr><tr><td>

data.table

</td><td>

Table that contains the source record to associate with the conference call. A source record can be any record, such as an "incident" or "problem", that is the topic of discussion in the conference call. This table name is stored in the Table column of the NotifyConference Call \[notify\_conference\_call\] table and can be tracked.

 This parameter is used in conjunction with the **data.sysId**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

 Actions for which this parameter is valid:

 -   start

</td></tr></tbody>
</table>The following example shows how to call getNotifyActionTemplate\(\) to obtain the data template necessary to define the actions for doConferenceAction\(\).

```

/**
 * 
 * @param {string} action - action to perform on the conference object or participant object
 * @param {Array} participants;
 */
function doConferenceAction(action, participants) {
    var data = NotifyOnTaskClient.getNotifyActionTemplate();
    data.serviceProvider = 'Telephony'; // e.g 'Zoom', 'WebEx'
    data.confId = 'Active conference sysId';
    data.items = participants;

    NotifyOnTaskClient.doConferenceAction(action, data).then(function (result) {
        var kickActionResult = result[0];
        if (kickActionResult.status)
            console.log(action + ' succeeded');
        else {
            kickActionResult.warnMessages.forEach(function (msg) {
                console.warn(msg);
            });
            kickActionResult.errorMessages.forEach(function (msg) {
                console.error(msg);
            });
        }
    }, function (errMsg) {
            console.log(errMsg)
    });
}

// kick participants

doConferenceAction('kick', [{notifyParticipantId: 'notifyParticipantSysId'}]);

// kick multiple participants

doConferenceAction('multiKick',
    [{notifyParticipantId: 'notifyParticipantSysId'},
    {notifyParticipantId: 'notifyParticipantSysId'}]);

// Mute participants
doConferenceAction('mute', [{notifyParticipantId: 'notifyParticipantSysId'}]);
doConferenceAction('mute', [{notifyParticipantId: 'notifyParticipantSysId'}]);

doConferenceAction('multiMute',
    [{notifyParticipantId: 'notifyParticipantSysId'},
    {notifyParticipantId: 'notifyParticipantSysId'}]);

// self join to any confernece. 
doConferenceAction('selfJoin', [{id: 'logged in userId'}]);

```

## NotifyOnTaskClient - start\(Object data\)

Starts a new conference call.

<table class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Object

</td><td>

Object that describes the conference call.

</td></tr><tr><td>

data.addToWorkNotes

</td><td>

Boolean

</td><td>

Optional.Flag that indicates whether to add information about the participants that were included in the conference call in the work notes field of the associated record. For this functionality to work, you must also specify values for the **data.table** and **data.sysId** parameters to identify the record in which to add the work notes.

 Default: false

</td></tr><tr><td>

data.allowMulticonference

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to allow multiple conference calls for a specific record at one time. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record that is allowed to have multiple conference calls.

 Default: false

</td></tr><tr><td>

data.fromNumber

</td><td>

String

</td><td>

Required. Service provider number to call into for the conference call. Locate this value in the Number or Phone number column of the Notify Phone Number \[notify\_number\] table.

</td></tr><tr><td>

data.items

</td><td>

Array

</td><td>

Optional. Information for each participant to include in the conference call. Valid array values:

 -   **id**: User Sys ID; located in the User \[sys\_User\] table.
-   **notifyParticipantId**: Participant Sys ID; located in the Notify Participant \[notify\_participant\] table.
-   **phoneNumber**: Phone number of the participant. If this value is passed in conjunction with either the **id** or**notifyParticipantId**, this value supersedes the phone numbers in the user/participant record and is used to place the call.
-   **email**: Email address of the participant.

</td></tr><tr><td>

data.message

</td><td>

String

</td><td>

Optional. Message that is read aloud when a user answers the call, such as, "P1 incident has been created please login to instance."

</td></tr><tr><td>

data.serviceProvider

</td><td>

String

</td><td>

Required. Name of conference service provider, such as Zoom or Webex.

</td></tr><tr><td>

data.sysId

</td><td>

String

</td><td>

Optional. Sys ID of the source record to associate with the conference call. For example, if a conference call is held to discuss a specific incident or problem, put the Sys ID of the incident or problem record in this value. This Sys ID is stored in the Source column of the NotifyConference Call \[notify\_conference\_call\] table and can later be tracked.

 This parameter is used in conjunction with the **data.Table**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

</td></tr><tr><td>

data.table

</td><td>

String

</td><td>

Optional. Table that contains the source record to associate with the conference call. A source record can be any record, such as an "incident" or "problem", that is the topic of discussion in the conference call. This table name is stored in the Table column of the NotifyConference Call \[notify\_conference\_call\] table and can be tracked.

 This parameter is used in conjunction with the **data.sysId**, **data.addToWorkNotes**, and **allowMulticonference** parameters.

</td></tr></tbody>
</table><table id="table_jrr_133_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

 -   Data type: Boolean
-   Valid values:
    -   true: Conference action succeeded
    -   false: Conference action failed

 `<action>.successMessages`: If *status* is true, success message\(s\), else empty.

 -   Data type: Array of Strings

 `<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

 -   Data type: Array of Strings

 `<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

 -   Data type: Array of Strings

</td></tr></tbody>
</table>```
function startConferenceCall() {
    var data = NotifyOnTaskClient.getNotifyActionTemplate();
    data.table = 'incident';
    data.sysId = '1234';
    data.serviceProvider = serviceProvider;
    data.addToWorkNotes = true;
    data.fromNumber = 'Telephony Number';
    data.items.push({ id: 'userSysId' });
    data.items.push({ phoneNumber: '+917799555332' });
    data.items.push({ email: 'yln99517@gmail.com' });

    NotifyOnTaskClient.start(data).then(function (result) {
        var startActionResult = result[0];
        if(startActionResult.status) {
            startActionResult.successMessages.forEach(function(msg) {
                console.log(msg);
            });
            return;
        }

        startActionResult.warnMessages.forEach(function(msg) {
            console.warn(msg);
        });
        startActionResult.errorMessages.forEach(function(msg) {
            console.error(msg);
        });
    }, function (errMsg) {
        console.log(errMsg);
    });
}
```

