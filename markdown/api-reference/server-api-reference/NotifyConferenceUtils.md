---
title: NotifyConferenceUtil - Scoped, Global
description: The NotifyConferenceUtil API provides methods to manage Notify conference calls and SMS messages for various telephony service providers, such as Zoom and Webex.Instantiates a NotifyConferenceUtils object \(constructor\).Adds a participant to a specified conference call using their phone number to identify the participant.Adds a participant to the conference call referenced by the passed in GlideRecord using their unique user identifier.Performs the specified conference call action, such as starting/ending a conference call or joining, removing, muting, or unmuting participants from a conference call.Returns a JSON data template to use with the doConferenceAction\(\) method. Using this template automatically structures the data object so that you don't have to manually create it.Returns the capabilities of all telephony service provider drivers in the instance.Determines whether a Notify conference action is supported by a telephony service provider.Removes the participant associated with the passed in GlideRecord from the current conference call.Mutes the participant associated with the passed in GlideRecord on the current conference call.Unmutes the participant associated with the passed in GlideRecord on the current conference call.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyConferenceUtil - Scoped, Global

The NotifyConferenceUtil API provides methods to manage Notify conference calls and SMS messages for various telephony service providers, such as Zoom and Webex.

Using the NotifyConferenceUtil API you can:

-   Create new conference calls
-   Add participants by phone number or user ID
-   Remove participants from a conference call
-   Mute participants in a conference call
-   Unmute participants in a conference call
-   Obtain the capabilities of a specified service provider
-   End a conference call

You can use this API in both scoped and global scripts. To use this API you must activate the Conference Notify plugin \(com.snc.notify\) which requires a separate subscription. For details on activating this plugin, see [Activate Notify](https://www.servicenow.com/docs/access?context=t_ActivateNotify&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyConferenceUtils - NotifyConferenceUtils\(\)

Instantiates a NotifyConferenceUtils object \(constructor\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
function () {
	var confGR = new GlideRecord('notify_conference_call');
	confGR.get('76d3364d0b5133008e64aabcb4673a6d');

	var confUtils = new NotifyConferenceUtils();
	var actionResult = confUtils.addToConferenceByPhoneNumber("+917799555331", confGR)
	if (actionResult.status)
		gs.info('Participant has been added to conference');
	else {
		gs.info('join operation failed');
		actionResult.warnMessages.forEach(function (msg) {
			gs.info(msg);
		});
		actionResult.errorMessages.forEach(function (msg) {
			gs.info(msg);
		})
	}
})();
```

## NotifyConferenceUtils - addToConferenceByPhoneNumber\(String toNumber, GlideRecord confGR\)

Adds a participant to a specified conference call using their phone number to identify the participant.

<table id="table_lt1_kth_nhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toNumber

</td><td>

String

</td><td>

Phone number of the participant to add to the conference call.

</td></tr><tr><td>

confGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the conference call to which to add the specified participant.Table: Notify Conference Call \[notify\_conference\_call\]

</td></tr></tbody>
</table><table id="table_mt1_kth_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

-   Data type: Boolean
-   Possible values:
    -   true: Conference action succeeded
    -   false: Conference action failed

`<action>.successMessages`: If *status* is true, success message\(s\), else empty.

-   Data type: Array of Strings

`<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

-   Data type: Array of Strings

`<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

-   Data type: Array of Strings

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
function () {
	var confGR = new GlideRecord('notify_conference_call');
	confGR.get('76d3364d0b5133008e64aabcb4673a6d');

	var confUtils = new NotifyConferenceUtils();
	var actionResult = confUtils.addToConferenceByPhoneNumber("+917799555331", confGR)
	if (actionResult.status)
		gs.info('Participant has been added to conference');
	else {
		gs.info('join operation failed');
		actionResult.warnMessages.forEach(function (msg) {
			gs.info(msg);
		});
		actionResult.errorMessages.forEach(function (msg) {
			gs.info(msg);
		})
	}
})();
```

## NotifyConferenceUtils - addToConferenceByUserId\(String userId, GlideRecord confGR\)

Adds a participant to the conference call referenced by the passed in GlideRecord using their unique user identifier.

<table id="table_xld_mwh_nhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userId

</td><td>

String

</td><td>

Sys ID of the participant to add to the specified conference call.Table: User \[sys\_user\]

</td></tr><tr><td>

confGR

</td><td>

GlideRecord

</td><td>

GlideRecord of the conference call to add the specified participant. Table: Notify Conference Call \[notify\_conference\_call\]

</td></tr></tbody>
</table><table id="table_yld_mwh_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

-   Data type: Boolean
-   Possible values:
    -   true: Conference action succeeded
    -   false: Conference action failed

`<action>.successMessages`: If *status* is true, success message\(s\), else empty.

-   Data type: Array of Strings

`<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

-   Data type: Array of Strings

`<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

-   Data type: Array of Strings

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
(function () {
	var confGR = new GlideRecord('notify_conference_call');
	confGR.get('76d3364d0b5133008e64aabcb4673a6d');

	var confUtils = new NotifyConferenceUtils();
	var actionResult = confUtils.addToConferenceByUserId(gs.getUserID(), confGR)
	if (actionResult.status)
		gs.info('Participant has been added to conference');
	else {
		gs.info('join operation failed');
		actionResult.warnMessages.forEach(function (msg) {
			gs.info(msg);
		});
		actionResult.errorMessages.forEach(function (msg) {
			gs.info(msg);
		})
	}
})();

```

## NotifyConferenceUtils - doConferenceAction\(String action, Object data\)

Performs the specified conference call action, such as starting/ending a conference call or joining, removing, muting, or unmuting participants from a conference call.

You can start a new conference call and add participants within a single call to this method or call the method multiple times to start the call and then manage participants separately. In addition, through the passed in data object, you can configure the method to:

-   Save pointers in the conference call record to the specific record \(source record\), such as an incident or problem, that is the topic of discussion for the conference call.
-   Allow/disallow multiple conference calls for a source record.
-   Automatically log the participants that were in the conference call in the "Work Notes" field of the source record.
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

-   end: Terminates the conference call identified in **data.confId**.
-   join: Adds the participant specified in the **data.items** array to the conference call identified in **data.confId**.
-   kick: Removes the participant specified in the **data.items** array from the conference call identified in **data.confId**.
-   multiJoin: Adds the participants specified in the **data.items** array to the conference call identified in **data.confId**
-   multiKick: Removes the participants specified in the **data.items** array from the conference call identified in **data.confId**.
-   multiMute: Mutes the participants specified in the **data.items** array on the conference call identified in **data.confId**.
-   multiUnmute: Unmutes the participants specified in the **data.items** array from the conference call identified in **data.confId**.
-   mute: Mutes the participant specified in the **data.items** array on the conference call identified in **data.confId**.
-   selfJoin: Adds the currently logged in user to the conference call \(no entry in **data.items** required.\)
-   start: Starts the conference call identified in **data.confId**.
-   unmute: Unmutes the participant specified in the **data.items** array from the conference call identified in **data.confId**.

</td></tr><tr id="data-row-NConf"><td>

data

</td><td>

Object

</td><td id="data-entry-NConf">

Object that describes the conference call.

</td></tr><tr><td>

data.addToWorkNotes

</td><td>

Boolean

</td><td id="data.addToWorkNotes-entry-NConf">

Flag that indicates whether to add information about the participants that were included in the conference call in the work notes field of the associated record. For this functionality to work, you must also specify values in the **data.table** and **data.sysId** parameters. These parameters identify the record in which to add the work notes.

Default: false

Actions for which this parameter is valid:

-   join
-   multiJoin
-   selfJoin
-   start

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

Sys\_id of the conference call. Table: Notify Conference Call \[notify\_conference\_call\]

Actions for which this parameter is required:

-   end
-   join
-   multiJoin
-   selfJoin

**Note:** Participant actions such as mute, unmute, and kick don't require this parameter to be set as the method obtains this information from the Notify Conference Call Participant \[notify\_participant\] table.

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

data.items

</td><td>

Array

</td><td id="data.items-entry-NConf">

Information for each participant to include in the conference call. Valid array values:

-   id: Sys\_id of user; located in the User \[sys\_User\] table.

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

String

</td><td id="data.message-entry-NConf">

Message that is read aloud when a user answers the call, such as, "P1 incident has been created please login to instance." Actions for which this parameter is valid:

-   join
-   multiJoin
-   start

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

Sys\_id of the source record to associate with the conference call. For example, if a conference call is held to discuss a specific incident or problem, put the sys\_id of the incident or problem record in this value. This sys\_id is stored in the Source column of the NotifyConference Call \[notify\_conference\_call\] table and can later be tracked.

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
-   Possible values:
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
(function (confId) {
	var confUtils = new NotifyConferenceUtils();
	var data = confUtils.getConferenceInputDataTemplate();
	data.table = 'incident';
	data.sysId = '1234';
	data.addToWorkNotes = false;
	data.confId = confId;
	data.message = 'p1 incident has been created';
	data.fromNumber = 'twilio/Telephony driver number';
	data.items.push({ id: 'user3SysId', phoneNumber: '+917799555332' });
	data.items.push({ id: 'user4SysId', email: 'yln99518@gmail.com' });

	var result = confUtils.doConferenceAction('start', data);
	if (result.status) {
		gs.info('Start conference action succeeded');
	} else
		gs.info('Start conference action failed');

	result.errorMessages.forEach(function (msg) {
		gs.info(msg);
	});
	result.warnMessages.forEach(function (msg) {
		gs.info(msg);
	});
	result.successMessages.forEach(function (msg) {
		gs.info(msg);
	});
})('activeConfSysId');

```

## NotifyConferenceUtils - getConferenceInputDataTemplate\(\)

Returns a JSON data template to use with the doConferenceAction\(\) method. Using this template automatically structures the data object so that you don't have to manually create it.

Call this method prior to calling the doConferenceAction\(\) method. For the desired conference call action, set the desired parameters within the template, and then pass the template in the doConferenceAction\(\) call. For additional information on the valid parameters for each action, see [doConferenceAction\(\)](NotifyConferenceUtils.md#).

**Note:** This is a helper method. You can also manually construct this object and pass that object into the doConferenceAction\(\) method and have the same outcome.

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

-   join
-   multiJoin
-   selfJoin
-   start

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

Sys\_id of the conference call. Table: Notify Conference Call \[notify\_conference\_call\]

Actions for which this parameter is required:

-   end
-   join
-   multiJoin
-   selfJoin

**Note:** Participant actions such as mute, unmute, and kick don't require this parameter to be set as the method obtains this information from the Notify Conference Call Participant \[notify\_participant\] table.

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

-   id: Sys\_id of user; located in the User \[sys\_User\] table.

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

-   join
-   multiJoin
-   start

</td></tr><tr><td>

data.serviceProvider

</td><td>

Required. Name of conference service provider, such as Zoom or Webex. Actions for which this parameter is required:

-   all

</td></tr><tr><td>

data.sysId

</td><td>

Sys\_id of the source record to associate with the conference call. For example, if a conference call is held to discuss a specific incident or problem, put the sys\_id of the incident or problem record in this value. This sys\_id is stored in the Source column of the NotifyConference Call \[notify\_conference\_call\] table and can later be tracked.

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
</table>```
(function (confId) {
	var confUtils = new NotifyConferenceUtils();
	var data = confUtils.getConferenceInputDataTemplate();
	data.confId = confId;
	var result = confUtils.doConferenceAction('end', data);
	if (result.status) {
		gs.info('Conference call has been ended');
	} else
		gs.info('End conference call action failed');

	result.errorMessages.forEach(function (msg) {
		gs.info(msg);
	});
	result.warnMessages.forEach(function (msg) {
		gs.info(msg);
	});
	result.successMessages.forEach(function (msg) {
		gs.info(msg);
	});
})('activeConfSysId');
```

## NotifyConferenceUtils - getServiceProvidersCapabilities\(\)

Returns the capabilities of all telephony service provider drivers in the instance.

Possible capabilities include:

-   archive: archives the conference after it ends
-   beepOnLeave: plays a "beep" tone when a participant leaves the conference call
-   beepOnJoin: plays a "beep" tone when a participant joins the conference call
-   end: ends the identified conference call
-   filesharing: allows file sharing between participants
-   join: adds a participant to a conference call
-   kick: removes a participant from a conference call
-   multiJoin: adds multiple participants to a conference call
-   multiKick: removes multiple participants from a conference call
-   muteOnJoin: mutes a participant when they initially join a conference call
-   multiUnmute: unmutes multiple participants for a conference call
-   record: records conference calls
-   recording: provides an on-screen indicator when the conference call is being recorded
-   screenSharing: allows participant screens to be shared with the group
-   selfJoin: adds the current logged in user to a conference call
-   speaking: provides an on-screen message as to who is currently speaking
-   start: starts the identified conference call
-   unmute: unmutes a participant in a conference call

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bzh_qyg_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Key-value pairs of the status of each driver capability.Valid values:

 -   isSupported = 0: capability is not supported
-   isSupported = 1: capability is supported

</td></tr></tbody>
</table>List driver capabilities for all telephony service provider drivers in the instance.

```
(function () {
	var confUtils = new NotifyConferenceUtils();
	var providerToCapability = confUtils.getServiceProvidersCapabilites();
	for (var provider in providerToCapability) {
		gs.info('{0} supported capabilities \n\n', provider);
		var capabilities = providerToCapability[provider]
		for (var cap in capabilities)
			if(confUtils.isActionSupported(capabilities[cap].isSupported))
				gs.info('"{0}" action supported', cap);
			else
				gs.info("'{0}' action is not supported by this conference driver", cap);
	}
})();

```

Output: The method returns a node similar to the following for each active telephony service provider within the instance.

```
{
    "Telephony": {
        "start": {
            "isSupported": 1,
            "meta": {}
        },
        "end": {
            "isSupported": 1,
            "meta": {}
        },
        "selfJoin": {
            "isSupported": 1,
            "meta": {}
        },
        "join": {
            "isSupported": 1,
            "meta": {}
        },
        "multiJoin": {
            "isSupported": 1,
            "meta": {}
        },
        "mute": {
            "isSupported": 1,
            "meta": {}
        },
        "multiMute": {
            "isSupported": 1,
            "meta": {}
        },
        "unmute": {
            "isSupported": 1,
            "meta": {}
        },
        "multiUnmute": {
            "isSupported": 1,
            "meta": {}
        },
        "kick": {
            "isSupported": 1,
            "meta": {}
        },
        "multiKick": {
            "isSupported": 1,
            "meta": {}
        },
        "record": {
            "isSupported": 0,
            "meta": {}
        },
        "speaking": {
            "isSupported": 0,
            "meta": {}
        },
        "recording": {
            "isSupported": 0,
            "meta": {}
        },
        "screenSharing": {
            "isSupported": 0,
            "meta": {}
        },
        "fileSharing": {
            "isSupported": 0,
            "meta": {}
        },
        "archive": {
            "isSupported": 0,
            "meta": {}
        },
        "muteOnJoin": {
            "isSupported": 0,
            "meta": {}
        },
        "beepOnJoin": {
            "isSupported": 0,
            "meta": {}
        },
        "beepOnLeave": {
            "isSupported": 0,
            "meta": {}
        }
    }
}

```

## NotifyConferenceUtils - isActionSupported\(Number action\)

Determines whether a Notify conference action is supported by a telephony service provider.

To use this method, you must first call the getServiceProviderCapabilities\(\) method. This method returns an object that contains information about the availability of each possible Notify conference action for each service provider configured in your instance.

For example:

```
{
    "Telephony": {
        "start": {
            "isSupported": 1,
            "meta": {}
        },
        "end": {
            "isSupported": 1,
            "meta": {}
        },
        "selfJoin": {
            "isSupported": 1,
            "meta": {}
        },
        "join": {
            "isSupported": 1,
            "meta": {}
        },
        "multiJoin": {
            "isSupported": 1,
            "meta": {}
        },
        "mute": {
            "isSupported": 1,
            "meta": {}
        },
        "multiMute": {
            "isSupported": 1,
            "meta": {}
        },
        "unmute": {
            "isSupported": 1,
            "meta": {}
        },
        "multiUnmute": {
            "isSupported": 1,
            "meta": {}
        },
        "kick": {
            "isSupported": 1,
            "meta": {}
        },
        "multiKick": {
            "isSupported": 1,
            "meta": {}
        },
        "record": {
            "isSupported": 0,
            "meta": {}
        },
        "speaking": {
            "isSupported": 0,
            "meta": {}
        },
        "recording": {
            "isSupported": 0,
            "meta": {}
        },
        "screenSharing": {
            "isSupported": 0,
            "meta": {}
        },
        "fileSharing": {
            "isSupported": 0,
            "meta": {}
        },
        "archive": {
            "isSupported": 0,
            "meta": {}
        },
        "muteOnJoin": {
            "isSupported": 0,
            "meta": {}
        },
        "beepOnJoin": {
            "isSupported": 0,
            "meta": {}
        },
        "beepOnLeave": {
            "isSupported": 0,
            "meta": {}
        }
    }
}
```

<table id="table_gsw_vd2_vhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

Number

</td><td>

Value of the **isSupported** parameter returned by the getServiceProvidersCapabilities\(\) method for a specific action and service provider.

 **Note:** Although the **isSupported** value may appear to be a Boolean, it is actually a Number. Do not try and evaluate the capabilities as Boolean values. Use this method as the associated values may be expanded in future versions.

</td></tr></tbody>
</table><table id="table_hsw_vd2_vhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the telephony service provider supports the specified action.Valid values:

 -   true: action is supported by the service provider
-   false: action is not supported by the service provider

</td></tr></tbody>
</table>```
(function () {
  var confUtils = new NotifyConferenceUtils();
  var providerToCapability = confUtils.getServiceProvidersCapabilites();
    for (var provider in providerToCapability) {
      gs.info('{0} supported capabilities \n\n', provider);
      var capabilities = providerToCapability[provider]
      for (var cap in capabilities)
        if (confUtils.isActionSupported(capabilities[cap].isSupported))
          gs.info('"{0}" action supported', cap);
        else
          gs.info("'{0}' action is not supported by this conference driver", cap);
    }
})();
```

## NotifyConferenceUtils - kickByParticipantGR\(GlideRecord notifyParticipantGR\)

Removes the participant associated with the passed in GlideRecord from the current conference call.

<table id="table_inj_thh_nhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyParticipantGR

</td><td>

GlideRecord

</td><td>

GlideRecord object of the participant to remove from the conference call.Table: Notify Participant \[notify\_participant\]

</td></tr></tbody>
</table><table id="table_jnj_thh_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

-   Data type: Boolean
-   Possible values:
    -   true: Conference action succeeded
    -   false: Conference action failed

`<action>.successMessages`: If *status* is true, success message\(s\), else empty.

-   Data type: Array of Strings

`<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

-   Data type: Array of Strings

`<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

-   Data type: Array of Strings

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
(function () {
    var confUtils = new NotifyConferenceUtils();
    var participantGR = new GlideRecord('notify_participant');  // Participant record contains conf call ID
    participantGR.get('validParticipantSysId');
    var actionResult = confUtils.kickByParticipantGR(participantGR);
    if (actionResult.status)
        gs.info('Participant has been kicked out of conference');
    else {
        gs.info('kick operation failed');
        actionResult.warnMessages.forEach(function (msg) {
            gs.info(msg);
        });
        actionResult.errorMessages.forEach(function (msg) {
            gs.info(msg);
        })
    }
})()

```

## NotifyConferenceUtils - muteByParticipantGR\(GlideRecord notifyParticipantGR\)

Mutes the participant associated with the passed in GlideRecord on the current conference call.

<table id="table_vpk_ckh_nhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

notifyParticipantGR

</td><td>

Object

</td><td>

GlideRecord object of the participant to mute.Table: Notify Participant \[notify\_participant\]

</td></tr></tbody>
</table><table id="table_wpk_ckh_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

-   Data type: Boolean
-   Possible values:
    -   true: Conference action succeeded
    -   false: Conference action failed

`<action>.successMessages`: If *status* is true, success message\(s\), else empty.

-   Data type: Array of Strings

`<action>.warnMessages`: If *status* is false, any warning messages thrown during processing.

-   Data type: Array of Strings

`<action>.errorMessages`: If *status* is false, any error messages thrown during processing.

-   Data type: Array of Strings

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
(function () {
    var confUtils = new NotifyConferenceUtils();
    var participantGR = new GlideRecord('notify_participant');
    participantGR.get('validSysId');
    var actionResult = confUtils.muteByParticipantGR(participantGR);
    if (actionResult.status)
        gs.info('Participant has been muted');
    else {
        gs.info('mute operation failed');
        actionResult.warnMessages.forEach(function (msg) {
            gs.info(msg);
        });
        actionResult.errorMessages.forEach(function (msg) {
            gs.info(msg);
        })
    }
})()
```

## NotifyConferenceUtils - unmuteByParticipantGR\(GlideRecord notifyParticipantGR\)

Unmutes the participant associated with the passed in GlideRecord on the current conference call.

|Name|Type|Description|
|----|----|-----------|
|notifyParticipantGR|GlideRecord|GlideRecord object of the participant to unmute. These records are located in the Notify Participant \[notify\_participant\] table.|

<table id="table_cyp_zqh_nhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Results of the conference action.`<action>.status`: Status of the conference action.

-   Data type: Boolean
-   Possible values:
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
(function () {
    var confUtils = new NotifyConferenceUtils();
    var participantGR = new GlideRecord('notify_participant');
    participantGR.get('validSysId');
    var actionResult = confUtils.unmuteByParticipantGR(participantGR);
    if (actionResult.status)
        gs.info('Participant has been Unmuted');
    else {
        gs.info('Unmute operation failed');
        actionResult.warnMessages.forEach(function (msg) {
            gs.info(msg);
        });
        actionResult.errorMessages.forEach(function (msg) {
            gs.info(msg);
        })
    }
})();

```

