---
title: Alarm Management Open API Developer Guide
description: Use the Alarm Management Open API to create and update data in the Events \[em\_event\] table.The Alarm Management Open API can be extended by editing script includes.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Developer guides, API implementation and reference]
---

# Alarm Management Open API Developer Guide

Use the Alarm Management Open API to create and update data in the Events \[em\_event\] table.

This developer guide provides information on how to extend the [Alarm Management Open API](../../../inbound-rest/concept/alarm-open-api.md#) to make various customizations.

## Extending the Alarm Management Open API

The Alarm Management Open API can be extended by editing script includes.

These script includes should only be edited with an understanding of the consequences of the changes.

-   `TMFAlarmAPIConstants`: Contains constants and required parameter information.
-   `TMFAlarmAPIUtil`: Contains functions to handle API requests.
-   `AlarmAPIProcessorOOB`: Contains helper functions that support functions in `TMFAlarmAPIUtil`.
-   `AlarmAPIProcessor`: An empty script include file. Use this file to define any functions that you want to override from `AlarmAPIProcessorOOB`.

Extend the Alarm Management Open API to make the following customizations.

### Required parameters

The Alarm Management API utilizes JSON schemas to hold required parameters information. These JSON schemas are defined in the TMFAlarmAPIConstants script include. These schemas are used to validate whether request payloads are valid. These schemas are not referenced directly in script includes and are returned by the following methods in the AlarmAPIProcessorOOB script include:

-   `getCreateEventSchema`: Returns the validating schema for creating an event.
-   `getClearEventSchema`: Returns the validating schema for clearing an event alarm.
-   `getPatchEventSchema`: Returns the validating schema for patching an event.

To override existing schemas, define new schemas in the `AlarmAPIProcessor` script include and override the `AlarmAPIProcessorOOB` script include methods.

```
var AlarmAPIProcessor = Class.create();
AlarmAPIProcessor.prototype = Object.extendsObject(AlarmAPIProcessorOOB, {
	// Define overriding functions here
	
	// Define getCreateEventSchema here to override OOTB method in AlarmAPIProcessorOOB
	getCreateEventSchema: function() {
		return JSON.parse(AlarmAPIProcessor.CUSTOMIZED_SCHEMA);
	},
    type: 'AlarmAPIProcessor'
});

// Define a new schema
AlarmAPIProcessor.CUSTOMIZED_SCHEMA = "{\"title\":\"CreateAlarm\",\"type\":\"object\",
\"properties\":{\"externalAlarmId\":{\"type\":\"string\"},\"alarmType\":{\"type\":\"string\"},
\"perceivedSeverity\":{\"type\":\"string\"},\"probableCause\":{\"type\":\"string\"},
\"alarmedObject\":{\"type\":\"object\",\"properties\":{\"id\":{\"type\":\"string\"},
\"href\":{\"type\":\"string\"}},\"required\":[\"id\"]},\"sourceSystemId\":{\"type\":\"string\"}},
\"required\":[\"externalAlarmId\",\"alarmType\",\"perceivedSeverity\",\"probableCause\",
\"alarmedObject\",\"sourceSystemId\"]}";
```

### Request body validation

To perform additional validation on the request body, override the following functions in the `AlarmAPIProcessorOOB` script include  . These functions are called by the specified functions in the `TMFAlarmAPIUtil` script include.

-   `verifyCreateEventPayload()` - Called by `processCreateEvent()`.
-   `verifyClearEventPayload()` - Called by `processClearEvent()`.
-   `verifyPatchEventPayload()` - Called by `processPatchEvent()`.

All of these functions return `true` by defalut. If a helper function returns `false` , it stops the API operation.

To apply custom validations, override AlarmAPIProcessorOOB helper functions with identically-named function names and parameters in AlarmAPIProcessor. The new AlarmAPIProcessor functions are called by TMFAlarmAPIUtil to replace the default AlarmAPIProcessorOOB helper functions.

In this example, a function in a custom AlarmAPIProcessor script include overrides a default function in AlarmAPIProcessorOOB to perform validation on the name attribute.

```
var AlarmAPIProcessor = Class.create();
AlarmAPIProcessor.prototype = Object.extendsObject(AlarmAPIProcessorOOB, {
	// Define overriding functions here
	
    verifyCreateEventPayload: function(eventPayload, apiResponseProcessor){
        // Returning false terminates the POST request
        // Make sure to assign error message and reason
        if (eventPayload.type != "unique") {
            apiResponseProcessor.setMessage("Failed");
            apiResponseProcessor.setReason("No reason needed");
            return false;
        }
    },
	
    type: 'AlarmAPIProcessor'
});
```

### Additional REST operations

To create additional operations beyond the existing GET, PATCH, and POST operations, [create additional scripted REST resources](../../../custom-web-services/task/t_CreateAScriptedRESTAPIResource.md) for the Alarm Management Open API. The logic of the new scripted REST resources should be consistent with the existing operations. Define functions for the new operations in TMFAlarmAPIUtil.

### Field mapping

When creating or updating records, the Alarm Management Open API maps request body parameters to event record fields. When retrieving records, the API maps record fields to response object attributes.

The AlarmAPIProcessorOOB script include contains the following functions to map a PATCH or POST request body to a record in the Event \[em\_event\] table.

-   `mapCreateAlarmObjectToEvent()`
-   `mapClearAlarmObjectToEvent()`
-   `mapPatchAlarmObjectToEvent()`

It also contains the following functions to map an event GlideRecord to a JSON response object for GET, PATCH, or POST requests.

-   `modifyCreateEventResponse()`
-   `modifyClearEventResponse()`
-   `modifyPatchEventResponse()`

You can customize field mappings to add and retrieve data for additional Event \[em\_event\] table fields or change the default field mappings. To work with mappings, create functions with identical names and parameters in AlarmAPIProcessor to override AlarmAPIProcessorOOB mapping functions. TMFAlarmAPIUtil uses these AlarmAPIProcessor functions to replace the default AlarmAPIProcessorOOB mapping functions.

In the following example, two AlarmAPIProcessor functions override the default functions in AlarmAPIProcessorOOB to change the **Type** field mapping and add a mapping for the **Severity** field.

```
var AlarmAPIProcessor = Class.create();
AlarmAPIProcessor.prototype = Object.extendsObject(AlarmAPIProcessorOOB, {
	// Define overriding functions here
	
    // Function name and parameters must be identical to the function it overrides
    mapCreateAlarmObjectToEvent: function(eventGr, eventObject){
        // Override default mapping for the severity field
        eventGr.severity = "High";
    },

    modifyCreateEventResponse: function(eventGr, eventObject){
        // Override default mapping for the type field
        eventGr.type = "Customized Event"; 
    },
	
    type: 'AlarmAPIProcessor'
});
```

