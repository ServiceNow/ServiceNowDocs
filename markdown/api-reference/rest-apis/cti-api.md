---
title: CTI API
description: The CTI API provides endpoints that enable Computer Telephony Integration \(CTI\) providers to interact with the Cloud Call Center framework.Renders transcripts and recordings for a specified agent call.Invokes Computer Telephony Integration \(CTI\) operations using a specified operation handlers within the Cloud Call Center framework.Passes events from a Contact Control Panel \(CCP\) provider to a ServiceNow instance.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CTI API

The CTI API provides endpoints that enable Computer Telephony Integration \(CTI\) providers to interact with the Cloud Call Center framework.

Using this API, integrators are able to:

-   Invoke CTI operations using custom operation handlers within the Cloud Call Center framework.
-   Pass events from a CCP provider to a ServiceNow instance.
-   Render transcripts and recordings for a specified agent call.

This API runs in the **sn\_cti\_core** namespace. Before you are able to access this API, you must install the Cloud Call Center Core \(sn\_cti\_core\) application. For information on this installation, see [Install Cloud Call Center applications](https://www.servicenow.com/docs/access?context=install-ccc-apps&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

For additional information on the Cloud Call Center, see [Cloud Call Center](https://www.servicenow.com/docs/access?context=cloud-call-center-overview&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CTI\_API - GET /sn\_cti\_core/cti\_api/call\_analysis/\{interaction\_sys\_id\}

Renders transcripts and recordings for a specified agent call.

Components use this endpoint in Agent and Manager workspaces to render associated agent call transcripts and recordings. To access this endpoint, the user credentials that you pass in the call must have the workspace\_user, interaction\_agent, or admin role.

This endpoint has a corresponding extension point, sn\_cti\_core.CTICallAnalysisExtractor, that is responsible for rendering the call data. The base system provides an implementation for Amazon Connect. If your implementation is different, you should customize this extension point before utilizing this endpoint. Also, the response parameters returned by this endpoint correspond to the implementation of this extension point. For additional information on implementing extension points, see [Using extension points to extend application functionality](../../../build/applications/concept/extension-points.md) and [Extension points in Cloud Call Center](https://www.servicenow.com/docs/access?context=extension-point-ccc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

### URL format

Default URL: `/api/sn_cti_core/cti_api/call_analysis/{interaction_sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interaction\_sys\_id

</td><td>

Sys\_id of the agent call for which to render to transcript and recording.Data type: String

Table: Interaction \[interaction\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|Various|Depends on the implementation in the sn\_cti\_core.CTICallAnalysisExtractor extension point.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|Depends on the implementation in the sn\_cti\_core.CTICallAnalysisExtractor extension point.||

### cURL request

The following example requests the rendering of a specific agent call.

```
curl -X POST \
  https://instance.servicenow.com/api/sn_cti_core/cti_api/call_analysis/88f2d9b7dbd7101058f05214dc96192a \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password'
```

Rendered call data based on the processing specified in the sn\_cti\_core.CTICallAnalysisExtractor extension point.

```
{
  "result":{
    "status":"success",
    "recordingData":{
      "recordingUrls":[
        "https://instance.awsapps.com/connect/get-recording?format=wav&callLegId=7626da7f-e083-4085-b77a-85bfea18fe24",
        "https://s3.console.aws.amazon.com/s3/object/connect-60f8665899b6/connect/instance/CallRecordings/2020/09/23/7626da7f-e083-4085-b77a-85bfea18fe24_20200923T18%3A24_UTC.wav"
      ],
      "status":"success"
    },
    "transcriptData":{
      "transcript":[
        {
          "content":"Okay. Hello? Mhm. Okay, okay.",
          "beginOffsetMillis":3940,
          "participantId":"CUSTOMER",
          "additionalInfo":[
            {
              "value":"Neutral",
              "highlightColor":"info"
            }
          ]
        },
        {
          "content":"bye.",
          "beginOffsetMillis":26040,
          "participantId":"AGENT",
          "additionalInfo":[
            {
              "value":"Neutral",
              "highlightColor":"info"
            }
          ]
        }
      ],
      "sentimentTrend":[
        {
          "x":0,
          "y":0
        },
        {
          "x":3939,
          "y":0
        },
        {
          "x":3940,
          "y":0
        },
        {
          "x":26450,
          "y":0
        }
      ],
      "sentimentPercents":{
        "positive":0,
        "neutral":100,
        "negative":0
      },
      "talkTimePercents":{
        "agent_talk_time":2.515491747959998,
        "customer_talk_time":28.82998956991226,
        "non_talk_time":68.65451868212774
      },
      "metadata":{
        "ctiVendor":"amazon_connect",
        "customerId":"Alice Smith",
        "agentId":"Piper Epps"
      },
      "status":"success"
    },
    "metadata":{
      "callMonitorURL":"https://instance.awsapps.com/connect/real-time-metrics?tableType=user",
      "recordingState":"success",
      "transcriptState":"success",
      "emptyStateImages":{
        "in_progress":"call_in_progress.png",
        "processing":"processing_post_call.png",
        "unavailable":"transcript_failed.png"
      }
    }
  }
}
```

## CTI\_API - POST /sn\_cti\_core/cti\_api/providers/\{provider\}/components/\{component\}/versions/\{version\}

Invokes Computer Telephony Integration \(CTI\) operations using a specified operation handlers within the Cloud Call Center framework.

Before calling this endpoint, you must create a provider configuration record and associated message transformers. This is typically done when the Cloud Call Center framework is initially implemented in your instance. For additional information, see [Provider configuration in Cloud Call Center](https://www.servicenow.com/docs/access?context=provider-configuration-ccc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

A message transformer is responsible for parsing the payload specified in the request body of this endpoint and setting the payload data on an associated [CTIOperationRequest](../../../app-store/dev_portal/API_reference/CTIOperationRequest/concept/CTIOperationRequestAPI.md#) object. An operation handler is then responsible for getting the information from the CTIOperationRequest object and using the data to process the requested operation.

After the message transformer finishes parsing the passed in payload, the Cloud Call Center framework instantiates the specified operation handler. The operating handler uses the [CTIOperationResponse](../../../app-store/dev_portal/API_reference/CTIOperationResponse/concept/CTIOperationResponseAPI.md#) [CTIOperationResponse - Scoped, Global](../../../app-store/dev_portal/API_reference/CTIOperationResponse/concept/CTIOperationResponseAPI.md#) API GET methods to obtain the information that it needs from the associated CTIOperationRequest object to process the requested operation.

You define the operation handler to invoke, and its associated parameters, in the request body of this endpoint call. The specified operation handler must be defined in your instance within the Operation Handler \[sn\_cti\_operation\_handler\] table. For additional information on creating operation handlers, see [Configure a contact flow for an automated caller interaction](https://www.servicenow.com/docs/access?context=establish-automated-bot-interactions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

The ServiceNow base system provides working operation handlers and message transformers that enable connection to Amazon Connect. When building contact flows within Amazon Connect, there are two integration points between Amazon services and a ServiceNow instance:

-   Amazon Web Services \(AWS\) Lambda Proxy \(Invoke AWS Lambda function\)
-   AWS Lex Bot \(Get Customer Input\)

You can find the available operation handlers and message transformers for these integration points in the Operation Handlers \[sn\_cti\_operation\_handler\] and Provider Message Transformer \[sn\_cti\_provider\_msg\_transormer\] tables.

In addition, the user credentials that you pass in the call must have the sn\_cti\_core.service or admin role to access this endpoint.

For additional information on the Cloud Call Center, see [Cloud Call Center](https://www.servicenow.com/docs/access?context=cloud-call-center-overview&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

### URL format

Default URL: `/api/sn_cti_core/cti_api/providers/{provider}/components/{component}/versions/{version}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

component

</td><td>

Label of your provider component, such as sn\_aws\_connect\_lambda\_proxy\_component or sn\_aws\_connect\_lex\_intent\_processor\_component.Data type: String

Table: Component field of the Provider Component \[sn\_cti\_provider\_component\]

</td></tr><tr><td>

provider

</td><td>

Sys\_id of your CTI provider record.Data type: String

Table: Provider Component \[sn\_cti\_provider\_component\]

</td></tr><tr><td>

version

</td><td>

Version of the specified provider record.Data type: String

Table: In the Version field of the Provider Component \[sn\_cti\_provider\_component\] table.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|Depends on the operation handler being called and its specific implementation.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|Various|Depends on the operation being called and its specific implementation.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|Depends on the operation being called and its specific implementation.||

### cURL request

The following example invokes the interactionEvent operation handler through the sn\_aws\_connect\_lambda\_proxy\_component component.

```
curl -X POST \
  https://instance.servicenow.com/api/sn_cti_core/cti_api/providers/c4b12aa6e700001034b36584c2f6a9bc/components/sn_aws_connect_lambda_proxy_component/versions/v1.0 \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password'
  -d '{
  "context": {
    "callbackWaitsForEmptyEventLoop": true,
    "functionVersion": "$LATEST",
    "functionName": "snRALJNLambda",
    "memoryLimitInMB": "128",
    "logGroupName": "/aws/lambda/snRALJNLambda",
    "logStreamName": "2020/09/24/[$LATEST]b604a9579ef548a1b3f6b6739d19e1d9",
    "invokedFunctionArn": "arn:aws:lambda:us-west-2:028738656045:function:snRALJNLambda",
    "awsRequestId": "b528a5a8-bb0b-4ec8-8e76-aa568f68fdc8"
  },
  "event": {
    "Details": {
      "ContactData": {
        "Attributes": {
          "$accepted_terms": "true"
        },
        "Channel": "VOICE",
        "ContactId": "8fe7c107-78df-4eec-85b3-91c6dcb8e912",
        "CustomerEndpoint": {
          "Address": "+16693504374",
          "Type": "TELEPHONE_NUMBER"
        },
        "Description": null,
        "InitialContactId": "8fe7c107-78df-4eec-85b3-91c6dcb8e912",
        "InitiationMethod": "INBOUND",
        "InstanceARN": "arn:aws:connect:us-west-2:028738656045:instance/d276bd83-6305-4f63-abee-e66fd5bdf503",
        "LanguageCode": "en-US",
        "MediaStreams": {
          "Customer": {
            "Audio": null
           }
         },
         "Name": null,
         "PreviousContactId": "8fe7c107-78df-4eec-85b3-91c6dcb8e912",
         "Queue": {
           "ARN": "arn:aws:connect:us-west-2:028738656045:instance/d276bd83-6305-4f63-abee-e66fd5bdf503/queue/0f17b62d-d493-439a-88c6-42db0d0e652f",
           "Name": "BasicQueue",
           "OutboundCallerId": {
             "Address": "+18335441399",
             "Type": "TELEPHONE_NUMBER"
           }
         },
         "References": {},
         "SystemEndpoint": {
           "Address": "+18335441399",
           "Type": "TELEPHONE_NUMBER"
         }
       },
       "Parameters": {
         "sn_component": "sn_aws_connect_lambda_proxy_component",
         "sn_operation": "interactionEvent"
       }
     },
     "Name": "ContactFlowEvent"
   }
 }'
```

Example response to the interactionEvent operation handler call.

```
{
  "result": {
    "snc_user_first_name": "Jane",
    "snc_user_last_name": "Doe",
    "snc_user_sys_id": "bbe591bfdb5710100231dbdb5e9619e3",
    "snc_user_vip": "false",
    "interactionTable": "interaction",
    "interactionId": "973b07c8dbe710100231dbdb5e961908",
    "statusCode": 200,
    "message": "success"
  }
}
```

## CTI\_API - POST /sn\_cti\_core/cti\_api/softphone/sources/\{source\}/actor/\{actor\}/events/\{event\}

Passes events from a Contact Control Panel \(CCP\) provider to a ServiceNow instance.

Typically you call this endpoint from your CCP UI page to perform various tasks \(events\), such as changing the presence state of an agent or changing the state of a record on call completion. To access this endpoint, the user credentials that you pass in the call must have the sn\_openframe\_user or admin role.

This endpoint has a corresponding extension point, sn\_cti\_core.SoftPhoneEventSink, that is responsible for determining the action that is actually performed by this endpoint call for each event. The base system provides an implementation for Amazon Connect events. If your implementation is different, you should customize this extension point before utilizing this endpoint. The request body and response formats of this endpoint correspond to the implementation of this extension point. For additional information on implementing extension points, see [Using extension points to extend application functionality](../../../build/applications/concept/extension-points.md) and [Extension points in Cloud Call Center](https://www.servicenow.com/docs/access?context=extension-point-ccc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

### URL format

Default URL: `/api/sn_cti_core/cti_api/softphone/sources/{source}/actor/{actor}/events/{event}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actor

</td><td>

Emitter of the event, such as agent or external\_system. The specific values are determined by the implementer.Data type: String

</td></tr><tr><td>

event

</td><td>

Name of the event in the Computer Telephony Integration \(CTI\) vendor’s system, such as Available or Offline. The specific values are determined by the implementer but must be a single word/phrase without spaces or special characters.Data type: String

</td></tr><tr><td>

sources

</td><td>

Identifier of the vendor's Softphone UI page, such as aws\_ccp.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|Implementation specific. Determined by the implementation of the sn\_cti\_core.SoftPhoneEventSink extension point.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

The following example passes AgentStatusOne event information to the ServiceNow instance. The request body parameters are determined by the implementation of the sn\_cti\_core.SoftPhoneEventSink extension point.

```
curl -X POST \
  https://instance.servicenow.com/api/sn_cti_core/cti_api/softphone/sources/aws_ccp/actor/agent/events/AgentStatusOne \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password'
  -d '{
   "agent":{
      "sys_id":"doe.john@snc",
      "status":{
         "agentStateARN":null,
         "type":"not_routable",
         "name":"AgentStatusOne",
         "startTimestamp":"2020-09-24T21:43:20.957Z"
      }
   },
   "window":{
      "location":{
         "href":"https://instance.servicenow.com/sn_cti_amzn_cct_aws_ccp.do?id=44106eabdb5710100231dbdb5e96191d",
         "search":"?id=44106eabdb5710100231dbdb5e96191d"
      }
   },
   "aws":{
      "connect":{
         "config":{
            "ccpHost":"instance.awsapps.com",
            "ccpUrl":"https://instance.awsapps.com/connect/ccp-v2/",
            "loginPopup":true,
            "audioRecordingUrlPrefix":"https://instance.awsapps.com/connect/get-recording?format=wav&callLegId=",
            "softphone":{
               "allowFramedSoftphone":true
            },
            "region":"us-west-2"
         }
      }
   }
}'
```

No response parameters are returned.

```
{
  "result": {}
}
```

