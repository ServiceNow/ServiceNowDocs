---
title: TMFTopicEventAPIUtilOOB - Scoped
description: The TMFTopicEventAPIUtilOOB script include contains functions to handle Event Notification Management Open API requests that are triggered by external trigger definitions to create, update, and delete events in the Event \[em\_event\] table.Returns the payload schema used when processing an alarm change event \(ALARM\_CHANGE\_EVENT\_SCHEMA\).Returns the payload schema used when processing an alarm create event \(ALARM\_CREATE\_EVENT\_SCHEMA\).Returns the payload schema used when processing an alarm delete event \(ALARM\_DELETE\_EVENT\_SCHEMA\).Maps the parameters in the passed change request payload to fields in the specified record in the Event \[em\_event\] table.Maps the parameters in the passed create request payload to fields in the specified record in the Event \[em\_event\] table.Maps the parameters in the passed delete request payload to fields in the specified record in the Event \[em\_event\] table.Generates the response object after event creation or update, including the clearing of an event.Starts the process of updating a record in the Event \[em\_event\] table when the eventType is set to AlarmChangeNotification.Starts the process of creating a record in the Event \[em\_event\] table when the eventType is set to AlarmCreateNotification.Starts the process of clearing the alarm event in the Event \[em\_event\] table when the eventType is set to AlarmDeleteNotification.Transforms the passed in create event payload using the associated create event mapping values and stores the information in Event \[em\_event\] table.Transforms the passed in change event payload using the associated change event mapping values and stores the updated information in the passed GlideRecord within the Event \[em\_event\] table.Transforms the passed in delete \(clear\) event payload using the associated delete event mapping values and stores the updated information in the passed GlideRecord within the Event \[em\_event\] table.Performs validation on the subscription.Provides the ability to define additional verification of the passed in change event payload.Provides the ability to define additional verification of the passed in create event payload.Provides the ability to define additional verification of the passed in delete event payload.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 21
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TMFTopicEventAPIUtilOOB- Scoped

The `TMFTopicEventAPIUtilOOB` script include contains functions to handle Event Notification Management Open API requests that are triggered by external trigger definitions to create, update, and delete events in the Event \[em\_event\] table.

This script include contains the default implementation for the Event Notification Management Open API. If you want to change the default functionality of this API, you need to override the functions contained in this script include in the `TMFTopicEventAPIUtil` script include.

This script include runs in the `sn_ind_tmf642` namespace and requires the Telecommunications Alarm Management Open API \(app-ind-tmfapi-alarm\) plugin to be activated.

For additional information on how to override these functions, see the [Event Notification Management Open API Developer Guide](../../../../../integrate/guides/telecom/concept/event-mgmt-notif_dev-guide.md#).

For additional information on the Event Notification Management Open API, see [Event Notification Management Open API](../../../../../integrate/inbound-rest/concept/event_open-api.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TMFTopicEventAPIUtilOOB - getAlarmChangeEventSchema\(\)

Returns the payload schema used when processing an alarm change event \(ALARM\_CHANGE\_EVENT\_SCHEMA\).

This function is called as part of the `AlarmChangeEvent` flow action call process. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include and the schema in the `TMFAlarmAPIConstants` script include.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Schema defined in `TMFAlarmAPIConstants.ALARM_CHANGE_EVENT_SCHEMA`.|

```
// Schema validation
var schema = this.getAlarmChangeEventSchema();
var validationResults = this.schemaValidator.validateJSON(changeAlarmPayload, schema);
if (validationResults.length > 0) {
  this.responseObject.status = TMFAlarmAPIConstants.EVENT_TRANSFORMATION_ERROR;
  this.responseObject.responseError.errorMessage = TMFAlarmAPIConstants.MESSAGES.CHANGE_ERROR;
  this.responseObject.responseError.errorReason = TMFAlarmAPIConstants.MESSAGES.CHANGE_ERROR_PAYLOAD;
  var messageDetails = [];
  for (var i = 0; i < validationResults.length; i++)
    messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
  this.responseObject.responseError.details = messageDetails;
  return this.responseObject;
```

## TMFTopicEventAPIUtilOOB - getAlarmCreateEventSchema\(\)

Returns the payload schema used when processing an alarm create event \(ALARM\_CREATE\_EVENT\_SCHEMA\).

This function is called as part of the `AlarmCreateEvent` flow action call process. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include and the schema in the `TMFAlarmAPIConstants` script include.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Schema defined in `TMFAlarmAPIConstants.ALARM_CREATE_EVENT_SCHEMA`|

```
// Schema validation
var schema = this.getAlarmCreateEventSchema();
var validationResults = this.schemaValidator.validateJSON(eventAlarmObject, schema);
if (validationResults.length > 0) {
  this.responseObject.status = TMFAlarmAPIConstants.EVENT_TRANSFORMATION_ERROR;
  this.responseObject.responseError.errorMessage = TMFAlarmAPIConstants.MESSAGES.CREATE_ERROR;
  this.responseObject.responseError.errorReason = TMFAlarmAPIConstants.MESSAGES.CREATE_ERROR_PAYLOAD;
  var messageDetails = [];
  for (var i = 0; i < validationResults.length; i++)
    messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
  this.responseObject.responseError.details = messageDetails;
  return this.responseObject;
}
```

## TMFTopicEventAPIUtilOOB - getAlarmDeleteEventSchema\(\)

Returns the payload schema used when processing an alarm delete event \(ALARM\_DELETE\_EVENT\_SCHEMA\).

This function is called as part of the `AlarmDeleteEvent` flow action call process. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include and the schema in the `TMFAlarmAPIConstants` script include.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Schema defined in `TMFAlarmAPIConstants.ALARM_DELETE_EVENT_SCHEMA`.|

```
// Schema validation
var schema = this.getAlarmDeleteEventSchema();
var validationResults = this.schemaValidator.validateJSON(deleteAlarmPayload, schema);
if (validationResults.length > 0) {
  this.responseObject.status = TMFAlarmAPIConstants.EVENT_TRANSFORMATION_ERROR;
  this.responseObject.responseError.errorMessage = TMFAlarmAPIConstants.MESSAGES.CLEAR_ERROR;
  this.responseObject.responseError.errorReason = TMFAlarmAPIConstants.MESSAGES.CLEAR_ERROR_PAYLOAD;
  var messageDetails = [];
  for (var i = 0; i < validationResults.length; i++)
    messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
  this.responseObject.responseError.details = messageDetails;
  return this.responseObject;
}
```

## TMFTopicEventAPIUtilOOB - mapAlarmChangeObjectToEvent\(alarmObject, GlideRecord newEventGr\)

Maps the parameters in the passed change request payload to fields in the specified record in the Event \[em\_event\] table.

You can customize field mappings to add data to the Event \[em\_event\] table or change the default field mappings. To modify mappings, create functions with identical names and parameters in the `TMFTopicEventAPIUtil` script include to override the mappings in the `TMFTopicEventAPIUtilOOB` script include. If you add fields to the mappings, these fields must also be added to the associated schema \(`TMFAlarmAPIConstants.ALARM_CHANGE_EVENT_SCHEMA`\).

This function is called as part of the transformAndPersistChangeEvent\(\) function.

|Name|Type|Description|
|----|----|-----------|
|alarmObject|Object|Payload should match what is defined in the schema defined in `TMFAlarmAPIConstants.ALARM_CHANGE_EVENT_SCHEMA`.|
|newEventGr|GlideRecord|GlideRecord of the record to updated in the Event \[em\_event\] table.|

|Type|Description|
|----|-----------|
|None| |

```
this.mapAlarmChangeObjectToEvent(additionalInfoObj, newEventGr);

var id = newEventGr.insert();
return gs.nil(id) ? id : newEventGr.message_key;
```

## TMFTopicEventAPIUtilOOB - mapCreateAlarmObjectToEvent\(Object alarmObject, GlideRecord eventGr\)

Maps the parameters in the passed create request payload to fields in the specified record in the Event \[em\_event\] table.

You can customize field mappings to add data to the Event \[em\_event\] table or change the default field mappings. To modify mappings, create functions with identical names and parameters in the `TMFTopicEventAPIUtil` script include to override the mappings in the `TMFTopicEventAPIUtilOOB` script include. If you add fields to the mappings, these fields must also be added to the associated schema \(`TMFAlarmAPIConstants.ALARM_CREATE_EVENT_SCHEMA`\).

This function is called as part of the transformAndPersistAlarmCreateEvent\(\) function.

|Name|Type|Description|
|----|----|-----------|
|alarmObject|Object|Payload should match what is defined in the schema defined in `TMFAlarmAPIConstants.ALARM_CREATE_EVENT_SCHEMA`.|
|eventGr|GlideRecord|GlideRecord of the record in the Event \[em\_event\] table.|

|Type|Description|
|----|-----------|
|None| |

```
this.mapCreateAlarmObjectToEvent(eventAlarmObject, eventGr);
var id = eventGr.insert();
return gs.nil(id) ? id : msgKey;
```

## TMFTopicEventAPIUtilOOB - mapDeleteAlarmObjectToEvent\(Object additionalInfoObj, GlideRecord newEventGr\)

Maps the parameters in the passed delete request payload to fields in the specified record in the Event \[em\_event\] table.

You can customize field mappings to add data to the Event \[em\_event\] table or change the default field mappings. To modify mappings, create functions with identical names and parameters in the `TMFTopicEventAPIUtil` script include to override the mappings in the `TMFTopicEventAPIUtilOOB` script include. If you add fields to the mappings, these fields must also be added to the associated schema \(`TMFAlarmAPIConstants.ALARM_DELETE_EVENT_SCHEMA`\).

This function is called as part of the transformAndPersistDeleteEvent\(\) function.

|Name|Type|Description|
|----|----|-----------|
|alarmObject|Object|Payload should match what is defined in the schema defined in `TMFAlarmAPIConstants.ALARM_DELETE_EVENT_SCHEMA`.|
|newEventGr|GlideRecord|GlideRecord of the record to use to map the fields in the payload to those in the Event \[em\_event\] table.|

|Type|Description|
|----|-----------|
|None| |

```
this.mapDeleteAlarmObjectToEvent(additionalInfoObj, newEventGr);
var id = newEventGr.insert();
return gs.nil(id) ? id : newEventGr.message_key;
```

## TMFTopicEventAPIUtilOOB - prepareEventAlarmRecordResponse\(String msgKey Object alarmObject, Object responseObject\)

Generates the response object after event creation or update, including the clearing of an event.

This function is called by the processAlarmCreateEvent\(\), processChangeAlarm\(\), and processDeleteAlarmEvent\(\) functions. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

<table id="table_tnr_qxs_zyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

msgKey

</td><td>

String

</td><td>

Message key. This key is generated when an event is created. Table: In the Message key field in the Events \[em\_event\] table.

</td></tr><tr><td>

alarmObject

</td><td>

Object

</td><td>

Event payload to process. The format of this payload should correlate to the event type that is being processed. The schemas for these payloads are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject

</td><td>

Object

</td><td id="responseObject-TMFEvtOOO-entry">

Empty response object. Use this object to record any issues with the verification of the payload schema.Data type: Object

```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Object

</td><td id="responseObject_responseError-TMFEvtOOO-entry">

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Array

</td><td id="responseObject_responseError_details-TMFEvtOOO-entry">

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

String

</td><td id="responseObject_responseError_errorMessage-TMFEvtOOO-entry">

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

String

</td><td id="responseObject_responseError_errorReason-TMFEvtOOO-entry">

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

String

</td><td id="responseObject_status-TMFEvtOOO-entry">

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Object

</td><td id="responseObject_successResponse-TMFEvtOOO-entry">

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table><table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr></tbody>
</table>```
processDeleteAlarm: function(additionalInfoObj, gr, deleteAlarmPayload, responseObject) {
var msgKey = this.transformAndPersistDeleteEvent(additionalInfoObj, gr);
var responsePayload = this.prepareEventAlarmRecordResponse(msgKey, deleteAlarmPayload, responseObject);
this._logger.logDebug("processDeleteAlarmEvent");
return responsePayload;
},
```

## TMFTopicEventAPIUtilOOB - processAlarmChangeEvent\(Object changeAlarmPayload\)

Starts the process of updating a record in the Event \[em\_event\] table when the **eventType** is set to `AlarmChangeNotification`.

This function is called by the `AlarmChangeEvent` flow action. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

|Name|Type|Description|
|----|----|-----------|
|changeAlarm​Payload|Object|Event change payload to process. The payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_CHANGE_EVENT_SCHEMA`.|

<table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>```
Called by the `AlarmChangeEvent` flow action
```

## TMFTopicEventAPIUtilOOB - processAlarmCreateEvent\(Object eventAlarmObject\)

Starts the process of creating a record in the Event \[em\_event\] table when the **eventType** is set to `AlarmCreateNotification`.

This function is called by the `AlarmCreateEvent` flow action. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

|Name|Type|Description|
|----|----|-----------|
|eventAlarm​Object|Object|Event create payload to process. The payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_CREATE_EVENT_SCHEMA`.|

<table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>```
Called by `AlarmCreateEvent` flow action.
```

## TMFTopicEventAPIUtilOOB - processDeleteAlarmEvent\(Object deleteAlarmPayload\)

Starts the process of clearing the alarm event in the Event \[em\_event\] table when the **eventType** is set to `AlarmDeleteNotification`.

This function clears the state field and closes the event alarm. It also updates any parameters in the passed payload.

This function is called by the `AlarmDeleteEvent` flow action. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

|Name|Type|Description|
|----|----|-----------|
|deleteAlarm​Payload|Object|Event delete payload to process. The payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_DELETE_EVENT_SCHEMA`.|

<table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>```
Called by `AlarmDeleteEvent` flow action.
```

## TMFTopicEventAPIUtilOOB - transformAndPersistAlarmCreateEvent\(Object alarmObject\)

Transforms the passed in create event payload using the associated create event mapping values and stores the information in Event \[em\_event\] table.

This function is called by the [processAlarmCreateEvent\(\)](tmftopiceventapiutiloobScopedAPI.md#) function as part of the flow action. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

|Name|Type|Description|
|----|----|-----------|
|alarmObject|Object|Payload to use to create a record in the Event \[em\_event\] table. The payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_CREATE_EVENT_SCHEMA`.|

|Type|Description|
|----|-----------|
|String|Unique ID \(Message key\) of the event.|

This function is only called by the `AlarmCreateEvent` flow action, so no code example is provided.

## TMFTopicEventAPIUtilOOB - transformAndPersistChangeEvent\(Object additionalInfoObj, GlideRecord existingGr\)

Transforms the passed in change event payload using the associated change event mapping values and stores the updated information in the passed GlideRecord within the Event \[em\_event\] table.

This function is called by the [processAlarmChangeEvent\(\)](tmftopiceventapiutiloobScopedAPI.md#) function as part of the flow action. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

|Name|Type|Description|
|----|----|-----------|
|additional​InfoObj|Object|Payload to use to update the fields in the record specified in the **existingGr** parameter. The payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_CHANGE_EVENT_SCHEMA`.|
|existingGr|GlideRecord|GlideRecord of the event record in the Event \[em\_event\] table to update.|

|Type|Description|
|----|-----------|
|String|Unique ID \(Message key\) of the event.|

This function is only called by the `AlarmChangeEvent` flow action, so no code example is provided.

## TMFTopicEventAPIUtilOOB - transformAndPersistDeleteEvent\(Object additionalInfoObj GlideRecord existingGr\)

Transforms the passed in delete \(clear\) event payload using the associated delete event mapping values and stores the updated information in the passed GlideRecord within the Event \[em\_event\] table.

This function is called by the [&gt;processAlarmDeleteEvent\(\)](tmftopiceventapiutiloobScopedAPI.md#) function as part of the flow action. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

|Name|Type|Description|
|----|----|-----------|
|additional​InfoObj|Object|Payload to use to update the clear event fields in the record specified in the **existingGr** parameter. The payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_DELETE_EVENT_SCHEMA`.|
|existingGr|GlideRecord|GlideRecord of the event record in the Event \[em\_event\] table for which to clear the alarm.|

|Type|Description|
|----|-----------|
|String|Unique ID \(Message key\) of the event.|

This function is only called by the `AlarmDeleteEvent` flow action, so no code example is provided.

## TMFTopicEventAPIUtilOOB - validateSubscription\(Object eventAlarmObject, Object responseObject\)

Performs validation on the subscription.

This validation includes checking if the callback URL used to make the event notification and the **eventType** in the payload are registered.

This function is called by the processAlarmCreateEvent\(\), processChangeAlarm\(\), and processDeleteAlarmEvent\(\) functions. You can change the functionality of this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

<table id="table_tnr_qxs_zyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventAlarm​Object

</td><td>

Object

</td><td>

Event payload to validate. The format of this payload should correlate to the event type that is being processed. The schemas for these payloads are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject

</td><td>

Object

</td><td id="responseObject-TMFEvtOOO-entry">

Empty response object. Use this object to record any issues with the verification of the payload schema.Data type: Object

```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​status

</td><td>

String

</td><td id="responseObject_status-TMFEvtOOO-entry">

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Object

</td><td id="responseObject_successResponse-TMFEvtOOO-entry">

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Object

</td><td id="responseObject_responseError-TMFEvtOOO-entry">

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Array

</td><td id="responseObject_responseError_details-TMFEvtOOO-entry">

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

String

</td><td id="responseObject_responseError_errorMessage-TMFEvtOOO-entry">

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

String

</td><td id="responseObject_responseError_errorReason-TMFEvtOOO-entry">

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr></tbody>
</table><table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>This function is only called by the `AlarmCHANGEEvent` flow action, so no code example is provided.

## TMFTopicEventAPIUtilOOB - verifyAlarmChangeEventPayload\(Object changeAlarmPayload, Object responseObject \)

Provides the ability to define additional verification of the passed in change event payload.

This function is called by the [processAlarmChangeEvent\(\)](tmftopiceventapiutiloobScopedAPI.md#) function as part of the flow action. Currently there is no additional payload verification provided for the change payload. You can add functionality for this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

<table id="table_tnr_qxs_zyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeAlarm​Payload

</td><td>

Object

</td><td>

Payload to verify. Payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_CHANGE_EVENT_SCHEMA`.

</td></tr><tr><td>

responseObject

</td><td>

Object

</td><td id="responseObject-TMFEvtOOO-entry">

Empty response object. Use this object to record any issues with the verification of the payload schema.Data type: Object

```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Object

</td><td id="responseObject_responseError-TMFEvtOOO-entry">

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Array

</td><td id="responseObject_responseError_details-TMFEvtOOO-entry">

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

String

</td><td id="responseObject_responseError_errorMessage-TMFEvtOOO-entry">

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

String

</td><td id="responseObject_responseError_errorReason-TMFEvtOOO-entry">

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

String

</td><td id="responseObject_status-TMFEvtOOO-entry">

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Object

</td><td id="responseObject_successResponse-TMFEvtOOO-entry">

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table><table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>```
 // Apply customized validations if applicable, defaults to no error
var changePayloadResponse = this.verifyAlarmChangeEventPayload(changeAlarmPayload, this.responseObject);
if (!gs.nil(changePayloadResponse.responseError.errorMessage))
  return changePayloadResponse;
```

## TMFTopicEventAPIUtilOOB - verifyAlarmCreateEventPayload\(Object alarmObject, Object responseObject\)

Provides the ability to define additional verification of the passed in create event payload.

This function is called by the [processAlarmCreateEvent\(\)](tmftopiceventapiutiloobScopedAPI.md#) function as part of the flow action. Currently there is no additional payload verification provided for the create payload. You can add functionality for this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

<table id="table_tnr_qxs_zyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alarmPayload

</td><td>

Object

</td><td>

Payload to verify. Payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_CREATE_EVENT_SCHEMA`.

</td></tr><tr><td>

responseObject

</td><td>

Object

</td><td id="responseObject-TMFEvtOOO-entry">

Empty response object. Use this object to record any issues with the verification of the payload schema.Data type: Object

```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​status

</td><td>

String

</td><td id="responseObject_status-TMFEvtOOO-entry">

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Object

</td><td id="responseObject_successResponse-TMFEvtOOO-entry">

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Object

</td><td id="responseObject_responseError-TMFEvtOOO-entry">

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Array

</td><td id="responseObject_responseError_details-TMFEvtOOO-entry">

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

String

</td><td id="responseObject_responseError_errorMessage-TMFEvtOOO-entry">

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

String

</td><td id="responseObject_responseError_errorReason-TMFEvtOOO-entry">

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr></tbody>
</table><table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>```
// Apply customized validations if applicable, defaults to no error
var creatPayloadResponse = this.verifyAlarmCreateEventPayload(eventAlarmObject, this.responseObject);
if (!gs.nil(creatPayloadResponse.responseError.errorMessage))
  return creatPayloadResponse;
```

## TMFTopicEventAPIUtilOOB - verifyDeleteEventPayload\(Object deleteAlarmPayload, Object responseObject\)

Provides the ability to define additional verification of the passed in delete event payload.

This function is called by the [processDeleteAlarmEvent\(\)](tmftopiceventapiutiloobScopedAPI.md#) function as part of the flow action. Currently there is no additional payload verification provided for the delete payload. You can add functionality for this function by overriding the default functionality in the `TMFTopicEventAPIUtil` script include.

<table id="table_tnr_qxs_zyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

deleteAlarm​Payload

</td><td>

Object

</td><td>

Payload to verify. Payload should match the schema defined in `TMFAlarmAPIConstants.ALARM_DELETE_EVENT_SCHEMA`.

</td></tr><tr><td>

responseObject

</td><td>

Object

</td><td id="responseObject-TMFEvtOOO-entry">

Empty response object. Use this object to record any issues with the verification of the payload schema.Data type: Object

```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​status

</td><td>

String

</td><td id="responseObject_status-TMFEvtOOO-entry">

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Object

</td><td id="responseObject_successResponse-TMFEvtOOO-entry">

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Object

</td><td id="responseObject_responseError-TMFEvtOOO-entry">

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Array

</td><td id="responseObject_responseError_details-TMFEvtOOO-entry">

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

String

</td><td id="responseObject_responseError_errorMessage-TMFEvtOOO-entry">

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

String

</td><td id="responseObject_responseError_errorReason-TMFEvtOOO-entry">

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr></tbody>
</table><table id="table_unr_qxs_zyb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

responseObject

</td><td>

Details about the status of the function call.```
"responseObject": {
  "responseError": {Object},
  "status": "String",
  "successResponse": {Object}
}
```

</td></tr><tr><td>

responseObject.​responseError

</td><td>

Details about any error that occurred during validation.```
"responseError": {
  "details": [Array],
  "errorMessage": "String",
  "errorReason": "String"
}
```

</td></tr><tr><td>

responseObject.​responseError.​details

</td><td>

Any additional information to pass back to the calling routine.For example:

```
var messageDetails = [];
for (var i = 0; i < validationResults.length; i++)
  messageDetails.push(this.createErrorObject(validationResults[i].message, validationResults[i].dataPath));
this.responseObject.responseError.details = messageDetails;
return this.responseObject
```

</td></tr><tr><td>

responseObject.​responseError.​errorMessage

</td><td>

Error message that describes the error that occurred. The available error messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​responseError.​errorReason

</td><td>

Reason why the endpoint failed. The available error reasons are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​status

</td><td>

Status of the function call. The available status messages are defined in the `TMFAlarmAPIConstants` script include.

</td></tr><tr><td>

responseObject.​successResponse

</td><td>

Successful response from the function call. For example, you could store the payload object in this value.

</td></tr></tbody>
</table>```
// Apply customized validations if applicable, defaults to no error
var deletePayloadResponse = this.verifyDeleteEventPayload(deleteAlarmPayload, this.responseObject);
if (!gs.nil(deletePayloadResponse.responseError.errorMessage))
  return deletePayloadResponse;
```

