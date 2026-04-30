---
title: Trouble Ticket Open API Developer Guide
description: Use the Trouble Ticket Open API to manage ticket information between external ticketing systems and the ServiceNow AI Platform. This API creates, updates, and retrieves data from the Case \[sn\_customerservice\_case\] and Incident \[incident\] tables.The Trouble Ticket Open API can be extended by editing script includes.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Developer guides, API implementation and reference]
---

# Trouble Ticket Open API Developer Guide

Use the Trouble Ticket Open API to manage ticket information between external ticketing systems and the ServiceNow AI Platform. This API creates, updates, and retrieves data from the Case \[sn\_customerservice\_case\] and Incident \[incident\] tables.

This developer guide provides information on how to extend the [Trouble Ticket Open API](../../../inbound-rest/concept/trouble-ticket-open-api.md#) to make various customizations.

## Extending the Trouble Ticket Open API

The Trouble Ticket Open API can be extended by editing script includes.

These script includes should only be edited with an understanding of the consequences of the changes.

-   `TMFTroubleTicketAPIConstants`: Contains constants and required parameter information.
-   `TMFTroubleTicketAPIUtil`: Contains functions to handle POST, GET, and PATCH requests.
-   `TroubleTicketProcessorOOB`: Contains helper functions that support functions in TMFTroubleTicketAPIUtil.
-   `TroubleTicketProcessor`: An empty script include file. Use this file to define any functions that you want to override from TroubleTicketProcessorOOB.

Extend the Trouble Ticket Open API to make the following customizations.

### Required parameters

To change which request body parameters are required or not required, update the TMFTroubleTicketAPIConstants script include. By default, the request body to create a ticket \(POST\) requires the parameters **description**, **severity**, and **ticketType**. By default, the request body to update a ticket \(PATCH\) doesn't have required parameters.

-   `TMFTroubleTicketAPIConstants.TROUBLE_TICKET_CREATION_SCHEMA`: Sets the required request body parameters to create a ticket.
-   `TMFTroubleTicketAPIConstants.TROUBLE_TICKET_UPDATE_SCHEMA`: Sets the required request body parameters to update a ticket.

In this example, the **description**, **severity**, **status**, and **ticketType** parameters are required to create a ticket.

```
// TMFTroubleTicketAPIConstants
TMFTroubleTicketAPIConstants.TROUBLE_TICKET_CREATION_SCHEMA = {
    "title": "CreateTroubleTicket",
    "type": "object",
    "properties": {
        "description": {
            "type": "string"
        },
        "severity": {
            "type": "string"
        },
        "status": {
            "type": "string"
        },
        "ticketType": {
            "type": "string"
        }
    },
    "required": [
        "description",
        "severity",
        "status",
        "ticketType"
    ]
};
```

### Request body validation

To perform additional validation on the request body, override TroubleTicketProcessorOOB functions. TroubleTicketProcessorOOB contains the following six helper functions that return `true` by default. These functions are called in TMFTroubleTicketAPIUtil.

-   `verifyGetRequestForCase()` - Called by `processGetRequestForCase()`.
-   `verifyPatchRequestForCase()` - Called by `processPatchRequestForCase()`.
-   `verifyPostRequestForCase()` - Called by `processPostRequestForCase()`.
-   `verifyGetRequestForIncident()` - Called by `processGetRequestForIncident()`.
-   `verifyPatchRequestForIncident()` - Called by `processPatchRequestForIncident()`.
-   `verifyPostRequestForIncident()` - Called by `processPostRequestForIncident()`.

If a helper function returns `false`, it stops the API operation. To apply custom validation, override TroubleTicketProcessorOOB helper functions by creating functions with identical names and parameters in TroubleTicketProcessor. These new TroubleTicketProcessor functions will be called by TMFTroubleTicketAPIUtil to replace the default TroubleTicketProcessorOOB helper functions.

In this example, a function in TroubleTicketProcessor overrides a default function in TroubleTicketProcessorOOB to perform validation on the name attribute.

```
// TroubleTicketProcessor
var TroubleTicketProcessor = Class.create();
TroubleTicketProcessor.prototype = Object.extendsObject(TroubleTicketProcessorOOB, {
    // Define overriding functions here
    // Function name and parameters must be identical to the function it overrides

    verifyPostRequestForCase: function(caseObject, apiResponseProcessor){
        // Returning false terminates the POST request
        // Make sure to assign error message and reason
        if (caseObject.name != "Hello world") {
            apiResponseProcessor.setMessage(TMFTroubleTicketAPIConstants.MESSAGES.CASE_CREATION_FAILURE);
            apiResponseProcessor.setReason("No reason needed");
            return false;
        }
    },

    type: 'TroubleTicketProcessor'
});

```

### Additional REST operations

To create additional operations beyond the existing GET, PATCH, and POST operations, [create additional scripted REST resources](../../../custom-web-services/task/t_CreateAScriptedRESTAPIResource.md) for the Trouble Ticket Open API. The logic of the new scripted REST resources should be consistent with the existing operations. Define functions for the new operations in TMFTroubleTicketAPIUtil.

### Field mapping

When creating or updating records, the API maps request body parameters to case and incident record fields. When retrieving records, the API maps record fields to response object attributes.

TroubleTicketProcessorOOB contains the following functions to map a PATCH or POST request body to a case or incident GlideRecord.

-   `mapPatchRequestToCase()`
-   `mapPostRequestToCase()`
-   `mapPatchRequestToIncident()`
-   `mapPostRequestToIncident()`

TroubleTicketProcessorOOB contains the following functions to map a case or incident GlideRecord to a JSON response object for GET, PATCH, or POST requests.

-   `createGetResponseForCase()`
-   `createPatchResponseForCase()`
-   `createPostResponseForCase()`
-   `createGetResponseForIncident()`
-   `createPatchResponseForIncident()`
-   `createPostResponseForIncident()`

Customize field mappings to add and retrieve data for additional case and incident fields, or to change the default mappings for fields. To customize the field mappings, override TroubleTicketProcessorOOB mapping functions by creating functions with identical names and parameters in TroubleTicketProcessor. These new TroubleTicketProcessor functions will be used by TMFTroubleTicketAPIUtil to replace the default TroubleTicketProcessorOOB mapping functions.

In this example, two functions in TroubleTicketProcessor override the default functions in TroubleTicketProcessorOOB to change the Description field mapping and add a mapping for the Contract field.

```
// TroubleTicketProcessor
var TroubleTicketProcessor = Class.create();
TroubleTicketProcessor.prototype = Object.extendsObject(TroubleTicketProcessorOOB, {
    // Define overriding functions here
    // Function name and parameters must be identical to the function it overrides

    mapPostRequestToCase: function(caseGr, caseObject){
        // Override default mapping for the Description field
        caseGr.description = "All cases will be created with this description";
        // Add new mapping to the Contract field
        caseGr.contract = caseObject.contract;
     },

    createPostResponseForCase: function(caseGr, caseObject){
        // Override default mapping for the description attribute
        caseObject.description = "This will always be the retrieved description";
        // Add new contract attribute to the response object
        caseObject.contract = caseGr.contract;    
    },

    type: 'TroubleTicketProcessor'
});

```

### Mapping logic for choice fields

The **State**, **Priority**, and **contact\_type** fields are choice fields, where each choice is composed of a label and a corresponding value. For example, if the **State** field is set to **New**, the label is **New** and the value is **1**. The mapping between choice labels and values can be changed by overriding the choice field mapping functions.

TroubleTicketProcessorOOB contains the following choice field mapping functions.

-   `transformCaseSeverity()`
-   `transformCaseChannel()`
-   `transformCaseStatus()`
-   `transformIncidentSeverityToUrgency()`
-   `transformIncidentSeverityToImpact()`
-   `transformIncidentChannel()`
-   `transformIncidentStatus()`

Override TroubleTicketProcessorOOB choice field mapping functions by creating functions with identical names and parameters in TroubleTicketProcessor. These new TroubleTicketProcessor functions will be used by TMFTroubleTicketAPIUtil to replace the default TroubleTicketProcessorOOB choice field mapping functions.

In this example, a function in TroubleTicketProcessor overrides a default function in TroubleTicketProcessorOOB to change the choice mapping for the **Status** field.

```
// TroubleTicketProcessor
var TroubleTicketProcessor = Class.create();
TroubleTicketProcessor.prototype = Object.extendsObject(TroubleTicketProcessorOOB, {
    // Define overriding functions here
    // Function name and parameters must be identical to the function it overrides

    transformCaseStatus: function(status){
        if (status == "Draft")
            return 1;
        else return 10;
    },

    type: 'TroubleTicketProcessor'
});

```

