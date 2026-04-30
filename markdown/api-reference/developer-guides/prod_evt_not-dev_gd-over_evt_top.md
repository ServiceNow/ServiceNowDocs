---
title: Override Event Management Topic Open API functionality
description: The Event Management Topic Open API enables you to save topic records in the Topic \[sn\_api\_notif\_mgmt\_topic\] table after validating the topic payload.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Override Event Management Topic Open API functionality

The Event Management Topic Open API enables you to save topic records in the Topic \[sn\_api\_notif\_mgmt\_topic\] table after validating the topic payload.

You can override the processing of a topic record by updating the methods in the [TopicAPIUtilsOOB](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#) API in the TopicAPIUtils API.

The following is the list of available methods within this API and the default functionality that they provide:

-   [TopicAPIUtilsOOB - createTopicHelper\(Object topicObject, Array warnings\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Inserts the payload passed in the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint into the Topic \[sn\_api\_notif\_mgmt\_topic\] table.
-   [TopicAPIUtilsOOB - getCreateTopicSchema\(\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Returns the defined schema for the payload used by the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint to validate the topic payload. The default payload schema, *Constants.SCHEMA*, is located in the `sn_api_notif_mgmt.Constants` script include.
-   [TopicAPIUtilsOOB - isValidCreateTopicPayload\(Object topicObject, String schema, Array warnings\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Validates the payload passed into the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint. This validation is performed on the request body and the schema.
-   [TopicAPIUtilsOOB - prepareCreateTopicResponse\(Object topicObject, String topicSysId, Array warnings\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Generates and returns the response to a Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint call.
-   [TopicAPIUtilsOOB - processTopicCreation\(Object topicObject\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Processes the request made by the Event Management Topic Open API endpoint. This method invokes the helper methods needed for data insertion, schema validation, request body validation, and response-orchestration. Override this method if you need to customize the fundamental processing of the [Event Management Topic Open - POST /sn\_api\_notif\_mgmt/topic](../../../inbound-rest/concept/event_management_topic-api.md#) request. Otherwise, override the individual helper methods.
-   [TopicAPIUtilsOOB - transformCreateTopicResponse\(Object topicObject, String topicSysId\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Provides the ability to add custom data to the response object returned to the Event Management Topic Open API - POST /sn\_api\_notif\_mgmt/topic endpoint.
-   [TopicAPIUtilsOOB - validateTopicAttributes\(Object topicObject, Array details\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Validates whether the topic name, header-query, content-query, and namespace combination passed in the Event Management Topic Open API endpoint payload is unique. The endpoint uses this attribute combinations to determine whether the topic currently exists in the Topic \[sn\_api\_notif\_mgmt\_topic\] table. The default implementation also checks whether the **name** attribute, which is defined as required in the default topic payload schema, is included in the passed payload.
-   [TopicAPIUtilsOOB - validateTopicExternalId\(Object topicObject, Array details\)](../../../../app-store/dev_portal/API_reference/TopicAPIUtilsOOB/concept/TopicAPIUtilsOOBAPIScoped.md#): Validates the topic external ID passed in the request body of the Event Management Topic Open API endpoint. In the base implementation this only validates that the external ID is not empty.

