---
title: Batch API
description: The Batch API provides endpoints to send a single request containing multiple REST API calls, and returns a stream of response payloads.Sends multiple REST API requests in a single call.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Batch API

The Batch API provides endpoints to send a single request containing multiple REST API calls, and returns a stream of response payloads.

This REST API enables integrators to:

-   Decrease the amount of time required to send API requests by batching them together, and reduce overhead by narrowing authentication, session setup, and round-trip traffic to a single step.
-   Create more efficient code for client-side integrations.
-   Mix batch item formats and include them in single batch request. For example, one batch can include a Bases64-encoded request in XML format to send to one endpoint and a Base64 encoded request in JSON format to send to a different endpoint.
-   Receive a stream of response payloads in return.
-   Apply existing ACLs to each API call in the batch.

You can include any API available on the instance in a Batch API call. For performance reasons, avoid including long-running requests and requests that retrieve large amounts of data.

**Important:** The Batch API has the same performance characteristics as individual API requests but avoids the overhead of multiple client-server requests. The Batch API is not intended for parallel transaction processing and long-running API requests may cause the API request to exceed the maximum transaction time and return a failure.

## Size and processing limits

Payloads adhere to these size limits:

-   Each item in the request: 5 MB​. You can change this default by updating the **glide.rest.batch.max.inputSize​** system property. Maximum value: 10 MB.
-   Each item in the response: 10 MB. You can change this default by updating the **glide.rest.batch.max.outputSize​** system property or adding the **X-BATCHREQUEST-MAX-OUTPUT-SIZE​** header to your request. The **X-BATCHREQUEST-MAX-OUTPUT-SIZE​** header value cannot exceed the value of the system property.

**Note:** If a request runs longer than 30 seconds, the **REST Batch API request timeout** transaction quota rule ends the transaction. Increasing the value of this transaction quota rule may result in performance issues.

When a batch request reaches a size or processing limit, the system cancels the transaction and returns unprocessed requests in the **unserviced** JSON array in the response.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Batch - POST /now/batch

Sends multiple REST API requests in a single call.

You can include any API available on the instance in a Batch API call. For performance reasons, avoid including long-running requests and requests that retrieve large amounts of data.

### URL format

Versioned URL: `/api/now/{api_version}/batch`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Version of the endpoint to access. For example, `v1` or `v2`.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batch\_request\_id

</td><td>

ID that identifies the batch of requests.Data type: String

</td></tr><tr><td>

rest\_requests

</td><td>

Required. List of request objects to include in the batch request. Data type: Array

 ```
"rest_requests":[
   {
      "body": "String",
      "exclude_response_headers": Boolean,
      "headers":[Array],
      "id": "String",
      "method": "String",
      "url": "String"
   }
]
```

</td></tr><tr><td>

rest\_requests.body

</td><td>

Base64-encoded body of the request. Only applies to methods that require a body, for example POST. Before encoding, the body can be in any format. For example, XML or JSON. Data type: String

</td></tr><tr><td>

rest\_requests.exclude\_response\_headers

</td><td>

Flag that indicates whether to exclude response headers from the response.Valid values:

-   true: Response headers are not included in the response.
-   false: Response headers are included in the response.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

rest\_requests.headers

</td><td>

List of request header objects to send to the endpoint.Data type: Array

 ```
"headers":[
  {
    "name":"String",
    "value":"String"
  }
]
```

</td></tr><tr><td>

rest\_requests.headers.name

</td><td>

Name of the header.Data type: String

</td></tr><tr><td>

rest\_requests.headers.value

</td><td>

Value of the header.Data type: String

</td></tr><tr><td>

rest\_requests.id

</td><td>

Required. ID for each item in the batch.Data type: String

</td></tr><tr><td>

rest\_requests.method

</td><td>

Required. Method to call for the associated endpoint.Data type: String

</td></tr><tr><td>

rest\_requests.url

</td><td>

Required. Relative path of the endpoint to send the request to. Includes the query parameters. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Only supports **application/json**.

</td></tr><tr><td>

X-BATCHREQUEST-MAX-OUTPUT-SIZE​

</td><td>

Size limit for each item in the batch response. Add this header to provide a lower size limit than the default set by the ​**glide.rest.batch.max.outputSize​** system property. You cannot set a value higher than the value in the system property. Default: 10 MB.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batch\_request\_id

</td><td>

ID of the batch that matches the **batch\_request\_id** parameter in the request.Data type: String

</td></tr><tr><td>

serviced\_requests

</td><td>

List of response objects from the batch request. Data type: Array

 ```
"serviced_requests":[
  {
    "body": "String",
    "error_message": "String",
    "execution_time": Number,
    "headers": [Array],
    "id": "String",
    "redirect_url: "String",
    "status_code": Number,
    "status_text": "String"
  }
]
```

</td></tr><tr><td>

serviced\_requests.body

</td><td>

Base64 encoded body of the response. To get the value of the body, Base64 decode the content of this parameter.Data type: String

</td></tr><tr><td>

serviced\_requests.error\_message

</td><td>

If present, the error messages.Data type: String

</td></tr><tr><td>

serviced\_requests.execution\_time

</td><td>

Time it took to execute the batch item request.Data type: Number

 Unit: Milliseconds

</td></tr><tr><td>

serviced\_requests.headers

</td><td>

Headers for the batch item.Data type: Array

 ```
"headers":[
  {
    "name":"String",
    "value":"String"
  }
]
```

</td></tr><tr><td>

serviced\_requests.headers.name

</td><td>

Name of the header.Data type: String

</td></tr><tr><td>

serviced\_requests.headers.value

</td><td>

Value of the header.Data type: String

</td></tr><tr><td>

serviced\_requests.id

</td><td>

ID of the batch item that matches the **rest\_requests.id** parameter in the request.Data type: String

</td></tr><tr><td>

serviced\_requests.redirect\_url

</td><td>

If present, the redirect URL.Data type: String

</td></tr><tr><td>

serviced\_requests.status\_code

</td><td>

Status code for the batch item.Data type: Number

</td></tr><tr><td>

serviced\_requests.status\_text

</td><td>

Text of the status code for the batch item.Data type: String

</td></tr><tr><td>

unserviced\_requests

</td><td>

IDs of the requests that were not processed because the batch request reached a size or processing limit. Data type: Array

</td></tr></tbody>
</table>### cURL request

This batch request sends two GET requests to the instance and one POST request to the incident table. The body of the POST request is Base64 encoded.

```
curl "https://instance.servicenow.com/api/now/v1/batch" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user "username":"password"\
--data "{
   \"batch_request_id\":\"1\",
   \"rest_requests\":[
      {
         \"id\":\"11\",
         \"headers\":[
            {
               \"name\":\"Content-Type\",
               \"value\":\"application/xml\"
            },
            {
               \"name\":\"Accept\",
               \"value\":\"application/xml\"
            }
         ],
         \"url\":\"/api/global/user_role_inheritance\",
         \"method\":\"GET\"
      },
      {
         \"id\":\"12\",
         \"exclude_response_headers\":true,
         \"headers\":[
            {
               \"name\":\"Content-Type\",
               \"value\":\"application/json\"
            },
            {
               \"name\":\"Accept\",
               \"value\":\"application/json\"
            }
         ],
         \"url\":\"/api/now/table/incident?sysparm_limit=1\",
         \"method\":\"GET\"
      },
      {
         \"id\":\"13\",
         \"exclude_response_headers\":true,
         \"headers\":[
            {
               \"name\":\"Content-Type\",
               \"value\":\"application/json\"
            },
            {
               \"name\":\"Accept\",
               \"value\":\"application/json\"
            }
         ],
         \"url\": \"/api/now/table/incident\",
         \"method\":\"POST\",
         \"body\": \"eyd1cmdlbmN5JzonMScsICdzaG9ydF9kZXNjcmlwdGlvbic6J015IGNvbXB1dGVyIG
          Jyb2tlJywgJ2NvbW1lbnRzJzonRWxldmF0aW5nIHVyZ2VuY3ksIHRoaXMgaXMgYSBibG9ja2luZyBpc3N1ZSd9\"
      }
   ]
}" \
```

```
{
    "batch_request_id": "1",
    "serviced_requests": [
        {
            "id": "11",
            "body": "PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz48cmVzcG9uc2U+PHJlc3VsdD48dX
            Nlcl9uYW1lLz48L3Jlc3VsdD48L3Jlc3BvbnNlPg==",
            "status_code": 200,
            "status_text": "OK",
            "headers": [
                {
                    "name": "Pragma",
                    "value": "no-store,no-cache"
                },
                {
                    "name": "Expires",
                    "value": "0"
                },
                {
                    "name": "Content-Length",
                    "value": "88"
                },
                {
                    "name": "Content-Type",
                    "value": "application/xml; charset=UTF-8"
                },
                {
                    "name": "Cache-control",
                    "value": "no-cache,no-store,must-revalidate,max-age=-1"
                }
            ],
            "execution_time": 5
        },
        {
            "id": "12",
            "body": "eyJyZXN1bHQiOlt7InBhcmVudCI6IiIsIm1hZGVfc2xhIjoidHJ1ZSIsImNhdXNlZF9
            ieSI6IiIsIndhdGNoX2xpc3QiOiIiLCJ1cG9uX3JlamVjdCI6ImNhbmNlbCIsInN5c191cGRhdGV
            kX29uIjoiMjAxNi0xMi0xNCAwMjo0Njo0NCIsImNoaWxkX2luY2lkZW50cyI6IjAiLCJob2xkX3J
            lYXNvbiI6IiIsInRhc2tfZWZmZWN0aXZlX251bWJlciI6IklOQzAwMDAwNjAiLCJhcHByb3ZhbF9
            oaXN0b3J5IjoiIiwibnVtYmVyIjoiSU5DMDAwMDA2MCIsInJlc29sdmVkX2J5Ijp7ImxpbmsiOiJ
            odHRwczovL2s4czAwNjc5Nzgtbm9kZTEudGh1bmRlci5sYWIzLnNlcnZpY2Utbm93LmNvbS9hcGk
            vbm93L3RhYmxlL3N5c191c2VyLzUxMzcxNTNjYzYxMTIyN2MwMDBiYmQxYmQ4Y2QyMDA3IiwidmF
            sdWUiOiI1MTM3MTUzY2M2MTEyMjdjMDAwYmJkMWJkOGNkMjAwNyJ9LCJzeXNfdXBkYXRlZF9ieSI
            6ImVtcGxveWVlIiwib3BlbmVkX2J5Ijp7ImxpbmsiOiJodHRwczovL2s4czAwNjc5Nzgtbm9kZTE
            udGh1bmRlci5sYWIzLnNlcnZpY2Utbm93LmNvbS9hcGkvbm93L3RhYmxlL3N5c191c2VyLzY4MWN
            jYWY5YzBhODAxNjQwMGI5OGEwNjgxOGQ1N2M3IiwidmFsdWUiOiI2ODFjY2FmOWMwYTgwMTY0MDB
            iOThhMDY4MThkNTdjNyJ9LCJ1c2VyX2lucHV0IjoiIiwic3lzX2NyZWF0ZWRfb24iOiIyMDE2LTE
            yLTEyIDE1OjE5OjU3Iiwic3lzX2RvbWFpbiI6eyJsaW5rIjoiaHR0cHM6Ly9rOHMwMDY3OTc4LW5
            vZGUxLnRodW5kZXIubGFiMy5zZXJ2aWNlLW5vdy5jb20vYXBpL25vdy90YWJsZS9zeXNfdXNlcl9
            ncm91cC9nbG9iYWwiLCJ2YWx1ZSI6Imdsb2JhbCJ9LCJzdGF0ZSI6IjciLCJyb3V0ZV9yZWFzb24
            iOiIiLCJzeXNfY3JlYXRlZF9ieSI6ImVtcGxveWVlIiwia25vd2xlZGdlIjoiZmFsc2UiLCJvcmR
            lciI6IiIsImNhbGVuZGFyX3N0YyI6IjEwMjE5NyIsImNsb3NlZF9hdCI6IjIwMTYtMTItMTQgMDI",
            "status_code": 200,
            "status_text": "OK",
            "headers": [],
            "execution_time": 8
        },
        {
            "id": "13",
            "body": "eyJyZXN1bHQiOnsicGFyZW50IjoiIiwibWFkZV9zbGEiOiJ0cnVlIiwiY2F1c2VkX2J
            5IjoiIiwid2F0Y2hfbGlzdCI6IiIsInVwb25fcmVqZWN0IjoiY2FuY2VsIiwic3lzX3VwZGF0ZWR
            fb24iOiIyMDIwLTA1LTEyIDAxOjQ0OjM1IiwiY2hpbGRfaW5jaWRlbnRzIjoiMCIsImhvbGRfcmV
            hc29uIjoiIiwidGFza19lZmZlY3RpdmVfbnVtYmVyIjoiSU5DMDAxMDAwNCIsImFwcHJvdmFsX2h
            pc3RvcnkiOiIiLCJudW1iZXIiOiJJTkMwMDEwMDA0IiwicmVzb2x2ZWRfYnkiOiIiLCJzeXNfdXB
            kYXRlZF9ieSI6ImFkbWluIiwib3BlbmVkX2J5Ijp7ImxpbmsiOiJodHRwczovL2s4czAwNjc5Nzg
            tbm9kZTEudGh1bmRlci5sYWIzLnNlcnZpY2Utbm93LmNvbS9hcGkvbm93L3RhYmxlL3N5c191c2V
            yLzY4MTZmNzljYzBhODAxNjQwMWM1YTMzYmUwNGJlNDQxIiwidmFsdWUiOiI2ODE2Zjc5Y2MwYTg
            wMTY0MDFjNWEzM2JlMDRiZTQ0MSJ9LCJ1c2VyX2lucHV0IjoiIiwic3lzX2NyZWF0ZWRfb24iOiI
            yMDIwLTA1LTEyIDAxOjQ0OjM1Iiwic3lzX2RvbWFpbiI6eyJsaW5rIjoiaHR0cHM6Ly9rOHMwMDY
            3OTc4LW5vZGUxLnRodW5kZXIubGFiMy5zZXJ2aWNlLW5vdy5jb20vYXBpL25vdy90YWJsZS9zeXN
            fdXNlcl9ncm91cC9nbG9iYWwiLCJ2YWx1ZSI6Imdsb2JhbCJ9LCJzdGF0ZSI6IjEiLCJyb3V0ZV9
            yZWFzb24iOiIiLCJzeXNfY3JlYXRlZF9ieSI6ImFkbWluIiwia25vd2xlZGdlIjoiZmFsc2UiLCJ",
            "status_code": 201,
            "status_text": "Created",
            "headers": [],
            "execution_time": 2638
        }
    ],
    "unserviced_requests": []
}
```

