---
title: NotifyUtil - Global
description: The NotifyUtil script include provides utility methods to use when interacting with Notify calls and SMS messages using server-side scripts.Instantiates a NotifyUtil class object.Returns all of the Notify telephone numbers and related Notify information from a specified source record, such as an incident.Returns the SMS-capable number associated with the specified Notify user.Returns a list of unique Notify telephone numbers.Determines whether there are any active conference calls for the specified source record.Validates a specified Notify telephone number.Verifies that the specified number is a valid E.164 telephone number.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifyUtil- Global

The NotifyUtil script include provides utility methods to use when interacting with Notify calls and SMS messages using server-side scripts.

To use this script include you must activate the Notify \(com.snc.notify\) plugin.

Using the NotifyUtil script include you can:

-   Obtain all of the Notify telephone numbers and related Notify information from a specified source record.
-   Obtain a list of unique Notify telephone numbers.
-   Determine whether there are any active conference calls for the specified source record.
-   Obtain the SMS-capable number associated with the specified Notify user.
-   Validate a specified Notify telephone number.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifyUtil - NotifyUtil\(\)

Instantiates a NotifyUtil class object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example instantiates a NotifyUtil object.

```
var notifyUtil = new NotifyUtil(); 
notifyUtil.getTelephonyProviers();
```

## NotifyUtil - getListOfNotifyNumbersAndProviders\(String sourceTable, String sourceSysId, String notifyGroupSelectorSysId, Boolean filterSMSCapableNums\)

Returns all of the Notify telephone numbers and related Notify information from a specified source record, such as an incident.

You can use this information to initiate a call or send an SMS message on a particular source record. The information that is returned is based on the configuration of the Notify Provider Selector framework. For additional information, see [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

<table id="table_pmg_pyt_kmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filterSMSCapableNums

</td><td>

Boolean

</td><td>

Optional. Flag that indicates if only numbers that are SMS-capable should be returned.Valid values:

-   true: Only return SMS-capable telephone numbers and information.
-   false: Return all notify telephone numbers and information.

 Default: false

</td></tr><tr><td>

notifyGroupSelectorSysId

</td><td>

String

</td><td>

Optional. Sys\_id of a Notify group for which to return the notify numbers and information. Default: All groups

</td></tr><tr><td>

sourceSysId

</td><td>

String

</td><td>

Sys\_id of the source record for which to return the Notify numbers and information. For example, this could be the sys\_id of a record in the Incident \[incident\] table.

</td></tr><tr><td>

sourceTable

</td><td>

String

</td><td>

Name of the table that contains the source record that contains the desired Notify numbers and information.

</td></tr></tbody>
</table><table id="table_qmg_pyt_kmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

confProviders

</td><td>

List of available conference providers.Data type: Array

</td></tr><tr><td>

numbers

</td><td>

List of objects, each describing a single Notify number.Data type: Array

 ```
"numbers": [{
  "defaultFlag": Boolean,
  "name": "String",
  "number": "String",
  "shortCode": Boolean,
  "sysId": "String
}]
```

</td></tr><tr><td>

numbers.defaultFlag

</td><td>

Flag that indicates whether the associated Notify number is the default number.Possible values:

-   true: Default number
-   false: Not the default number

 Data type: Boolean

</td></tr><tr><td>

numbers.name

</td><td>

Name or label of the number.Data type: String

</td></tr><tr><td>

numbers.number

</td><td>

Notify number.Data type: String

</td></tr><tr><td>

numbers.shortCode

</td><td>

Flag that indicates whether the associated Notify number is a short code.Possible values:

-   true: Short code
-   false: Not a short code

 Data type: Boolean

</td></tr><tr><td>

numbers.sysId

</td><td>

Sys\_id of the Notify number.Data type: String

</td></tr></tbody>
</table>This example shows how to obtain the Notify telephone numbers and related Notify information from a specified source record.

```
function updateConferenceBridges(sourceTable, sourceId) {

  var notifyUtil = new global.NotifyUtil();
  var numbersAndProviders = notifyUtil.getListOfNotifyNumbersAndProviders(sourceTable, sourceId);
  var confBridges = [];
  if (numbersAndProviders.confProviders) {
    numbersAndProviders.confProviders.forEach(function(provider){
    confBridges.push(provider);
    });
  }
  if (numbersAndProviders.numbers) {
    numbersAndProviders.numbers.forEach(function(number){
      confBridges.push(number.name);
    });
  }
} 
```

## NotifyUtil - getSMSNumberForUser\(String userGrOrId\)

Returns the SMS-capable number associated with the specified Notify user.

|Name|Type|Description|
|----|----|-----------|
|userGROrId|String or [GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)|Sys\_id of the user record, located in the User \[sys\_user\] table, or the sys\_user GlideRecord of the user for whom to return the SMS-capable telephone number.|

|Type|Description|
|----|-----------|
|String|User SMS-capable telephone number. Returns null if the specified user is not found.|

This example shows how to obtain an SMS-capable telephone number using the associated GlideRecord.

```
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var fromNumber = getFromNumber();
  var nUtil = new NotifyUtil();
  var toNumber = nUtil.getSMSNumberForUser(sourceRecord.assigned_to.getRefRecord());
  var message = 'Incident ' + sourceRecord.getDisplayValue() + ' has been assigned to you.';
  if (fromNumber && nUtil.validateOutboundNotifyPhoneNumber(fromNumber) && toNumber && nUtil.validatePhoneNumber(toNumber)) {
    var notifySMS = new NotifySMS();
    notifySMS.sendToNumber(fromNumber, toNumber, message, sourceRecord);
  }
}

function getFromNumber() {
  var prop = gs.getProperty('custom_property_name', '');
  if (!prop){
    return getFallbackFromNumber();
  }
  return prop;
} 

function getFallbackFromNumber() {
  var notifyNumGr = new GlideRecord("notify_number");
  notifyNumGr.addActiveQuery();
  notifyNumGr.addQuery('has_sms_out', 'yes');
  notifyNumGr.query();
  if (notifyNumGr.next()) {
    return notifyNumGr.number + '';
  }
  return '';
} 
```

## NotifyUtil - getUniquePhoneNumbersForUsersAndGroups\(Array numbers, Array users, Array groups, String type, Boolean getData\)

Returns a list of unique Notify telephone numbers.

If you don't pass any parameters in the call, all Notify numbers within the Notify Phone Number \[notify\_number\] table are checked for duplicates, with each available phone number only appearing once in the returned list. You can refine the return results by specifying a list of users or groups to check, or by specifying a set of numbers or number types \(SMS or voice.\) You can also request that the metadata associated with each number be returned along with the unique numbers. If you do not want to use a parameter, simply pass `null` as a placeholder. For example: `return nUtil.getUniquePhoneNumbersForUsersAndGroups(null, userIds, null, 'sms', false);`.

<table id="table_kxw_hs5_kmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

getData

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to return metadata along with the list of unique phone numbers.Valid values:

-   true: Return metadata.
-   false: Do not return metadata.

 Default: false

</td></tr><tr><td>

groups

</td><td>

Array

</td><td>

Optional. List of sys\_id groups to check. Located in the Group \[sys\_user\_group\] table.Default: Check all groups.

</td></tr><tr><td>

numbers

</td><td>

Array

</td><td>

Optional. List of specific Notify telephone numbers to check.Default: Check all phone numbers.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Optional. Type of telephone numbers to check.Valid values \(case-sensitive\):

-   voice
-   sms

 Default: Check all phone number types

</td></tr><tr><td>

users

</td><td>

Array

</td><td>

Optional. List of sys\_ids of specific users to check. Located in the User \[sys\_user\] table. Default: Check all users

</td></tr></tbody>
</table><table id="table_lxw_hs5_kmb" class="returns"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

numbers

</td><td>

Unique Notify telephone numbers.Data type: Array

</td></tr><tr><td>

result

</td><td>

Only returned if **getData** is set to true. Metadata associated with each unique number.Data type: Object

```
"result": {
  "number": "String",
  "sysId": "String",
  "type": "String",
  "valid": Boolean
}
```

</td></tr><tr><td>

result.number

</td><td>

Unique Notify telephone number.Data type: String

</td></tr><tr><td>

result.sysId

</td><td>

Sys\_id of the record that contains the Notify telephone number. Located in the Notify Phone Number \[notify\_number\] table.Data type: String

</td></tr><tr><td>

result.type

</td><td>

Always contains "u" for user.Data type: String

</td></tr><tr><td>

result.valid

</td><td>

Flag that indicates whether the Notify telephone number is in valid E.164 format.Possible values:

-   true: Valid E.164 format.
-   false: Not in E.164 format.

 Data type: Boolean

</td></tr></tbody>
</table>This example shows how to request a specific set of unique Notify telephone numbers that have SMS capabilities.

```
var fromNumber = getFromNumber();
var toNumbers = getRecipientNumbers();
var message = 'This is an example SMS';
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var notifySMS = new NotifySMS();
  notifySMS.sendToNumber(fromNumber, toNumbers, message, sourceRecord);
}

function getRecipientNumbers() {
  var userGr = new GlideRecord('sys_user');
  userGr.addActiveQuery();
  userGr.addQuery('first_name', 'STARTSWITH', 'A');
  userGr.setLimit(5);
  userGr.query(); 
  var userIds = [];
  while (userGr.next()) {
    userIds.push(userGr.getUniqueValue());
  }
  if (userIds.length > 0) {
    var nUtil = new NotifyUtil();
    return nUtil.getUniquePhoneNumbersForUsersAndGroups(null, userIds, null, 'sms', false);
  } 
}

function getFromNumber() {
  var prop = gs.getProperty('custom_property_name', '');
  if (!prop){
    return getFallbackFromNumber();
  } 
  return prop; 
}

function getFallbackFromNumber() {
  var notifyNumGr = new GlideRecord("notify_number");
  notifyNumGr.addActiveQuery();
  notifyNumGr.addQuery('has_sms_out', 'yes');
  notifyNumGr.query();
  if (notifyNumGr.next()) {
    return notifyNumGr.number + '';
  }
  return '';
}
```

## NotifyUtil - hasActiveConferenceCalls\(String sourceRecSysId\)

Determines whether there are any active conference calls for the specified source record.

|Name|Type|Description|
|----|----|-----------|
|sourceRecSysId|String|Sys\_id of the record to check for active conference calls. For example the sys\_id of a record in the Incident table.|

<table id="table_xwv_ktm_kmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified record has associated active conference calls.Possible values:

-   true: Active conference calls are available for the specified record.
-   false: No active conference calls.

</td></tr></tbody>
</table>This example displays an information message if there are any active conference calls associated with an incident record.

```
(function executeRule(current, previous /*null when async*/) {
  var nUtil = new NotifyUtil();
  if (nUtil.hasActiveConferenceCalls(current.getUniqueValue())) {
    gs.addInfoMessage("There are active conference calls related to this Incident.");
  } 
})(current, previous);
```

## NotifyUtil - validateOutboundNotifyPhoneNumber\(String number\)

Validates a specified Notify telephone number.

The method performs three types of validation:

1.  Whether the Notify number exists in the Notify Phone Number \[notify\_number\] table.
2.  Whether the Notify number has a Notify group associated with it.
3.  Whether the Notify number is active.

If any one of these validations fail, the method throws an exception.

|Name|Type|Description|
|----|----|-----------|
|number|String|Notify number to validate.|

|Type|Description|
|----|-----------|
|None| |

This example illustrates how to validate a notify number.

```
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var fromNumber = getFromNumber();
  var nUtil = new NotifyUtil();
  var toNumber = nUtil.getSMSNumberForUser(sourceRecord.assigned_to.getRefRecord());
  var message = 'Incident ' + sourceRecord.getDisplayValue() + ' has been assigned to you.';
  if (fromNumber && nUtil.validateOutboundNotifyPhoneNumber(fromNumber) && toNumber && nUtil.validatePhoneNumber(toNumber)) {
    var notifySMS = new NotifySMS();
    notifySMS.sendToNumber(fromNumber, toNumber, message, sourceRecord);
  }
}

function getFromNumber() {
  var prop = gs.getProperty('custom_property_name', '');
  if (!prop){
    return getFallbackFromNumber();
  }
  return prop;
} 

function getFallbackFromNumber() {
  var notifyNumGr = new GlideRecord("notify_number");
  notifyNumGr.addActiveQuery();
  notifyNumGr.addQuery('has_sms_out', 'yes');
  notifyNumGr.query();
  if (notifyNumGr.next()) {
    return notifyNumGr.number + '';
  }
  return '';
} 
```

## NotifyUtil - validatePhoneNumber\(String number\)

Verifies that the specified number is a valid E.164 telephone number.

|Name|Type|Description|
|----|----|-----------|
|number|String|Telephone number to validate.|

<table id="table_oyd_b5t_kmb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified number is a valid telephone number.Possible values:

-   true: Valid E.164 telephone number.
-   false: Invalid telephone number.

</td></tr></tbody>
</table>This example illustrates how to validate a telephone number.

```
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var fromNumber = getFromNumber();
  var nUtil = new NotifyUtil();
  var toNumber = nUtil.getSMSNumberForUser(sourceRecord.assigned_to.getRefRecord());
  var message = 'Incident ' + sourceRecord.getDisplayValue() + ' has been assigned to you.';
  if (fromNumber && nUtil.validateOutboundNotifyPhoneNumber(fromNumber) && toNumber && nUtil.validatePhoneNumber(toNumber)) {
    var notifySMS = new NotifySMS();
    notifySMS.sendToNumber(fromNumber, toNumber, message, sourceRecord);
  }
}

function getFromNumber() {
  var prop = gs.getProperty('custom_property_name', '');
  if (!prop){
    return getFallbackFromNumber();
  }
  return prop;
} 

function getFallbackFromNumber() {
  var notifyNumGr = new GlideRecord("notify_number");
  notifyNumGr.addActiveQuery();
  notifyNumGr.addQuery('has_sms_out', 'yes');
  notifyNumGr.query();
  if (notifyNumGr.next()) {
    return notifyNumGr.number + '';
  }
  return '';
} 
```

