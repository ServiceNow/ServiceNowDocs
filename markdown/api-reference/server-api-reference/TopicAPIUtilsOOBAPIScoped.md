---
title: TopicAPIUtilsOOB - Scoped
description: The TopicAPIUtilsOOB script include provides methods that are used when processing the Event Management Topic Open API endpoint.Inserts the information passed in the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint into the Topic \[sn\_api\_notif\_mgmt\_topic\] table.Returns the defined schema for the payload used by the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint to validate the topic payload.Validates the payload passed into the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint. This validation is performed on the request body and the schema.Generates and returns the response to a Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint call.Processes the request made by the Event Management Topic Open API endpoint.Provides the ability to add custom data to the response object returned to the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint.Validates whether the topic name, header-query, content-query, and namespace combination passed in the Event Management Topic Open API endpoint payload is unique.Validates the topic external ID passed in the request body of the Event Management Topic Open API endpoint.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TopicAPIUtilsOOB- Scoped

The TopicAPIUtilsOOB script include provides methods that are used when processing the Event Management Topic Open API endpoint.

If you want to change the default functionality of Event Management Topic Open API, you need to override the functions contained in this script include in the `TopicAPIUtils` script include.

This script include runs in the `sn_api_notif_mgmt` namespace and requires the sn\_api\_notif\_mgmt.event\_mgmt\_integration role.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TopicAPIUtilsOOB - createTopicHelper\(Object topicObject, Array warnings\)

Inserts the information passed in the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint into the Topic \[sn\_api\_notif\_mgmt\_topic\] table.

If you want to modify this insertion process, you need to override this method in the TopicAPIUtils script include.

<table id="table_jkr_mjr_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

warnings

</td><td>

Array

</td><td id="TopicAPIUtilsOOB-warnings-entry">

Warning messages to return in the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint response if the method encounters an issue at the level of "warning".This parameter allows you to add custom warning messages to your implementation of this endpoint.

If there are no additional warning messages, you must pass an empty array.

</td></tr></tbody>
</table><table id="table_kkr_mjr_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Response object.```
{
  "contentQuery": "String",
  "eventType": "String",
  "externalId": "String",
  "headerQuery": "String",
  "id": "String",
  "name": "String"
}
```

For details on these parameters, see the return results for [Event Management Topic Open - POST /sn\_api\_notif\_mgmt/topic](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#).

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
processTopicCreation: function(topicObject) {
  try {
    var warnings = [];

    var schema = this.getCreateTopicSchema();
    if (!this.isValidCreateTopicPayload(topicObject, schema, warnings)) {
      this._logger.logDebug("Create Topic : validation failed");
      return this.response;
    }
    this.createTopicHelper(topicObject, warnings);
    this._logger.logDebug("Create Topic: Topic created succesfully");
  } catch (ex) {
    this._logger.logErr("Create Topic : Process aborted, error is: " + ex);
    var errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.INTERNAL_ERROR, Constants.MESSAGES.TOPIC_CREATE_ERROR, Constants.MESSAGES.TOPIC_CREATE_ERROR);
    var details = [];
    details.push(this.apiCoreUtil.getErrorDetailsObj(ex.message + '', ''));
    errorObj.details = details;
    this.response.details = errorObj;
  }

  return this.response;
},
```

## TopicAPIUtilsOOB - getCreateTopicSchema\(\)

Returns the defined schema for the payload used by the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint to validate the topic payload.

If you want to customize the schema for the topic payload, you need to override the default payload schema, *Constants.SCHEMA*, located in the `sn_api_notif_mgmt.Constants` script include. This default value of this schema is:

```
CREATE_TOPIC_SCHEMA: "{
  \"title\":\"Topic\",
  \"type\":\"object\",
  \"properties\":{
    \"name\":{
      \"type\":\"string\"
    },
    \"contentQuery\":{
      \"type\":\"string\"
    },
    \"headerQuery\":{
      \"type\":\"string\"
    },
    \"namespace\":{
      \"type\":\"string\"
    }
  },
  \"required\":[\"name\"]
}"
```

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Schema for the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint payload. Use this schema to validate the schema passed into the endpoint using the [TopicAPIUtilsOOB - isValidCreateTopicPayload\(Object topicObject, String schema, Array warnings\)](TopicAPIUtilsOOBAPIScoped.md#) method.|

The following code example shows how to call this method.

```
processTopicCreation: function(topicObject) {
  try {
    var warnings = [];

    var schema = this.getCreateTopicSchema();
    if (!this.isValidCreateTopicPayload(topicObject, schema, warnings)) {
      this._logger.logDebug("Create Topic : validation failed");
      return this.response;
    }
    this.createTopicHelper(topicObject, warnings);
    this._logger.logDebug("Create Topic: Topic created succesfully");
  } catch (ex) {
    this._logger.logErr("Create Topic : Process aborted, error is: " + ex);
    var errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.INTERNAL_ERROR, Constants.MESSAGES.TOPIC_CREATE_ERROR, Constants.MESSAGES.TOPIC_CREATE_ERROR);
    var details = [];
    details.push(this.apiCoreUtil.getErrorDetailsObj(ex.message + '', ''));
    errorObj.details = details;
    this.response.details = errorObj;
  }

  return this.response;
},
```

## TopicAPIUtilsOOB - isValidCreateTopicPayload\(Object topicObject, String schema, Array warnings\)

Validates the payload passed into the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint. This validation is performed on the request body and the schema.

If you want to modify the validation process for the payload, you need to override this method in the TopicAPIUtils script include.

<table id="table_jkr_mjr_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

schema

</td><td>

String

</td><td>

Schema to use to validate the topic payload. Use the [TopicAPIUtilsOOB - getCreateTopicSchema\(\)](TopicAPIUtilsOOBAPIScoped.md#) method to obtain this schema.

</td></tr><tr><td>

warnings

</td><td>

Array

</td><td>

Warning messages to return in the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint response if the method encounters an issue at the level of "warning".This parameter allows you to add custom warning messages to your implementation of this endpoint.

If there are no additional warning messages, you must pass an empty array.

</td></tr></tbody>
</table><table id="table_kkr_mjr_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the payload passed in the **topicObject** parameter passed the schema and request body validations.Valid values:

-   true: Payload is valid.
-   false: Payload is invalid.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
processTopicCreation: function(topicObject) {
  try {
    var warnings = [];

    var schema = this.getCreateTopicSchema();
    if (!this.isValidCreateTopicPayload(topicObject, schema, warnings)) {
      this._logger.logDebug("Create Topic : validation failed");
      return this.response;
    }
    this.createTopicHelper(topicObject, warnings);
    this._logger.logDebug("Create Topic: Topic created succesfully");
  } catch (ex) {
    this._logger.logErr("Create Topic : Process aborted, error is: " + ex);
    var errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.INTERNAL_ERROR, Constants.MESSAGES.TOPIC_CREATE_ERROR, Constants.MESSAGES.TOPIC_CREATE_ERROR);
    var details = [];
    details.push(this.apiCoreUtil.getErrorDetailsObj(ex.message + '', ''));
    errorObj.details = details;
    this.response.details = errorObj;
  }

  return this.response;
},
```

## TopicAPIUtilsOOB - prepareCreateTopicResponse\(Object topicObject, String topicSysId, Array warnings\)

Generates and returns the response to a Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint call.

If you want to customize the response object returned by the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint, you need to override this method in the TopicAPIUtils script include.

<table id="table_jkr_mjr_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

topicSysId

</td><td>

String

</td><td>

Sys\_id of the topic created as part of the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic call. Table: Topic \[sn\_api\_notif\_mgmt\_topic\]

</td></tr><tr><td>

warnings

</td><td>

Array

</td><td>

Warning messages to return in the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint response if the method encounters an issue at the level of "warning".This parameter allows you to add custom warning messages to your implementation of this endpoint.

If there are no additional warning messages, you must pass an empty array.

</td></tr></tbody>
</table><table id="table_kkr_mjr_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Endpoint response object.For example:

```

{
  "externalId": "ext001",
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "namespace": "telecomEvents",
  "id": "7ee9850443c3f550461f99612bb8f223"
}
```

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
 createTopicHelper: function(topicObject, warnings) {
  var topicObj = new sn_tmt_core.BaseObject();
  topicObj.setValue('topic_name', topicObject.name);
  if (!gs.nil(topicObject.headerQuery))
    topicObj.setValue('header_query', topicObject.headerQuery);
  if (!gs.nil(topicObject.contentQuery))
    topicObj.setValue('content_query', topicObject.contentQuery);
  if (!gs.nil(topicObject.namespace))
    topicObj.setValue('namespace', topicObject.namespace);
  if (!gs.nil(topicObject.externalId))
    topicObj.setValue('topic_id', topicObject.externalId);
  topicObj.setValue('type', "egress");
  topicObj.setValue('user_created', false);

  new TopicUtil().createTopic(topicObj);

  // If topic external id is passed by external system, add it in topic id field. This will act as an external id for us.

  var topicGr = TopicDAO.getTopicByNameHeaderContentNamespace(topicObject.name, topicObject.headerQuery, topicObject.contentQuery, topicObject.namespace, '');

  if (topicGr && topicGr.next())
    var newTopicSysId = topicGr.getValue('sys_id');

    this.prepareCreateTopicResponse(topicObject, newTopicSysId, warnings);
    return this.response;

},
```

## TopicAPIUtilsOOB - processTopicCreation\(Object topicObject\)

Processes the request made by the Event Management Topic Open API endpoint.

This method invokes the helper methods needed for data insertion, schema validation, request body validation, and response-orchestration. Override this method if you need to customize the fundamental processing of the [Event Management Topic Open - POST /sn\_api\_notif\_mgmt/topic](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) request. Otherwise, override the individual helper methods.

<table id="table_s2k_n3k_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr></tbody>
</table><table id="table_t2k_n3k_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Endpoint response object.For example:

```

{
  "externalId": "ext001",
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "namespace": "telecomEvents",
  "id": "7ee9850443c3f550461f99612bb8f223"
}
```

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
try {
  var topicAPIUtils = new TopicAPIUtils();
  var apiResponse = topicAPIUtils.processTopicCreation(request.body.data);
  response.setStatus(apiResponse.status);
  return tsmOpenAPIUtil.responseBuilder(response, apiResponse.details);
} 
```

## TopicAPIUtilsOOB - transformCreateTopicResponse\(Object topicObject, String topicSysId\)

Provides the ability to add custom data to the response object returned to the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint.

To customize this response object, override this method in the TopicAPIUtils script include.

<table id="table_jkr_mjr_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

topicSysId

</td><td>

String

</td><td>

Sys\_id of the topic created as part of the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic call. You can add information from this record to the topic response object.Table: Topic \[sn\_api\_notif\_mgmt\_topic\]

</td></tr></tbody>
</table><table id="table_kkr_mjr_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Transformed endpoint response object. This object should be TMF688 compliant.For example:

```

{
  "externalId": "ext001",
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "namespace": "telecomEvents",
  "id": "7ee9850443c3f550461f99612bb8f223"
}
```

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
prepareCreateTopicResponse: function(topicObject, topicSysId, warnings) {
  if (!gs.nil(topicSysId)) {
    topicObject.id = topicSysId;
    this.response.status = sn_tmt_core.Constants.STATUS_CODES.CREATED;
    topicObject = this.transformCreateTopicResponse(topicObject, topicSysId); // Customize response payload as per requirement.
    this.response.details = topicObject;
    if (!gs.nil(warnings) && warnings.length > 0) {
      this.response.details.warnings = warnings;
    }
  } else {
    var errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.INTERNAL_ERROR, Constants.MESSAGES.CREATE_TOPIC_ERROR, Constants.MESSAGES.CREATE_TOPIC_ERROR);
    var details = [];
    details.push(this.apiCoreUtil.getErrorDetailsObj(Constants.MESSAGES.CREATE_TOPIC_ERROR, ''));
    errorObj.details = details;
    this.response.details = errorObj;
  }
},
```

The following code example shows code for overriding the default functionality of this method.

```
transformCreateTopicResponse: function(topicObject, topicSysId) {
  new sn_tmt_core.BaseAPIUtil().removeNulls(topicObject);

  // Add custom attributes to the topicObject
  topicObject.origin = “ServiceNow”,
  topicObject.ServiceId= “service001”,
  return topicObject;
},
```

## TopicAPIUtilsOOB - validateTopicAttributes\(Object topicObject, Array details\)

Validates whether the topic name, header-query, content-query, and namespace combination passed in the Event Management Topic Open API endpoint payload is unique.

The endpoint uses this attribute combinations to determine whether the topic currently exists in the Topic \[sn\_api\_notif\_mgmt\_topic\] table.

If you want to modify the validation process you need to override this method in the TopicAPIUtils script include.

<table id="table_i1s_zqr_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

details

</td><td>

Array

</td><td>

Warning messages to return in the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint response if the method encounters an issue at the level of "warning".This parameter allows you to add custom warning messages to your implementation of this endpoint.

If there are no additional warning messages, you must pass an empty array.

</td></tr></tbody>
</table><table id="table_j1s_zqr_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the topic name, header-query, content-query, and namespace combination passed in the **topicObject** parameter is unique.Valid values:

-   true: Parameter combination is unique.
-   false: Parameter combination isn't unique.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
isValidCreateTopicPayload: function(topicObject, schema, warnings) {
  var isValidPayload = true;
  var details = [];
  var validationResults = this.jsonSchemaValidation.validateJSON(topicObject, schema, ''); // Schema validation
  var errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.MISSING_BODY_FIELD, sn_tmt_core.Constants.MESSAGES.MISSING_BODY_FIELD, sn_tmt_core.Constants.MESSAGES.MISSING_BODY_FIELD);

  if (validationResults.length > 0) {
    if (validationResults[0].message == Constants.PAYLOAD_MISSING) {
      this._logger.logDebug("isValidCreateTopicPayload: Missing request body, invalid payload");
      errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.MISSING_BODY, sn_tmt_core.Constants.MESSAGES.MISSING_BODY, sn_tmt_core.Constants.MESSAGES.MISSING_BODY);
      details.push(this.apiCoreUtil.getErrorDetailsObj(sn_tmt_core.Constants.MESSAGES.MISSING_BODY, ''));
      errorObj.details = details;
      this.response.details = errorObj;
      return false;
    } else {
      for (var i = 0; i < validationResults.length; i++) {
        var missingFieldMsg = sn_tmt_core.Constants.MESSAGES.MISSING_FIELD_KEY;
        var message = validationResults[i].message;
        var errorMessage = '';
        if (message.indexOf('missing') != -1) {
          var newMessage = this.apiCoreUtil.constructErrorMsg(message, validationResults[i].dataPath);
          errorMessage = missingFieldMsg.replace(/\$key/g, newMessage);
        } else {
          errorMessage = message;
        }
        details.push(this.apiCoreUtil.getErrorDetailsObj(errorMessage, validationResults[i].dataPath));
      }
    }
    isValidPayload = false;
  }
  var isValidTopicExternalId = this.validateTopicExternalId(topicObject, details);
  var isValidTopicAttributes = this.validatateTopicAttributes(topicObject, details);

  isValidPayload = isValidPayload && isValidTopicExternalId && isValidTopicAttributes;
    if (!isValidPayload) {
      errorObj.details = details;
      this.response.details = errorObj;
    }
    return isValidPayload;
  },
```

## TopicAPIUtilsOOB - validateTopicExternalId\(Object topicObject, Array details\)

Validates the topic external ID passed in the request body of the Event Management Topic Open API endpoint.

In the base implementation this only validates that the external ID is not empty. If you want to modify the validation process for the topic external ID, you need to override this method in the TopicAPIUtils script include. The passed external ID is mapped to the topic\_id field in the Topic \[sn\_api\_notif\_mgmt\_topic\] table.

<table id="table_dyg_5mr_tzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObject

</td><td>

Object

</td><td id="TopicAPIUtilsOOB-topicObject-entry">

Topic payload object passed into the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint.For example:

```
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

The schema of this object must match what is defined in *Constants.SCHEMA.CREATE\_TOPIC\_SCHEMA* located in the `sn_api_notif_mgmt.Constants` script include.

</td></tr><tr><td>

details

</td><td>

Array

</td><td>

Error/detail messages to return in the [Event Management Topic Open API](../../../../../integrate/inbound-rest/concept/event_management_topic-api.md#) endpoint response if the method encounters an issue at the level of "error".This parameter allows you to add custom error messages to your implementation of this endpoint.

If there are no additional error messages, you must pass an empty array.

</td></tr></tbody>
</table><table id="table_eyg_5mr_tzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the external ID passed in the **topicObject** parameter is valid.Valid values:

-   true: External ID is valid.
-   false: External ID is invalid.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
isValidCreateTopicPayload: function(topicObject, schema, warnings) {
  var isValidPayload = true;
  var details = [];
  var validationResults = this.jsonSchemaValidation.validateJSON(topicObject, schema, ''); // Schema validation
  var errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.MISSING_BODY_FIELD, sn_tmt_core.Constants.MESSAGES.MISSING_BODY_FIELD, sn_tmt_core.Constants.MESSAGES.MISSING_BODY_FIELD);

  if (validationResults.length > 0) {
    if (validationResults[0].message == Constants.PAYLOAD_MISSING) {
      this._logger.logDebug("isValidCreateTopicPayload: Missing request body, invalid payload");
      errorObj = this.apiCoreUtil.getErrorObj(sn_tmt_core.Constants.ERROR_CODES.MISSING_BODY, sn_tmt_core.Constants.MESSAGES.MISSING_BODY, sn_tmt_core.Constants.MESSAGES.MISSING_BODY);
      details.push(this.apiCoreUtil.getErrorDetailsObj(sn_tmt_core.Constants.MESSAGES.MISSING_BODY, ''));
      errorObj.details = details;
      this.response.details = errorObj;
      return false;
    } else {
      for (var i = 0; i < validationResults.length; i++) {
        var missingFieldMsg = sn_tmt_core.Constants.MESSAGES.MISSING_FIELD_KEY;
        var message = validationResults[i].message;
        var errorMessage = '';
        if (message.indexOf('missing') != -1) {
          var newMessage = this.apiCoreUtil.constructErrorMsg(message, validationResults[i].dataPath);
          errorMessage = missingFieldMsg.replace(/\$key/g, newMessage);
        } else {
          errorMessage = message;
        }
        details.push(this.apiCoreUtil.getErrorDetailsObj(errorMessage, validationResults[i].dataPath));
      }
    }
    isValidPayload = false;
  }
  var isValidTopicExternalId = this.validateTopicExternalId(topicObject, details);
  var isValidTopicAttributes = this.validatateTopicAttributes(topicObject, details);

  isValidPayload = isValidPayload && isValidTopicExternalId && isValidTopicAttributes;
    if (!isValidPayload) {
      errorObj.details = details;
      this.response.details = errorObj;
    }
    return isValidPayload;
  },
```

