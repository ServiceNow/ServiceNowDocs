---
title: Event Notification Management Open API Developer Guide
description: Use the Event Notification Management Open API to create, update, and delete event records in the Events \[em\_event\] table.You can extend and modify the functionality of the Event Notification Management Open API by editing its associated script include files.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Developer guides, API implementation and reference]
---

# Event Notification Management Open API Developer Guide

Use the Event Notification Management Open API to create, update, and delete event records in the Events \[em\_event\] table.

This developer guide provides information on how to extend the Event Notification Management Open API to make various customizations.

## Extending the Event Notification Management Open API

You can extend and modify the functionality of the Event Notification Management Open API by editing its associated script include files.

The following are the script includes that the Event Notification Management Open API uses to process event notification requests passed to the API:

-   `AlarmAPIProcessorOOB`: Contains helper functions that support functions in the `TMFTopicEventAPIUtil` script include. For additional information on the `AlarmAPIProcessorOOB` script include, see the [Alarm Management Open API Developer Guide](alarm-mgmt_dev-guide.md#).
-   `AlarmAPIProcessor`: An empty script include file. Update this file to define any functions that you want to override in the `AlarmAPIProcessorOOB` script include.
-   `JSONSchemaValidation`: Contains functions to handle the validation of schemas for the payload defined in the `TMFAlarmAPIConstants` script include. This script include is under the tmt\_core plugin.
-   `TMFAlarmAPIConstants`: Contains constants and required parameter information. It also contains the schemas for the payloads passed in the Event Notification Management Open endpoint.
-   [`TMFTopicEventAPIUtilOOB`](../../../../app-store/dev_portal/API_reference/TMFTopicEventAPIUtilOOB/concept/tmftopiceventapiutiloobScopedAPI.md#): Contains functions to handle API requests that are triggered by [external trigger definition flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/set-up-flow-ihub.md) that have the actions `AlarmCreateNotification`, `AlarmChangeNotification`, `AlarmDeleteNotification` which create, update, and delete events.
-   `TMFTopicEventAPIUtil`: An empty script include file. Update this file to define any functions that you want to override in the `TMFTopicEventAPIUtilOOB` script include.

The following sections provide examples of some of the customizations that you can make to the Event Notification Management Open API processing by extending/modifying these script include files.

### Required parameters

The Event Notification Management API utilizes JSON schemas to define required parameters. These JSON schemas are defined in the `TMFAlarmAPIConstants` script include. These schemas are used to validate whether request payloads are valid. These schemas are not directly referenced in the script includes, but are returned by the following functions in the TMFTopicEventAPIUtilOOB script include:

-   `getAlarmCreateEventSchema()`: Returns the validating schema for creating an event.
-   `getAlarmDeleteEventSchema()`: Returns the validating schema for deleting an event alarm.
-   `getAlarmChangeEventSchema()`: Returns the validating schema for changing fields in an event.

To override the existing schemas, define new schemas in the `TMFTopicEventAPIUtilOOB` script include and override the `TMFTopicEventAPIUtil` script include functions.

For example:

```
var TMFTopicEventAPIUtil = Class.create();
TMFTopicEventAPIUtil.prototype = Object.extendsObject(TMFTopicEventAPIUtilOOB, {
	// Define overriding functions here	
	// Define getAlarmCreateEventSchema here to override OOTB function in TMFTopicEventAPIUtilOOB
	getAlarmCreateEventSchema: function() {
		return JSON.parse(TMFTopicEventAPIUtil.CUSTOMIZED_SCHEMA);
	},
    type: ‘TMFTopicEventAPIUtil’
});

// New schema
TMFTopicEventAPIUtil.CUSTOMIZED_SCHEMA = "{
  \"title\":\"AlarmCreateEvent\",
  \"type\":\"object\",
  \"properties\":{
    \"event\":{
      \"type\":\"object\",
      \"properties\":{
        \"alarm\":{
          \"type\":\"object\",
          \"properties\":{
            \"id\":{
              \"type\":\"string\"
            },
            \"href\":{
              \"type\":\"string\"
            },
            \"externalAlarmId\":{
              \"type\":\"string\"
            },
            \"alarmType\":{
              \"type\":\"string\"
            },
            \"perceivedSeverity\":{
              \"type\":\"string\"
            },
            \"probableCause\":{
              \"type\":\"string\"
            },
            \"alarmedObject\":{
              \"type\":\"object\",
              \"properties\":{
                \"id\":{
                  \"type\":\"string\"
                },
                \"href\":{
                  \"type\":\"string\"
                }
              },
              \"required\":[
                \"id\"
              ]
            },
            \"crossedThresholdInformation\":{
              \"type\":\"object\",
              \"properties\":{
                \"thresholdId\":{
                  \"type\":\"string\"
                }
              },
              \"required\":[
                \"thresholdId\"
              ]
            },
            \"affectedService\":{
              \"type\":\"array\",
              \"properties\":{
                \"id\":{
                  \"type\":\"string\"
                },
                \"href\":{
                  \"type\":\"string\"
                }
              },
              \"items\":{
                \"type\":\"object\",
                \"required\":[
                  \"id\"
                ]
              }
            },
            \"sourceSystemId\":{
              \"type\":\"string\"
            },
            \"specificProblem\":{
              \"type\":\"string\"
            }
          },
          \"required\":[
            \"externalAlarmId\",\"alarmType\",\"perceivedSeverity\",\"probableCause\",\"sourceSystemId\",\"alarmedObject\"
          ]
        }
      },
      \"required\":[
        \"alarm\"
      ]
    }
  },
  \"required\":[
    \"event\"
  ]
}";
```

### Request body validation

To perform additional validation on the request body, override the following functions in the `TMFTopicEventAPIUtilOOB` script include. These functions are called by the specified functions in the same script include.

-   `verifyAlarmCreateEventPayload()`: Called by `processAlarmCreateEvent()`.
-   `verifyAlarmDeleteEventPayload()`: Called by `processAlarmDeleteEvent()`.
-   `verifyAlarmChangeEventPayload()`: Called by `processAlarmChangeEvent()`.

All of these functions return success by default. If a helper function returns an error, it stops the API operation.

To apply custom validations, override the helper functions in the `TMFTopicEventAPIUtilOOB` script include with identical function names and parameters in the `TMFTopicEventAPIUtil` script include.

In this example, a function in a custom `TMFTopicEventAPIUtil` script include overrides the default function in the `TMFTopicEventAPIUtilOOB` script include to perform validation on the name attribute.

```
var TMFTopicEventAPIUtil = Class.create();
TMFTopicEventAPIUtil.prototype = Object.extendsObject(TMFTopicEventAPIUtilOOB, {

    // Define overriding functions here
    verifyAlarmCreateEventPayload: function(eventPayload,responseObject){

        // Returning error status terminates the POST request
        // Make sure to assign error message and reason
        if (eventPayload.type != "unique") {
            responseObject.setMessage("Failed");
            responseObject.setReason("No reason needed");
            return responseObject.status = “error”;
        }
    },
	
    type: ‘TMFTopicEventAPIUtil’
});
```

### Request body subscription validation

To modify the request body subscription validation for the API, you need to override the `validateSubscription()` function in the `TMFTopicEventAPIUtilOOB` script include. This function validates whether the callbackURL you are using to create the event notification is registered and determines whether the **eventType** is registered for the raised callback. This function is called by the processAlarmCreateEvent\(\), processAlarmDeleteEvent\(\), and processAlarmChangeEvent\(\) functions which are also in the `TMFTopicEventAPIUtilOOB` script include.

### Field mapping

When creating or updating records, the Event Notification Management Open API maps request body parameters to Event record fields. When retrieving records, the API maps Event record fields to response object attributes.

The `TMFTopicEventAPIUtilOOB` script include contains the following functions that map change, create, and delete requests, based on the value in the **eventType** parameter, to a record in the Event \[em\_event\] table.

-   mapAlarmChangeObjectToEvent\(\)
-   mapCreateAlarmObjectToEvent\(\)
-   mapDeleteAlarmObjectToEvent\(\)

You can customize field mappings to add and retrieve data for additional Event \[em\_event\] table fields or change the default field mappings. To work with mappings, create functions with identical names and parameters in `TMFTopicEventAPIUtil` to override `TMFTopicEventAPIUtilOOB` mapping functions.

