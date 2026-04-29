---
title: NotifySMS - Global
description: The NotifySMS script include provides methods that enable you to send Short Message Service \(SMS\) messages from Notify telephone numbers to devices using either their telephone numbers or a GlideRecord that has a field that contains telephone number information.Creates an instance of a NotifySMS object.Triggers an asynchronous flow action that sends a Short Message Service \(SMS\) message from a specified Notify phone number to a list of phone numbers.Sends a Short Message Service \(SMS\) message from a specified Notify telephone number to a specified telephone number.Sends a Short Message Service \(SMS\) message from a specified Notify phone number to a list of phone numbers.Sends a Short Message Service \(SMS\) message from a specified phone number to the user identified in a specified GlideRecord.Sends a Short Message Service \(SMS\) message from a specified Notify phone number to users found in a specified GlideRecord.Sets the method within a script include to use to obtain the target telephone number in the GlideRecord that is passed in the NotifySMS.sendToUser\(\) and NotifySMS.sendToUsers\(\) methods.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NotifySMS- Global

The NotifySMS script include provides methods that enable you to send Short Message Service \(SMS\) messages from Notify telephone numbers to devices using either their telephone numbers or a GlideRecord that has a field that contains telephone number information.

To use this script include you must activate the Notify \(com.snc.notify\) plugin.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NotifySMS - NotifySMS\(\)

Creates an instance of a NotifySMS object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example shows how to instantiate a NotifySMS object.

```
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var fromNumber = getFromNumber();
  var groupId = sourceRecord.assignment_group + '';
  var toGr = getRecipientGRs(groupId);
  var message = 'An Incident ' + sourceRecord.getDisplayValue() + ' has been assigned to your group';
  if (fromNumber && toGr) {
    var notifySMS = new NotifySMS();
    notifySMS.sendToUsers(fromNumber, toGr, message, sourceRecord);
  } 
}
```

## NotifySMS - sendBulkSMS\(String fromNumber, Array toNumber, String message, GlideRecord sourceRecord\)

Triggers an asynchronous flow action that sends a Short Message Service \(SMS\) message from a specified Notify phone number to a list of phone numbers.

<table id="table_dsz_2sj_5xb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fromNumber

</td><td>

String

</td><td>

Notify telephone number sending the SMS message.

</td></tr><tr><td>

toNumber

</td><td>

Array

</td><td>

List of telephone numbers to receive the SMS message.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message to send.

</td></tr><tr><td>

sourceRecord

</td><td>

GlideRecord

</td><td>

Optional. Incident GlideRecord to store in the Source field of the associated SMS message record in the Notify Message \[notify\_message\] table. This links the Incident record that caused the SMS message to be generated to that SMS message.Default: None. If this parameter is not passed in, this information is not tracked.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|ScriptableFlowRunnerResult|[ScriptableFlowRunnerResult - Scoped](../../ScriptableFlowRunnerResultScoped/concept/ScriptableFlowRunnerResultScopedAPI.md#) object.|

The follow code example shows how you can use this method to send a bulk SMS message.

```
var fromNumber = getFromNumber();
var toNumbers = getRecipientNumbers();
var message = 'This is an example SMS';
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var notifySMS = new NotifySMS();
  notifySMS.sendBulkSMS(fromNumber, toNumbers, message, sourceRecord);  
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

## NotifySMS - sendToNumber\(String fromNumber, String toNumber, String message, Object sourceRecord\)

Sends a Short Message Service \(SMS\) message from a specified Notify telephone number to a specified telephone number.

In addition, you can optionally associate the Incident record that caused the SMS message to be generated to the SMS message.

<table id="table_zp2_znf_kmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fromNumber

</td><td>

String

</td><td>

Notify telephone number sending the SMS message.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message to send.

</td></tr><tr><td>

sourceRecord

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

Optional. Incident GlideRecord to store in the Source field of the associated SMS message record in the Notify Message \[notify\_message\] table. This links the Incident record that caused the SMS message to be generated to that SMS message.Default: None. If this parameter is not passed in, this information is not tracked.

</td></tr><tr><td>

toNumber

</td><td>

String

</td><td>

Telephone number of the device to receive the SMS message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example illustrates how to send an SMS message to a specified phone number and stamp the associated Incident record with the message information.

```
var fromNumber = getFromNumber();  
var toNumber = '+123456789';  
var message = 'This is an example SMS';  
var sourceRecord = new GlideRecord('incident');  
sourceRecord.query();  
if (sourceRecord.next()) { 
  var notifySMS = new NotifySMS();
  notifySMS.sendToNumber(fromNumber, toNumber, message, sourceRecord);  
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

## NotifySMS - sendToNumbers\(String fromNumber, Array toNumber, String message, Object sourceRecord\)

Sends a Short Message Service \(SMS\) message from a specified Notify phone number to a list of phone numbers.

In addition, you can optionally associate the Incident record that caused the SMS message to be generated with the SMS message.

**Note:** Internally this method uses the [NotifySMS - sendBulkSMS\(String fromNumber, Array toNumber, String message, GlideRecord sourceRecord\)](NotifySMSAPI.md#) method to trigger an asynchronous flow action.

<table id="table_ukh_nsf_kmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fromNumber

</td><td>

String

</td><td>

Notify telephone number sending the SMS message.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message to send.

</td></tr><tr><td>

sourceRecord

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

Optional. Incident GlideRecord to store in the Source field of the associated SMS message record in the Notify Message \[notify\_message\] table. This links the Incident record that caused the SMS message to be generated to that SMS message.Default: None. If this parameter is not passed in, this information is not tracked.

</td></tr><tr><td>

toNumber

</td><td>

Array

</td><td>

List of telephone numbers to receive the SMS message.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example illustrates how to send an SMS message to multiple telephone numbers and store the information in the associated Incident record.

```
var fromNumber = getFromNumber();
var toNumbers = getRecipientNumbers()
var message = 'This is an example SMS';
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var notifySMS = new NotifySMS();
  notifySMS.sendToNumbers(fromNumber, toNumbers, message, sourceRecord);  
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

## NotifySMS - sendToUser\(String fromNumber, Object toGr, String message, Object sourceRecord\)

Sends a Short Message Service \(SMS\) message from a specified phone number to the user identified in a specified GlideRecord.

This method extracts the telephone number from the specified GlideRecord. In addition, you can optionally associate the Incident record that caused the SMS message to be generated with the SMS message.

<table id="table_jsc_c1g_kmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fromNumber

</td><td>

String

</td><td>

Notify telephone number sending the SMS message.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message to send.

</td></tr><tr><td>

sourceRecord

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

Optional. Incident GlideRecord to store in the Source field of the associated SMS message record in the Notify Message \[notify\_message\] table. This links the Incident record that caused the SMS message to be generated to that SMS message.Default: None. If this parameter is not passed in, this information is not tracked.

</td></tr><tr><td>

toGr

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

GlideRecord of a record type that contains a field that resolves to a user's telephone number. The record type must correlate with the record type used by the phone number resolver that is currently implemented. A phone number resolver is simply a method that obtains the user telephone number from a specific type of GlideRecord, such as a User record or a Case record. When using the default resolver, the records correspond to the User \[sys\_user\] table. To change the type of record that the resolver uses to obtain the telephone number, use the [NotifySMS - setRecordToNumberResolver\(Object scriptIncludeInstance, String methodName\)](NotifySMSAPI.md#) method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example illustrates how to send an SMS message to a user identified in the associated Incident record and stamp the associated Incident record with the message information.

```
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var fromNumber = getFromNumber();
  var toGr = sourceRecord.assigned_to.getRefRecord();
  var message = 'An Incident ' + sourceRecord.getDisplayValue() + ' has been assigned to you'; 
  if (fromNumber && toGr.isValidRecord()) { 
    var notifySMS = new NotifySMS();
    notifySMS.sendToUser(fromNumber, toGr, message, sourceRecord);
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

## NotifySMS - sendToUsers\(String fromNumber, Object toGr, String message, Object sourceRecord\)

Sends a Short Message Service \(SMS\) message from a specified Notify phone number to users found in a specified GlideRecord.

This method extracts the destination telephone numbers from the passed-in GlideRecord. In addition, you can optionally associate the Incident record that caused the SMS message to be generated with the SMS message.

**Note:** Internally this method uses the [NotifySMS - sendBulkSMS\(String fromNumber, Array toNumber, String message, GlideRecord sourceRecord\)](NotifySMSAPI.md#) method to trigger an asynchronous flow action.

<table id="table_pdp_kpg_kmb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fromNumber

</td><td>

String

</td><td>

Notify telephone number sending the SMS message.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Message to send.

</td></tr><tr><td>

sourceRecord

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

Optional. Incident GlideRecord to store in the Source field of the associated SMS message record in the Notify Message \[notify\_message\] table. This links the Incident record that caused the SMS message to be generated to that SMS message.Default: None. If this parameter is not passed in, this information is not tracked.

</td></tr><tr><td>

toGr

</td><td>

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#)

</td><td>

GlideRecord of a record type that contains a field that resolves to a user's telephone number. The record type must correlate with the record type used by the phone number resolver that is currently implemented. A phone number resolver is simply a method that obtains the user telephone number from a specific type of GlideRecord, such as a User record or a Case record. When using the default resolver, the records correspond to the User \[sys\_user\] table. To change the type of record that the resolver uses to obtain the telephone number, use the [NotifySMS - setRecordToNumberResolver\(Object scriptIncludeInstance, String methodName\)](NotifySMSAPI.md#) method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to send an SMS message to users within a specified incident record.

```
var sourceRecord = new GlideRecord('incident');
sourceRecord.query();
if (sourceRecord.next()) {
  var fromNumber = getFromNumber();
  var groupId = sourceRecord.assignment_group + '';
  var toGr = getRecipientGRs(groupId);
  var message = 'An Incident ' + sourceRecord.getDisplayValue() + ' has been assigned to your group';
  if (fromNumber && toGr) {
    var notifySMS = new NotifySMS();
    notifySMS.sendToUsers(fromNumber, toGr, message, sourceRecord);
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

function getRecipientGRs(groupId) {
  if (!groupId)
    return;
  var userMemberGr = new GlideRecord('sys_user_grmember');
  userMemberGr.addQuery('group', groupId);
  userMemberGr.query();
  var userIds = [];
  while (userMemberGr.next()) {
    userIds.push(userMemberGr.user + ''); 
  }
  var userGr = new GlideRecord('sys_user');
  userGr.addActiveQuery();
  userGr.addQuery('sys_id', 'IN', userIds.join(','));
  userGr.query();
  return userGr; 
} 
```

## NotifySMS - setRecordToNumberResolver\(Object scriptIncludeInstance, String methodName\)

Sets the method within a script include to use to obtain the target telephone number in the GlideRecord that is passed in the NotifySMS.sendToUser\(\) and NotifySMS.sendToUsers\(\) methods.

By default, the NotifyUtil.getSMSNumberForUser\(\) method is used to obtain the telephone number from a User \[sys\_user\] based GlideRecord. Use the setRecordToNumberResolver\(\) method if you need to create a custom method to obtain this information from a different record type, such as a Case record.

|Name|Type|Description|
|----|----|-----------|
|methodName|String|Name of the method to use to obtain the target telephone number in a GlideRecord.|
|scriptIncludeInstance|Object|Instance of the script include that contains the specified number resolver method.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set the phone number resolver to the getSMSNumberForConsumer\(\) method within the csmUtils script include.

```
// Script include that contains the logic to retrieve a phone number for a consumer.
var csmUtils = new global.CSMExampleUtils();
 
// Example Case record used as source for sending SMS
var caseGr = new GlideRecord('sn_customerservice_case');
caseGr.get('3af265b3d1cb5010f877cb055160faxx'); // Case sys_id
 
var notifySms = new global.NotifySMS();
 
// Use the getSMSNumberForConsumer method of the csmUtils script include (CSMExampleUtils) to obtain the phone number of the consumer.
notifySms.setRecordToNumberResolver(csmUtils, 'getSMSNumberForConsumer');
 
// Send an SMS message to a user whose telephone number is in the specified Case GlideRecord.
var smsText = 'This is a test message for ' + caseGr.getValue('number');
notifySms.sendToUser('+1xxxxxxxxxx', caseGr.getValue('consumer'), smsText, caseGr); // First param is the Notify phone number
```

This example shows the code needed for the telephone resolver method getSMSNumberForConsumer\(\).

```
getSMSNumberForConsumer: function(consumerGrOrId) {
  if (!consumerGrOrId)
    return;
 
  var consumerId, consumerGr;
  if (typeof consumerGrOrId === "string")
    consumerId = consumerGrOrId;
  if (typeof consumerGrOrId === "object" && consumerGrOrId["isValidRecord"]) {
    consumerGr = consumerGrOrId;
    consumerId = consumerGr.getUniqueValue();
  }
          
  if (!consumerId)
    return;
          
  if (!consumerGr) {
    consumerGr = new GlideRecord('csm_consumer');
    consumerGr.get(consumerId);
  }
          
  if (consumerGr.isValidRecord()) {
    return consumerGr.getValue('mobile_phone');
  }
}
```

